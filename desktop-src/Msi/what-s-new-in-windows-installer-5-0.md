---
description: Les informations contenues dans cette rubrique identifient les ajouts et les modifications qui sont disponibles dans Windows Installer&\# 160 ; 5.0.
ms.assetid: c088c15b-0eef-4a92-bb65-e7fe871afbfe
title: Nouveautés de Windows Installer 5,0
ms.topic: article
ms.date: 11/08/2019
ms.openlocfilehash: ae7986cec60341127ab00ad08a3032aad80209bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861890"
---
# <a name="whats-new-in-windows-installer-50"></a>Nouveautés de Windows Installer 5,0

Les informations contenues dans cette rubrique identifient les ajouts et les modifications qui sont disponibles dans Windows Installer 5,0.

Windows Installer 5,0 est inclus avec les versions suivantes de Windows :

* Client : Windows 7 et toutes les versions ultérieures.
* Serveur : Windows Server 2008 R2 et toutes les versions ultérieures.

> [!NOTE]
> Il n’existe aucun redistribuable pour Windows Installer 5,0. Pour obtenir la liste des fichiers redistribuables disponibles pour les versions précédentes de Windows Installer, consultez [Windows Installer redistribuables](windows-installer-redistributables.md). Pour obtenir la liste complète des versions de Windows Installer, consultez [versions publiées de Windows Installer](released-versions-of-windows-installer.md).

Cette page est fournie en tant que guide de la documentation. Vous devez vous reporter à la section relative à la configuration requise sur les pages de référence principales pour déterminer la configuration requise du système d’exploitation. Les parties du Windows Installer qui ne sont pas liées à partir de cette page peuvent être disponibles dans une autre version du Windows Installer. Pour plus d’informations sur les autres versions de Windows Installer, consultez [What’s New in Windows Installer](what-s-new-in-windows-installer.md).

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

[Propriétés des informations de résumé](summary-information-stream-reference.md)

-   Le [**Résumé du modèle**](template-summary.md) a de nouvelles valeurs pour indiquer que la base de données est compatible avec Windows RT ou la plateforme Arm64.

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

[Évaluateurs de cohérence internes-CIEM](internal-consistency-evaluators-ices.md)

-   [ICE101](ice-101.md)
-   [ICE102](ice-102.md)
-   [ICE103](ice-103.md)
-   [ICE104](ice-104.md)
-   [ICE105](ice-105.md)

[Interface d’automatisation](automation-interface.md)

-   Propriétés de l' [ **objet installer**](installer-object.md)

    -   [**Programme d’installation. ClientsEx**](installer-clientsex.md)
    -   [**Programme d’installation. ComponentsEx**](installer-componentsex.md)
    -   [**Programme d’installation. ComponentPathEx**](installer-componentpathex.md)

-   Propriétés de l' [ **objet Components**](components.md)

    -   [**Components. ComponentCode**](component-componentcode.md)
    -   [**Components. UserSID**](component-usersid.md)
    -   [**Components. Context**](component-context.md)

-   Propriétés de l' [ **objet client**](client.md)

    -   [**Client. ProductCode**](client-productcode.md)
    -   [**Client. ComponentCode**](client-componentcode.md)
    -   [**Client. UserSID**](client-usersid.md)
    -   [**Client. Context**](client-context.md)

-   Propriétés de l’objet [**ComponentInfo**](componentinfo.md)

    -   [**ComponentInfo.ComponentCode**](componentinfo-componentcode.md)
    -   [**ComponentInfo. Path**](componentinfo-path.md)
    -   [**ComponentInfo. State**](componentinfo-state.md)

## <a name="notes"></a>Notes

Les développeurs du programme d’installation peuvent utiliser Windows Installer 5,0 pour créer un package d’installation unique pouvant être installé par ordinateur ou par utilisateur de l’application. Pour plus d’informations, consultez [création de package unique](single-package-authoring.md). L’évaluateur de cohérence interne [ICE105](ice-105.md) vérifie que le package a été créé pour être installé dans un contexte par utilisateur. Une application qui peut être installée, mise à jour, exécutée et supprimée par un utilisateur standard sans élévation est appelée Per-User application (PUA.) Un PUA peut offrir une meilleure expérience utilisateur, réduire les effets sur le système et les autres utilisateurs de l’ordinateur, et réserve les invites UAC aux situations qui nécessitent réellement l’élévation des privilèges de l’utilisateur. Les fonctionnalités de création de package unique de Windows Installer 5,0 peuvent faciliter le développement d’applications Per-User.

Les options de configuration des services permettent à un package Windows Installer de personnaliser les [services](../services/services.md) sur un ordinateur. Pour plus d’informations, consultez Utilisation de la [Configuration des services](using-services-configuration.md).

À partir de Windows Installer 5,0, un package Windows Installer peut sécuriser les nouveaux comptes, les [services](../services/services.md)Windows, les fichiers, les dossiers et les clés de registre. La table [MsiLockPermissionsEx](msilockpermissionsex-table.md) peut spécifier un descripteur de sécurité qui refuse des autorisations, spécifie l’héritage des autorisations d’une ressource parent ou spécifie les autorisations d’un nouveau compte. Pour plus d’informations, consultez [sécurisation des ressources](securing-resources-.md).

Windows Installer 5,0 peut énumérer tous les composants installés sur l’ordinateur et obtenir le chemin d’accès à la clé du composant. Pour plus d’informations, consultez [énumération de composants](enumerating-components-.md).

Windows Installer 5,0 s’exécutant sur Windows Server 2012 ou Windows 8 prend en charge l’installation d’applications approuvées sur Windows RT. Un package Windows Installer, un correctif ou une transformation qui n’a pas été signé par Microsoft ne peut pas être installé sur Windows RT. La propriété [**Résumé du modèle**](template-summary.md) indique la plateforme qui est compatible avec la base de données d’installation et doit inclure la valeur pour Windows RT.

Windows Installer 5,0 s’exécutant sur Windows 10 sur des processeurs Arm64 prend en charge l’installation d’applications compilées spécifiquement pour la plate-forme Arm64.  La propriété [**Résumé du modèle**](template-summary.md) de ces packages doit inclure la valeur Arm64. 

 
