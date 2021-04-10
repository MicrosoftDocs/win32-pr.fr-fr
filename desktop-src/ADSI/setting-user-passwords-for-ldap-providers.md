---
title: Définition et modification des mots de passe utilisateur à l’aide du fournisseur LDAP
description: Pour définir le mot de passe d’un utilisateur, utilisez la méthode IADsUser. SetPassword.
ms.assetid: da3d9861-dd04-406c-9356-db1e4ff0eebc
ms.tgt_platform: multiple
keywords:
- ADSI fournisseur LDAP, objet utilisateur, définition des mots de passe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5488146de271ac1108a904cd85163fad9d7dd205
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316445"
---
# <a name="setting-and-changing-user-passwords-with-the-ldap-provider"></a>Définition et modification des mots de passe utilisateur à l’aide du fournisseur LDAP

Pour définir le mot de passe d’un utilisateur, utilisez la méthode [**IADsUser. SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) .

Le fournisseur LDAP pour Active Directory utilise l’un des trois processus pour définir le mot de passe (les annuaires LDAP tiers tels que iPlanet n’utilisent pas ce processus d’authentification par mot de passe). La méthode peut varier en fonction de la configuration du réseau. Les méthodes Set Password se produisent dans l’ordre suivant :

-   Tout d’abord, le fournisseur LDAP tente d’utiliser le protocole LDAP sur une connexion SSL 128 bits. Pour que le protocole SSL LDAP fonctionne correctement, le serveur LDAP doit disposer du certificat d’authentification serveur approprié et les clients qui exécutent le code ADSI doivent approuver l’autorité qui a émis ces certificats. Le serveur et le client doivent prendre en charge le chiffrement 128 bits.
-   Deuxièmement, si la connexion SSL échoue, le fournisseur LDAP tente d’utiliser Kerberos. Sur Windows 2000, Kerberos peut ne pas prendre en charge l’authentification inter-forêts. Les améliorations ultérieures de Kerberos prennent en charge l’authentification inter-forêts.
-   Troisièmement, si Kerberos échoue, le fournisseur LDAP tente un appel d’API [**NetUserSetInfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo) . Dans les versions précédentes, ADSI a appelé **NetUserSetInfo** dans le contexte de sécurité dans lequel le thread était en cours d’exécution, et non dans le contexte de sécurité spécifié dans l’appel à [**IADsOpenDSObject. OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) ou [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject). Dans les versions ultérieures, cela a été modifié afin que le fournisseur LDAP ADSI emprunte l’identité de l’utilisateur spécifié dans l’appel **OpenDSObject** lorsqu’il appelle **NetUserSetInfo**.

Pour modifier le mot de passe d’un utilisateur, utilisez la méthode [**IADsUser. ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) . Comme [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword), cette méthode peut utiliser plusieurs processus pour modifier le mot de passe. Les méthodes de modification de mot de passe se produisent dans l’ordre suivant :

-   Tout d’abord, le fournisseur LDAP tente d’utiliser le protocole LDAP sur une connexion SSL 128 bits.
-   Deuxièmement, si la connexion 128-SSL échoue, le fournisseur LDAP tente un appel d’API [**NetUserChangePassword**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserchangepassword) . Comme [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword), dans les versions antérieures, le fournisseur LDAP ADSI emprunte l’identité des informations d’identification de l’utilisateur transmises à l’aide de la méthode [**IADsOpenDSObject. OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) ou de la fonction [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .

 

 