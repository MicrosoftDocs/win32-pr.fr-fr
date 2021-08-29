---
title: Type complexe TLSExtensionsType
description: En savoir plus sur le type complexe TLSExtensionsType. Ce type active les améliorations futures du schéma.
ms.assetid: 5e4f8ef8-1adb-4683-8001-ba7d2d392523
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ac12ad6d3b1229f4fcb75506a9e7ae7655db0287ad58fa9a8079ba12c14e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984100"
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



## <a name="remarks"></a>Remarques

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

 

 




