---
description: utilisez les instructions suivantes pour créer une installation de Windows Installer qui affiche un message invitant l’utilisateur à insérer un disque.
ms.assetid: 8b53a490-921f-4d89-83b7-dbc62231ef92
title: Messages d’invite de création de disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a27b324600b7098c4b11dd94528ce0f3aa624e6859df8d02ef43ee90d632068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381374"
---
# <a name="authoring-disk-prompt-messages"></a>Messages d’invite de création de disque

utilisez les instructions suivantes pour créer une installation de Windows Installer qui affiche un message invitant l’utilisateur à insérer un disque.

**Pour afficher un message invitant l’utilisateur à insérer un disque**

1.  Utilisez les fonctionnalités de création du programme d’installation pour définir la chaîne de propriété [**DiskPrompt**](diskprompt.md) dans la table de [Propriétés](property-table.md) . Cela doit inclure le nom du produit en cours d’installation et un paramètre d’espace réservé dans la chaîne pour le titre imprimé sur le disque. par exemple, pour Microsoft Publisher la propriété **DiskPrompt** peut être « Microsoft Publisher : Disk \[ 1 \] », où \[ 1 \] est l’espace réservé pour le nom du disque.
2.  Entrez les titres de chacun des disques à demander dans des lignes distinctes de la colonne DiskPrompt de la table [multimédia](media-table.md) . Par exemple, la première et seule entrée dans la table des médias peut être « 1 – install ».
3.  Au cours de l’action [InstallFiles](installfiles-action.md) , la valeur de la colonne DiskPrompt de la table [Media](media-table.md) est remplacée par l’espace réservé dans la chaîne de la propriété [**DiskPrompt**](diskprompt.md) .
4.  Le message affiché par la boîte de message est créé à partir d’une chaîne de modèle intégrée dans la [table d’erreurs](error-table.md). Il s’agit de l’erreur 1302 et la chaîne de modèle est : « Insérez le disque : \[ 2 \] », et le \[ 2 \] représente un espace réservé pour la propriété [**DiskPrompt**](diskprompt.md) .

l’exemple affiche le message suivant à l’utilisateur : « veuillez insérer le disque : Microsoft Publisher : disk 1 – Install ».

Notez que les messages d’invite de disque sont affichés par tous les niveaux de l' [interface utilisateur](user-interface-levels.md) , sauf aucun.

 

 



