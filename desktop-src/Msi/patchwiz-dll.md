---
description: Pour générer un package de correctifs, il est recommandé d’utiliser un outil de création de correctifs comme Msimsp.exe et Patchwiz.dll.
ms.assetid: aca3bbd2-440a-405f-bddc-5f9cc831b811
title: Patchwiz.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6dc1135a9e2c09bb8a96e041f77bae39f0057ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009790"
---
# <a name="patchwizdll"></a>Patchwiz.dll

Pour générer un package de correctifs, il est recommandé d’utiliser un outil de création de correctifs comme [Msimsp.exe](msimsp-exe.md) et Patchwiz.dll. Patchwiz.dll version 4,0 est compatible avec les packages et les correctifs qui ont été créés à l’aide de versions antérieures du Patchwiz.dll. l’outil Patchwiz.dll est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

Patchwiz.dll version 4,0 a une nouvelle fonction, [UiCreatePatchPackageEx (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), qui étend les fonctionnalités de [UiCreatePatchPackage (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md). Ces fonctions prennent un fichier de propriétés de création de correctifs (fichier. PCP) et génèrent un [package de correctifs](patch-packages.md)du programme d’installation.

le fichier. pcp est un fichier de base de données binaire avec le même format qu’une base de données Windows Installer (fichier .msi), mais avec un schéma de base de données différent. Par conséquent, un fichier. PCP peut être créé à l’aide des mêmes outils que ceux utilisés pour une base de données du programme d’installation.

vous pouvez créer un fichier. pcp à l’aide d’un éditeur de tables comme [Orca.exe](orca-exe.md) pour entrer des informations dans la base de données blank. pcp fournie avec le kit de développement logiciel (SDK) Windows Installer, Template. pcp. Pour plus d’informations, consultez [un exemple de mise à jour corrective de petite taille](a-small-update-patching-example.md).

Les tables de base de données suivantes sont requises dans chaque fichier. PCP :

-   [Table Properties (Patchwiz.dll)](properties-table-patchwiz-dll-.md)
-   [Table ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md)
-   [Table UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md)
-   [Table TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md)

Les tables de base de données suivantes sont facultatives :

-   [UpgradedFiles \_ OptionalData, table (Patchwiz.dll)](upgradedfiles-optionaldata-table-patchwiz-dll-.md)
-   [Table FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)
-   [TargetFiles \_ OptionalData, table (Patchwiz.dll)](targetfiles-optionaldata-table-patchwiz-dll-.md)
-   [Table ExternalFiles (Patchwiz.dll)](externalfiles-table-patchwiz-dll-.md)
-   [Table UpgradedFilesToIgnore (Patchwiz.dll)](upgradedfilestoignore-table-patchwiz-dll-.md)

Le tableau suivant est requis dans les fichiers. PCP qui ont un MinimumRequiredMsiVersion égal à 300 dans le tableau des [Propriétés](properties-table-patchwiz-dll-.md) .

-   [Table PatchMetadata (Patchwiz.dll)](patchmetadata-table--patchwiz-dll-.md)

> [!Note]  
> La table est facultative si MinimumRequiredMsiVersion n’est pas égal à 300.

 

la version de Patchwiz.dll publiée avec Windows Installer 3,0 peut générer automatiquement des informations de séquencement de correctifs et les ajouter à la [Table MsiPatchSequence](msipatchsequence-table.md) d’un nouveau correctif. La [table PatchSequence](patchsequence-table--patchwiz-dll-.md) peut être utilisée pour ajouter manuellement des informations de séquencement de correctifs à la table MsiPatchSequence. Pour plus d’informations, consultez [génération d’informations sur les séquences de correctifs](generating-patch-sequence-information---patchwiz-dll-.md).

À partir de Patchwiz.dll version 2,0, vous pouvez augmenter la vitesse de création des correctifs suivants à l’aide de [la mise en cache des informations sur les correctifs (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md).

L’utilisation de symboles publics pour vos fichiers binaires image de mise à niveau et cible peut réduire d’environ une demi-taille des correctifs binaires. Pour plus d’informations, consultez [utilisation de symboles pour réduire la taille des correctifs binaires](using-symbols-to-reduce-binary-patch-size.md).

Vous pouvez spécifier que certaines régions du fichier cible soient conservées lors de la mise à jour corrective et que les informations contenues dans ces régions soient conservées. Pour plus d’informations, consultez Mise à [jour corrective des régions sélectionnées d’un fichier](patching-selected-regions-of-a-file.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Versions, outils et redistribuables publiés](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



