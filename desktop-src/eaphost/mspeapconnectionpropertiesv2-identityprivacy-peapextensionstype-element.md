---
title: Élément IdentityPrivacy (PeapExtensionsType)
description: Indique si l’identité réelle d’un utilisateur ou une identité anonyme est envoyée. | Élément IdentityPrivacy (PeapExtensionsType)
ms.assetid: 57b8747e-6919-4243-a379-3a85c4a2023a
keywords:
- Élément IdentityPrivacy EAPHost
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
ms.openlocfilehash: 2701352ee0e192dfd2d33fc2647b9ec6df96dd5c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530645"
---
# <a name="the-identityprivacy-peapextensionstype-element"></a>Élément IdentityPrivacy (PeapExtensionsType)

L’élément **IdentityPrivacy (PeapExtensionsType)** indique si l’identité réelle d’un utilisateur ou une identité anonyme est envoyée.

``` syntax
<xs:element name="IdentityPrivacy"
    type="IdentityPrivacyParameters"
 />
```

L’élément **IdentityPrivacy** est défini par l’élément [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .

## <a name="remarks"></a>Notes

L’élément **IdentityPrivacy** est facultatif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
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

 

 





