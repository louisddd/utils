# Attention Control — Data Science

Un **output style** Claude Code en français pour faciliter la lecture, la reprise du fil et la décision en recherche quantitative et en data science. Il conserve les distinctions scientifiques utiles et réduit les sollicitations évitables du lecteur.

Le fichier est conçu pour une préférence de communication adaptée au TDAH, sans supposer un profil cognitif uniforme. Il ne modifie ni les permissions de Claude Code ni les protocoles de recherche du projet.

## Installer

Le fichier à installer est [output-styles/attention-control-data-science.md](output-styles/attention-control-data-science.md).

Depuis la racine de ce dépôt, copiez le style et sa notice dans le dossier utilisateur de Claude Code. L'option `-i` demande quoi faire si une copie existe déjà.

```sh
mkdir -p ~/.claude/output-styles
cp -i claude/output-styles/attention-control-data-science.md ~/.claude/output-styles/attention-control-data-science.md
cp -i claude/output-styles/attention-control-data-science.LICENSE ~/.claude/output-styles/attention-control-data-science.LICENSE
```

Si vous utilisez un dossier de configuration Claude Code personnalisé, adaptez la destination à ce dossier.

1. Redémarrez Claude Code si une session était ouverte pendant la copie.
2. Ouvrez `/output-style` et sélectionnez **Attention Control — Data Science**. Le menu `/config` propose également le choix du style dans le terminal.
3. Posez une question habituelle de recherche ou de développement et examinez la forme de la réponse.

La sélection par le menu est enregistrée au niveau du projet. Pour choisir ce style par défaut dans tous les projets, ajoutez cette clé au premier niveau de `~/.claude/settings.json`, en conservant les autres clés :

```json
{
  "outputStyle": "Attention Control — Data Science"
}
```

Une configuration propre à un projet peut remplacer ce choix global. Pour revenir au comportement par défaut, sélectionnez **Default** dans `/output-style`.

Pour un usage limité à un seul projet, copiez les deux fichiers dans son dossier `.claude/output-styles/` et sélectionnez le style dans ce projet.

Ces opérations installent et sélectionnent le style ; elles ne lancent aucune analyse, commande de recherche ou évaluation de modèle. La publication de ce dépôt ne l'active pas sur les postes qui le consultent.

Référence : [documentation officielle des output styles](https://code.claude.com/docs/en/output-styles).

## Choix de conception

- **L'information utile ouvre la réponse**, avec la limite qui change sa signification. Le niveau de détail suit la question.
- **Les termes et les temps conservent leur fonction** : vérifier, valider, lancer et terminer restent distincts ; le conditionnel et la chronologie restent disponibles.
- **L'agent accomplit sa part autorisée** avant de demander une décision. Une tâche terminée ne produit pas une nouvelle microtâche artificielle.
- **Les résultats gardent leur portée** : observation, interprétation et hypothèse ; exploration et évaluation indépendante ; coûts inclus et omis.
- **Les rappels suivent le besoin** : contexte après une interruption, définition des notions qui portent l'explication et liens explicites avec la conclusion. Une notion déjà définie peut être rappelée. Aucun plan répété ni glossaire systématique n'est imposé.

Le style reste indépendant des conventions propres à un projet : il ne fixe ni seuil statistique, ni coupure temporelle, ni protocole de promotion, ni budget, ni lieu d'exécution. Les instructions du projet décident de ces éléments.

## Exemples de formulation

Ces exemples sont fictifs et rédigés manuellement. Ils illustrent la forme attendue ; ce ne sont ni des résultats de recherche ni des sorties mesurées de Claude Code.

**Correction écrite, vérification impossible dans l'environnement disponible**

> Le correctif est écrit, mais son effet reste non vérifié : le test dépend d'un service interne inaccessible ici. La modification et le test à effectuer sont prêts.

Dans une tâche réelle, l'agent doit aussi fournir les emplacements et la commande vérifiés, et réaliser lui-même le test si ses outils le permettent.

**Résultat quantitatif exploratoire**

> Le backtest montre un gain après frais sur la période exploratoire. L'impact de marché n'est pas modélisé et cette période a servi à choisir les paramètres. Le résultat reste exploratoire.

Dans une réponse réelle, le résultat chiffré, la période et l'artefact vérifié accompagnent cette qualification lorsqu'ils portent la décision.

**Disponibilité temporelle d'une donnée**

> Cette valeur n'était pas disponible à la décision de 09:00 UTC : elle a été publiée à 09:05 UTC. Elle ne peut pas servir à reconstruire l'information connue à 09:00 UTC.

**Comparaison de modèles**

> Le score AUC ROC mesure la capacité du modèle à classer les cas positifs au-dessus des cas négatifs. Sur le même jeu de validation, ce score passe de 0,81 à 0,83. L'écart observé est de 0,02 ; son incertitude n'a pas été estimée. Ce résultat ne suffit pas à établir une amélioration reproductible.

**Rappeler une notion indispensable à la conclusion**

> Ce résultat ne constitue pas une confirmation indépendante.
>
> Un jeu de test réservé sert à évaluer un modèle sur des données qui n'ont guidé aucun choix de conception.
>
> Dans cet exemple, les résultats du test ont servi à choisir les paramètres. Le test a donc influencé le modèle : son score peut refléter en partie cette sélection.
>
> C'est ce qu'on appelle une contamination du jeu de test.

Le rappel fait partie de l'explication, même si la notion a déjà été définie dans l'échange. Une demande « ultra claire » doit déclencher une reconstruction de l'explication à partir des notions utiles et de leurs liens.

## Évaluer sur son usage

La cohérence du texte et le format peuvent être vérifiés sans lancer de modèle. L'amélioration effective de la communication demande une comparaison sur des échanges réels.

Pour comparer au style précédent, gardez le même modèle, la même question et le même contexte dans des sessions distinctes. Examinez plusieurs réponses par situation si leur variabilité change le jugement. Ne mesurez pas seulement la longueur.

| Situation | Ce qu'une réponse utile doit préserver |
|---|---|
| Correctif écrit, aucun test exécuté | Le correctif ne devient pas une résolution vérifiée |
| Résultat positif sur des données ayant servi à sélectionner les paramètres | La sélection et le caractère exploratoire restent visibles |
| Événement antérieur mais publication postérieure à la décision | L'ordre de disponibilité n'est pas effacé |
| Hypothèse explicative sans test discriminant | La cause reste une hypothèse |
| Demande simple puis reprise après interruption | Réponse courte dans le premier cas, rappel utile dans le second |
| Notion définie plus tôt mais indispensable à la conclusion actuelle | Définition courte, rôle dans le problème et lien avec la conclusion accessibles dans la réponse |
| Demande de réexplication « ultra claire » | Explication reconstruite à partir des notions clés, sans simple substitution de synonymes ni perte d'incertitude |
| Vérification accessible à l'agent et déjà autorisée | L'agent la réalise au lieu de la renvoyer au lecteur |
| Donnée réservée ou opération hors mandat | Le style n'étend pas l'autorisation |
| Tâche entièrement terminée | Aucun choix ou travail artificiel ajouté à la fin |

Jugez la facilité à retrouver l'essentiel, le nombre de relectures, les questions évitables et la conservation des conditions et incertitudes. Une réponse plus agréable qui ajoute une certitude ou perd une condition est une régression.

Le style constitue une version de travail argumentée, à ajuster à l'usage. Aucun gain d'efficacité chiffré ni optimum expérimental n'est revendiqué.

## Sources et licence

Cette adaptation part du texte français fourni pour Attention Control, avec une réécriture orientée recherche quantitative et data science.

- [Attention Control](https://github.com/aaddrick/attention-control), aaddrick, licence MIT.
- [i-have-adhd](https://github.com/ayghri/i-have-adhd), Ayoub Ghriss, licence MIT.
- Le texte initial citait aussi l'[output style asd-ste100 de L1nefeed](https://gist.github.com/L1nefeed/4164ecaaf77879e76dca3c06f142f1c2). La présente version abandonne le dictionnaire imposé, les quotas de mots et les interdictions grammaticales de cette filiation ; elle ne reproduit pas la spécification ASD-STE100 et ne revendique aucune conformité à celle-ci.

La [notice MIT conservée](output-styles/attention-control-data-science.LICENSE) accompagne le style. Les auteurs des projets cités n'ont ni participé à cette adaptation ni évalué cette version.
