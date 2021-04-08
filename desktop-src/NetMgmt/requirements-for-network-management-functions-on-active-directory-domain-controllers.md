---
title: Configuration requise pour les fonctions de gestion de réseau sur les contrôleurs domaine Active Directory
description: Si vous appelez l’une des fonctions de gestion de réseau répertoriées dans cette rubrique sur un contrôleur de domaine exécutant Active Directory, l’accès à un objet sécurisable est autorisé ou refusé en fonction de la liste de contrôle d’accès (ACL) de l’objet.
ms.assetid: 4dfb3180-3ca5-4e22-b7a1-4e6b132431fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6b646290ef6352a529a37243a6ea30c8b0d39
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842406"
---
# <a name="requirements-for-network-management-functions-on-active-directory-domain-controllers"></a>Configuration requise pour les fonctions de gestion de réseau sur les contrôleurs domaine Active Directory

Si vous appelez l’une des fonctions de gestion de réseau répertoriées dans cette rubrique sur un contrôleur de domaine exécutant Active Directory, l’accès à un [objet sécurisable](/windows/desktop/SecAuthZ/securable-objects) est autorisé ou refusé en fonction de la [liste de contrôle d’accès](/windows/desktop/SecAuthZ/access-control-lists) (ACL) de l’objet. (Les listes de contrôle d’accès sont spécifiées dans le répertoire.)

Des exigences d’accès différentes s’appliquent aux requêtes d’informations et aux mises à jour d’informations.

## <a name="queries"></a>Requêtes

Pour les requêtes, l’ACL par défaut autorise tous les utilisateurs authentifiés et les membres du groupe «[accès compatible pré-Windows 2000](/windows/desktop/SecAuthZ/allowing-anonymous-access)» à lire et énumérer les informations. Les fonctions répertoriées ci-dessous sont affectées :

-   [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)
-   [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)
-   [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (niveaux 1 et 2 uniquement)
-   [**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (niveaux 2 et 502 uniquement)
-   [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)
-   [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)

L’accès anonyme aux informations de groupe nécessite que l’utilisateur anonyme soit explicitement ajouté au groupe « accès compatible pré-Windows 2000 ». Cela est dû au fait que les jetons anonymes n’incluent pas le SID du groupe tout le monde.

**Windows 2000 :** Par défaut, le groupe « accès compatible avec les versions antérieures à Windows 2000 » comprend tous les membres. Cela permet l’accès anonyme (ouverture de session anonyme) aux informations si le système autorise l’accès anonyme. Les administrateurs peuvent supprimer tout le monde du groupe « accès compatible avec les versions antérieures à Windows 2000 » à tout moment. La suppression de tout le monde du groupe restreint l’accès aux informations aux utilisateurs authentifiés uniquement. Pour plus d’informations sur l’accès anonyme, consultez [identificateurs de sécurité](/windows/desktop/SecAuthZ/security-identifiers) et [sid connus](/windows/desktop/SecAuthZ/well-known-sids).

Vous pouvez remplacer la valeur système par défaut en définissant la clé suivante dans le registre à la valeur 1 :

**HKEY \_ \_ \\ \\ \\ Contrôle \\ CurrentControlSet du système de l’ordinateur local**, \\ **EveryoneIncludesAnonymous** = 1

Pour plus d’informations sur l’accès anonyme aux informations de groupe lors de l’appel de ces deux fonctions, consultez [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) et [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum) .

## <a name="updates"></a>Mises à jour

Pour les mises à jour, la liste de contrôle d’accès par défaut autorise uniquement les administrateurs de domaine et les opérateurs de compte à écrire des informations. Une exception est que les utilisateurs peuvent modifier leur propre mot de passe et définir le \* \_ champ de commentaire usr usri \_ . Une autre exception est que les opérateurs de compte ne peuvent pas modifier les comptes d’administration. Les fonctions répertoriées ci-dessous sont affectées :

-   [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd), [**NetGroupAddUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser), [**NetGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel), [**NetGroupDelUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser), [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo), [**NetGroupSetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers)
-   [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd), [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers), [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel), [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers), [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo), [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers)
-   [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)
-   [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel), [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset), [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups), [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)

En règle générale, les appelants doivent avoir un accès en écriture à l’objet entier pour que les appels à [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset), [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo), [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) et [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo) fonctionnent. Pour un contrôle d’accès plus fin, vous devez envisager d’utiliser ADSI. Pour plus d’informations sur ADSI, consultez [Active Directory interfaces de service](/windows/desktop/ADSI/active-directory-service-interfaces-adsi).

Pour plus d’informations sur le contrôle de l’accès aux objets sécurisables, consultez [Access Control](/windows/desktop/SecAuthZ/access-control), [privilèges](/windows/desktop/SecAuthZ/privileges)et [objets sécurisables](/windows/desktop/SecAuthZ/securable-objects). Pour plus d’informations sur l’appel de fonctions qui requièrent des privilèges d’administrateur, consultez [exécution avec des privilèges spéciaux](/windows/desktop/SecBP/running-with-special-privileges).

 

 