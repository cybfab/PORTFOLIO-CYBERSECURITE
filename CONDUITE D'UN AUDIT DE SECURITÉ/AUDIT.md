# Évaluation des contrôles et de la conformité  
### Étude de cas

### Cette étude est basée sur une entreprise fictive :

Botium Toys est une petite entreprise américaine qui développe et vend des jouets. L'entreprise dispose d'un seul emplacement physique, qui sert à la fois de bureau principal, de vitrine et d'entrepôt pour ses produits. Cependant, la présence en ligne de Botium Toys s'est développée, attirant des clients aux États-Unis et à l'étranger. En conséquence, le département informatique (IT) est de plus en plus sollicité pour soutenir leur marché en ligne à l'échelle mondiale.

Le responsable du département informatique a décidé qu'un audit informatique interne devait être réalisé. Elle exprime des préoccupations quant à l'absence d'un plan d'action solide pour assurer la continuité des activités et la conformité, alors que l'entreprise se développe. Elle pense qu'un audit interne peut aider à mieux sécuriser l'infrastructure de l'entreprise et à identifier et atténuer les risques, menaces ou vulnérabilités potentiels pour les actifs critiques. Le responsable souhaite également s'assurer que l'entreprise respecte les réglementations relatives au traitement interne et à l'acceptation des paiements en ligne, ainsi qu'à la conduite des affaires dans l'Union européenne (UE).

Le responsable informatique commence par mettre en œuvre le cadre de cybersécurité du National Institute of Standards and Technology (NIST CSF), en établissant l'étendue et les objectifs de l'audit, en listant les actifs actuellement gérés par le département IT et en réalisant une évaluation des risques. Le but de l'audit est de fournir une vue d'ensemble des risques et/ou des amendes que l'entreprise pourrait subir en raison de l'état actuel de sa posture de sécurité.

## Scénario

### Botium Toys : Étendue, Objectifs et Rapport d'évaluation des risques

#### Étendue

L'étendue est définie comme l'ensemble du programme de sécurité de Botium Toys. Cela signifie que tous les actifs doivent être évalués, ainsi que les processus et procédures internes liés à la mise en œuvre des meilleures pratiques en matière de contrôles et de conformité.

#### Objectifs

Évaluer les actifs existants et compléter la liste de vérification des contrôles et de la conformité afin de déterminer les contrôles et les meilleures pratiques à mettre en œuvre pour améliorer la posture de sécurité de Botium Toys.

#### Actifs actuels

Les actifs gérés par le département IT incluent :

- Équipements sur site pour les besoins professionnels au bureau
- Équipements des employés : appareils utilisateurs finaux (ordinateurs de bureau/portables, smartphones), postes de travail à distance, casques, câbles, claviers, souris, stations d'accueil, caméras de surveillance, etc.
- Produits en vitrine disponibles à la vente au détail sur place et en ligne, stockés dans l'entrepôt attenant de l'entreprise
- Gestion des systèmes, logiciels et services : comptabilité, télécommunications, base de données, sécurité, e-commerce et gestion des stocks
- Accès Internet
- Réseau interne
- Conservation et stockage des données
- Maintenance des systèmes obsolètes : systèmes en fin de vie nécessitant une surveillance humaine

#### Évaluation des risques

##### Description des risques

Actuellement, la gestion des actifs est insuffisante. De plus, Botium Toys n'a pas mis en place tous les contrôles nécessaires et pourrait ne pas être pleinement conforme aux réglementations et normes américaines et internationales.

##### Meilleures pratiques de contrôle

La première des cinq fonctions du NIST CSF est **Identifier**. Botium Toys devra consacrer des ressources pour identifier les actifs afin de pouvoir les gérer correctement. En outre, ils devront classer les actifs existants et déterminer l'impact de la perte de ces actifs, y compris des systèmes, sur la continuité des activités.

##### Score de risque

Sur une échelle de 1 à 10, le score de risque est de **8**, ce qui est relativement élevé. Cela est dû à l'absence de contrôles et de respect des meilleures pratiques en matière de conformité.

##### Commentaires supplémentaires

L'impact potentiel de la perte d'un actif est évalué comme **moyen**, car le département IT ne sait pas quels actifs seraient en danger. Le risque pour les actifs ou les amendes des organismes de réglementation est **élevé**, car Botium Toys n'a pas mis en place tous les contrôles nécessaires et ne respecte pas entièrement les meilleures pratiques liées aux réglementations de conformité visant à garder les données critiques privées/sécurisées. Voici quelques détails spécifiques :

### Informations supplémentaires

En cybersécurité, les types de contrôles peuvent être classés de trois manières :

1. **Contrôles administratifs/gestionnaires**
2. **Contrôles techniques**
3. **Contrôles physiques/opérationnels**

Les types de contrôles (fournissant une défense et protégeant les actifs) incluent, mais ne sont pas limités à :

- **Préventifs** (prévenir la survenue d'un incident)
- **Correctifs** (restaurer un actif après un incident)
- **Détectifs** (déterminer si un incident s'est produit ou est en cours)
- **Dissuasifs** (décourager les attaques)

---

## Liste de vérification des contrôles

| Botium Toys a-t-il actuellement ce contrôle en place ? | Contrôle | Explication |
| --- | --- | --- |
| Non | Moindre privilège | Les employés ont accès aux données des clients. Cela doit être modifié pour réduire le risque de violation. |
| Non | Plan de reprise après sinistre | Il n'y a actuellement aucun plan pour gérer les catastrophes. Mettre en place ce plan garantit la continuité des activités. |
| Oui | Pare-feu | L'organisation dispose d'un pare-feu pour bloquer le trafic en fonction d'un ensemble de règles de sécurité définies. |
| ? | Politiques de mot de passe | Une politique de mot de passe existe, mais les exigences sont considérées comme faibles et mettent en danger la gestion de l'accès. |
| Oui | Antivirus | Le logiciel antivirus est actif et régulièrement surveillé par l'équipe IT. |
| Non | Sauvegardes | Comme pour le plan de reprise après sinistre, ils ne sont pas préparés en cas de violation. Ils doivent mettre en œuvre un plan de sauvegarde, qu'il soit incrémental, complet ou partiel. |
| Non | Chiffrement | Cela permettrait de protéger la confidentialité des données. |
| Non | IDS | Cela aiderait l'équipe IT à identifier les intrusions potentielles par des acteurs malveillants. |
| Oui | Vitrine | Bien que l'équipe IT ne soit pas responsable de la gestion de la vitrine, l'organisation doit disposer de serrures adéquates. |
| Oui | CCTV | Cela fonctionne correctement. |
| Oui | Détection d'incendie | L'organisation en dispose. Cependant, l'équipe doit le maintenir et établir un plan d'utilisation. |

---

## Liste de vérification de la conformité

| Botium Toys adhère-t-il actuellement à cette meilleure pratique de conformité ? | Meilleure Pratique | Explication |
| --- | --- | --- |
| Non | Les utilisateurs autorisés ont accès à la carte de crédit des clients. | Actuellement, tous les employés y ont accès, ce qui est une mauvaise pratique pour l'entreprise. |
| Non | La carte de crédit est stockée dans un environnement sécurisé. | Elle n'est pas chiffrée et viole les lois et réglementations. |
| Non | Le chiffrement est sécurisé. | Non, le chiffrement n'a pas encore été mis en place. |
| Non | Les clients de l'UE sont sécurisés. | L'organisation n'applique pas les pratiques du RGPD, ce qui la met en danger d'amende par le gouvernement de l'UE. |
| Oui | Les politiques de confidentialité sont correctement maintenues. | Selon le scénario, cela a été appliqué par les membres de l'équipe IT et le reste du personnel. |

---

### Recommandations (optionnel)

Après avoir examiné la posture de sécurité de Botium Toys, les analystes ont conclu que la pratique de sécurité est loin des attentes. Elle manque de protection de la confidentialité des informations sensibles. Les recommandations sont les suivantes :

- Mise en œuvre du **moindre privilège**
- Établissement d'un **plan de reprise après sinistre**
- Amélioration des **politiques de mot de passe**
- Mise en œuvre du **chiffrement**
- Système de gestion des mots de passe

Pour combler les lacunes en matière de conformité, Botium doit mettre en place et établir les politiques mentionnées ci-dessus. Botium doit également mettre à jour ses actifs afin que des contrôles supplémentaires puissent être identifiés et améliorer ainsi ses pratiques de sécurité.
