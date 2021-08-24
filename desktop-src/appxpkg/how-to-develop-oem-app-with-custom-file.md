---
title: Comment développer une application OEM qui utilise un fichier personnalisé
description: Découvrez comment développer une application qui utilise un fichier personnalisé pour transmettre des informations de l’OEM à l’application.
ms.assetid: BCDB4B13-3644-44E4-9A70-04D8E90500EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4780e930d057c325038c94dc86fc375c70bdb1cc8dca34ac6169436bc0f0e323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855319"
---
# <a name="how-to-develop-an-oem-app-that-uses-a-custom-file"></a>Comment développer une application OEM qui utilise un fichier personnalisé

Pour plus d’informations sur la création et l’utilisation de fichiers de données personnalisés, consultez [options de maintenance de package d’application DISM (. AppX ou. appxbundle) Command-Line options](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).

Découvrez comment développer une application qui utilise un fichier personnalisé pour transmettre des informations de l’OEM à l’application.

Pour les applications que vous créez pour le déploiement OEM, vous pouvez utiliser un fichier personnalisé pour transmettre les informations du fabricant OEM aux applications. Pour transmettre des informations OEM à une application, vous créez un fichier. Data personnalisé dans le dossier microsoft.sysTEM. Package. Metadata. Ce nom de fichier est spécial pour le système d’exploitation et est automatiquement transféré au cours des mises à jour du système d’exploitation. Les fabricants d’ordinateurs OEM peuvent utiliser ce fichier pour transmettre des identificateurs personnalisés, afin que les applications sachent quand les OEM les ont déployées. Vous ne pouvez avoir qu’un seul fichier. Data personnalisé par application. Les applications doivent être en mesure de rechercher et de lire ce fichier correctement. Les développeurs traitent le fichier comme des données non fiables.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Démarrage rapide : interroger les informations du manifeste du package d’application](how-to-query-package-identity-information.md)

### <a name="prerequisites"></a>Prérequis

-   Vous avez besoin de l’outil [gestion et maintenance des images de déploiement (DISM)](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) pour ajouter le package d’application avec le fichier de données personnalisé.

## <a name="instructions"></a>Instructions

### <a name="step-1-create-custom-file-and-add-it-to-the-package-metadata-folder"></a>Étape 1 : créer un fichier personnalisé et l’ajouter au dossier de métadonnées du package

Vous pouvez concevoir votre application pour qu’elle utilise le format de votre choix pour les données personnalisées. Par exemple, vous pouvez utiliser XML, un fichier texte ou un autre type de fichier pour organiser vos données. Nous vous recommandons de réfléchir à la façon dont vous pouvez tester et valider le fichier. Par exemple, vous pouvez créer un schéma XML pour valider un fichier XML.

Vous pouvez spécifier n’importe quel type de fichier avec n’importe quel nom de fichier pour les données personnalisées. Lorsque vous ajoutez le package d’application avec le fichier de données personnalisé à l’aide de l’outil [DISM](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) , DISM renomme le fichier personnalisé en Custom. Data et enregistre le fichier dans le dossier microsoft.sysTEM. Package. Metadata.

> [!Note]  
> Le fichier de données personnalisé ne peut pas être modifié par l’application. Il s’agit d’une ressource en lecture seule.

 

### <a name="step-2-access-the-custom-data-file-for-an-app"></a>Étape 2 : accéder au fichier de données personnalisé pour une application

vous pouvez accéder au fichier. data personnalisé d’une application à partir de votre code à l’aide d’api Windows pour obtenir des informations sur le package actuel. Par exemple :

``` syntax
Windows.ApplicationModel.Package.current.installedLocation.getFileAsync(
"microsoft.system.package.metadata\\custom.data")
```

Pour plus d’informations sur le développement avec la propriété [**Package. Current**](/uwp/api/windows.applicationmodel.package.current) , consultez [démarrage rapide : interroger les informations du manifeste du package d’application](how-to-query-package-identity-information.md).

Pour plus d’informations sur l’accès au fichier. Data personnalisé via [**IStorageFolder. GetFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) et l’utilisation d’objets [**StorageFile**](/uwp/api/Windows.Storage.StorageFile) , consultez [accès aux données et aux fichiers](/previous-versions/windows/apps/hh464959(v=win.10)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Démarrage rapide : interroger les informations du manifeste du package d’application](how-to-query-package-identity-information.md)
</dt> </dl>

 

 