---
description: Les modules de fusion fournissent une méthode standard permettant aux développeurs de fournir des composants de Windows Installer partagés et une logique de configuration à leurs applications.
ms.assetid: 3eb087b1-0f44-40d8-a950-67d489f09408
title: Utilisation de l’API pour fusionner un module de fusion dans une base de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e68298671045825dda41ad120896fa22c89f068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535457"
---
# <a name="using-the-api-to-merge-a-merge-module-into-a-database"></a>Utilisation de l’API pour fusionner un module de fusion dans une base de données

Les [modules de fusion](merge-modules.md) fournissent une méthode standard permettant aux développeurs de fournir des [*composants*](c-gly.md) de Windows Installer partagés et une logique de configuration à leurs applications. Les modules de fusion doivent être fusionnés dans un package d’installation à l’aide d’un outil de fusion. La meilleure solution consiste à obtenir un outil de fusion distribué librement ou à acheter l’un des outils de fusion disponibles auprès des éditeurs de logiciels indépendants. Par exemple, vous pouvez utiliser la fonctionnalité fournie par [Mergemod.dll](merge-module-automation.md).

Utilisez les étapes suivantes dans l’ordre pour fusionner un module de fusion dans une base de données d’installation Windows Installer par l’API de [Mergemod.dll](merge-module-automation.md).

**Pour fusionner un module de fusion dans une base de données d’installation Windows Installer**

1.  Ouvrez un fichier journal à l’aide de [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog). Cette étape est requise uniquement si vous devez créer un fichier journal ou ajouter un fichier journal existant pour le processus de fusion.
2.  Ouvrez la base de données d’installation, un [fichier. msi](windows-installer-file-extensions.md), qui recevra le module de fusion à l’aide de l’opération [**OpenDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-opendatabase). Cette étape est obligatoire.
3.  Ouvrez le module de fusion, un [fichier. msm](windows-installer-file-extensions.md), qui est fusionné dans la base de données à l’aide de [**OuvrirModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule). Vous devez ouvrir un module avant de pouvoir le fusionner avec une base de données d’installation. Cette étape est obligatoire.
4.  Fusionnez le module dans la base de données d’installation à l’aide de [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) ou de [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex). Notez que **Merge** ou **MergeEx** ne peut être appelé qu’une seule fois pour fusionner une combinaison particulière de fichiers. msi et. msm. **MergeEx** est disponible uniquement lors de l’utilisation de [Mergemod.dll version 2,0](merge-module-automation.md) ou ultérieure et uniquement lors de l’utilisation de l’interface [IMsmMerge2](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) . Cette étape est obligatoire.
5.  Appelez [**obtenir des \_ Erreurs**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) et examinez la collection d’erreurs Récupérée pour les conflits de fusion ou d’autres erreurs. La récupération est non destructrice. Plusieurs instances de la collection d’erreurs peuvent être récupérées en lisant à plusieurs reprises les **\_ Erreurs d’extraction**. Vous devrez résoudre toutes les erreurs en fonction de votre cas.
6.  Associez les composants du module de fusion à toutes les fonctionnalités supplémentaires qui ont été ou seront fusionnées dans la base de données d’installation à l’aide de [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect). La fonctionnalité doit déjà exister avant d’appeler cette méthode. Cette étape est requise uniquement si vous disposez de fonctionnalités supplémentaires. pour plus d’informations, consultez [connexion d’un module de fusion à plusieurs fonctionnalités](connecting-a-merge-module-to-multiple-features.md) .
7.  Si nécessaire, extrayez les fichiers sources du module en exécutant une ou plusieurs des opérations suivantes.

    Pour extraire des fichiers d’un fichier. cab incorporé puis les copier dans un répertoire spécifié, utilisez [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) ou [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex). Notez que **ExtractFilesEx** requiert [Mergemod.dll version 2,0](merge-module-automation.md) ou ultérieure.

    Pour extraire des fichiers d’un fichier. cab incorporé, puis enregistrer dans un fichier spécifié, utilisez [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab).

    Pour extraire des fichiers d’un module, puis les copier vers une image source sur le disque après la fusion, utilisez [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage). Notez que **CreateSourceImage** est disponible uniquement avec [Mergemod.dll version 2,0](merge-module-automation.md) ou ultérieure.

8.  Fermez le module de fusion ouvert en cours à l’aide de [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule). Cette étape est obligatoire.
9.  Fermez la base de données d’installation actuellement ouverte à l’aide de [**FermerBase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase). Cette étape est obligatoire. La fermeture d’une base de données efface toutes les informations de dépendance, mais n’affecte pas les erreurs qui n’ont pas été récupérées.
10. Fermez le fichier journal actuel à l’aide de [**CloseLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closelog). Cette étape est requise si vous avez ouvert un fichier journal.

Une fois le module fusionné dans la base de données à l’aide de [Mergemod.dll](merge-module-automation.md), la [table de supports](media-table.md) doit être mise à jour pour décrire la disposition souhaitée de l’image source. Le processus de fusion fourni par Mergemod.dll ne met pas à jour la table multimédia, car l’utilisateur du module de fusion peut sélectionner différentes méthodes pour la disposition de l’image source.

 

 
