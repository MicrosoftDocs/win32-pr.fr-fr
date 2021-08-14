---
title: Attributs d’objet utilisateur
description: Un objet utilisateur a plusieurs attributs. cette section décrit les attributs clés utilisés par Windows, les outils d’administration et le carnet d’adresses Windows (WAB). Elle ne décrit pas tous les attributs ; de nombreux attributs ne sont pas utilisés pour l’objet utilisateur.
ms.assetid: c173c5d1-2680-4b9c-961d-251fba6e2c7c
ms.tgt_platform: multiple
keywords:
- Attributs de l’objet utilisateur Active Directory
- Utilisateurs AD, attributs d’objet utilisateur
- Objets AD, utilisateur, attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a1bb6b347bd55daceb07dfe1fad4adc3e1352afc91ec14018aab6b24615c2b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182628"
---
# <a name="user-object-attributes"></a>Attributs d’objet utilisateur

Un objet utilisateur a plusieurs attributs. cette section décrit les attributs clés utilisés par Windows, les outils d’administration et le carnet d’adresses Windows (WAB). Elle ne décrit pas tous les attributs ; de nombreux attributs ne sont pas utilisés pour l’objet utilisateur.

Certains attributs sont stockés dans l’annuaire, tels que [**CN**](/windows/desktop/ADSchema/a-cn), [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), etc., et répliqués sur tous les contrôleurs de domaine au sein d’un domaine. Un sous-ensemble de ces attributs est également répliqué dans le catalogue global.

Les attributs non répliqués sont stockés sur chaque contrôleur de domaine, mais ne sont pas répliqués ailleurs, tels que [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon), [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff), etc. Les attributs non répliqués sont des attributs qui se rapportent à un contrôleur de domaine particulier. Par exemple, **lastLogon** est la dernière date et heure auxquelles l’ouverture de session réseau de l’utilisateur a été validée par le contrôleur de domaine particulier qui retourne la propriété.

Un objet utilisateur a également des attributs construits qui ne sont pas stockés dans l’annuaire, mais qui sont calculés par le contrôleur de domaine, tel que [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes), etc.

Les attributs des objets utilisateur sont classés comme suit :

<dl> <dt>

<span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Attributs d’objet de base
</dt> <dd>

Cette catégorie comprend les attributs requis pour tous les objets d’annuaire, tels que [**objectClass**](/windows/desktop/ADSchema/a-objectclass), [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), etc.

</dd> <dt>

<span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Nommer des attributs
</dt> <dd>

Cette catégorie comprend les attributs utilisés pour faire référence à l’objet ou l’identifier, par exemple [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSID**](/windows/desktop/ADSchema/a-objectsid), etc. Pour plus d’informations sur les attributs d’attribution de noms pour les objets utilisateur, consultez [User Naming Attributes](naming-properties.md).

</dd> <dt>

<span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Attributs de sécurité
</dt> <dd>

Cette catégorie comprend des attributs pour l’ouverture de session et le contrôle d’accès. Pour plus d’informations sur les attributs de sécurité pour les objets utilisateur, consultez [attributs de sécurité](security-properties.md)de l’utilisateur.

</dd> <dt>

<span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Attributs du carnet d’adresses
</dt> <dd>

Cette catégorie comprend les attributs des données de messagerie et utilisateur. Pour plus d’informations sur les attributs de carnet d’adresses pour les objets utilisateur, consultez [attributs de carnet d’adresses utilisateur](address-book-properties.md).

</dd> <dt>

<span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Attributs spécifiques à l’application
</dt> <dd>

Cette catégorie comprend des données de configuration spécifiques à l’utilisateur pour des applications spécifiques.

</dd> </dl>

Pour plus d’informations sur la lecture et la modification des attributs d’un objet utilisateur, consultez [lecture et écriture des attributs d’objets dans Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).

Pour plus d’informations sur la classe User, y compris la liste complète des attributs [**mayContain**](/windows/desktop/ADSchema/a-maycontain) et [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) de la classe, consultez [**User**](/windows/desktop/ADSchema/c-user).

## <a name="setting-passwords"></a>Définition des mots de passe

Le mot de passe d’un utilisateur ne peut pas être modifié directement, car cela implique l’envoi d’un mot de passe non chiffré sur le réseau. Pour définir le mot de passe d’un utilisateur, il est nécessaire d’utiliser la méthode [**IADsUser. ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) ou [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) . La méthode **IADsUser. ChangePassword** est utilisée lorsque l’application permet à l’utilisateur de modifier son propre mot de passe. La méthode **IADsUser. SetPassword** est utilisée lorsque l’application permet à un administrateur de réinitialiser un mot de passe.

 

 