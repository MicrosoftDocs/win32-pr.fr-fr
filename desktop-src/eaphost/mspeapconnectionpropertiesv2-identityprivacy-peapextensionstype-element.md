---
title: Élément IdentityPrivacy (PeapExtensionsType)
description: L’élément IdentityPrivacy (PeapExtensionsType) indique si l’identité réelle d’un utilisateur est envoyée dans le schéma mspeapconnectionpropertiesv2.
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
ms.openlocfilehash: d0a23ce28a1a807bb948c114435463102561570b
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988945"
---
# <a name="the-identityprivacy-peapextensionstype-element"></a>Élément IdentityPrivacy (PeapExtensionsType)

L’élément **IdentityPrivacy (PeapExtensionsType)** indique si l’identité réelle d’un utilisateur ou une identité anonyme est envoyée.

``` syntax
<xs:element name="IdentityPrivacy"
    type="IdentityPrivacyParameters"
 />
```

L’élément **IdentityPrivacy** est défini par l’élément [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .

## <a name="remarks"></a>Remarques

L’élément **IdentityPrivacy** est facultatif.

## <a name="requirements"></a>Spécifications



| Condition requise | Value |
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

 

 





