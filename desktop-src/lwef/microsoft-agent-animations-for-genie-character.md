---
title: Animations Microsoft Agent pour le caractère génie
description: Animations Microsoft Agent pour le caractère génie
ms.assetid: 56c42d7a-32af-47cb-8578-0a89507a41ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f583fc6540b5fe13cc157542d69352a8ea5b31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381954"
---
# <a name="microsoft-agent-animations-for-genie-character"></a>Animations Microsoft Agent pour le caractère génie

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Le [caractère Microsoft Agent génie](https://www.microsoft.com/downloads/details.aspx?FamilyID=da86ba4e-bc2d-4c1d-b5a0-3183fe206414) est un travail protégé par des droits d’auteur de Microsoft Corporation.

Génie prend en charge les animations indiquées dans le tableau ci-dessous. Reportez-vous à [la rubrique programmation de l’interface du serveur Microsoft Agent](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) et [programmation du contrôle Microsoft Agent](programming-the-microsoft-agent-control.md) pour plus d’informations sur la façon d’appeler les animations du caractère.

Si vous accédez à ces animations de caractères à l’aide du protocole HTTP et de la méthode [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) d' [**obtention**](get-method.md) ou du serveur du contrôle, réfléchissez à la façon dont vous allez les télécharger. Au lieu de télécharger toutes les animations simultanément, vous souhaiterez peut-être d’abord récupérer les animations d’état d' **émission** et de **dictée** . Cela vous permettra d’afficher rapidement le caractère et de le faire parler tout en rapprochant les autres animations de manière asynchrone. En outre, pour garantir le chargement correct des données de caractères et d’animation, utilisez l’événement [**RequestComplete**](requestcomplete-event.md) . En cas d’échec d’une demande de chargement, vous pouvez réessayer de charger les données ou afficher un message approprié.

Si les animations de **retour** d’une animation sont définies à l’aide de branches de sortie, vous n’avez pas besoin de l’appeler explicitement ; Agent lit automatiquement l’animation de **retour** avant l’animation suivante. Toutefois, si une animation de **retour** est listée, vous devez appeler l’animation à l’aide de la méthode [**Play**](play-method.md) avant une autre animation pour fournir une transition lisse. Si aucune animation de **retour** n’est indiquée, l’animation se termine normalement sans avoir besoin d’une animation de transition.

Le fichier de caractères comprend des effets sonores pour certaines animations, comme indiqué dans le tableau suivant. Les effets sonores s’exécutent uniquement si cette option est activée dans la feuille de propriétés de l’agent Microsoft. Vous pouvez également désactiver les effets sonores dans votre application.



| Animation                 | Retourner l’animation         | Prend en charge la parole | Effets sonores | Affecté à l’État                            | Description                                                    |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|----------------------------------------------------------------|
| **Reconnaître**           | Aucun                     | Non                | **Non**        | Aucun                                         | Tête nœuds                                                      |
| **Alert**                 | Oui, utilisation des branches de sortie | Oui               | **Non**        | **Listen**                                | Redresser et déclencher des sourcils                                |
| **Annoncé**              | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Soulève la main                                                    |
| **Blink**                 | Aucun                     | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Clignoter les yeux                                                    |
| **Confus**              | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Tête Scratch                                                 |
| **Féliciter**          | Oui, utilisation des branches de sortie | Oui               | **Oui**       | Aucun                                         | Applauds                                                       |
| **Féliciter \_ 2**       | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Donne un mouvement de pouce vers le haut                                        |
| **Refuser**               | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Soulève des mains et des secousses                                   |
| **DoMagic1**              | Aucun                     | Oui               | **Non**        | Aucun                                         | Se transforme et soulève des mains                                 |
| **DoMagic2**              | Oui, utilisation des branches de sortie | Non                | **Oui**       | Aucun                                         | Réduit les mains, les clouds apparaissent                                    |
| **DontRecognize**         | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Tient à l’oreille                                              |
| **Expliquer**               | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Étend les bras à la côte                                           |
| **GestureDown**           | Oui, utilisation des branches de sortie | Oui               | **Non**        | **GesturingDown**                            | Mouvements vers le dessous                                                  |
| **GestureLeft**           | Oui, utilisation des branches de sortie | Oui               | **Non**        | **GesturingLeft**                            | Mouvements restants                                                  |
| **GestureRight**          | Oui, utilisation des branches de sortie | Oui               | **Non**        | **GesturingRight**                           | Mouvements droite                                                 |
| **GestureUp**             | Oui, utilisation des branches de sortie | Oui               | **Non**        | **GesturingUp**                              | Mouvements vers le haut                                                    |
| **GetAttention**          | **GetAttentionReturn**   | Oui               | **Non**        | Aucun                                         | Armes vagues                                                     |
| **GetAttentionContinued** | **GetAttentionReturn**   | Oui               | **Non**        | Aucun                                         | Des ondulations de vagues                                               |
| **GetAttentionReturn**    | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                                    |
| **Greet**                 | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Sacs                                                           |
| **Audition \_ 1**            | Aucun                     | Non                | **Non**        | **Ouïe**                                  | Ears extend ( \* animation de bouclage)                              |
| **Audition \_ 2**            | Aucun                     | Non                | **Non**        | **Ouïe**                                  | En-tête gauche ( \* animation en boucle)                          |
| **Audition \_ 3**            | Aucun                     | Non                | **Non**        | **Ouïe**                                  | Active la tête gauche ( \* animation de boucle)                          |
| **Audition \_ 4**            | Aucun                     | Non                | **Non**        | **Ouïe**                                  | Active la tête à droite ( \* animation de boucle)                         |
| **Masquer**                  | Aucun                     | Non                | **Oui**       | **Masquage**                                   | Disparaît en fumée                                          |
| **Idle1 \_ 1**              | Aucun                     | Non                | **Non**        | **IdlingLevel1** IdlingLevel2                | Est à l’air                                                   |
| **Idle1 \_ 2**              | Aucun                     | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Vue d’ensemble des bons et des clignotements                                       |
| **Idle1 \_ 3**              | Oui, utilisation des branches de sortie | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Aperçus de gauche et de clignotement                                        |
| **Idle1 \_ 4**              | Aucun                     | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Vue d’ensemble de la droite et des clignotements                             |
| **Idle1 \_ 5**              | Oui, utilisation des branches de sortie | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Vue d’ensemble des clignotements et des clignotements                                        |
| **Idle1 \_ 6**              | Aucun                     | Non                | **Non**        | **IdlingLevel1** **IdlingLevel2**<br/> | Vue d’ensemble et clignotement                                          |
| **Idle2 \_ 1**              | Aucun                     | Non                | **Non**        | **IdlingLevel2**                             | Serpenteurs WISP                                                    |
| **Idle2 \_ 2**              | Oui, utilisation des branches de sortie | Non                | **Non**        | **IdlingLevel2**                             | Révèle le défilement et les lectures                                       |
| **Idle2 \_ 3**              | Oui, utilisation des branches de sortie | Non                | **Non**        | **IdlingLevel2**                             | Révèle le défilement et les écritures                                      |
| **Idle3 \_ 1**              | Aucun                     | Non                | **Oui**       | **IdlingLevel3**                             | Réactions                                                          |
| **Idle3 \_ 2**              | Oui, utilisation des branches de sortie | Non                | **Oui**       | **IdlingLevel3**                             | Passe en veille ( \* animation de bouclage)                             |
| **LookDown**              | **LookDownReturn**       | Non                | **Non**        | Aucun                                         | Recherche vers le                                                     |
| **LookDownBlink**         | **LookDownReturn**       | Non                | **Non**        | Aucun                                         | Clignote en regardant                                            |
| **LookDownReturn**        | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                                    |
| **LookLeft**              | **LookLeftReturn**       | Non                | **Non**        | Aucun                                         | Semble à gauche                                                     |
| **LookLeftBlink**         | **LookLeftReturn**       | Non                | **Non**        | Aucun                                         | Clignoter en regardant à gauche                                            |
| **LookLeftReturn**        | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                                    |
| **LookRight**             | **LookRightReturn**      | Non                | **Non**        | Aucun                                         | Semble à droite                                                    |
| **LookRightBlink**        | **LookRightReturn**      | Non                | **Non**        | Aucun                                         | Clignote en regardant vers la droite                                           |
| **LookRightReturn**       | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                                    |
| **Directes**                | **LookUpReturn**         | Non                | **Non**        | Aucun                                         | Recherche                                                       |
| **LookUpBlink**           | **LookUpReturn**         | Non                | **Non**        | Aucun                                         | Clignotement de la recherche                                              |
| **LookUpReturn**          | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                                    |
| **Descendre**              | Oui, utilisation des branches de sortie | Non                | **Oui**       | **MovingDown**                               | Brusque                                                     |
| **MoveLeft**              | Oui, utilisation des branches de sortie | Non                | **Oui**       | **MovingLeft**                               | À gauche                                                     |
| **MoveRight**             | Oui, utilisation des branches de sortie | Non                | **Oui**       | **MovingRight**                              | À droite                                                    |
| **MoveUp**                | Oui, utilisation des branches de sortie | Non                | **Oui**       | **MovingUp**                                 | Envole                                                       |
| **Heureux**               | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Sourires et conserve les mains                                |
| **Processus**               | Non                       | Non                | **Non**        | Aucun                                         | Tourne dans un Cloud                                             |
| **Traitement**            | Oui, utilisation des branches de sortie | Non                | **Non**        | Aucun                                         | Tourne dans un Cloud ( \* animation de boucle)                       |
| **Lire**                  | **ReadReturn**           | Oui               | **Oui**       | Aucun                                         | Révèle le défilement, les lectures et les recherches                             |
| **ReadContinued**         | **ReadReturn**           | Oui               | **Non**        | Aucun                                         | Lectures et recherches                                             |
| **ReadReturn**            | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                                    |
| **Lecture**               | Oui, utilisation des branches de sortie | Non                | **Oui**       | Aucun                                         | Afficher le défilement et les lectures ( \* animation de bouclage)                  |
| **RestPose**              | Aucun                     | Oui               | **Non**        | **Parlez**                                 | Position neutre                                               |
| **Fer**                   | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Expression Sad                                                 |
| **Recherche**                | Non                       | Non                | **Non**        | Aucun                                         | Révèle les jumelles et les tours                                   |
| **Dans**             | Oui, utilisation des branches de sortie | Non                | **Non**        | Aucun                                         | Affiche des jumelles et des virages ( \* animation de boucle)             |
| **Afficher**                  | Aucun                     | Non                | **Oui**       | **Affichage**                                  | Semble manquer de fumée                                           |
| **StartListening**        | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Place à l’oreille                                               |
| **StopListening**         | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Place les mains sur les oreilles                                           |
| **Suggérer**               | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Affiche les ampoules                                             |
| **Étonne**             | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Semble surpris                                                |
| **Réflexion**                 | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Recherche avec la main sur le menton                                     |
| **Opération en cours**              | Non                       | Non                | **Non**        | Aucun                                         | Recherche avec la main sur le menton ( \* animation de bouclage)               |
| **Connaître**             | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Déplace d’une main vers un menton, autre vers Hip, et déclenche un sourcil approprié |
| **Wave**                  | Oui, utilisation des branches de sortie | Oui               | **Non**        | Aucun                                         | Fréquences                                                          |
| **Écrire**                 | **WriteReturn**          | Oui               | **Oui**       | Aucun                                         | Révèle le défilement, les écritures et les recherches                            |
| **WriteContinued**        | **WriteReturn**          | Oui               | **Oui**       | Aucun                                         | Écritures et recherches                                            |
| **WriteReturn**           | Aucun                     | Non                | **Non**        | Aucun                                         | Retourne à la position neutre                                    |
| **Écriture**               | Oui, utilisation des branches de sortie | Non                | **Oui**       | Aucun                                         | Révèle le défilement, les écritures ( \* animation de bouclage)                   |



 

\* Si vous lisez une animation de bouclage, vous devez utiliser [**Stop**](stop-method.md) pour la supprimer avant que d’autres animations de la file d’attente du caractère ne soient lues.

 

