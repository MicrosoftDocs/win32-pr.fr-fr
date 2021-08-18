---
title: États de l’agent
description: États de l’agent
ms.assetid: 8c3c5b12-81af-4ba5-b834-9f0a7ff5d075
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbfb927cbe9ad703e733caa827df7c5a63bac67b93d49edbb8f59884c89b6ee7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976799"
---
# <a name="agent-states"></a>États de l’agent

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Les services d’animation Microsoft Agent lisent automatiquement certaines animations pour vous. Par exemple, lorsque vous utilisez des commandes [**MoveTo**](moveto-method.md) ou [**GestureAt**](gestureat-method.md) , les services d’animation jouent une animation appropriée. De même, après le délai d’inactivité, les services lisent automatiquement les animations. Pour prendre en charge ces États, vous pouvez définir les animations appropriées, puis les assigner aux États. Vous pouvez toujours lire toute animation que vous définissez directement à l’aide de la méthode [**Play**](play-method.md) , même si vous l’affectez à un État.

Vous pouvez affecter plusieurs animations au même État, et les services d’animation choisissent l’une de vos animations de manière aléatoire. Cela permet à votre caractère d’exposer une variété beaucoup plus naturelle dans son comportement.

Bien que les animations que vous attribuez aux États puissent inclure des frames de branchement, évitez les animations de boucle (animations qui se définissent indéfiniment). Dans le cas contraire, vous devrez utiliser la méthode [**Stop**](play-method.md) avant de pouvoir lire une autre animation.

Il est important de définir et d’assigner au moins une animation pour chaque État qui se produit pour le caractère. Si vous ne fournissez pas ces animations et attributions d’État, votre caractère peut ne pas sembler se comporter de manière appropriée à l’utilisateur. Toutefois, si un État ne se produit pas pour un caractère particulier, vous n’avez pas besoin d’affecter une animation à cet État. Par exemple, si votre application hôte n’appelle jamais la méthode [**MoveTo**](moveto-method.md) , vous pouvez ignorer la création et l’affectation d’animations d’état de **déplacement** .



| État              | Exemple d’utilisation                                                                         |
|--------------------|----------------------------------------------------------------------------------------|
| **GesturingDown**  | Lors du traitement de la méthode d’animation [**GestureAt**](gestureat-method.md) .          |
| **GesturingLeft**  | Lors du traitement de la méthode d’animation [**GestureAt**](gestureat-method.md) .          |
| **GesturingRight** | Lors du traitement de la méthode d’animation [**GestureAt**](gestureat-method.md) .          |
| **GesturingUp**    | Lors du traitement de la méthode d’animation [**GestureAt**](gestureat-method.md) .          |
| **Ouïe**        | Lorsque le début de l’entrée parlée est détecté.                                        |
| **Masquage**         | Lorsque l’utilisateur ou l’application masque le caractère.                                  |
| **IdlingLevel1**   | Lorsque le caractère commence à l’état **ralenti** .                                        |
| **IdlingLevel2**   | Lorsque le caractère commence le deuxième État de niveau de **ralenti** .                           |
| **IdlingLevel3**   | Lorsque le caractère commence à l’état de niveau de **ralenti** final.                            |
| **Listen**      | Lorsque le caractère commence à écouter (l’utilisateur appuie d’abord sur la touche d’accès rapide d’entrée vocale). |
| **MovingDown**     | Lorsque la méthode d’animation [**MoveTo**](moveto-method.md) est traitée.                |
| **MovingLeft**     | Lorsque la méthode d’animation [**MoveTo**](moveto-method.md) est traitée.                |
| **MovingRight**    | Lorsque la méthode d’animation [**MoveTo**](moveto-method.md) est traitée.                |
| **MovingUp**       | Lorsque la méthode d’animation [**MoveTo**](moveto-method.md) est traitée.                |
| **Affichage**        | Lorsque l’utilisateur ou l’application affiche le caractère.                                  |
| **Parlez**       | Lors du traitement de la méthode d’animation [**Speak**](speak-method.md) .                  |



 

### <a name="the-hearing-and-listening-states"></a>États d’audition et d’écoute

L’animation que vous affectez à l’état d' **écoute** est lue lorsque l’utilisateur appuie sur la touche d’accès rapide pour l’entrée vocale. Créez et assignez une petite animation qui rend le caractère précis. De même, définissez son animation de **retour** sur une durée réduite afin que le caractère joue son animation d’état **auditif** lorsque l’utilisateur parle. Une animation d’état **auditif** doit également être brève et conçue pour permettre à l’utilisateur de savoir que le personnage écoute activement ce que l’utilisateur prétend. Les inclinaisons de la tête ou d’autres légers mouvements sont appropriés. Pour fournir une variabilité naturelle, fournissez plusieurs animations d’état **auditif** .

### <a name="the-gesturing-states"></a>États gesturing

Vous devez créer et assigner des animations d’état **gesturing** uniquement si vous envisagez d’utiliser la méthode [**GestureAt**](gestureat-method.md) . Les animations d’état **gesturing** jouent quand Microsoft Agent traite un appel à la méthode **GestureAt** . Si vous définissez des superpositions de bouche pour vos animations d’état **gesturing** , le caractère peut parler comme des mouvements.

Les services d’animation déterminent l’emplacement du caractère et sa relation avec l’emplacement des coordonnées spécifiées dans la méthode, et lisent une animation appropriée. La direction gesturing est toujours en ce qui concerne le caractère ; par exemple, **GestureRight** doit être un geste vers le droit du caractère.

### <a name="the-showing-and-hiding-states"></a>États d’émission et de masquage

Les États d' **affichage** et de **masquage** lisent les animations affectées lorsque l’utilisateur ou l’application hôte demande d’afficher ou de masquer le caractère. Ces États définissent également de manière appropriée l’état **visible** du cadre de caractère. Lors de la définition d’animations pour ces États, gardez à l’esprit qu’un caractère peut apparaître ou s’arrêter à n’importe quel emplacement de l’écran. Étant donné que l’utilisateur peut afficher ou masquer n’importe quel caractère, prenez toujours en charge au moins une animation pour ces États.

Les animations que vous affectez à l’état d' **exposition** se terminent généralement par un frame contenant l’image de la position neutre du caractère. À l’inverse, le **masquage** des animations d’état commence généralement par la position neutre. L' **illustration** et le **masquage** des animations d’État peuvent inclure un frame vide au début ou à la fin, respectivement, pour fournir une transition à partir de l’état actuel du caractère.

### <a name="the-idling-states"></a>États de ralenti

Les États de **ralenti** sont progressifs. Les services d’animation commencent à utiliser les assignations de niveau 1 pour la première période d’inactivité et utilisent les animations de niveau 2 pour la seconde. Après cela, le cycle inactif progresse vers les animations de niveau 3 affectées et reste dans cet État jusqu’à l’annulation, par exemple lors du démarrage d’une nouvelle demande d’animation.

Concevez des animations pour les États **ralentis** afin de communiquer l’état du personnage, mais pas de distraire l’utilisateur. Les animations doivent refléter de manière appropriée la réactivité du caractère en mode discret mais clair. Par exemple, les parcourants ou les clignotements sont de bonnes animations à assigner à l’état **IdlingLevel1** . La lecture des animations fonctionne bien pour l’état **IdlingLevel2** . Le sommeil ou l’écoute de musique avec casque sont de bons exemples d’animations à assigner à l’état **IdlingLevel3** . Les animations qui incluent un grand nombre ou de grands mouvements ne sont pas adaptées aux animations inactives, car elles attirent l’attention de l’utilisateur. Étant donné que les animations d’état **ralenti** sont jouées fréquemment, fournissez plusieurs animations d’état **ralenti** , en particulier pour les États **IdlingLevel1** et **IdlingLevel2** .

Notez qu’une application peut désactiver le traitement d’inactivité automatique d’un caractère et gérer l’état de **ralenti** du caractère lui-même. Les États de **ralenti** des agents sont conçus pour vous aider à éviter toute situation dans laquelle le caractère n’a pas d’animation à lire. Une image de caractère qui ne change pas après un bref laps de temps est comme une application qui affiche un pointeur d’attente pendant une longue période, ce qui désigne le sens de la sensation et de l’interactivité. La maintenance de l’illusion n’est pas très importante : parfois, il s’agit simplement d’un clignotement animé, d’un souffle visible ou d’un décalage de corps.

### <a name="the-speaking-state"></a>État parlant

Les services d’animation utilisent l’état de **parole** lorsqu’une animation de parole est introuvable pour l’animation actuelle. Assigner une animation simple parlant à cet État. Par exemple, vous pouvez utiliser un cadre unique constitué de la position neutre du caractère avec des superpositions de bouche.

### <a name="the-moving-states"></a>États mobiles

Les États **mobiles** jouent quand une application appelle la méthode [**MoveTo**](moveto-method.md) . Les services d’animation déterminent l’animation à lire en fonction de l’emplacement actuel du caractère et des coordonnées spécifiées. La direction du mouvement est basée sur la position du caractère. Par conséquent, l’animation que vous affectez à l’animation **MovingLeft** doit être basée sur le caractère gauche du caractère. Si vous n’utilisez pas la méthode **MoveTo** , vous pouvez ignorer la création et l’affectation d’une animation.

Les animations d’état de **déplacement** doivent animer le caractère dans sa position mobile. La dernière image de cette animation s’affiche lorsque l’image du caractère est déplacée à l’écran. Il n’existe aucune prise en charge pour animer le caractère pendant le déplacement de son frame.

### <a name="standard-animation-set"></a>Ensemble d’animations standard

Bien que vous puissiez concevoir un caractère personnalisé pour avoir les animations que vous souhaitez utiliser, Microsoft Agent définit un ensemble d’animations standard. Les caractères conformes à cette définition peuvent être sélectionnés comme caractère par défaut.

Le tableau suivant répertorie les animations incluses dans le jeu d’animations standard. Même si vous créez un caractère personnalisé, vous souhaiterez peut-être utiliser la liste comme guide pour concevoir vos propres caractères. Les caractères qui prennent en charge l’ensemble d’animations standard doivent prendre en charge au moins les animations suivantes.



| Animation                        | Exemple d’utilisation                                                                                           | Exemple d’animation                                                                                                                                                                                                      |
|----------------------------------|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Reconnaître**                  | Lorsque le caractère accuse réception de la demande de l’utilisateur.                                                      | Caractère nœuds ou clignotement « OK ». Notez que cette animation doit retourner le caractère à sa position neutre.<br/>                                                                                  |
| **Alerte**<sup>1, 2</sup>          | Lorsque le caractère attend des instructions, généralement joué lorsque l’utilisateur active le mode d’écoute. | Les caractères sont des faces avant, respiratoires, clignotants occasionnellement, mais en attente d’instructions.                                                                                                                             |
| **Annoncer**<sup>1, 2</sup>       | Lorsque le caractère a trouvé des informations pour l’utilisateur.                                                   | Des mouvements de caractères en déclenchant des sourcils et main ou en ouvrant une enveloppe.                                                                                                                                                  |
| **Blink**                        | Lorsque le caractère se termine ou est inactif.                                                            | Le caractère clignote naturellement les yeux.                                                                                                                                                                                       |
| **Confus**<sup>1, 2</sup>       | Lorsque le caractère ne comprend pas ce que vous devez faire.                                                        | Début des personnages.                                                                                                                                                                                              |
| **Féliciter**<sup>1, 2</sup>   | Lorsque le caractère ou l’utilisateur termine une tâche (forme plus puissante de l’animation de **reconnaissance** ).          | Le caractère effectue un geste de félicitation, transmet « Oui ! »                                                                                                                                                              |
| **Refuser**<sup>1, 2</sup>        | Lorsque le caractère ne peut pas faire ou refuser la demande de l’utilisateur.                                             | Le caractère tremble, transmet « non possible ».                                                                                                                                                                            |
| **DoMagic1**                     | Le caractère se prépare à afficher un résultat.                                                                 | Ondulations de caractères mains ou baguette.                                                                                                                                                                                         |
| **DoMagic2**                     | L’affichage des caractères se termine par un caractère.                                                                | Le caractère se termine par Magic geste.                                                                                                                                                                                     |
| **DontRecognize**<sup>1, 2</sup>  | Lorsque le caractère ne reconnaît pas la demande de l’utilisateur.                                                  | Le caractère est la main à l’oreille.                                                                                                                                                                                           |
| **Expliquer**<sup>1, 2</sup>        | Lorsque le caractère explique un événement à l’utilisateur.                                                       | Gestes de caractère comme si vous expliquiez quoi que ce soit.                                                                                                                                                                         |
| **GestureDown**<sup>1, 2</sup>    | Lorsque le caractère doit pointer vers une valeur inférieure à celle-ci.                                                 | Le caractère pointe vers le dessous.                                                                                                                                                                                                 |
| **GestureLeft**<sup>1, 2</sup>    | Lorsque le caractère doit pointer vers un point de gauche.                                              | Points de caractère avec gauche ou morphes en une flèche pointant vers la gauche.                                                                                                                                                 |
| **GestureRight**<sup>1, 2</sup>   | Lorsque le caractère doit pointer vers un point de droite.                                             | Points de caractère avec la main droite ou courbes dans une flèche pointant vers la droite.                                                                                                                                               |
| **GestureUp**<sup>1, 2</sup>      | Lorsque le caractère doit pointer vers une valeur supérieure à celle-ci.                                                 | Caractère vers le haut.                                                                                                                                                                                                   |
| **GetAttention**                 | Lorsque le caractère doit avertir l’utilisateur des éléments importants.                                   | Ondulations de caractères mains ou sauts vers le haut et vers le haut.                                                                                                                                                                            |
| **GetAttentionContinued**        | Pour insister sur l’importance de la notification.                                                         | Continuation ou répétition du mouvement initial.                                                                                                                                                                       |
| **GetAttentionReturn**           | Lorsque le caractère termine l’animation **GetAttention** ou **GetAttentionContinued** .                | Le caractère revient à sa position neutre.                                                                                                                                                                             |
| **Salue**<sup>1, 2</sup>          | Lorsque l’utilisateur démarre le système.                                                                      | Sourires et vagues de caractères.                                                                                                                                                                                            |
| **Hearing1**                     | Lorsque le caractère entend le début d’un énoncé oral (écoute active).                           | Les caractères se rapprochent de la nœuds, ou activent la réponse à l’entrée vocale. Remarque : cette animation effectue une boucle sur un cadre intermédiaire qui se produit après le déplacement du caractère vers une position appropriée.<br/>   |
| **Hearing2**                     | Lorsque le caractère entend le début d’un énoncé oral (écoute active).                           | Autre variation du type d’animation utilisé dans **Hearing1** Remarque : cette animation effectue une boucle sur un cadre intermédiaire qui se produit après le déplacement du caractère vers une position appropriée.<br/>                      |
| **Masquer**                         | Lorsque l’utilisateur ignore le caractère.                                                                   | Le caractère s’efface automatiquement de l’écran.                                                                                                                                                                                    |
| **Idle1 \_ 1**                     | Lorsque le caractère n’a pas de tâche et que l’utilisateur n’interagit pas avec le caractère.                       | Le caractère clignote ou regarde, reste dans ou retourne à la position neutre.                                                                                                                                   |
| **Idle1 \_ 2**                     | Lorsque le caractère n’a pas de tâche et que l’utilisateur n’interagit pas avec le caractère.                       | Autre variation du type d’animation utilisé dans **Idle1 \_ 1**.                                                                                                                                                       |
| **Idle2 \_ 1**                     | Lorsque le caractère est inactif pendant un certain temps.                                                          | Caractère réactions ou lit le magazine restant dans ou revenant à la position neutre.                                                                                                                                   |
| **Idle2 \_ 2**                     | Lorsque le caractère est inactif pendant un certain temps.                                                          | Autre variation du type d’animation utilisé dans **Idle2 \_ 1**.                                                                                                                                                       |
| **Idle3 \_ 1**                     | Lorsque le caractère est inactif pendant une longue période.                                                        | Réactions de caractères.                                                                                                                                                                                                       |
| **Idle3 \_ 2**                     | Lorsque le caractère est inactif pendant une longue période.                                                        | Les caractères sont mis en veille ou s’insèrent sur un casque pour écouter de la musique. Remarque : cette animation effectue une boucle sur un cadre intermédiaire qui se produit après le déplacement du caractère vers une position appropriée.<br/>                          |
| **LookDown**                     | Lorsque le caractère doit être recherché.                                                                   | Le caractère ressemble à.                                                                                                                                                                                                  |
| **LookLeft**                     | Quand le caractère doit ressembler à gauche.                                                                   | Le caractère se présente à gauche.                                                                                                                                                                                           |
| **LookRight**                    | Lorsque le caractère doit s’afficher à droite.                                                                  | Le caractère se présente à droite.                                                                                                                                                                                          |
| **Directes**                       | Lorsque le caractère doit être recherché.                                                                     | Recherche d’un caractère.                                                                                                                                                                                                    |
| **Descendre**                     | Lorsque le caractère se prépare à descendre.                                                                | Transitions de caractères vers la position de marche/vol.                                                                                                                                                               |
| **MoveLeft**                     | Lorsque le caractère se prépare à se déplacer vers la gauche.                                                                | Transitions de caractères vers la position gauche de marche/vol.                                                                                                                                                               |
| **MoveRight**                    | Lorsque le caractère se prépare à se déplacer vers la droite.                                                               | Transitions de caractères vers la position de droite de marche/vol.                                                                                                                                                              |
| **MoveUp**                       | Lorsque le caractère se prépare au déplacement vers le haut.                                                                  | Transitions de caractères vers la position de marche/vol.                                                                                                                                                                 |
| **Heureux**<sup>1, 2</sup>        | Lorsque le caractère est heureux avec la demande ou le choix de l’utilisateur.                                         | Sourires de caractères.                                                                                                                                                                                                      |
| **Processus**                      | Lorsque le caractère effectue un certain type de tâche générique.                                                   | Le caractère appuie sur les boutons ou utilise un type d’outil.                                                                                                                                                                   |
| **Traitement**                   | Lorsque le caractère est occupé à travailler sur une tâche générique.                                                    | Griffonnages de caractères sur le bloc de papier ou utilise un type d’outil. Remarque : cette animation effectue une boucle sur un cadre intermédiaire qui se produit après le déplacement du caractère vers une position appropriée.<br/>                      |
| **Lecture**                         | Lorsque le caractère lit un résultat pour l’utilisateur.                                                          | Le caractère affiche le livre ou le papier, lit et regarde à l’utilisateur.                                                                                                                                                       |
| **ReadContinued**                | Lorsque le caractère est lu à l’utilisateur.                                                            | Les lectures de caractères s’affichent à nouveau, puis reviennent à l’utilisateur.                                                                                                                                                                        |
| **ReadReturn**                   | Lorsque le caractère termine l’animation **Read** ou **ReadContinued** .                                | Le caractère revient à sa position neutre.                                                                                                                                                                             |
| **Lecture**                      | Lorsque le caractère lit une valeur, mais ne peut pas accepter d’entrée.                                              | Lectures de caractères à partir d’une feuille de papier. Remarque : cette animation effectue une boucle sur un ou plusieurs frames intermédiaires qui se produisent après le déplacement du caractère vers une position appropriée.<br/>                                           |
| **RestPose**                     | Lorsque le caractère parle de sa position neutre.                                                     | Le caractère correspond à la position souple mais précis.                                                                                                                                                                   |
| **Sad**<sup>1, 2</sup>            | Lorsque le caractère est déçu par le choix de l’utilisateur.                                               | Les caractères mécontents ou semblent déçus.                                                                                                                                                                                |
| **action**                       | Quand caractère recherche un caractère.                                                                   | Le caractère est aléatoire dans un tiroir de fichier ou un autre conteneur à la recherche d’éléments.                                                                                                                                       |
| **Dans**                    | Quand caractère recherche des informations spécifiées par l’utilisateur.                                              | Le caractère est aléatoire dans un tiroir de fichier ou un autre conteneur à la recherche d’éléments. Remarque : cette animation effectue une boucle sur un ou plusieurs frames intermédiaires qui se produisent après le déplacement du caractère vers une position appropriée.<br/> |
| **Afficher**                         | Lorsque le caractère démarre ou est retourné après avoir été convoqué.                                            | Les caractères s’affichent à l’écran dans le souffle d’une fumée, des poutres ou des parcours à l’écran.                                                                                                                                                    |
| **StartListening**<sup>1, 2</sup> | Lorsque le caractère est à l’écoute.                                                                         | Le caractère place à l’oreille.                                                                                                                                                                                            |
| **StopListening**<sup>1, 2</sup>  | Lorsque le caractère cesse d’écouter.                                                                      | Le caractère pose des mains sur les oreilles.                                                                                                                                                                                        |
| **Suggérer**<sup>1, 2</sup>        | Lorsque le caractère contient un Conseil ou une suggestion pour l’utilisateur.                                                 | L’ampoule apparaît en regard de caractère.                                                                                                                                                                                  |
| **Surpris**<sup>1, 2</sup>      | Lorsque le caractère est surpris par l’action ou le choix de l’utilisateur.                                          | Le caractère élargit les yeux, ouvre la bouche.                                                                                                                                                                                    |
| <sup>1, 2</sup>          | Lorsque le caractère envisage un caractère.                                                          | Le caractère s’affiche et reste en tête.                                                                                                                                                                             |
| **Incertaine**<sup>1, 2</sup>      | Lorsque le caractère a besoin que l’utilisateur confirme une demande.                                                  | Le caractère ressemble à un quiz, porte (« êtes-vous sûr ? »)                                                                                                                                                                   |
| **Vague**<sup>1, 2</sup>           | Lorsque l’utilisateur choisit d’arrêter le serveur ou le système.                                                 | Vagues de caractères bonne-Bye ou Hello.                                                                                                                                                                                     |
| **Écriture**                        | Lorsque le caractère est à l’écoute des instructions de l’utilisateur.                                          | Le caractère affiche le papier, écrit et regarde l’utilisateur.                                                                                                                                                              |
| **WriteContinued**               | Lorsque le caractère continue à écouter les instructions de l’utilisateur.                                   | Les caractères écrits sur une feuille de papier et remontent à l’utilisateur.                                                                                                                                                           |
| **WriteReturn**                  | Lorsque le caractère termine l’animation **Write** ou **WriteContinued** .                              | Le caractère revient à sa position neutre.                                                                                                                                                                             |
| **Écriture**                      | Lorsque le caractère écrit des informations pour l’utilisateur.                                                  | Écriture de caractères sur la feuille de papier. Remarque : cette animation effectue une boucle.<br/>                                                                                                                                             |



 

  L’animation nécessite des superpositions de bouche et une image de parole définie.

  L’animation nécessite une animation de retour assignée en fonction de sa branche de sortie ou d’une animation de retour explicite.

En outre, un caractère doit avoir les assignations d’État suivantes.



| État          | Animations requises                           |
|----------------|-----------------------------------------------|
| GesturingDown  | GestureDown                                   |
| GesturingLeft  | GestureLeft                                   |
| GesturingRight | GestureRight                                  |
| GesturingUp    | GestureUp                                     |
| Ouïe        | Hearing1, Hearing2                            |
| Masquage         | Masquer                                          |
| IdlingLevel1   | Blink, Idle1 \_ 1, Idle1 \_ 2                     |
| IdlingLevel2   | Blink, Idle1 \_ 1, Idle1 \_ 2, Idle2 \_ 1, Idle2 \_ 2 |
| IdlingLevel3   | Idle3 \_ 1, Idle3 \_ 2                            |
| Listen      | Alerte                                         |
| MovingDown     | Descendre                                      |
| MovingLeft     | MoveLeft                                      |
| MovingRight    | MoveRight                                     |
| MovingUp       | MoveUp                                        |
| Affichage        | Afficher                                          |
| Parlez       | RestPose                                      |



 

 

 





