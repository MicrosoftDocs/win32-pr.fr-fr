---
title: Liaison à Active Directory Domain Services
description: Dans Active Directory Domain Services, l’action consistant à associer un objet de programmation à un objet Active Directory Domain Services spécifique est appelée liaison.
ms.assetid: f48de4d4-c53a-4e40-a34e-4236c3e6cb21
ms.tgt_platform: multiple
keywords:
- liaison à Active Directory Domain Services Active Directory
- Active Directory Domain Services Active Directory, liaison à
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f57aef2b2a3c21ac860d05dd1b7a1e1079d1720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950459"
---
# <a name="binding-to-active-directory-domain-services"></a>Liaison à Active Directory Domain Services

Dans Active Directory Domain Services, l’action consistant à associer un objet de programmation à un objet Active Directory Domain Services spécifique est appelée *liaison*. Lorsqu’un objet de programmation, tel qu’un objet [**IADs**](/windows/desktop/api/iads/nn-iads-iads) ou [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) , est associé à un objet d’annuaire spécifique, l’objet de programmation est considéré comme *lié à* l’objet d’annuaire.

## <a name="binding-functions-and-methods"></a>Liaison de fonctions et de méthodes

La méthode de liaison par programmation à un objet Active Directory dépend de la technologie de programmation utilisée. Pour plus d’informations sur la liaison à des objets dans Active Directory Domain Services avec une technologie de programmation spécifique, consultez les rubriques figurant dans le tableau suivant.



| Technologie de programmation                                                                       | Informations supplémentaires                                                           |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Interfaces de service Active Directory](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [Liaison à un objet ADSI](/windows/desktop/ADSI/binding-to-an-adsi-object)                    |
| [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [Établissement d’une session LDAP](/previous-versions/windows/desktop/ldap/establishing-an-ldap-session)              |
| [System.DirectoryServices](/dotnet/api/system.directoryservices)                 | [Liaison à des objets d’annuaire](/previous-versions/ms180840(v=vs.90)) |



 

## <a name="binding-strings"></a>Chaînes de liaison

Toutes les fonctions et méthodes de liaison requièrent une chaîne de liaison. Le formulaire de la chaîne de liaison dépend du fournisseur. Les Active Directory Domain Services sont pris en charge par deux fournisseurs, LDAP et Winnt.

À partir de Windows 2000, le fournisseur LDAP est utilisé pour accéder à Active Directory Domain Services. La chaîne de liaison LDAP peut prendre l’une des formes suivantes :

-   « LDAP:// <host name> / <object name> »
-   « GC:// <host name> / <object name> »

Dans les exemples ci-dessus, « LDAP : » spécifie le fournisseur LDAP. « GC : » utilise le fournisseur LDAP pour effectuer une liaison au service de catalogue global afin d’exécuter des requêtes rapides.

« &lt; host name &gt; » spécifie le serveur auquel se lier et est facultatif. Si possible, ne spécifiez pas de serveur. Il est également possible de créer une liaison avec un objet dans un autre domaine. Pour ce faire, transmettez le nom DNS du domaine cible pour « &lt; nom d’hôte &gt; ». Par exemple, pour effectuer une liaison au conteneur Users dans le domaine domaine2 de fabrikam.com, la chaîne de liaison serait « LDAP://domain2.fabrikam.com/CN=Users,DC=domain2,DC=fabrikam,DC=com ».

« &lt; nom de l’objet &gt; » représente un objet spécifique dans Active Directory Domain Services. Le nom de l’objet peut être un nom unique ou un GUID d’objet.

Pour plus d’informations sur les chaînes de liaison LDAP, consultez [LDAP ADsPath](/windows/desktop/ADSI/ldap-adspath).

Pour Windows NT 4,0, le fournisseur Winnt est utilisé pour accéder aux données d’annuaire, telles que les utilisateurs, les groupes d’utilisateurs, les ordinateurs, les services et d’autres objets réseau dans Windows 2000. Le fournisseur Winnt sur les systèmes Windows 2000 et versions ultérieures a des fonctionnalités limitées par rapport au fournisseur LDAP. Pour plus d’informations sur les chaînes de liaison WinNT, consultez [winnt ADsPath](/windows/desktop/ADSI/winnt-adspath).

Un ADsPath de « LDAP:// » ou « GC:// » peut être utilisé pour établir une liaison à la racine de l’espace de noms. Lorsqu’il est lié à la racine de l’espace de noms, l’objet Namespace fourni ne contient aucune propriété et contient l’objet de domaine pour LDAP et un objet Container contenant un réplica partiel de tous les domaines de la forêt pour GC.

Pour plus d’informations sur la liaison dans Active Directory Domain Services, consultez :

-   [Liaison sans serveur et RootDSE](serverless-binding-and-rootdse.md)
-   [Liaison au catalogue global](binding-to-the-global-catalog.md)
-   [Utilisation d’objectGUID pour la liaison à un objet](using-objectguid-to-bind-to-an-object.md)
-   [Liaison à des objets Well-Known à l’aide de WKGUID](binding-to-well-known-objects-using-wkguid.md)
-   [Liaison à un objet à l’aide d’un SID](binding-to-an-object-using-a-sid.md)
-   [Activation de la liaison de Rename-Safe avec la propriété otherWellKnownObjects](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md)
-   [Authentification](authentication.md)

 

 
