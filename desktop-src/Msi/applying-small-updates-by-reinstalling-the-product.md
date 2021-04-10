---
description: Une petite mise à jour peut être appliquée à une application en réinstallant complètement ou partiellement l’application à partir de la ligne de commande ou d’un programme.
ms.assetid: 6f8b68da-7748-436d-bc95-96e39cf42143
title: Application de petites mises à jour en réinstallant le produit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27b97ff0274baac5a4ec30df244394a609ed525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951780"
---
# <a name="applying-small-updates-by-reinstalling-the-product"></a>Application de petites mises à jour en réinstallant le produit

Une petite mise à jour peut être appliquée à une application en réinstallant complètement ou partiellement l’application à partir de la ligne de commande ou d’un programme.

**Pour propager la petite mise à jour aux utilisateurs actuels (il s’agit d’une réinstallation complète) à partir de la ligne de commande**

1.  À partir de la ligne de commande, utilisez : **msiexec/fvomus \[** _chemin d’accès au fichier. msi mis à jour_ *_\]_* ou **msiexec/i \[** chemin d' _accès à la mise à jour. msi_ *_\] REINSTALL = ALL REINSTALLMODE = vomus_*.
2.  Le fichier. msi mis à jour est mis en cache sur l’ordinateur de l’utilisateur. Notez qu’il n’est pas possible pour l’utilisateur de réinstaller le produit à l’aide de la fonction Ajout/suppression de programmes, car le fichier. msi mis à jour n’est pas encore sur l’ordinateur de l’utilisateur.

**Pour propager une petite mise à jour à des utilisateurs actuels (il s’agit d’une réinstallation complète) à partir d’un programme**

1.  À partir d’un programme, appelez [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) et spécifiez le \_ package REINSTALLMODE, REINSTALLMODE \_ FILEOLDERVERSION, REINSTALLMODE \_ MACHINEDATA, REINSTALLMODE \_ UserData et REINSTALLMODE \_ Shortcut
2.  Le fichier. msi mis à jour est mis en cache sur l’ordinateur de l’utilisateur.

La méthode suivante lance une réinstallation des seules fonctionnalités ou composants qui sont affectés par la petite mise à jour.

**Pour propager une petite mise à jour aux utilisateurs actuels (il s’agit d’une réinstallation partielle)**

1.  Obtenez la liste des noms des fonctionnalités et des composants qui sont affectés par la petite mise à jour.
2.  À partir de l’invite de commandes, utilisez : **\[ msiexec/i** _chemin d’accès mis à jour. msi_ *_\] REINSTALL = \[_*_Feature List \]_ **REINSTALLMODE = vomus**.
3.  Le fichier. msi mis à jour est mis en cache sur l’ordinateur de l’utilisateur.

 

 



