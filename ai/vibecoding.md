# Fabriquer un outil sur mesure, en un seul fichier

**Codage conversationnel · prompts prêts à copier**

> [!NOTE]
> Cette page rassemble ce qu'il faut pour fabriquer un outil qui ne sert qu'à vous, à votre classe ou à votre service : une page HTML, un seul fichier, qui s'ouvre hors ligne et s'envoie comme un document.
> Les prompts proposés peuvent être copiés tels quels ou modifiés selon vos besoins.

---

## La méthode, en deux mots

Vous n'écrivez pas de code : vous **décrivez en langage naturel** ce que l'outil doit faire à un assistant d'IA générative (comme ChatGPT, Claude, Mistral ou Copilot) et c'est lui qui produit le code. Vous ouvrez le résultat, vous l'essayez, vous décrivez ce qui ne va pas, il corrige. Et ainsi de suite.

On appelle cela le **codage conversationnel**, ou *vibe coding*, terme popularisé par Andrej Karpathy en 2025.  C'est comme coder sans se soucier du code.

---

## Ce qui est obligatoire

- **Les données personnelles** sont soumises au cadre de votre établissement et aux règlements nationaux en vigueur.
- **Les systèmes d'IA** : utilisez en priorité ceux explicitement approuvés par votre employeur. Un service approuvé et sous contrat peut autoriser des traitements interdits par un service grand public.
- **Mettre l'outil en ligne sur un réseau d'établissement ne dépend pas uniquement de vous.** La décision appartient à votre établissement, qui l'instruira conformément à ses procédures : hébergement, données personnelles, accessibilité, maintenance. Présentez l'outil en répondant au prompt d'audit ci-dessous : c'est à peu près ce qu'on vous demandera.

En cas de doute sur l'un de ces points, l'interlocuteur varie d'un établissement à l'autre : service informatique, personne en charge de la protection des données, ou direction.

**Et sur votre propre ordinateur ?** Un fichier que vous ouvrez sur votre ordinateur pour votre propre travail ne demande rien à personne, tant qu'il ne traite pas de données personnelles. Dès qu'il en traite ou que vous le confiez à quelqu'un d'autre, vous n'êtes plus le seul concerné. C'est à ce moment que le prompt d'audit entre en jeu.

## Ce qui est conseillé

- **Des exemples fictifs suffisent.**
	- Vous n'avez jamais besoin de données réelles pour vérifier qu'un outil fait ce que vous voulez.
- **Restez petit.**
	- Un outil qui fait une seule chose est plus facile à corriger, à partager et à refaire entièrement.

---

## Le prompt générique minimal, pour essayer tout de suite

Quatre lignes, à adapter en remplaçant la seule zone entre crochets. C'est le plus court chemin vers une première page qui s'ouvre.

```
Crée un outil web dans un SEUL fichier HTML autonome, qui fonctionne hors ligne, sans bibliothèque externe et sans envoyer de données nulle part.

Besoin : [ce que l'outil doit faire, et pour qui]

Donne-moi le fichier complet, puis dis-moi en trois lignes ce que je dois vérifier.
```

Il vous laisse sans prise sur le reste : l'accessibilité, le zoom, la langue de l'interface, les champs. Pour un outil que vous garderez, ou que vous donnerez à quelqu'un, passez au gabarit ci-dessous.

---

## Le prompt générique plus avancé et à adapter

Remplacez les zones entre crochets. Ne touchez pas au reste.

**Seule la première est obligatoire.** Si vous ne savez pas encore ce que la personne fera ni ce qu'elle obtiendra, écrivez dans les deux autres : *à toi de proposer, je corrigerai*. Vous déciderez en voyant le résultat.

Ce gabarit ne suppose pas un formulaire : il vaut aussi bien pour un calculateur, un minuteur, une liste de vérification, un tirage au sort ou un tableau de suivi.

```
Tu es développeur web. Crée une application web d'une seule page,
dans un SEUL fichier HTML autonome.

# BESOIN
[Deux ou trois phrases : ce que l'outil doit faire, pour qui,
et ce que la personne y gagne.]

# CE QUE LA PERSONNE FAIT
[Ce qu'elle saisit, choisit, coche, déplace ou déclenche
— ou : à toi de proposer, je corrigerai]

# CE QU'ELLE OBTIENT
[Un texte prêt à copier, un calcul, une liste, un tableau, un minuteur
qui tourne, un fichier à télécharger…
— ou : à toi de proposer, je corrigerai]

# CONTRAINTES TECHNIQUES — à ne pas modifier
- Un seul fichier .html : le HTML, le CSS et le JavaScript sont dedans.
  Aucun fichier séparé.
- Aucune requête réseau, aucune bibliothèque externe, aucun compte utilisateur.
- Le fichier doit fonctionner hors ligne, à ouvrir directement dans un navigateur.
- Aucune donnée n'est envoyée nulle part : tout reste dans le navigateur.
- Accessible : HTML sémantique, navigation complète au clavier, focus visible,
  contrastes conformes aux WCAG 2.2 niveau AA, libellés associés aux champs.
- Adaptatif, utilisable jusqu'à un zoom de 200 %.
- Interface en français, sobre, sans logo ni image.
- Code court et lisible, sans framework.

# RÉPONSE ATTENDUE
1. Le fichier HTML complet, en un seul bloc de code.
2. Puis, en trois lignes maximum et sans jargon technique : ce que fait l'outil, et ce que je dois vérifier en l'essayant.
```

---

## Un exemple complet, rempli

Le gabarit ci-dessus, rempli pour un outil précis : un formulaire d'aide à la rédaction de prompts. **Remarquez le niveau de détail du besoin** — deux ou trois phrases qui disent ce que fait l'outil, pour qui, et ce que la personne y gagne. C'est ce niveau-là qui évite de devoir tout reprendre au deuxième essai. Copiez-le, collez-le dans votre assistant : vous obtiendrez un outil de ce genre.

```
Tu es développeur web. Crée une application web d'une seule page,
dans un SEUL fichier HTML autonome.

# BESOIN
Un formulaire qui aide à rédiger un prompt structuré, pour des collègues
qui se servent d'une IA sans être à l'aise avec la formulation des consignes.
Ils remplissent des champs, l'outil écrit le prompt à leur place : ils n'ont
plus à savoir comment on rédige un prompt, seulement à dire ce qu'ils veulent.

# CE QUE LA PERSONNE FAIT
Elle remplit cinq champs, dans cet ordre : rôle, objectif, contexte,
public cible, contraintes. Chacun avec un exemple court en texte d'aide,
pour montrer ce qu'on attend sans avoir à l'expliquer.

# CE QU'ELLE OBTIENT
Le prompt correspondant, affiché en permanence et mis à jour au fil de la
saisie, avec un bouton « copier » qui confirme que la copie a eu lieu.

# CONTRAINTES TECHNIQUES — à ne pas modifier
- Un seul fichier .html : le HTML, le CSS et le JavaScript sont dedans.
  Aucun fichier séparé.
- Aucune requête réseau, aucune bibliothèque externe, aucun compte utilisateur.
- Le fichier doit fonctionner hors ligne, à ouvrir directement dans un navigateur.
- Aucune donnée n'est envoyée nulle part : tout reste dans le navigateur.
- Accessible : HTML sémantique, navigation complète au clavier, focus visible,
  contrastes conformes aux WCAG 2.2 niveau AA, libellés associés aux champs.
- Adaptatif, utilisable jusqu'à un zoom de 200 %.
- Interface en français, sobre, sans logo ni image.
- Code court et lisible, sans framework.

# RÉPONSE ATTENDUE
1. Le fichier HTML complet, en un seul bloc de code.
2. Puis, en trois lignes maximum et sans jargon technique : ce que fait l'outil, et ce que je dois vérifier en l'essayant.
```

---

## Ce que vous faites du code obtenu

L'assistant d'IA générative vous répond par un long bloc de code. Pour en faire un outil :

1. **Copiez tout le code**, du premier `<!DOCTYPE html>` au dernier `</html>`. La plupart des assistants ont un bouton « copier » au-dessus du bloc.
2. **Collez-le dans un éditeur de texte brut** : le Bloc-notes sous Windows, TextEdit sur Mac, ou un éditeur de code si vous en avez un.
3. **Enregistrez le fichier sous un nom qui finit par `.html`**, par exemple `generateur-prompt.html`.
4. **Double-cliquez dessus** : il s'ouvre dans votre navigateur.

> [!WARNING]
> **Deux pièges fréquents**, qui font afficher du code au lieu de l'outil :
> - **Sur Mac, TextEdit** enregistre par défaut au format texte enrichi. Avant d'enregistrer, allez dans le menu *Format → Convertir au format texte*.
> - **Sous Windows, le Bloc-notes** peut ajouter l'extension `.txt` à la fin du nom. Dans la fenêtre d'enregistrement, choisissez *Type : Tous les fichiers*.

Si votre assistant affiche l'outil directement dans la conversation, ou propose un bouton de téléchargement, c'est encore plus simple : utilisez-le.

---

## Le prompt de réparation, quand ça ne marche pas

```
Voici mon outil : [collez le contenu complet du fichier]

Problème :
- Ce que je voulais : [décrivez]
- Ce qui se passe réellement : [décrivez]

Identifie l'origine du problème et propose la correction la plus petite
possible. Renvoie le fichier complet corrigé, puis dis-moi en trois lignes ce que tu as changé.
```

**« La correction la plus petite possible »** compte : sans cette consigne, l'IA a tendance à tout réécrire, et à casser autre chose au passage.

---

## Le prompt d'ajout, pour une fonctionnalité de plus

```
Voici mon outil : [collez le contenu complet du fichier]

Ajoute : [décrivez la fonctionnalité en une ou deux phrases].

Ne change rien d'autre. Respecte les contraintes techniques d'origine :
un seul fichier, aucune requête réseau, accessible au clavier.
Renvoie le fichier complet.
```

---

## Le prompt d'audit, avant de partager le fichier

Il établit un constat, il ne répare rien : vous choisirez ensuite ce que vous faites corriger, avec le prompt de réparation.

```
Analyse ce fichier et réponds en français, sans jargon technique :
1. Envoie-t-il des données quelque part ?
2. Charge-t-il quelque chose depuis internet ?
3. Est-il utilisable entièrement au clavier, et avec un lecteur d'écran ?
4. S'affiche-t-il correctement sur un téléphone, et à un zoom de 200 % ?
5. Que se passe-t-il si on laisse un champ vide, si on colle un texte
   très long, ou si on saisit des caractères inattendus ?
6. Qu'est-ce qui pourrait mal se passer pour quelqu'un qui l'utilise ?

Pour chaque point : le constat, le niveau (critique / majeur / mineur),
et la correction que tu proposes.

Ne modifie rien pour l'instant : ne renvoie pas de code, seulement le constat.

Voici le fichier : [collez le contenu complet]
```

---

## Le prompt de nettoyage, quand le fichier devient long

Un fichier plus court se relit mieux, se corrige mieux, et tient plus facilement dans la fenêtre de contexte de l'IA — voir l'annexe. À n'utiliser qu'après avoir testé l'outil, et à retester aussitôt après.

```
Nettoie ce fichier sans changer son comportement : rien de ce qui marche
ne doit changer, ni à l'écran, ni dans ce que l'outil produit.

Tu peux : supprimer le code inutilisé, regrouper ce qui se répète,
renommer ce qui porte un nom obscur, simplifier ce qui est inutilement
compliqué.

Tu ne peux pas : ajouter de fonctionnalité, retirer de fonctionnalité,
modifier l'apparence, ni introduire une bibliothèque externe.

Renvoie le fichier complet, puis liste en cinq lignes maximum ce que tu as changé et ce que je dois réessayer en priorité pour vérifier que rien
n'est cassé.

Voici le fichier : [collez le contenu complet]
```

---

## Annexe · Quelques notions techniques

### Ce que contient un fichier `.html`

| Couche | Rôle |
|---|---|
| **HTML** | la structure et le contenu |
| **CSS** | la mise en forme |
| **JavaScript** | le comportement et l'interactivité |

Les trois tiennent dans le même document. C'est ce que demande la contrainte « un seul fichier ».

### Pourquoi un seul fichier

| Avantage | Ce que ça change |
|---|---|
| **Autonome** | tout tient dans un document, rien à installer |
| **Portable** | un fichier à envoyer, à sauvegarder, à déposer où vous voulez |
| **Modifiable par une IA** | « voici mon outil, ajoute ceci » suffit |
| **Durable** | rien à mettre à jour quand l'écosystème change |

### Dépendances et CDN

- Une **dépendance** est une bibliothèque externe qui ajoute une capacité à l'outil : graphiques, sélecteur de dates, rendu Markdown.
- Un **CDN** permet de la charger depuis le web au moment où la page s'ouvre, sans rien installer.

C'est commode, et c'est pourquoi les IA en proposent spontanément. Mais une dépendance chargée depuis le web signifie que l'outil **ne fonctionne plus hors ligne**, qu'il **émet une requête vers un tiers** à chaque ouverture, et qu'il **cessera de marcher** le jour où cette adresse change. D'où la contrainte du prompt générique. Si vous acceptez une dépendance, sachez que vous renoncez à ces trois propriétés.

### Rester petit, et pourquoi ça compte avec une IA

Un petit outil est plus facile à comprendre, à corriger et à refaire. Avec une IA, il y a une raison supplémentaire : **le fichier entier tient dans sa fenêtre de contexte**. Le modèle le lit en entier, et peut le régénérer ou le restructurer en une seule opération. Passé une certaine taille, il ne travaille plus que sur des fragments, et c'est là que les corrections se mettent à casser autre chose.

### Versionner son travail

Déposer le fichier dans un dépôt Git (GitHub, GitLab, la Forge des communs...) présente les bénéfices suivants : 

- **sauvegarder sans écraser** : chaque version est conservée et récupérable
- **revenir en arrière** : si une modification casse quelque chose
- **partager** : un lien suffit
- **collaborer** : plusieurs personnes sur le même outil
- **documenter** : l'historique garde la trace des décisions

### Deux prompts pour l'accessibilité

Le prompt générique demande déjà la conformité WCAG 2.2 AA. Ces deux-ci servent à réviser un outil déjà fabriqué : **le premier constate, le second corrige**.

**1. Constater**

```
Évalue l'accessibilité de ce fichier au regard des WCAG 2.2 niveau AA.
Réponds en français, sans jargon, sans renvoyer de code.

Vérifie au moins :
- la langue de la page est déclarée, et la page a un titre explicite
- la structure des titres est hiérarchisée, sans niveau sauté
- chaque champ a une étiquette qui lui est réellement liée, et les
  messages d'erreur sont rattachés au champ concerné
- tout est atteignable et actionnable au clavier, dans un ordre logique,
  sans piège, avec un indicateur de focus visible et non masqué
- les messages d'état — « copié », « enregistré », une erreur — sont
  annoncés aux lecteurs d'écran
- la couleur n'est jamais le seul moyen de distinguer une information
- les contrastes : 4,5:1 pour le texte, 3:1 pour les éléments d'interface
- les cibles cliquables sont assez grandes et assez espacées
- la page reste utilisable à un zoom de 200 % et sur une largeur de téléphone
- les animations respectent une préférence de mouvement réduit

Pour chaque point : le constat, le niveau (critique / majeur / mineur),
et la correction que tu proposes.

Termine par une liste honnête de ce que tu N'AS PAS pu vérifier en lisant
le code seul, et qui demande un essai réel.

Voici le fichier : [collez le contenu complet]
```

**2. Corriger**

```
Corrige les points que tu viens de signaler, en commençant par les plus
graves. Ne change ni le comportement de l'outil, ni son apparence, au-delà
de ce qu'exige la correction.

Renvoie le fichier complet, puis, pour chaque correction, dis en une ligne
ce qu'elle change pour la personne qui utilise l'outil.
```

**Et quatre vérifications que vous seul pouvez faire**, en deux minutes et sans aucun outil : parcourez toute la page à la touche de tabulation, en vérifiant que vous voyez toujours où vous êtes et que vous n'êtes jamais bloqué ; zoomez à 200 % ; réduisez la fenêtre à la largeur d'un téléphone ; et faites une action qui déclenche un message — une copie, une erreur — pour vérifier qu'il se voit. Une relecture par l'IA ne remplace pas un essai réel, et ne vous autorise pas à déclarer l'outil conforme.

---

## Pour aller plus loin

- Un exemple de [**Constructeur d'instructions**](https://github.com/jourde/prompt-builder)
- **D'autres prototypes** par François Jourde — [github.com/jourde](https://github.com/jourde)
- **CréeIAppli**, par Arnaud Champollion — un formulaire qui rédige à votre place le prompt de création d'une application web, et qui va plus loin : stockage du code, test, mise en ligne, choix de licence — [bidouiage.forge.apps.education.fr/creiappli](https://bidouiage.forge.apps.education.fr/creiappli/)
- **EDUVAIBE**, par Marie-Charlotte Hoyer — le même principe, orienté classe : un parcours en sept étapes qui rédige le prompt d'une application pédagogique (quiz, cartes, frise, simulateur) — [mchoyer.forge.apps.education.fr/eduvibe](https://mchoyer.forge.apps.education.fr/eduvibe/)
- Un catalogue sans cesse grandissant d'applications proposées par le personnel éducatif en France : **La Ressourcerie de la Forge des communs numériques éducatifs** — [ressourcerie.forge.apps.education.fr](https://ressourcerie.forge.apps.education.fr/)
- **Conseils de Yann Houry sur le vibe coding** — [ralentirtravaux.com/apps/vibe-coding](https://www.ralentirtravaux.com/apps/vibe-coding/)

**Des questions, ou envie de montrer ce que vous avez fabriqué :** [francois@jourde.dev](mailto:francois@jourde.dev)

---

Cette page, par François Jourde, est mise à disposition selon les termes de la licence [Creative Commons Attribution – Partage dans les Mêmes Conditions 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/deed.fr). Reprenez-la, adaptez-la, diffusez-la : citez la source et gardez la même licence.
