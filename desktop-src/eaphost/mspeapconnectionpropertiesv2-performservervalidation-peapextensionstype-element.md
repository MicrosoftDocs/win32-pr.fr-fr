---
title: PerformServerValidation (PeapExtensionsType), élément (schéma v2)
description: En savoir plus sur l’élément PerformServerValidation (PeapExtensionsType). Cet élément indique si la validation du serveur est effectuée. | PerformServerValidation (PeapExtensionsType), élément (schéma v2)
ms.assetid: a9c383d4-2582-47dd-bdf1-dd4e6c1689f7
keywords:
- Élément PerformServerValidation EAPHost
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
ms.openlocfilehash: 32bc213aa67e87eb8af0643a15f16b298cfb3204
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211549"
---
# <a name="performservervalidation-peapextensionstype-element-v2-schema"></a>PerformServerValidation (PeapExtensionsType), élément (schéma v2)

L’élément **PerformServerValidation (PeapExtensionsType)** indique si la validation du serveur est effectuée.

``` syntax
<xs:element name="PerformServerValidation"
    type="xs:boolean"
 />
```

L’élément **PerformServerValidation** est défini par l’élément [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .

## <a name="remarks"></a>Notes

L’élément **PerformServerValidation** est facultatif.

## <a name="requirements"></a>Configuration requise



| Role | Version minimale du système d’exploitation |
|------|--------------------|
| Client<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



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

 

 





