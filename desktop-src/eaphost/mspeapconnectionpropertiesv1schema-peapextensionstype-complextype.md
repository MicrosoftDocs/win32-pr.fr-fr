---
title: Type complexe PeapExtensionsType
description: contient des améliorations de schéma effectuées dans Windows 7. Les futures améliorations du schéma seront gérées par PeapExtensionsTypeV2.
ms.assetid: a8fb8474-a375-4401-83b0-4fa87d637209
keywords:
- PeapExtensionsType type complexe EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 212c8bf6b1421cfc461288e8f57258b40e11e9118c9ea2b2f620986e91d226f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984029"
---
# <a name="peapextensionstype-complex-type"></a>Type complexe PeapExtensionsType

le type complexe **PeapExtensionsType** contient des améliorations de schéma effectuées dans Windows 7. Les futures améliorations du schéma seront gérées par [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md).

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PerformServerValidation"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:AcceptServerName"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:IdentityPrivacy"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PeapExtensionsV2"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                                               | Type | Description                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------|------|------------------------------------------------------------------------------------------------------------|
| [**extendedPeap:PerformServerValidation**](mspeapconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |      | Windows 7 et versions ultérieures : indique si la validation du serveur est effectuée.<br/>                          |
| [**extendedPeap:AcceptServerName**](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)               |      | Windows 7 et versions ultérieures : indique si le nom d’un serveur est lu.<br/>                            |
| [**extendedPeap:IdentityPrivacy**](mspeapconnectionpropertiesv1schema-identityprivacy-peapextensionstype-element.md)                 |      | Windows 7 et versions ultérieures : indique si l’identité réelle d’un utilisateur ou une identité anonyme est envoyée.<br/> |
| [**extendedPeap:PeapExtensionsV2**](mspeapconnectionpropertiesv1-peapextensionsv2-peapextensionstype-element.md)                     |      | Windows 7 et versions ultérieures : active les améliorations futures du schéma.<br/>                                 |



## <a name="remarks"></a>Remarques

L’élément **PeapExtensionsType** est facultatif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Types complexes de schéma mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





