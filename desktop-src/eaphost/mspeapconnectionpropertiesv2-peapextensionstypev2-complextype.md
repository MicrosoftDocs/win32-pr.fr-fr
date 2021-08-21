---
title: Type complexe PeapExtensionsTypeV2
description: En savoir plus sur le type complexe PeapExtensionsTypeV2. Ce type active les améliorations futures du schéma.
ms.assetid: cb011182-afec-4813-bd56-add894c74c9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baea42ec60fe84085ea5e4541848fd43b786419bedab17e938044ff0a713fa07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086028"
---
# <a name="peapextensionstypev2-complex-type"></a>Type complexe PeapExtensionsTypeV2

Le type complexe **PeapExtensionsTypeV2** permet de futures améliorations du schéma.


```XML
<xs:complexType name="PeapExtensionsTypeV2">
    <xs:sequence>
        <xs:any processContents="lax" 
            minOccurs="0" 
            maxOccurs="unbounded" 
            namespace="##other"
        />
    <xs:sequence>
</xs:complexType>

```



## <a name="remarks"></a>Remarques

L’élément **PeapExtensionsTypeV2** est facultatif.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Types complexes mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> </dl>

 

 




