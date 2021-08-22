---
description: les Windows Installer fonctions, les tables et les propriétés répertoriées sur cette page ne sont pas prises en charge par Windows Installer&\# 160 ; 4.0 et versions antérieures.
ms.assetid: 7256b759-3fb5-4195-b0e4-a1631327ebb7
title: non pris en charge dans Windows Installer 4,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444040fca716b6bd64c8598d2d2e36013fe19cc62971483507756a66f3e961bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558799"
---
# <a name="not-supported-in-windows-installer-40"></a>non pris en charge dans Windows Installer 4,0

les fonctions Windows Installer, les tables et les propriétés répertoriées sur cette page ne sont pas prises en charge par Windows Installer 4,0 et versions antérieures. L’absence d’une fonctionnalité dans cette liste ne garantit pas que la fonctionnalité est prise en charge. consultez la documentation principale pour déterminer quelle version de Windows Installer est requise pour une fonctionnalité particulière. pour plus d’informations sur les autres versions [de Windows Installer, consultez nouveautés de Windows Installer](what-s-new-in-windows-installer.md).

Windows le programme d’installation 4,0 est disponible pour Microsoft Windows Server 2008 et Windows Vista. pour obtenir la liste complète de toutes les versions de Windows Installer et des fichiers redistribuables, consultez [versions publiées de Windows Installer](released-versions-of-windows-installer.md).

les fonctionnalités suivantes ne sont pas prises en charge dans Windows Installer 4,0 et versions antérieures.

[Fonctions du programme d’installation](installer-functions.md)

-   [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona)
-   [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)
-   [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)

[Propriétés](properties.md)

-   [**MSIDISABLEEEUI**](msidisableeeui.md)
-   [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md)

[Tables de base de données](database-tables.md)

-   [Table MsiEmbeddedChainer](msiembeddedchainer-table.md)
-   [Table MsiEmbeddedUI](msiembeddedui-table.md)
-   [Table MsiPackageCertificate](msipackagecertificate-table.md)
-   [Table des composants](component-table.md)
- **msidbComponentAttributesUninstallOnSupersedence**  
    **msidbComponentAttributesShared**  
    
-   [CustomAction](customaction-table.md) Colonne ExtendedType  
    

[Option de désinstallation corrective de l’action personnalisée](custom-action-patch-uninstall-option.md)



[MsiTransformView\<PatchGUID\>](msitransformview.md)  

**msidbCustomActionTypePatchUninstall**  


[Stratégie système](system-policy.md)

-   [DisableSharedComponent](disablesharedcomponent.md)
-   [MsiDisableEmbeddedUI](msidisableembeddedui.md)

Prototypes de fonctions de rappel

-   *EmbeddedUIHandler*
-   *InitializeEmbeddedUI*
-   *ShutdownEmbeddedUI*

[Évaluateurs de cohérence internes-CIEM](internal-consistency-evaluators-ices.md)

-   [ICE92](ice92.md) vérifie qu’aucun composant n’a à la fois les attributs **msidbComponentAttributesPermanent** et **msidbComponentAttributesUninstallOnSupersedence** .

## <a name="notes"></a>Notes

Windows Le programme d’installation 4,0 ne peut pas effectuer [plusieurs installations de package](multiple-package-installations.md) à l’aide du [*traitement des transactions*](t-gly.md).

à l’aide de Windows Installer 4,0 ou des versions antérieures du programme d’installation, les petites mises à jour et les mises à niveau mineures peuvent échouer lors de l’utilisation de la stratégie [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) ou [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) , car la mise à jour supprime un composant.

une interface utilisateur personnalisée ne peut pas être incorporée dans le package Windows Installer à l’aide de la méthode décrite dans [utilisation d’une interface utilisateur incorporée](using-an-embedded-ui.md).

 

 



