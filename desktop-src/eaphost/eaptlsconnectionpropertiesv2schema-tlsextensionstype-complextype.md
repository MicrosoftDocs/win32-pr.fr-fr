---
title: Type complexe TLSExtensionsType
description: En savoir plus sur le type complexe TLSExtensionsType. Ce type active les améliorations futures du schéma.
ms.assetid: 5e4f8ef8-1adb-4683-8001-ba7d2d392523
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833a93b9ecb0ba32a95e4c85856ac015f5135fb5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730332"
---
# <a name="tlsextensionstype-complex-type"></a>Type complexe TLSExtensionsType

Le type complexe **TLSExtensionsType** permet de futures améliorations du schéma.


```XML
<xs:complexType name="TLSExtensionsType">
    <xs:sequence>
        <xs:any processContents="lax" 
            minOccurs="0" 
            maxOccurs="unbounded" 
            namespace="##other"
        />
    <xs:sequence>
</xs:complexType>

```



## <a name="remarks"></a>Notes

L’élément **TLSExtensionsType** est facultatif.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>


</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Types complexes eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[**TLSExtensions (TLSExtensionsType)**](eaptlsconnectionpropertiesv2schema-performservervalidation-eaptype-element.md)
</dt> </dl>

 

 




