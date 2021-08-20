---
description: les fonctions Windows Installer, les tables et les propriétés répertoriées sur cette page ne sont pas prises en charge par Windows Installer&\# 160 ; 2.0 et les versions antérieures.
ms.assetid: 850b598a-338e-4f84-8336-01e962256a08
title: non pris en charge dans Windows Installer 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d244dc962e65bb017dbd5fb56c7fda644b46524df7890ede7b71bf0bdf8ad66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074859"
---
# <a name="not-supported-in-windows-installer-20"></a>non pris en charge dans Windows Installer 2,0

les fonctions Windows Installer, les tables et les propriétés répertoriées sur cette page ne sont pas prises en charge par Windows Installer 2,0 et versions antérieures. L’absence d’une fonctionnalité dans cette liste ne garantit pas que la fonctionnalité est prise en charge. consultez la documentation principale pour déterminer quelle version de Windows Installer est requise pour une fonctionnalité particulière. pour plus d’informations sur les autres versions [de Windows Installer, consultez nouveautés de Windows Installer](what-s-new-in-windows-installer.md).

Windows le programme d’installation 2,0 peut s’exécuter sur microsoft Windows 2000, microsoft Windows XP ou Windows Server 2003. pour obtenir la liste de toutes les versions de Windows Installer, consultez [versions publiées de Windows Installer](released-versions-of-windows-installer.md).

les fonctionnalités suivantes ne sont pas prises en charge dans Windows Installer 2,0 et versions antérieures.

[Fonctions du programme d’installation](installer-functions.md)

-   [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
-   [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
-   [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
-   [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
-   [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
-   [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
-   [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)
-   [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
-   [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
-   [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
-   [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
-   [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
-   [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
-   [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
-   [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
-   [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa)
-   [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
-   [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
-   [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
-   [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
-   [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)

[Windows Structures du programme d’installation](installer-structures.md)

-   [**MSIPATCHSEQUENCEINFO**](/windows/win32/api/msi/ns-msi-msipatchsequenceinfoa)

[Tables de base de données](database-tables.md)

-   [MsiPatchCertificate](msipatchcertificate-table.md)
-   [MsiPatchSequence](msipatchsequence-table.md)
-   [MsiPatchMetadata](msipatchmetadata-table.md)

[Propriétés](properties.md)

-   [**MSIDISABLELUAPATCHING**](msidisableluapatching.md)
-   [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)
-   [**MSIPATCHREMOVE**](msipatchremove.md)
-   [**MsiPatchRemovalList**](msipatchremovallist.md)
-   [**MsiUISourceResOnly**](msiuisourceresonly.md)
-   [**MsiUIHideCancel**](msiuihidecancel.md)
-   [**MsiUIProgressOnly**](msiuiprogressonly.md)

[Stratégie système](system-policy.md)

-   [DisableLUAPatching](disableluapatching.md)
-   [DisablePatchUninstall](disablepatchuninstall.md)
-   [DisableFlyWeightPatching](disableflyweightpatching.md)
-   [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md)
-   [MaxPatchCacheSize](maxpatchcachesize.md)

[Codes d’erreur](error-codes.md)

-   ERREUR \_ de \_ Suppression de correctif \_ non prise en charge
-   ERREUR \_ de \_ correctif inconnu
-   correctif d’erreur- \_ \_ aucune \_ séquence
-   ERREUR de \_ Suppression de correctif non \_ \_ autorisée
-   ERREUR \_ de \_ code XML de correctif non valide \_
-   ERREUR de mise à \_ jour du \_ \_ \_ produit publié

Modes de journalisation

-   [**INSTALLLOGMODE \_ LOGONLYONERROR**](/windows/desktop/api/Msi/nf-msi-msienableloga)

[Interface d’automatisation](automation-interface.md)

-   Propriétés de l' [ **objet Product**](product-object.md)

    -   [**Produit. UserSid**](product-usersid.md)
    -   [**Product. sources**](product-sources.md)
    -   [**Product. MediaDisks**](product-mediadisks.md)
    -   [**Product. FeatureState**](product-featurestate.md)
    -   [**Produit. Context**](product-context.md)
    -   [**Product. InstallProperty**](product-installproperty.md)
    -   [**Product. ProductCode**](product-productcode.md)
    -   [**Product. ComponentState**](product-componentstate.md)
    -   [**Product. State**](product-state.md)
    -   [**Product. SourceListInfo**](product-sourcelistinfo.md)

-   Méthodes de l' [ **objet Product**](product-object.md)

    -   [**Product. SourceListForceResolution**](product-sourcelistforceresolution.md)
    -   [**Product. SourceListClearMediaDisk**](product-sourcelistclearmediadisk.md)
    -   [**Product. SourceListClearAll**](product-sourcelistclearall.md)
    -   [**Product. SourceListClearSource**](product-sourcelistclearsource.md)
    -   [**Product. SourceListAddSource**](product-sourcelistaddsource.md)
    -   [**Product. SourceListAddMediaDisk**](product-sourcelistaddmediadisk.md)

-   Propriétés de l' [ **objet patch**](patch-object.md)

    -   [**Patch. UserSid**](patch-usersid.md)
    -   [**Patch. State**](patch-state.md)
    -   [**Patch. sources**](patch-sources.md)
    -   [**Patch. SourceListInfo**](patch-sourcelistinfo.md)
    -   [**Patch. ProductCode**](patch-productcode.md)
    -   [**Patch. PatchProperty**](patch-patchproperty.md)
    -   [**Patch. PatchCode**](patch-patchcode.md)
    -   [**Patch. MediaDisks**](patch-mediadisks.md)
    -   [**Patch. Context**](patch-context.md)

-   Méthodes de l' [ **objet patch**](patch-object.md)

    -   [**Patch. SourceListForceResolution**](patch-sourcelistforceresolution.md)
    -   [**Patch. SourceListClearAll**](patch-sourcelistclearall.md)
    -   [**Patch. SourceListClearSource**](patch-sourcelistclearsource.md)
    -   [**Patch. SourceListClearMediaDisk**](patch-sourcelistclearmediadisk.md)
    -   [**Patch. SourceListAddSource**](patch-sourcelistaddsource.md)
    -   [**Patch. SourceListAddMediaDisk**](patch-sourcelistaddmediadisk.md)

-   Propriétés de l' [ **objet installer**](installer-object.md)

    -   [**Programme d’installation. ProductsEx**](installer-productsex.md)
    -   [**Programme d’installation. ProductInfo**](installer-productinfo.md)
    -   [**Programme d’installation. PatchesEx**](installer-patchesex.md)

-   Méthodes de l' [ **objet installer**](installer-object.md)

    -   [**Programme d’installation. ApplyMultiplePatches**](installer-applymultiplepatches.md)
    -   [**Programme d’installation. ApplyPatch**](installer-applypatch.md)
    -   [**Programme d’installation. RemovePatches**](installer-removepatches.md)
    -   [**Programme d’installation. ExtractPatchXMLData**](installer-extractpatchxmldata.md)

les fonctionnalités suivantes ne sont pas non plus prises en charge dans Windows Installer version 2.0.2600. Windows la version du programme d’installation 2.0.2600 a été publiée avec Windows XP et Windows serveur 2000. les fonctionnalités sont disponibles à partir de Windows Installer version 2.0.3790 publiée avec Windows Server 2003. pour obtenir la liste de toutes les versions de Windows Installer, consultez [versions publiées de Windows Installer](released-versions-of-windows-installer.md).

[Fonctions du programme d’installation](installer-functions.md)

-   [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)
    -   \_instance MSIADVERTISEOPTIONS
-   [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)

[Interface d’automatisation](automation-interface.md)

-   Méthodes de l' [ **objet installer**](installer-object.md)

    -   [**Programme d’installation. ApplyPatch**](installer-applypatch.md)
    -   [**Programme d’installation. ProductInfo**](installer-productinfo.md)

[Propriétés](properties.md)

-   [**MSINEWINSTANCE**](msinewinstance.md)
-   [**MSIINSTANCEGUID**](msiinstanceguid.md)
-   [**MsiNTSuiteWebServer**](msintsuitewebserver.md)

[Options d’exécution d’une action personnalisée In-Script](custom-action-in-script-execution-options.md)

-   [**msidbCustomActionTypeTSAware**](custom-action-in-script-execution-options.md)

[Codes d’erreur](error-codes.md)

-   [ERREUR \_ d' \_ installation \_ interdite à distance](error-codes.md)

[Stratégies d’ordinateur](machine-policies.md)

-   [DisableMSI](disablemsi.md)
-   [Stratégie TransformsSecure](transformssecure-policy.md)

[Options de ligne de commande](command-line-options.md)

-   [/c](command-line-options.md)
-   [/n](command-line-options.md)
-   [/Lx](command-line-options.md)

[Attributs du contrôle](control-attributes.md)

-   **ImageHandle** a été supprimé

## <a name="notes"></a>Notes

les [Options du programme d’installation Standard Command-Line](standard-installer-command-line-options.md) ne sont pas prises en charge par Windows Installer 2,0. au lieu de cela [, utilisez les Options de ligne de commande](command-line-options.md)Windows Installer.

lorsque Windows Installer 2,0 installe un package de correctifs, il ignore les informations contenues dans les tables [MsiPatchSequence](msipatchsequence-table.md) ou [MsiPatchMetadata](msipatchmetadata-table.md) . les versions ultérieures de la Windows Installer peuvent utiliser les informations de ces tableaux pour améliorer le séquencement, la suppression et l’optimisation des correctifs. pour plus d’informations sur la fonctionnalité de mise à jour corrective améliorée dans Windows Installer, consultez mise à [jour corrective](patching.md).

Windows Le programme d’installation 2,0 ne prend pas en charge les [correctifs non installables](uninstallable-patches.md) et la seule méthode permettant de supprimer des correctifs particuliers d’une application consiste à désinstaller l’ensemble de l’application corrigée, puis à réinstaller sans réappliquer les correctifs en cours de suppression.

Windows Le programme d’installation 2,0 ne prend pas en charge le séquencement des correctifs et installe les correctifs dans l’ordre dans lequel ils sont fournis au système lors de [l’installation de plusieurs correctifs](installing-multiple-patches.md).

Windows Le programme d’installation 2,0 ne prend pas en charge l’utilisation de la mise à [jour corrective du contrôle de compte d’utilisateur (UAC)](user-account-control--uac--patching.md) pour activer les correctifs signés numériquement qui peuvent être appliqués par les utilisateurs non-administrateurs.

Windows Le programme d’installation 2,0 ne prend pas en charge l' [optimisation des correctifs](patch-optimization.md). l’application de correctifs peut prendre beaucoup plus de temps que dans les versions ultérieures Windows Installer qui met à jour uniquement les fichiers affectés par le correctif.

Windows le programme d’installation 2,0 ne prend pas en charge [l’utilisation de Windows Installer pour inventorier des produits et des correctifs](inventory-products-and-patches-.md).

Windows le programme d’installation 2,0 ne prend pas en charge la récupération et la modification des informations de liste source pour les applications Windows Installer et les correctifs installés sur le système pour tous les utilisateurs. les versions ultérieures de Windows Installer permettent aux administrateurs de gérer des listes sources et des propriétés de liste source pour les sources de réseau, d’URL et de média. Les versions ultérieures permettent aux administrateurs de gérer des listes de sources à partir d’un processus externe. Pour plus d’informations, consultez [gestion des sources d’installation](managing-installation-sources.md).

Windows Le programme d’installation 2,0 ne prend pas en charge l’installation de plusieurs instances de produits ou de correctifs sans un package d’installation distinct pour chaque instance. les versions ultérieures de Windows Installer peuvent installer plusieurs instances d’un produit à l’aide de transformations de code de produit et d’un package .msi ou d’un correctif. Pour plus d’informations [, consultez Installation de plusieurs instances de produits et de correctifs](installing-multiple-instances-of-products-and-patches.md).

à compter de Windows XP avec Service Pack 2 (SP2), Windows Installer pouvez utiliser les protocoles http, https et de fichiers. Le programme d’installation ne prend pas en charge les protocoles FTP et GOPHER.

 

 



