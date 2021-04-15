---
description: Le fait de pouvoir désinstaller un correctif dépend de la manière dont le correctif a été créé, de la version de Windows Installer utilisée pour installer le correctif et des modifications apportées par le correctif à l’application.
ms.assetid: 95a5365c-e2ae-4e35-9aeb-67d04e67c7df
title: Correctifs désinstallés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad46d85318378ed81d2278d3ea1290152723704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524886"
---
# <a name="uninstallable-patches"></a>Correctifs désinstallés

Le fait de pouvoir désinstaller un correctif dépend de la manière dont le correctif a été créé, de la version de Windows Installer utilisée pour installer le correctif et des modifications apportées par le correctif à l’application. Si un correctif ne peut pas être installé, le seul moyen de supprimer le correctif consiste à désinstaller l’application entière et à la réinstaller sans appliquer le correctif en cours de suppression.

Vous pouvez appeler pour la désinstallation des correctifs appliqués avec Windows Installer version 3,0 en utilisant les [options de ligne de commande](command-line-options.md), la fonction [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) ou la [**méthode RemovePatches**](installer-removepatches.md) comme décrit dans la section [désinstallation des correctifs](uninstalling-patches.md) . Le Windows Installer vérifie que chacun des correctifs listés pour suppression dans la propriété [**MSIPATCHREMOVE**](msipatchremove.md) est impossible à installer. Si l’utilisateur n’a pas les privilèges nécessaires pour supprimer le correctif, si le correctif est inconnu pour le produit, si la stratégie de correctifs empêche la suppression ou si le correctif a été marqué comme ne faisant pas l’être, le programme d’installation renvoie une erreur indiquant la défaillance d’une transaction d’installation.

**Windows Installer 2,0 :** Non pris en charge. Les correctifs appliqués à l’aide d’une version de Windows Installer antérieure à Windows Installer 3,0 ne peuvent pas être installés.

## <a name="patches-that-are-not-uninstallable"></a>Correctifs qui ne peuvent pas être installés

Les correctifs (fichiers. msp) appliqués à une application installée ne sont pas désinstallés dans les cas suivants. La seule méthode pour supprimer un correctif logiciel qui ne peut pas être installé consiste à désinstaller l’application corrigée, puis à réinstaller l’application sans réappliquer le correctif. Dans ce cas, vous devez réappliquer tous les correctifs que vous ne souhaitez pas supprimer de l’application.

-   Les correctifs appliqués à l’aide d’une version de Windows Installer inférieure à Windows Installer 3,0 ne peuvent pas être installés.
-   Les correctifs appliqués aux applications installées sur un ordinateur sur lequel la stratégie [DisablePatchUninstall](disablepatchuninstall.md) est définie par un administrateur ne peuvent pas être installés. Une fois cette [stratégie d’ordinateur](machine-policies.md)définie, aucun correctif sur l’ordinateur ne peut être désinstallé, même par un administrateur.
-   Les correctifs qui n’ont pas de table [MsiPatchMetadata](msipatchmetadata-table.md) dans leur base de données ne peuvent pas être installés.
-   Les correctifs qui n’incluent pas la ligne suivante dans leur table [MsiPatchMetadata](msipatchmetadata-table.md) ne peuvent pas être installés. Le correctif ne peut pas être installé pour d’autres valeurs de société, propriété et valeur.

    | Company | Propriété     | Valeur |
    |---------|--------------|-------|
    | Nul  | AllowRemoval | 1     |

    

     

-   Le correctif a été appliqué à une application installée dans un contexte pour lequel l’utilisateur ne dispose pas des privilèges suffisants pour désinstaller les correctifs. Les mots « non autorisés » dans le tableau suivant indiquent qu’un utilisateur administrateur ou non-administrateur ne peut pas désinstaller les correctifs des applications corrigées installées dans ce contexte. Le mot « autorisé » dans ce tableau signifie que les privilèges n’empêchent pas un administrateur ou un utilisateur non-administrateur de désinstaller des correctifs, mais pour l’une des autres raisons évoquées dans cette section, il n’est pas toujours possible de désinstaller le correctif.

    | Contexte d’installation de l’application        | Désinstallation du correctif par l’administrateur | Désinstallation du correctif non-administrateur                                                                                                                                                                                                                                                                             |
    |-----------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Per-Machine                             | Autorisé                          | En général, cette exception n’est pas autorisée uniquement si le correctif a été appliqué à l’aide de la mise à jour corrective (LUA). Un correctif marqué comme correctif LUA peut être désinstallé par les administrateurs ou les non-administrateurs. La mise à jour corrective LUA est disponible uniquement pour les packages installés par ordinateur à partir du support et nécessitant une création spéciale.<br/> |
    | Per-User non géré pour l’utilisateur actuel   | Autorisé                          | Autorisé                                                                                                                                                                                                                                                                                                          |
    | Per-User non géré pour un autre utilisateur | Non autorisée                      | Non autorisée                                                                                                                                                                                                                                                                                                      |
    | Per-User géré pour l’utilisateur actuel       | Autorisé                          | Non autorisée                                                                                                                                                                                                                                                                                                      |
    | Per-User géré pour un autre utilisateur     | Non autorisée                      | Non autorisée                                                                                                                                                                                                                                                                                                      |

    

     

-   Une [mise à niveau majeure](major-upgrades.md) appliquée par un correctif logiciel n’est pas désinstallée. Les mises à niveau majeures d’une application doivent être effectuées en installant l’application mise à niveau (fichier. msi) plutôt qu’un correctif.
-   Les correctifs appliqués à une installation d’administration ne peuvent pas être installés. La mise à jour corrective des installations administratives n’est pas recommandée. L’ensemble actuel de correctifs doit être appliqué sur l’ordinateur de l’utilisateur une fois que l’utilisateur a installé l’application à partir de l’image administrative. Cela peut empêcher le [Code du package](package-codes.md) mis en cache sur l’ordinateur de l’utilisateur de devenir différent du code du package sur l’installation d’administration. Si le code de package mis en cache sur l’ordinateur de l’utilisateur est différent de celui utilisé lors de l’installation administrative, réinstallez l’application à partir de l’installation administrative, puis corrigez l’ordinateur client.
-   Lorsqu’un correctif ajoute du nouveau contenu à l’une des tables de la liste suivante, Windows Installer marque le correctif comme ne devant pas être installé. Un correctif pouvant être installé peut ajouter de nouveaux fichiers, des assemblys, des entrées de Registre, des composants ou des fonctionnalités à une installation en ajoutant de nouvelles lignes aux tables de base de données qui ne sont pas incluses dans cette liste.

    -   [AppId](appid-table.md)
    -   [BindImage](bindimage-table.md)
    -   [Classe](class-table.md)
    -   [ComPlus](complus-table.md)
    -   [CreateFolder](createfolder-table.md)
    -   [DuplicateFile](duplicatefile-table.md)
    -   [Environment](environment-table.md)
    -   [Extension](extension-table.md)
    -   [Police](font-table.md)
    -   [IniFile](inifile-table.md)
    -   [IsolatedComponent](isolatedcomponent-table.md)
    -   [LockPermissions](lockpermissions-table.md)
    -   [MsiLockPermissionsEx](msilockpermissionsex-table.md)
    -   [MIME](mime-table.md)
    -   [MoveFile](movefile-table.md)
    -   [MsiServiceConfig](msiserviceconfig-table.md)
    -   [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md)
    -   [ODBCAttribute](odbcattribute-table.md)
    -   [ODBCDataSource](odbcdatasource-table.md)
    -   [ODBCDriver](odbcdriver-table.md)
    -   [ODBCSourceAttribute](odbcsourceattribute-table.md)
    -   [ODBCTranslator](odbctranslator-table.md)
    -   [ProgId](progid-table.md)
    -   [PublishComponent](publishcomponent-table.md)
    -   [RemoveIniFile](removeinifile-table.md)
    -   [SelfReg](selfreg-table.md)
    -   [ServiceControl](servicecontrol-table.md)
    -   [ServiceInstall](serviceinstall-table.md)
    -   [Exportation](typelib-table.md)
    -   [Verbe](verb-table.md)
    -   [!Note]  
        > Si un correctif ajoute du nouveau contenu aux tables [RemoveFile](removefile-table.md) ou [RemoveRegistry](removeregistry-table.md) , Windows Installer ne marque pas le correctif comme ne devant pas être installé. Toutefois, le correctif ne peut pas être installé, sauf si la ressource pour supprimer le nouveau contenu n’existe pas déjà dans le package d’installation d’origine. Par exemple, si le correctif ajoute une nouvelle ligne à la table RemoveFile, le fichier supprimé ne peut pas être restauré en désinstallant le correctif si le fichier est externe à la [table de fichiers](file-table.md). Le fichier doit avoir été créé dans la table de fichiers du package d’origine, plus les correctifs appliqués pour le correctif à des fins de désinstallation.

         

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Séquencement des correctifs](sequencing-patches.md)
</dt> <dt>

[Suppression des correctifs](removing-patches.md)
</dt> <dt>

[Désinstallation des correctifs](uninstalling-patches.md)
</dt> <dt>

[Actions personnalisées de désinstallation des correctifs](patch-uninstall-custom-actions.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 




