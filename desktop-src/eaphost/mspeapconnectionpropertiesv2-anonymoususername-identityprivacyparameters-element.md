---
title: Élément AnonymousUserName (IdentityPrivacyParameters)
description: Contient une identité anonyme utilisée à la place de la véritable identification d’un utilisateur. Il est envoyé au cours de la première phase de l’authentification PEAP lorsque l’identité est envoyée en texte brut.
ms.assetid: 74a33a75-cf21-4346-a984-f2f8564c3b57
keywords:
- Élément AnonymousUserName EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6bbc973160a8865e246a6cec87ce02ced136d786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384944"
---
# <a name="anonymoususername-identityprivacyparameters-element"></a>Élément AnonymousUserName (IdentityPrivacyParameters)

L’élément **AnonymousUserName (IdentityPrivacyParameters)** contient une identité anonyme utilisée à la place de la véritable identification d’un utilisateur. Il est envoyé au cours de la première phase de l’authentification PEAP lorsque l' **identité** est envoyée en texte brut.

L’utilisation de l’identité anonyme est déterminée par l’élément [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) .

``` syntax
<xs:element name="AnonymousUserName"
    type="xs:String"
    minOccurs="0"
 />
```

L’élément **AnonymousUserName** est défini par [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .

## <a name="remarks"></a>Notes

L’élément **AnonymousUserName** est facultatif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Éléments de schéma mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





