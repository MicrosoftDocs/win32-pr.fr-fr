---
description: Si l’action InstallValidate détecte l’installation d’un fichier en cours d’utilisation, elle affiche la boîte de dialogue FilesInUse et enregistre les informations suivantes.
ms.assetid: 59237d2c-6dda-4edc-bbaf-39c6b4c221b9
title: Journalisation des demandes de redémarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a256f9042dc40633932a36e288ad18d8194f4739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530232"
---
# <a name="logging-of-reboot-requests"></a>Journalisation des demandes de redémarrage

Si l' [action InstallValidate](installvalidate-action.md) détecte l’installation d’un fichier en cours d’utilisation, elle affiche la [boîte de dialogue FilesInUse](filesinuse-dialog.md) et enregistre les informations suivantes.

``` syntax
Info 1603. The file E:\testdb\Test\CustAct1.dll is being held in use
by the following process: Name: test, Id: 137, Window Title: 'Test'.
```

Si le programme d’installation détecte qu’il va remplacer un fichier en cours d’utilisation, il enregistre les informations suivantes.

``` syntax
Info 1603. The file E:\testdb\Test\CustAct2.dll is being held in use.

Info 1903.Scheduling reboot operation: Deleting file [filename]. Must 
reboot to complete operation.
```

Le \[ jeton de nom de \] fichier peut en fait contenir un chemin d’accès à un fichier avec une extension. RBF. Dans ce cas, le fichier. RBF est en fait le fichier d’origine journalisé par le message 1603, qui a été renommé en fichier. RBF. Le fichier en cours d’utilisation est d’abord renommé avec une extension. RBF, puis supprimé.

Pour obtenir plus d’informations sur la raison pour laquelle le programme d’installation tente de remplacer ce fichier particulier, vous pouvez utiliser l’option de journalisation détaillée. Utilisez la \_ valeur de commentaires INSTALLLOGMODE dans un appel à [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) ou utilisez l’option de sortie verbose des [options de ligne de commande](command-line-options.md). Les informations suivantes sont consignées dans le journal.

``` syntax
MSI (s) (D0:F0): File: E:\testdb\Test\CustAct2.dll;  Overwrite;  
REINSTALLMODE specifies all files to be overwritten
```

Le journal inclut un message tel que « le fichier existant est une version antérieure » ou « le fichier existant est endommagé (somme de contrôle non valide) »

 

 



