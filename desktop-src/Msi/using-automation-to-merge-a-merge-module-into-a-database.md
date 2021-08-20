---
description: les Modules de fusion fournissent une méthode standard pour vous permettre de fournir des composants de Windows Installer partagés et une logique de configuration aux applications.
ms.assetid: 63ced106-12e3-4483-8bfe-22c54fe7a204
title: Utilisation de l’automatisation pour fusionner un module de fusion dans une base de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513a765670df44396c34537721eb6f75ed98796dd31ddefd5d26387e2a6b5d0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141328"
---
# <a name="using-automation-to-merge-a-merge-module-into-a-database"></a>Utilisation de l’automatisation pour fusionner un module de fusion dans une base de données

les [Modules de fusion](merge-modules.md) fournissent une méthode standard pour vous permettre de fournir des [*composants*](c-gly.md)de Windows Installer partagés et une logique de configuration aux applications.

Les modules de fusion doivent être fusionnés dans un package d’installation à l’aide d’un outil de fusion. La meilleure pratique consiste à obtenir un outil de fusion distribué librement, ou à acheter l’un des outils de fusion disponibles auprès des éditeurs de logiciels indépendants, par exemple, vous pouvez utiliser [Mergemod.dll](merge-module-automation.md).

la procédure suivante montre comment fusionner un module de fusion dans une base de données Windows Installer à l’aide de l' [automatisation des modules de fusion](merge-module-automation.md).

**Pour fusionner un module dans une base de données**

1.  Ouvrez un fichier journal à l’aide de la méthode [**OpenLog**](merge-openlog.md) .

    Cette étape est requise uniquement si vous devez créer un fichier journal ou ajouter un fichier journal existant pour le processus de fusion.

2.  Ouvrez la base de données d’installation [.msi](windows-installer-file-extensions.md) à l’aide de la méthode [**OpenDatabase**](merge-opendatabase.md) de l' [**objet Merge**](merge-object.md).

    Cette étape est obligatoire.

    La base de données que vous ouvrez est celle pour laquelle vous souhaitez recevoir le module de fusion.

3.  Ouvrez le module de fusion [. msm](windows-installer-file-extensions.md) à l’aide de la méthode [**OpenModule**](merge-openmodule.md) .

    Cette étape est obligatoire.

    Il s’agit du module de fusion qui est fusionné dans la base de données. Vous devez ouvrir un module avant de pouvoir le fusionner avec une base de données d’installation.

4.  Fusionnez le module dans la base de données d’installation en appelant la méthode [**Merge**](merge-object.md) ou la méthode [**MergeEx**](merge-mergeex.md) .

    Cette étape est obligatoire.

    La méthode [**Merge**](merge-object.md) ou la méthode [**MergeEx**](merge-mergeex.md) ne peut être appelée qu’une seule fois pour fusionner une combinaison spécifique de fichiers [.msi](windows-installer-file-extensions.md) et. msm.

    > [!Note]  
    > La méthode [**MergeEx**](merge-mergeex.md) est uniquement disponible dans [Mergemod.dll version 2,0](merge-module-automation.md) ou ultérieure, et uniquement lors de l’utilisation de l’interface [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) .

     

5.  Récupérez la propriété [**Errors**](merge-errors.md) et examinez la collection d’objets d' [**erreur**](error-object.md) qu’elle renvoie pour les conflits de fusion ou d’autres erreurs.

    Vous devez résoudre toutes les erreurs.

    La récupération n’est pas destructrice et plusieurs instances de la collection d’erreurs peuvent être récupérées en lisant de manière répétée la propriété [**Errors**](merge-errors.md) .

6.  associez les composants du module de fusion aux fonctionnalités à l’aide de la méthode [**Connecter**](merge-connect.md) .

    Cette étape est requise uniquement si vous disposez de fonctionnalités existantes et que vous souhaitez ajouter des fonctionnalités à fusionner dans la base de données d’installation.

    Une fonctionnalité doit exister avant d’appeler cette méthode. Pour plus d’informations, consultez [connexion d’un module de fusion à plusieurs fonctionnalités](connecting-a-merge-module-to-multiple-features.md).

7.  Si nécessaire, extrayez les fichiers sources du module en exécutant une ou plusieurs des opérations suivantes :
    -   Utilisez [**ExtractFiles**](merge-extractfiles.md) ou [**ExtractFilesEx**](merge-extractfilesex.md) pour extraire des fichiers d’un fichier .cab incorporé, puis copiez-les dans un répertoire spécifié.
        > [!Note]  
        > [**ExtractFilesEx**](merge-extractfilesex.md) requiert [Mergemod.dll version 2,0](merge-module-automation.md) ou ultérieure.

         

    -   Utilisez [**ExtractCAB**](merge-extractcab.md) pour extraire les fichiers d’un fichier .cab incorporé, puis enregistrez-les dans un fichier spécifié.
    -   Utilisez [**CreateSourceImage**](merge-createsourceimage.md) pour extraire les fichiers d’un module, puis, après la fusion, copiez-les dans une image source sur le disque.
        > [!Note]  
        > [**CreateSourceImage**](merge-createsourceimage.md) est disponible uniquement dans [Mergemod.dll version 2,0](merge-module-automation.md) ou ultérieure.

         
8.  Fermez le module de fusion ouvert en cours à l’aide de la méthode [**CloseModule**](merge-closemodule.md) .

    Cette étape est obligatoire.

9.  Fermez la base de données d’installation ouverte à l’aide de la méthode [**FermerBase**](merge-closedatabase.md) .

    Cette étape est obligatoire.

    La fermeture d’une base de données efface toutes les informations de dépendance, mais n’affecte pas les erreurs qui ne sont pas récupérées.

10. Fermez le fichier journal actuel à l’aide de la méthode [**CloseLog**](merge-closelog.md) .

    Cette étape est requise si vous disposez d’un fichier journal ouvert.

Une fois le module fusionné dans la base de données à l’aide de [Mergemod.dll](merge-module-automation.md), la [table de supports](media-table.md) doit être mise à jour pour décrire la disposition souhaitée de l’image source. Le processus de fusion fourni par Mergemod.dll ne met pas à jour la table multimédia, car l’utilisateur du module de fusion peut sélectionner différentes méthodes pour la disposition de l’image source.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Versions, outils et redistribuables publiés](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



