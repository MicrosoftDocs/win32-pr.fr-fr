---
title: Animations Microsoft Agent pour le caractère Robby
description: Animations Microsoft Agent pour le caractère Robby
ms.assetid: 05baf1ab-3217-4da4-9562-6719c58cd744
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347c95fd6a29af72041d3b9e1192167d34602260
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725917"
---
# <a name="microsoft-agent-animations-for-robby-character"></a>Animations Microsoft Agent pour le caractère Robby

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Le [caractère Microsoft Agent Robby](https://www.microsoft.com/downloads/details.aspx?FamilyID=fa36d1d5-d828-494a-ad0a-7b571db5bd2e) est un travail protégé par des droits d’auteur de Microsoft Corporation.

Robby prend en charge les animations indiquées dans le tableau ci-dessous. Reportez-vous à [la rubrique programmation de l’interface du serveur Microsoft Agent](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) et [programmation du contrôle Microsoft Agent](programming-the-microsoft-agent-control.md) pour plus d’informations sur la façon d’appeler les animations du caractère.

Si vous accédez à ces animations de caractères à l’aide du protocole HTTP et de la méthode [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) d' [**obtention**](get-method.md) ou du serveur du contrôle, réfléchissez à la façon dont vous allez les télécharger. Au lieu de télécharger toutes les animations simultanément, vous souhaiterez peut-être d’abord récupérer les animations d’état d' **émission** et de **dictée** . Cela vous permettra d’afficher rapidement le caractère et de le faire parler tout en rapprochant les autres animations de manière asynchrone. En outre, pour garantir le chargement correct des données de caractères et d’animation, utilisez l’événement [**RequestComplete**](requestcomplete-event.md) . En cas d’échec d’une demande de chargement, vous pouvez réessayer de charger les données ou afficher un message approprié.

Si l’animation de **retour** d’une animation est définie à l’aide de branches de sortie, vous n’avez pas besoin de l’appeler explicitement ; Agent lit automatiquement l’animation de **retour** avant l’animation suivante. Toutefois, si une animation de **retour** est listée, vous devez appeler l’animation à l’aide de la méthode [**Play**](play-method.md) avant une autre animation pour fournir une transition lisse. Si aucune animation de **retour** n’est indiquée, l’animation se termine normalement sans avoir besoin d’une animation de transition.

Le fichier de caractères comprend des effets sonores pour certaines animations, comme indiqué dans le tableau suivant. Les effets sonores s’exécutent uniquement si cette option est activée dans la feuille de propriétés de l’agent Microsoft. Vous pouvez également désactiver les effets sonores dans votre application.



| Animation                 | Retourner l’animation         | Prend en charge la parole | Effets sonores | Affecté à l’État                            | Description                                                |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|------------------------------------------------------------|
| **Reconnaître**           | Aucun                     | Non                | **Non**        | Aucun                                         | Tête nœuds                                                  |
| **Alert**                 | Oui, utilisation des branches de sortie | Oui               | **Non**        | **Listen**                                | Redresser                                                |
| **Annoncé**              | Oui, utilisation des branches de sortie | Oui               | **Oui**       | Aucun                                         | Imprime le papier et les rapports                               |
| **Blink**                 | Aucun                     | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Clignoter les yeux                                                |
| **Confus**              | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Tête Scratch                                             |
| **Féliciter**          | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Soulève ensuite les mains                             |
| **Refuser**               | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Soulève des mains et des secousses                                |
| **DoMagic1**              | Aucun                     | Oui               | **Non**        | Aucun                                         | Supprime l’appareil                                             |
| **DoMagic2**              | Oui, utilisation des branches de sortie | Non                | **Oui**       | Aucun                                         | Le bouton enfoncé et le faisceau s’affichent                            |
| **DontRecognize**         | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Tient à l’oreille                                          |
| **Expliquer**               | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Mouvements avec des bras                                         |
| **GestureDown**           | Oui, utilisation des branches de sortie | Oui               | **Non**        | **GesturingDown**                            | Mouvements vers le dessous                                              |
| **GestureLeft**           | Oui, utilisation des branches de sortie | Oui               | **Non**        | **GesturingLeft**                            | Mouvements restants                                              |
| **GestureRight**          | Oui, utilisation des branches de sortie | Oui               | **Non**        | **GesturingRight**                           | Mouvements droite                                             |
| **GestureUp**             | Oui, utilisation des branches de sortie | Oui               | **Non**        | **GesturingUp**                              | Mouvements vers le haut                                                |
| **GetAttention**          | **GetAttentionReturn**   | Oui               | **Non**        | Aucun                                         | Armes vagues                                                 |
| **GetAttentionContinued** | **GetAttentionReturn**   | Oui               | **Non**        | Aucun                                         | Des ondulations de vagues                                           |
| **GetAttentionReturn**    | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                                |
| **Greet**                 | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Contient la main                                              |
| **Audition \_ 1**            | Oui, utilisation des branches de sortie | Non                | **Non**        | **Ouïe**                                  | Inclinaison de l’en-tête à droite ( \* animation de bouclage)                     |
| **Audition \_ 2**            | Oui, utilisation des branches de sortie | Non                | **Non**        | **Ouïe**                                  | En-tête gauche ( \* animation en boucle)                      |
| **Audition \_ 3**            | Oui, utilisation des branches de sortie | Non                | **Non**        | **Ouïe**                                  | Tête de robinet gauche ( \* animation de bouclage)                      |
| **Audition \_ 4**            | Oui, utilisation des branches de sortie | Non                | **Non**        | **Ouïe**                                  | Incliner vers le début ( \* animation de boucle)                      |
| **Masquer**                  | Aucun                     | Non                | **Oui**       | **Masquage**                                   | Disparaît dans la porte                                    |
| **Idle1 \_ 1**              | Aucun                     | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Aperçus à droite                                              |
| **Idle1 \_ 2**              | Aucun                     | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Vue d’ensemble et clignotement                                      |
| **Idle1 \_ 3**              | Aucun                     | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Vue d’ensemble des clignotements et des clignotements                                    |
| **Idle1 \_ 4**              | Aucun                     | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Aperçus de gauche et de clignotement                                    |
| **Idle2 \_ 1**              | Aucun                     | Non                | **Non**        | **IdlingLevel2**                             | Bras des plis                                                 |
| **Idle2 \_ 2**              | Aucun                     | Non                | **Oui**       | **IdlingLevel2**                             | Supprime l’en-tête et effectue un ajustement                          |
| **Idle3 \_ 1**              | Aucun                     | Non                | **Non**        | **IdlingLevel3**                             | Réactions                                                      |
| **Idle3 \_ 2**              | Aucun                     | Non                | **Oui**       | **IdlingLevel3**                             | S’arrête                                                 |
| **LookDown**              | **LookDownReturn**       | Non                | **Non**        | Aucun                                         | Recherche vers le                                                 |
| **LookDownReturn**        | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                                |
| **LookLeft**              | **LookLeftReturn**       | Non                | **Non**        | Aucun                                         | Semble à gauche                                                 |
| **LookLeftReturn**        | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                                |
| **LookRight**             | **LookRightReturn**      | Non                | **Non**        | Aucun                                         | Semble à droite                                                |
| **LookRightReturn**       | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                                |
| **Directes**                | **LookUpReturn**         | Non                | **Non**        | Aucun                                         | Recherche                                                   |
| **LookUpReturn**          | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                                |
| **Descendre**              | Oui, utilisation des branches de sortie | Non                | **Oui**       | **MovingDown**                               | Brusque                                                 |
| **MoveLeft**              | Oui, utilisation des branches de sortie | Non                | **Oui**       | **MovingLeft**                               | À gauche                                                 |
| **MoveRight**             | Oui, utilisation des branches de sortie | Non                | **Oui**       | **MovingRight**                              | À droite                                                |
| **MoveUp**                | Oui, utilisation des branches de sortie | Non                | **Oui**       | **MovingUp**                                 | Envole                                                   |
| **Heureux**               | Oui, utilisation des branches de sortie | Oui               | **Oui**       | Aucun                                         | Sourires et redresser                                  |
| **Processus**               | Non                       | Non                | **Oui**       | Aucun                                         | Appuie sur les boutons, imprime, lit, puis rejette l’impression       |
| **Traitement**            | Oui, utilisation des branches de sortie | Non                | **Oui**       | Aucun                                         | Appuie sur les boutons, imprime, lit, puis rejette l’impression       |
| **Lire**                  | **ReadReturn**           | Oui               | **Oui**       | Aucun                                         | Impressions, lectures et recherches                                |
| **ReadContinued**         | **ReadReturn**           | Oui               | **Oui**       | Aucun                                         | Lectures et recherches                                         |
| **ReadReturn**            | Aucun                     | Non                | **Oui**       | Aucun                                         | Retourne à la position neutre                                |
| **Lecture**               | Oui, utilisation des branches de sortie | Non                | **Oui**       | Aucun                                         | Impressions, lectures et recherches (animation de \* bouclage)          |
| **RestPose**              | Aucun                     | Oui               | **Non**        | **Parlez**                                 | Position neutre                                           |
| **Fer**                   | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Expression Sad                                             |
| **Recherche**                | Non                       | Non                | **Oui**       | Aucun                                         | Affiche la boîte à outils et supprime l’outil                           |
| **Dans**             | Oui, utilisation des branches de sortie | Non                | **Oui**       | Aucun                                         | Affiche la boîte à outils et supprime les outils ( \* animation de bouclage)    |
| **Afficher**                  | Aucun                     | Non                | **Oui**       | **Affichage**                                  | S’affiche via la porte                                    |
| **StartListening**        | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Place à l’oreille                                           |
| **StopListening**         | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Place les mains sur les oreilles                                       |
| **Suggérer**               | Oui, utilisation des branches de sortie | Oui               | **Oui**       | Aucun                                         | Affiche les ampoules                                         |
| **Étonne**             | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Semble surpris                                            |
| **Réflexion**                 | Oui, utilisation des branches de sortie | Oui               | **Oui**       | Aucun                                         | Tête Scratch                                             |
| **Opération en cours**              | Non                       | Non                | **Oui**       | Aucun                                         | Tête Scratch ( \* animation de bouclage)                       |
| **Connaître**             | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Shrugs                                                     |
| **Wave**                  | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Fréquences                                                      |
| **Écrire**                 | **WriteReturn**          | Oui               | **Oui**       | Aucun                                         | Révèle le crayon et le presse-papiers, les écritures et les recherches          |
| **WriteContinued**        | **WriteReturn**          | Oui               | **Oui**       | Aucun                                         | Écritures et recherches                                        |
| **WriteReturn**           | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                                |
| **Écriture**               | Oui, utilisation des branches de sortie | Non                | **Oui**       | Aucun                                         | Révèle le crayon et le presse-papiers, les écritures ( \* animation de bouclage) |



 

\* Si vous lisez une animation de bouclage, vous devez utiliser [**Stop**](stop-method.md) pour la supprimer avant que d’autres animations de la file d’attente du caractère ne soient lues.

 

