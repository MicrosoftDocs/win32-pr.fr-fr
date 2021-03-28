---
description: Montre comment inscrire un verbe qui étend le &\# 0034 ; Sync&\# 0034 ; et &\# 0034 ; Partagez&\# 0034 ; verbes dans la barre de commandes de l’Explorateur Windows.
title: Verbes Sync et Share
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78267C74-7597-4b98-9DAE-89F2FD515C6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 734d59ce7b527ad068c03be9083ca67dfca20667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973747"
---
# <a name="sync-and-share-verbs"></a>Verbes Sync et Share

Montre comment inscrire un verbe qui étend les verbes « Sync » et « Share » dans la barre de commandes de l’Explorateur Windows.

Cette rubrique contient les sections suivantes.

-   [Configuration requise](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Exécution de l’exemple](#running-the-sample)
-   [Suppression de l'exemple](#removing-the-sample)

## <a name="requirements"></a>Spécifications



| Produit                                | Version minimale du produit |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Kit de développement logiciel Windows | 7.0                     |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

| Emplacement      | URL du chemin                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemple SyncAndShareVerbs](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/SyncAndShareVerbs) |

## <a name="running-the-sample"></a>Exécution de l'exemple

Pour exécuter l’exemple (Sync) :

1.  Accédez au répertoire qui contient le `sync.reg` fichier.
2.  Tapez `sync.reg ` sur la ligne de commande ou double-cliquez sur l’icône pour l' `sync.reg` inscrire.
3.  Ouvrez l’Explorateur Windows et sélectionnez un fichier.
4.  Cliquez sur l’option **synchronisation** dans la barre de commandes et sélectionnez une sous-option, par exemple **Paint**.

Pour exécuter l’exemple (partage) :

1.  Accédez au répertoire qui contient le `share.reg` fichier.
2.  Tapez `share.reg` sur la ligne de commande ou double-cliquez sur l’icône pour l' `share.reg` inscrire.
3.  Ouvrez l’Explorateur Windows et sélectionnez un fichier. Cliquez sur l’option **partager** dans la barre de commandes.
4.  Cliquez sur l’option **partager avec** dans la barre de commandes et sélectionnez une sous-option, par exemple **Paint**.

## <a name="removing-the-sample"></a>Suppression de l'exemple

Pour supprimer l’exemple (Sync) :

1.  Accédez au répertoire qui contient le fichier Uninstallsync. reg.
2.  Tapez `uninstallsync.reg` sur la ligne de commande ou double-cliquez sur l’icône de `uninstallsync.reg` .

Pour supprimer l’exemple (partage) :

1.  Accédez au répertoire qui contient le fichier Uninstallshare. reg.
2.  Tapez `uninstallshare.reg` sur la ligne de commande ou double-cliquez sur l’icône pour `uninstallshare.reg.`

 

 



