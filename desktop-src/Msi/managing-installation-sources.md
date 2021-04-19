---
description: Les utilisateurs et les applications avec des privilèges d’administrateur peuvent récupérer et modifier les informations de liste de sources de données, d’URL et de réseau pour Windows Installer les applications et les correctifs sur le système.
ms.assetid: e8c66bad-f594-4926-b3b4-c8b245dcfa83
title: Gestion des sources d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7fc45253af20ae5f9792ee3a5ec7dd318c80295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541238"
---
# <a name="managing-installation-sources"></a>Gestion des sources d’installation

Les utilisateurs et les applications avec des privilèges d’administrateur peuvent récupérer et modifier les informations de liste de sources de données, d’URL et de réseau pour Windows Installer les applications et les correctifs sur le système.

**Windows Installer 2,0 :** Non pris en charge. Les administrateurs ne peuvent pas lire, réorganiser ou remplacer des entrées dans la liste source et ne peuvent pas modifier ou récupérer les propriétés de la liste source. Il est possible de gérer des sources réseau, mais pas des sources d’URL ou de médias. Les administrateurs peuvent uniquement gérer des listes de sources pour les applications par ordinateur ou les applications installées en fonction de l’utilisateur actuel. Cela empêche les administrateurs qui utilisent des versions antérieures à Windows Installer version 3,0 de gérer les informations de liste source pour tous les utilisateurs du système.

**Windows Installer 3,0 et versions ultérieures :** Les utilisateurs et les applications qui possèdent des privilèges d’administrateur peuvent récupérer et modifier les informations de liste source pour les applications Windows Installer et les correctifs installés sur le système pour tous les utilisateurs. Les fonctions de liste source peuvent être utilisées pour gérer des listes sources et des propriétés de liste source pour les sources de réseau, d’URL et de média. Le programme d’installation peut réorganiser les listes de sources à partir d’un processus externe.

Les utilisateurs et les applications qui ont des privilèges d’administrateur peuvent lire et modifier les types suivants d’informations de liste source :

-   Listes de sources pour les applications et les correctifs installés pour tous les utilisateurs sur le système.
-   Listes sources pour les sources de correctifs qui existent indépendamment des sources de l’application.
-   Listes sources pour les sources d’URL et de supports qui existent en dehors des sources réseau.
-   Propriétés de la liste source, telles que [**MEDIAPACKAGEPATH**](mediapackagepath.md), [**DiskPrompt**](diskprompt.md), **LastUsedSource**, **LastUsedType** et **PackageName**.

Les fonctions de listes de sources peuvent limiter l’étendue des listes sources trouvées en spécifiant le contexte d’installation et le contexte de l’utilisateur. Il existe trois contextes d’installation possibles : par utilisateur (non géré), par ordinateur et par utilisateur. Le contexte de l’utilisateur peut être un utilisateur particulier ou tous les utilisateurs du système.

Les non-administrateurs ne peuvent pas modifier la liste source d’une instance d’une application ou d’un correctif qui existe dans le contexte d’un autre utilisateur (managé ou non géré). Les non-administrateurs peuvent modifier les listes sources d’une instance d’une application ou d’un correctif installé dans les contextes suivants :

-   Leur propre contexte par utilisateur (non managé).
-   Le contexte de l’ordinateur, mais uniquement si les stratégies [DisableBrowse](disablebrowse.md), [AllowLockdownBrowse](allowlockdownbrowse.md)et [AlwaysInstallElevated a](alwaysinstallelevated.md) les permettent de rechercher une source d’application ou de correctif.
-   Leur propre contexte géré par utilisateur, mais uniquement si les stratégies [DisableBrowse](disablebrowse.md), [AllowLockdownBrowse](allowlockdownbrowse.md)et [AlwaysInstallElevated a](alwaysinstallelevated.md) leur permettent de rechercher une source d’application ou de correctif.

Les administrateurs peuvent modifier les listes de sources qu’un non-administrateur peut modifier. En outre, les administrateurs et les applications qui possèdent des privilèges d’administrateur peuvent modifier les listes sources d’une application ou d’un correctif installé dans les contextes suivants :

-   Contexte par ordinateur.
-   Leur propre utilisateur (non managé) ou son propre contexte géré par utilisateur.
-   Contexte géré par utilisateur d’un autre utilisateur.

> [!Note]  
> Les utilisateurs et les applications qui ont des privilèges d’administration ne peuvent pas modifier la liste source d’une instance d’une application ou d’un correctif installé dans le contexte par utilisateur (non géré) d’un autre utilisateur.

 

## <a name="managing-network-and-url-sources-for-products-and-patches"></a>Gestion des sources de réseau et d’URL pour les produits et les correctifs

Utilisez la fonction [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) pour ajouter ou réorganiser la liste source des sources réseau et URL pour un correctif ou une application dans un contexte particulier. Utilisez le paramètre *dwContext* pour spécifier le contexte d’installation. Utilisez le paramètre *szUserSid* pour spécifier le contexte de l’utilisateur.

Utilisez la fonction [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) pour créer une liste source pour un correctif qui n’a pas encore été appliqué à une application dans le contexte spécifié. Cela peut être utile lors de l’inscription d’un correctif à des privilèges élevés. Pour plus d’informations sur l’inscription des privilèges élevés pour un correctif, consultez Mise à [jour corrective Per-User applications gérées](patching-per-user-managed-applications.md).

Utilisez la fonction [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea) pour supprimer une source existante pour une application ou un correctif dans un contexte spécifié. La suppression de la source actuelle d’une application ou d’un correctif force le programme d’installation à rechercher une source dans la liste source la prochaine fois qu’une source est requise.

Utilisez la fonction [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) pour énumérer les sources dans la liste source d’un correctif ou d’une application spécifique.

## <a name="managing-media-sources-for-products-and-patches"></a>Gestion des sources multimédias pour les produits et les correctifs

Utilisez la fonction [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska) pour ajouter ou mettre à jour les informations de disque de la source du média d’une application ou d’un correctif inscrit. Chaque entrée est identifiée de manière unique par un ID de disque. Si le disque existe déjà, il est mis à jour avec les nouvelles valeurs de nom de volume et d’invite de disque. Si le disque n’existe pas, une nouvelle entrée de disque est créée avec les nouvelles valeurs.

Utilisez la fonction [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska) pour supprimer un disque inscrit existant sous la source du média pour une application ou un correctif dans un contexte spécifique.

Utilisez la fonction [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa) pour énumérer une liste de disques enregistrés sous la source du média pour une application ou un correctif.

## <a name="retrieval-and-modification-of-source-list-information"></a>Récupération et modification des informations de la liste source

Utilisez les fonctions [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) et [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) pour récupérer ou modifier des informations sur la liste source pour une application ou un correctif dans un contexte spécifique. Utilisez le paramètre *dwContext* pour spécifier le contexte d’installation. Utilisez le paramètre *szUserSid* pour spécifier le contexte de l’utilisateur.

Vous pouvez accéder aux propriétés de la liste source, telles que [**MEDIAPACKAGEPATH**](mediapackagepath.md), [**DiskPrompt**](diskprompt.md), **LastUsedSource**, **LastUsedType** et **PackageName** .

> [!Note]  
> La propriété de la liste source **LastUsedType** peut uniquement être lue. Elle ne peut pas être définie directement à l’aide de la fonction [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) .

 

## <a name="clearing-the-complete-source-list-or-forcing-a-source-resolution"></a>Effacement de la liste source complète ou forçage d’une résolution source

Utilisez la fonction [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa) pour supprimer toutes les sources existantes d’un type de source donné pour l’application ou l’instance de correctif spécifiée. L’inscription du correctif est également supprimée si le correctif n’est pas installé par une application dans le même contexte. Utilisez le paramètre *dwContext* pour spécifier le contexte d’installation. Utilisez le paramètre *szUserSid* pour spécifier le contexte de l’utilisateur.

Utilisez [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa) pour effacer la dernière entrée source utilisée pour une application ou un correctif dans le contexte spécifié. Cette fonction supprime l’inscription de la propriété appelée **LastUsedSource**. Cette fonction n’affecte pas la liste des sources inscrites. La désactivation de l’inscription **LastUsedSource** force le programme d’installation à effectuer une résolution de la source par rapport aux sources inscrites la prochaine fois qu’il requiert la source.

 

 



