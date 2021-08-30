---
description: un correctif Windows Installer (fichier. msp) est un fichier utilisé pour fournir des mises à jour à des applications Windows Installer.
ms.assetid: f59736d7-0b5a-466c-ab60-f210ccccb07f
title: Packages de correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c933ff632774652c7c2a6f23a57ea94ebfff20ac5ac263006a567f66e628ac0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074829"
---
# <a name="patch-packages"></a>Packages de correctifs

un correctif Windows Installer (fichier. msp) est un fichier utilisé pour fournir des mises à jour à des applications Windows Installer. Le correctif est un package autonome qui contient toutes les informations requises pour mettre à jour l’application. un package correctif (fichier. msp) peut être bien plus petit que le package Windows Installer (fichier .msi) pour l’ensemble de l’application mise à jour. Pour plus d’informations sur la distribution de petites mises à jour pour les applications, consultez réduction de la [taille des correctifs](reducing-patch-size.md).

Un package correctif contient les mises à jour réelles de l’application et décrit les versions de l’application qui peuvent recevoir le correctif. Les correctifs contiennent au minimum deux transformations de base de données. Une transformation met à jour les informations dans la base de données d’installation de l’application. L’autre transformation ajoute des informations que le programme d’installation utilise pour l’application de correctifs aux fichiers. Le programme d’installation utilise les informations fournies par les transformations pour appliquer les fichiers correctifs stockés dans le flux de fichier CAB du package correctif. Un package de correctifs n’a pas de base de données comme un package d’installation (fichier .msi.)

à partir de Windows Installer version 3,0, les packages de correctifs peuvent contenir des informations qui décrivent la séquence de mise à jour corrective pour le correctif par rapport à d’autres mises à jour dans la table [MsiPatchSequence](msipatchsequence-table.md) et des informations descriptives supplémentaires dans la table [MsiPatchMetadata](msipatchmetadata-table.md) .

Les utilisateurs peuvent installer des applications et des mises à jour à partir d’une image administrative réseau. Bien que les packages de correctifs puissent être appliqués aux installations administratives, la méthode recommandée pour fournir des mises à jour consiste à faire en sorte que les utilisateurs installent l’application d’origine, puis appliquent les correctifs à l’instance locale de l’application sur leur ordinateur. Cela permet aux utilisateurs de synchroniser avec l’image administrative. Si un correctif est appliqué à l’installation administrative, tous les clients de cette installation administrative doivent remettre en cache et réinstaller l’application pour recevoir la mise à jour. Tant qu’un utilisateur n’est pas remis en cache et réinstallé, il ne peut pas installer les installations à la demande et de réparation à partir de l’installation d’administration corrigée.

à partir de Windows Installer 3,0, les utilisateurs non-administrateurs peuvent appliquer des correctifs aux applications gérées par l’utilisateur une fois que le correctif a été approuvé par un administrateur. Pour plus d’informations sur la façon de procéder, consultez Mise à [jour corrective des Applications Per-User gérées](patching-per-user-managed-applications.md). Une autre méthode consiste à utiliser la mise à jour corrective des comptes d’utilisateur avec le moins de privilèges possible.

> [!Note]  
> Si la stratégie [AllowLockdownPatch](allowlockdownpatch.md) a été définie, les utilisateurs non-administrateurs peuvent appliquer un correctif à une application existante tout en exécutant une installation avec des privilèges élevés. Cette méthode n’est pas recommandée, car elle permet d’appliquer des correctifs non approuvés à une application pouvant s’exécuter avec des privilèges élevés.

 

Les packages de correctifs sont composés des éléments suivants. Pour plus d’informations sur la construction des packages de correctifs, consultez [création d’un package de correctifs](creating-a-patch-package.md).

## <a name="summary-information-stream"></a>Flux d’informations de synthèse

Le flux d’informations de synthèse du package correctif fournit des informations sur l’identité et l’objectif du correctif.

Le flux d’informations de Résumé contient au minimum les éléments suivants :

-   GUID qui identifie de façon unique le correctif. Le GUID de ce correctif est ajouté à une liste de GUID pour les correctifs antérieurs qui sont remplacés par ce correctif.
-   Liste délimitée par des points-virgules des codes de produit pour les cibles valides pour ce correctif.
-   Liste délimitée par des points-virgules de noms de sous-stockage de transformation dans l’ordre dans lequel ils doivent être traités.
-   Liste de sources délimitées par des points-virgules pour ce correctif.

## <a name="transform-substorage"></a>Transformer le sous-stockage

Un package correctif contient des transformations qui permettent d’ajouter ou de supprimer des fichiers, des entrées de Registre, des interfaces utilisateur et des personnalisations. Les transformations sont incluses en tant que sous-stockage dans le package. Un package correctif contient deux transformations pour chaque base de données cible. Une transformation correspond aux mises à jour réelles de la base de données d’installation et est générée à partir des différences entre les images d’origine et les images mises à jour du package d’installation. L’autre transformation ajoute des entrées aux tables [patch](patch-table.md), [PatchPackage](patchpackage-table.md), [Media](media-table.md), [InstallExecuteSequence](installexecutesequence-table.md)et [AdminExecuteSequence](adminexecutesequence-table.md) . Les informations contenues dans le sous-stockage l’associent à une [**UpgradeCode**](upgradecode.md), [**ProductCode**](productcode.md), [**ProductVersion**](productversion.md)et [**ProductLanguage**](productlanguage.md)spécifiques. Un package correctif qui peut être appliqué à plusieurs cibles contient plusieurs paires de ces transformations.

## <a name="cabinet-file-stream"></a>Flux de fichier CAB

Le flux de fichier CAB inclus dans un correctif peut contenir les types de fichiers suivants :

-   Fichiers correctifs contenant les informations nécessaires pour modifier l’ancienne version du fichier dans la nouvelle version. Un seul fichier correctif peut être utilisé pour mettre à jour une ou plusieurs anciennes versions d’un fichier.
-   Les fichiers supplémentaires ajoutés à l’application ne sont pas présents dans l’ancienne version.
-   Un fichier de remplacement entier. Dans les rares cas où la nouvelle version d’un fichier est plus petite que le correctif requis pour mettre à jour l’ancienne version de ce fichier, le nouveau fichier peut être inclus dans son intégralité. Il s’agit de nouveaux fichiers qui sont installés sur leurs anciennes versions.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’un package de correctifs](creating-a-patch-package.md)
</dt> </dl>

 

 



