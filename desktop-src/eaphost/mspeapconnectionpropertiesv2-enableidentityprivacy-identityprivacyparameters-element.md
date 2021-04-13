---
title: Élément EnableIdentityPrivacy (IdentityPrivacyParameters)
description: Indique si l’identité réelle d’un utilisateur ou une identité anonyme est envoyée. | Élément EnableIdentityPrivacy (IdentityPrivacyParameters)
ms.assetid: 7751e5fa-895e-47f7-99d9-aa7ef2451eb1
keywords:
- Élément EnableIdentityPrivacy EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a96b49fe462f4ef8cedad550d1a6c87d680939
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322485"
---
# <a name="enableidentityprivacy-identityprivacyparameters-element"></a>Élément EnableIdentityPrivacy (IdentityPrivacyParameters)

L’élément **EnableIdentityPrivacy (IdentityPrivacyParameters)** indique si l’identité réelle d’un utilisateur ou une identité anonyme est envoyée.

``` syntax
<xs:element name="EnableIdentityPrivacy"
    type="xs:Boolean"
    minOccurs="0"
 />
```

L’élément **EnableIdentityPrivacy** est défini par [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .

## <a name="remarks"></a>Notes

L’élément **EnableIdentityPrivacy** est facultatif.

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


</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Éléments de schéma mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





