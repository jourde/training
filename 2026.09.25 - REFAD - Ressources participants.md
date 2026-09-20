# Fabriquer votre premier outil

**Atelier REFAD du 25 septembre 2026 — Du prompt partagé au codage conversationnel**

**Cette page vous accompagne pendant l'atelier, et vous reste après.** Tous les prompts montrés à l'écran sont ici, prêts à copier.

---

## Chez vous, en quatre étapes

1. Ouvrez l'assistant IA dont vous disposez déjà — celui de votre établissement fait très bien l'affaire.
2. Copiez le **prompt générique** ci-dessous, remplacez les trois zones entre crochets, envoyez.
3. Copiez le code obtenu dans un fichier texte, enregistrez-le sous un nom qui finit par **`.html`**, puis ouvrez-le en double-cliquant dessus. Il s'ouvre dans votre navigateur.
4. Ça ne fait pas exactement ce que vous vouliez ? **C'est normal, et c'est la boucle.** Utilisez le prompt de correction.

**Trois règles, et l'atelier tient dans ces trois lignes.**

- **Les données personnelles suivent le cadre de votre établissement**, pas une règle générale du prompt : un service approuvé et sous contrat peut les autoriser dans les limites de ses conditions, un service grand public non. **Utilisez en priorité les systèmes d'IA explicitement approuvés par votre employeur.** Et pour fabriquer un outil, des exemples fictifs suffisent.
- Jugez l'outil sur **ce qu'il fait quand vous l'utilisez**, jamais sur son code. Vous n'avez pas à lire le code.
- Restez petit. Un outil qui fait une seule chose est plus facile à corriger, à partager, et à refaire entièrement.

---

## 1 · Le prompt générique

**Cinq blocs — et ce ne sont pas ceux du Constructeur.** Les cinq champs du Constructeur d'instructions décrivent *un texte à produire* ; ces cinq blocs-ci décrivent *un outil à fabriquer*. Même logique, autre objet.

Remplacez les trois zones entre crochets. Ne touchez pas au reste.

```
Tu es développeur web. Crée une application web d'une seule page,
dans un SEUL fichier HTML autonome.

# BESOIN
[Décrivez en deux ou trois phrases ce que l'outil doit faire, et pour qui.]

# CE QUE L'UTILISATEUR REMPLIT
[Listez les informations que la personne devra saisir.
Trois ou quatre champs suffisent pour commencer.]

# CE QUE L'OUTIL PRODUIT
[Décrivez le résultat attendu : un texte prêt à copier, un tableau,
un fichier à télécharger...]

# CONTRAINTES TECHNIQUES — à ne pas modifier
- Un seul fichier .html : le HTML, le CSS et le JavaScript sont dedans.
  Aucun fichier séparé.
- Aucune requête réseau, aucune bibliothèque externe, aucun compte utilisateur.
  Le fichier doit fonctionner hors ligne, ouvert directement dans un navigateur.
- Aucune donnée n'est envoyée nulle part : tout reste dans le navigateur.
- Accessible : HTML sémantique, navigation complète au clavier, focus visible,
  contrastes conformes aux WCAG 2.1 niveau AA, libellés associés aux champs.
- Adaptatif, utilisable jusqu'à un zoom de 200 %.
- Interface en français, sobre, sans logo ni image.
- Code court et lisible, sans framework.

# RÉPONSE ATTENDUE
1. Le fichier HTML complet, en un seul bloc de code.
2. Puis, en trois lignes maximum et sans jargon technique : ce que fait l'outil,
   et ce que je dois vérifier en l'essayant.
```

**Le point 2 de la réponse attendue est le plus important.** Il vous donne de quoi juger le résultat sans ouvrir le code.

---

## L'exemple de l'atelier

Les trois zones telles qu'elles ont été remplies pendant l'atelier. C'est ce prompt, et pas un autre, qui a produit l'outil que vous avez vu se construire.

```
# BESOIN
Un formulaire qui aide à rédiger un prompt.

# CE QUE L'UTILISATEUR REMPLIT
Rôle, objectif, public cible, contraintes.

# CE QUE L'OUTIL PRODUIT
Le prompt correspondant, mis à jour au fil de la saisie,
avec un bouton « copier ».
```

*Trois zones, trois phrases. C'est volontaire : un outil qui fait une seule chose se corrige, se partage et se refait.*

### Le prompt complet, prêt à envoyer

Le gabarit ci-dessus, avec ces trois zones à leur place. Copiez-le, collez-le dans votre assistant : vous obtiendrez un outil du même genre que celui de l'atelier.

```
Tu es développeur web. Crée une application web d'une seule page,
dans un SEUL fichier HTML autonome.

# BESOIN
Un formulaire qui aide à rédiger un prompt.

# CE QUE L'UTILISATEUR REMPLIT
Rôle, objectif, public cible, contraintes.

# CE QUE L'OUTIL PRODUIT
Le prompt correspondant, mis à jour au fil de la saisie,
avec un bouton « copier ».

# CONTRAINTES TECHNIQUES — à ne pas modifier
- Un seul fichier .html : le HTML, le CSS et le JavaScript sont dedans.
  Aucun fichier séparé.
- Aucune requête réseau, aucune bibliothèque externe, aucun compte utilisateur.
  Le fichier doit fonctionner hors ligne, ouvert directement dans un navigateur.
- Aucune donnée n'est envoyée nulle part : tout reste dans le navigateur.
- Accessible : HTML sémantique, navigation complète au clavier, focus visible,
  contrastes conformes aux WCAG 2.1 AA, libellés associés aux champs.
- Adaptatif, utilisable jusqu'à un zoom de 200 %.
- Interface en français, sobre, sans logo ni image.
- Code court et lisible, sans framework.

# RÉPONSE ATTENDUE
1. Le fichier HTML complet, en un seul bloc de code.
2. Puis, en trois lignes maximum et sans jargon technique : ce que fait l'outil,
   et ce que je dois vérifier en l'essayant.
```

---

## 2 · Quand ça ne marche pas

```
Voici mon outil : [collez le contenu complet du fichier]

Problème :
- Ce que je voulais : [décrivez]
- Ce qui se passe réellement : [décrivez]

Identifie l'origine du problème et propose la correction la plus petite
possible. Renvoie le fichier complet corrigé, puis dis-moi en trois lignes
ce que tu as changé.
```

**« La correction la plus petite possible »** compte : sans cette consigne, l'IA a tendance à tout réécrire, et à casser autre chose au passage.

---

## 3 · Quand vous voulez ajouter quelque chose

```
Voici mon outil : [collez le contenu complet du fichier]

Ajoute : [décrivez la fonctionnalité en une ou deux phrases].

Ne change rien d'autre. Respecte les contraintes techniques d'origine :
un seul fichier, aucune requête réseau, accessible au clavier.
Renvoie le fichier complet.
```

---

## 4 · Avant de le partager à des collègues

```
Analyse ce fichier et réponds en français, sans jargon technique :
1. Envoie-t-il des données quelque part ?
2. Charge-t-il quelque chose depuis internet ?
3. Est-il utilisable entièrement au clavier, et avec un lecteur d'écran ?
4. Qu'est-ce qui pourrait mal se passer pour quelqu'un qui l'utilise ?

Pour chaque point : le constat, le niveau (critique / majeur / mineur),
et la correction que tu proposes.

Voici le fichier : [collez le contenu complet]
```

**Mettre l'outil sur un réseau d'établissement ne dépend pas de vous.** Cela passe par la personne responsable de l'informatique, qui appliquera ses propres procédures : hébergement, données personnelles, accessibilité, maintenance. Ce que vous pouvez faire, c'est lui présenter l'outil avec les réponses au prompt ci-dessus, car c'est à peu près ce qu'elle vous demandera.

Un fichier que vous ouvrez sur votre ordinateur, ou que vous envoyez à un collègue, ne demande en revanche l'autorisation de personne.

---

## Pour aller plus loin

- **Le Constructeur d'instructions**, montré pendant l'atelier — [à ouvrir directement]({{URL-CONSTRUCTEUR}}) · [le dépôt](https://github.com/jourde/prompt-builder)
- **L'outil construit pendant l'atelier** — {{URL-OUTIL}}
- **D'autres prototypes** — [github.com/jourde](https://github.com/jourde)
- **La Ressourcerie de la Forge des communs numériques éducatifs** — [ressourcerie.forge.apps.education.fr](https://ressourcerie.forge.apps.education.fr/)
- **Conseils de Yann Houry sur le vibe coding** — [ralentirtravaux.com/apps/vibe-coding](https://www.ralentirtravaux.com/apps/vibe-coding/)

**Des questions, ou envie de montrer ce que vous avez fabriqué :** [francois@jourde.dev](mailto:francois@jourde.dev)

---

*Et la suite logique, si l'outil vous sert : donnez-le à un collègue, avec son mode d'emploi. C'est là que le travail d'une personne devient celui d'une équipe.*

---

**Fabriquer votre premier outil**, par François Jourde, est mis à disposition selon les termes de la licence [Creative Commons Attribution – Partage dans les Mêmes Conditions 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/deed.fr). Reprenez-la, adaptez-la, diffusez-la : citez la source et gardez la même licence.
