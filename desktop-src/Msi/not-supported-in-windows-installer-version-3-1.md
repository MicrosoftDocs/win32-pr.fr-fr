---
description: les Windows Installer fonctions, les tables et les propriétés répertoriées sur cette page ne sont pas prises en charge par Windows Installer&\# 160 ; 3.1 et versions antérieures.
ms.assetid: fbf75dbe-3fa1-424b-83bb-cfd0b179107c
title: non pris en charge dans Windows Installer 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a221d80f56c5737cc5ae92a040a005ae42449e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111017"
---
# <a name="not-supported-in-windows-installer-31"></a>non pris en charge dans Windows Installer 3,1

les fonctions Windows Installer, les tables et les propriétés répertoriées sur cette page ne sont pas prises en charge par Windows Installer 3,1 et versions antérieures. L’absence d’une fonctionnalité dans cette liste ne garantit pas que la fonctionnalité est prise en charge. consultez la documentation principale pour déterminer quelle version de Windows Installer est requise pour une fonctionnalité particulière. pour plus d’informations sur les autres versions [de Windows Installer, consultez nouveautés de Windows Installer](what-s-new-in-windows-installer.md).

Windows le programme d’installation 3,1 est disponible pour Windows Server 2003, Windows XP ou Windows 2000. pour obtenir la liste de toutes les versions de Windows Installer et des fichiers redistribuables, consultez [versions publiées de Windows Installer](released-versions-of-windows-installer.md).

les fonctionnalités suivantes ne sont pas prises en charge dans Windows Installer 3,1 et versions antérieures.

[Fonctions du programme d’installation](installer-functions.md)

-   [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)

[Propriétés](properties.md)

-   [**MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)
-   [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md)
-   [**MSIDISABLERMRESTART**](msidisablermrestart.md)
-   [**MsiLogFileLocation**](msilogfilelocation.md)
-   [**MsiLogging**](msilogging.md)
-   [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)
-   [**MsiRestartManagerSessionKey**](msirestartmanagersessionkey.md)
-   [**MSIRMSHUTDOWN**](msirmshutdown.md)
-   [**MsiRunningElevated**](msirunningelevated-.md)
-   [**MsiSystemRebootPending**](msisystemrebootpending.md)
-   [**MsiTabletPC**](msitabletpc.md)
-   [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md)

[Propriétés des informations de résumé](summary-information-stream-reference.md)

-   La [**propriété Résumé du nombre de mots**](word-count-summary.md) contient de nouveaux bits d’indicateur pour spécifier si l’installation du package requiert des privilèges élevés.

[Stratégie système](system-policy.md)

-   [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md)
-   [DisableLoggingFromPackage](disableloggingfrompackage.md)

[Tables de base de données](database-tables.md)

-   [Tableau de raccourcis](shortcut-table.md)

    Nouvelles colonnes : DisplayResourceDLL, DisplayResourceId, DescriptionResourceDLL et DescriptionResourceId

[Boîtes de dialogue](dialog-boxes.md)

-   [Boîte de dialogue MsiRMFilesInUse](msirmfilesinuse-dialog.md)

[Attributs du contrôle](control-attributes.md)

-   [ElevationShield](elevationshield-attribute.md)

[ControlEvents](control-events.md)

-   [RmShutdownAndRestart](rmshutdownandrestart-controlevent.md)

[Types de messages d’interface utilisateur externes](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)

-   INSTALLLOGMODE \_ RMFILESINUSE

[Windows Programme d’installation sur les systèmes d’exploitation 64 bits](windows-installer-on-64-bit-operating-systems.md)

-   attribut **msidbComponentAttributesDisableRegistryReflection** dans la [table des composants](component-table.md)

[Interface d’automatisation](automation-interface.md)

-   Méthodes de l' [ **objet installer**](installer-object.md)

    -   [**Programme d’installation. AdvertiseProduct**](installer-advertiseproduct.md)
    -   [**Programme d’installation. AdvertiseScript**](installer-advertisescript.md)
    -   [**Programme d’installation. CreateAdvertiseScript**](installer-createadvertisescript.md)
    -   [**Installer. ProvideAssembly**](installer-provideassembly.md)

-   Propriétés de l' [ **objet installer**](installer-object.md)

    -   [**Programme d’installation. PatchFiles**](installer-patchfiles.md)
    -   [**Programme d’installation. ProductElevated**](installer-productelevated.md)
    -   [**Programme d’installation. ProductInfoFromScript**](installer-productinfofromscript.md)

## <a name="notes"></a>Notes

le service Windows Installer doit s’exécuter sur Windows Vista pour permettre l’utilisation du [gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md), du [*contrôle de compte d’utilisateur*](u-gly.md)et des mises à [jour correctives du contrôle de compte d’utilisateur (UAC)](user-account-control--uac--patching.md). pour plus d’informations, consultez [utilisation de Windows Installer avec le gestionnaire de redémarrage](using-windows-installer-with-restart-manager.md) et [utilisation de Windows Installer avec](using-windows-installer-with-uac.md) [le contrôle de compte d’utilisateur](user-account-control--uac--patching.md)et la mise à jour corrective.

Windows le programme d’installation 3,1 prend en charge la Protection de fichiers Windows (WFP) et ne prend pas en charge Protection des ressources Windows (WRP). WRP dans Windows server 2008 et Windows Vista remplace WFP dans Windows server 2003, Windows XP et Windows 2000. pour plus d’informations sur les Windows Installer et WFP, consultez [utilisation de Windows Installer et de Protection des ressources Windows](windows-resource-protection-on-windows-vista.md).

 

 
