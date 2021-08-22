---
title: Utilisation des services de domaine Active Directory
description: Cette section fournit des instructions relatives à l’écriture d’applications qui utilisent ou publient des données dans un service d’annuaire Active Directory.
ms.assetid: 2ae20169-08a5-4e15-8430-ea99a917725f
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, utilisation
- Active Directory Active Directory Domain Services, utilisation
- Exemples de Active Directory Active Directory
- Exemples de Active Directory Domain Services Active Directory
- exemples Active Directory
- Active Directory Active Directory, exemples voir Active Directory Domain Services exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e1ef5428242e6d83fcb0c517c91abaee24de8181689a3aa1922eafea4d76703
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024537"
---
# <a name="using-active-directory-domain-services"></a>Utilisation des services de domaine Active Directory

Cette section fournit des instructions relatives à l’écriture d’applications qui utilisent ou publient des données dans un service d’annuaire Active Directory.

> [!Note]  
> La documentation suivante est destinée aux programmeurs informatiques. Si vous essayez de résoudre une erreur d’impression Active Directory, consultez les [suggestions suivantes](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) sur les pages de la communauté Microsoft. Si cela ne vous aide pas, essayez ces recommandations à partir de [TechNet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint).

 

Active Directory Domain Services sont conformes à Lightweight Directory Access Protocol 3,0, qui est défini par RFC 2251 et d’autres RFC. Les jeux d’API suivants peuvent être utilisés pour accéder à Active Directory Domain Services. Chaque ensemble d’API présente des avantages et des inconvénients qui dépendent du langage de programmation, de l’environnement de programmation et de la méthode d’exécution prévue. la majorité des exemples de ce guide utilisent ADSI, qui est pris en charge par les langages tels que C et C++, ainsi que les langages compatibles automation tels que Microsoft Visual Basic et Visual Basic édition de scripts.

Pour plus d’informations sur les technologies Active Directory Domain Services spécifiques, consultez :

-   [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api)
-   [Interfaces de service Active Directory](../adsi/active-directory-service-interfaces-adsi.md)
-   [System.DirectoryServices](/dotnet/api/system.directoryservices)

Cette section aborde les sujets suivants :

-   [Liaison à Active Directory Domain Services](binding-to-active-directory-domain-services.md)
-   [Recherche dans Active Directory Domain Services](searching-in-active-directory-domain-services.md)
-   [Création et suppression d’objets dans Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md)
-   [Déplacement d’objets](moving-objects.md)
-   [Lecture et écriture des attributs d’objets dans Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md)
-   [Contrôle de l’accès aux objets dans Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md)
-   [Extension du schéma](extending-the-schema.md)
-   [Extension de l’interface utilisateur pour les objets d’annuaire](extending-the-user-interface-for-directory-objects.md)
-   [Gestion des utilisateurs](managing-users.md)
-   [Gestion des groupes](managing-groups.md)
-   [Suivi des modifications](tracking-changes.md)
-   [Publication de service](service-publication.md)
-   [Comptes d’ouverture de session du service](service-logon-accounts.md)
-   [Authentification mutuelle à l'aide de Kerberos](mutual-authentication-using-kerberos.md)
-   [Sauvegarde et restauration de Active Directory](backing-up-and-restoring-an-active-directory-server.md)
-   [Stockage des Dynamic Data](storing-dynamic-data.md)
-   [Partitions de l’annuaire d’applications](application-directory-partitions.md)
-   [Détection du mode d’opération d’un domaine](detecting-the-operation-mode-of-a-domain.md)

 

 