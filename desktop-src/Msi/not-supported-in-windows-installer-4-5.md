---
description: les fonctions Windows Installer, les tables et les propriétés répertoriées sur cette page ne sont pas prises en charge par Windows Installer&\# 160 ; 4.5 et les versions antérieures.
ms.assetid: 89662e62-53fb-4b50-8583-80518c6fda6d
title: non pris en charge dans Windows Installer 4,5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a285094610f0a00a39a26bb2d0683cb41afdfa3ed126ac27f7655c3cd56df17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979349"
---
# <a name="not-supported-in-windows-installer-45"></a>non pris en charge dans Windows Installer 4,5

les fonctions Windows Installer, les tables et les propriétés répertoriées sur cette page ne sont pas prises en charge par Windows Installer 4,5 et versions antérieures. L’absence d’une fonctionnalité dans cette liste ne garantit pas que la fonctionnalité est prise en charge. consultez la documentation principale pour déterminer quelle version de Windows Installer est requise pour une fonctionnalité particulière. pour plus d’informations sur les autres versions [de Windows Installer, consultez nouveautés de Windows Installer](what-s-new-in-windows-installer.md).

Windows le programme d’installation 4,5 est disponible en tant que redistribuable pour Windows Server 2008, Windows Vista avec service pack 1 (SP1), Windows XP avec service pack 2 (SP2) et versions ultérieures et Windows Server 2003 avec service pack 1 (sp1) et versions ultérieures. pour obtenir la liste complète de toutes les versions de Windows Installer et des fichiers redistribuables, consultez [versions publiées de Windows Installer](released-versions-of-windows-installer.md).

les fonctionnalités suivantes ne sont pas prises en charge dans Windows Installer 4,5 et versions antérieures.

[Actions standard](standard-actions.md)

-   [MsiConfigureServices](msiconfigureservices-action.md)

[Fonctions du programme d’installation](installer-functions.md)

-   [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
-   [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
-   [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)

[Types de données de colonne](column-data-types.md)

-   [**FormattedSDDLText**](formattedsddltext.md)

[Propriétés](properties.md)

-   [**MSIFASTINSTALL**](msifastinstall.md)
-   [**MSIINSTALLPERUSER**](msiinstallperuser.md)

[Tables de base de données](database-tables.md)

-   [Table MsiServiceConfig](msiserviceconfig-table.md)
-   [Table MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md)
-   [Table MsiShortcutProperty](msishortcutproperty-table.md)
-   [Table MsiLockPermissionsEx](msilockpermissionsex-table.md)

[ControlEvents](control-events.md)

-   [MsiPrint ControlEvent,](msiprint-controlevent.md)
-   [MsiLaunchApp ControlEvent,](msilaunchapp-controlevent.md)

[Contrôles](controls.md)

-   [Contrôle HyperLink](hyperlink-control.md)
-   Prise en charge du [contrôle bitmap](bitmap-control.md) des formats de fichiers image WIC

[Évaluateurs de cohérence internes-CIEM](internal-consistency-evaluators-ices.md)

-   [ICE102](ice-102.md)
-   [ICE103](ice-103.md)
-   [ICE104](ice-104.md)
-   [ICE105](ice-105.md)

[Interface d’automatisation](automation-interface.md)

-   Propriétés de l' [ **objet installer**](installer-object.md)

    -   [**Programme d’installation. ClientsEx**](installer-clientsex.md)
    -   [**Programme d’installation. ComponentsEx**](installer-componentsex.md)
    -   [**Programme d’installation. ComponentPathEx**](installer-componentpathex.md)

-   Propriétés de l' [ **objet Component**](components.md)

    -   [**Composant. ComponentCode**](component-componentcode.md)
    -   [**Composant. UserSID**](component-usersid.md)
    -   [**Composant. Context**](component-context.md)

-   Propriétés de l' [ **objet client**](client.md)

    -   [**Client. ProductCode**](client-productcode.md)
    -   [**Client. ComponentCode**](client-componentcode.md)
    -   [**Client. UserSID**](client-usersid.md)
    -   [**Client. Context**](client-context.md)

-   Propriétés de l’objet [**ComponentInfo**](componentinfo.md)

    -   [**ComponentInfo.ComponentCode**](componentinfo-componentcode.md)
    -   [**ComponentInfo. Path**](componentinfo-path.md)
    -   [**ComponentInfo. State**](componentinfo-state.md)

## <a name="notes"></a>Remarques

Windows Le programme d’installation 4,5 ne prend pas en charge certaines fonctionnalités qui permettent l’installation d’un package d’installation unique dans le contexte d’installation par ordinateur ou par utilisateur. Pour plus d’informations, consultez [création de package unique](single-package-authoring.md).

Windows Le programme d’installation 4,5 ne prend pas en charge certaines options de configuration de services qui peuvent permettre à un package de personnaliser les [services](../services/services.md) sur un ordinateur. Pour plus d’informations, consultez Utilisation de la [Configuration des services](using-services-configuration.md).

Windows le programme d’installation 4,5 ne prend pas en charge certaines fonctionnalités qui permettent au Windows Installer de sécuriser de nouveaux comptes, [services](../services/services.md)Windows, fichiers, dossiers et clés de registre. Pour plus d’informations, consultez [sécurisation des ressources](securing-resources-.md).

Windows Le programme d’installation 4,5 ne prend pas en charge certaines fonctionnalités permettant à l’installation d’énumérer tous les composants installés sur l’ordinateur et d’obtenir le chemin d’accès à la clé du composant. Pour plus d’informations, consultez [énumération de composants](enumerating-components-.md).

 

 
