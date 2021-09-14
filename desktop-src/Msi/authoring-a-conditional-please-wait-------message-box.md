---
description: L’exemple suivant montre comment créer une boîte de message conditionnelle qui s’affiche et avertit l’utilisateur qu’une tâche en arrière-plan est toujours en cours d’exécution chaque fois que l’utilisateur active un contrôle affiché prématurément.
ms.assetid: 4a99a96b-50c2-42eb-82ad-acdfa186a71f
title: Création d’un «Veuillez patienter. . ." Boîte de message
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c5f0cb1e4f1a0224c3b71d42d6fc63c1940483
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092533"
---
# <a name="authoring-a-conditional-please-wait-message-box"></a>Création d’une condition « Veuillez patienter... » Boîte de message

L’exemple suivant montre comment créer une boîte de message conditionnelle qui s’affiche et avertit l’utilisateur qu’une tâche en arrière-plan est toujours en cours d’exécution chaque fois que l’utilisateur active un contrôle affiché prématurément.

L’exemple illustre également comment le [ControlEvent, SpawnWaitDialog](spawnwaitdialog-controlevent.md) peut généralement être utilisé pour protéger un contrôle qui déclenche une action en fonction de la fin d’une tâche en arrière-plan.

Dans cet exemple, une [boîte de dialogue de sélection](selection-dialog.md) contenant trois contrôles de bouton de commande étiquetés **Installer maintenant**, **suivant** et **coût du disque** s’affiche pour l’utilisateur pendant le processus d’installation. Toutefois, le programme d’installation effectue également une tâche de coût de l’espace disque en arrière-plan lors de l’affichage de cette boîte de dialogue. L’auteur souhaite protéger ces boutons de l’activation et souhaite qu’une boîte de message « Veuillez patienter » s’affiche si l’utilisateur clique sur l’un des boutons avant que l’évaluation des coûts soit terminée. L’auteur souhaite également que cette boîte de message contienne un bouton **Annuler** et disparaisse dès que la tâche en arrière-plan est terminée.

**Pour afficher une boîte de dialogue demandant à l’utilisateur d’attendre l’achèvement de l’évaluation des coûts du disque en arrière-plan**

1.  Utilisez les fonctionnalités de création du programme d’installation pour ajouter une nouvelle boîte de dialogue modale, nommée **WaitForCosting**, à la [table de dialogue](dialog-table.md). La boîte de dialogue doit afficher une chaîne de texte indiquant « Veuillez patienter pendant l’exécution du coût de l’espace disque ».
2.  Ajoutez un contrôle de bouton de commande unique à cette boîte de dialogue, intitulé **Annuler**, en le créant dans la [table de contrôle](control-table.md).
3.  Liez le bouton **Annuler** Push à un ControlEvent, qui ferme la boîte de dialogue **WaitForCosting** en créant un [ControlEvent, EndDialog](enddialog-controlevent.md) dans la [table ControlEvent,](controlevent-table.md). Définissez l’argument de l’événement de contrôle EndDialog sur Exit.
4.  Liez un [ControlEvent, SpawnWaitDialog](spawnwaitdialog-controlevent.md) aux contrôles de bouton d’installation de l' **installation** existante, **suivant** et du **coût du disque** affichés dans la boîte de dialogue de [sélection](selection-dialog.md) . Définissez l’argument de ce ControlEvent, dans la table ControlEvent, comme boîte de dialogue **WaitForCosting** et définissez l’expression dans la colonne condition de la table sur : [**CostingComplete**](costingcomplete.md) = 1.

 

 



