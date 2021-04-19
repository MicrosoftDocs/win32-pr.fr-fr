---
description: Utilisez les instructions suivantes pour créer une installation de Windows Installer qui affiche un message invitant l’utilisateur à insérer un disque.
ms.assetid: 8b53a490-921f-4d89-83b7-dbc62231ef92
title: Messages d’invite de création de disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f536a27c2adb5896992eb19a86bff64b9498d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519067"
---
# <a name="authoring-disk-prompt-messages"></a>Messages d’invite de création de disque

Utilisez les instructions suivantes pour créer une installation de Windows Installer qui affiche un message invitant l’utilisateur à insérer un disque.

**Pour afficher un message invitant l’utilisateur à insérer un disque**

1.  Utilisez les fonctionnalités de création du programme d’installation pour définir la chaîne de propriété [**DiskPrompt**](diskprompt.md) dans la table de [Propriétés](property-table.md) . Cela doit inclure le nom du produit en cours d’installation et un paramètre d’espace réservé dans la chaîne pour le titre imprimé sur le disque. Par exemple, pour Microsoft Publisher, la propriété **DiskPrompt** peut être « Microsoft Publisher : Disk \[ 1 \] », où \[ 1 \] est l’espace réservé pour le nom du disque.
2.  Entrez les titres de chacun des disques à demander dans des lignes distinctes de la colonne DiskPrompt de la table [multimédia](media-table.md) . Par exemple, la première et seule entrée dans la table des médias peut être « 1 – install ».
3.  Au cours de l’action [InstallFiles](installfiles-action.md) , la valeur de la colonne DiskPrompt de la table [Media](media-table.md) est remplacée par l’espace réservé dans la chaîne de la propriété [**DiskPrompt**](diskprompt.md) .
4.  Le message affiché par la boîte de message est créé à partir d’une chaîne de modèle intégrée dans la [table d’erreurs](error-table.md). Il s’agit de l’erreur 1302 et la chaîne de modèle est : « Insérez le disque : \[ 2 \] », et le \[ 2 \] représente un espace réservé pour la propriété [**DiskPrompt**](diskprompt.md) .

L’exemple affiche le message suivant à l’utilisateur : « veuillez insérer le disque : Microsoft Publisher : Disk 1 – install ».

Notez que les messages d’invite de disque sont affichés par tous les niveaux de l' [interface utilisateur](user-interface-levels.md) , sauf aucun.

 

 



