---
title: Définition des autorisations sur une propriété spécifique
description: Les autorisations peuvent être définies pour s’appliquer à une propriété spécifique d’un objet.
ms.assetid: 7bafba5a-a437-4777-98a0-f478b738a8ca
ms.tgt_platform: multiple
keywords:
- Définition des autorisations sur une propriété Active Directory spécifique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7f55fba3ae2be54a29ade3dee1dc161fa0c6d2dbe478fb42f39319fbeaf4fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183313"
---
# <a name="setting-permissions-to-a-specific-property"></a>Définition des autorisations sur une propriété spécifique

Les autorisations peuvent être définies pour s’appliquer à une propriété spécifique d’un objet.

**Pour définir des autorisations qui s’appliquent à une propriété spécifique d’un objet**

1.  Affectez à la propriété [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) la valeur **ADS \_ Right \_ \_ lire \_ prop** et/ou **ad \_ \_ DS \_ Write \_ prop**.
2.  Définissez la propriété [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur **ADS \_ AceType \_ Access \_ allowed \_ Object** ou **ADS \_ AceType \_ accès \_ refusé \_ Object**.
3.  Définissez la propriété [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur le **schemaIDGUID** de la propriété. Il s’agit du **schemaIDGUID** de l’objet **attributeSchema** qui définit la propriété dans le schéma. Le GUID doit être spécifié sous la forme d’une chaîne sous la forme produite par la fonction [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) dans la bibliothèque com.
4.  Définissez [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sur le **\_ type d’objet indicateur ADS \_ \_ \_ présent**.

Pour plus d’informations sur le **schemaIDGUID** d’un attribut prédéfini, consultez [Active Directory Domain Services référence](active-directory-domain-services-reference.md).

Pour plus d’informations et pour obtenir un exemple de code qui peut être utilisé pour récupérer un schemaIDGUID, consultez [lecture des objets AttributeSchema et classSchema](reading-attributeschema-and-classschema-objects.md).

Pour plus d’informations sur la création d’une entrée du contrôle d’accès, consultez [définition des droits d’accès sur un objet](setting-access-rights-on-an-object.md).

Pour plus d’informations et pour obtenir un exemple de code qui peut être utilisé pour définir une entrée du contrôle d’accès spécifique à une propriété, consultez [l’exemple de code permettant de définir une entrée du contrôle d’accès sur un objet d’annuaire](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 