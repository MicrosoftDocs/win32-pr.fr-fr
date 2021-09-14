---
title: TLSExtensions (schéma v1)
description: En savoir plus sur l’élément TLSExtensions (EapType). Cet élément active les améliorations futures du schéma.
ms.assetid: f968d91d-e226-44a9-98db-347cbedfa201
keywords:
- élément EAPHost
topic_type:
- apiref
api_name:
- TLSExtensions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 886f1ab2a6f00a4a8a9d530fa41865b2fd0cf0b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221393"
---
# <a name="tlsextensions-v1-schema"></a>TLSExtensions (schéma v1)

L’élément **TLSExtensions (EapType)** permet de futures améliorations du schéma.

``` syntax
<xs:element
    minOccurs="0"
    maxOccurs="1"
    ref="extendedTLS: TLSExtensions"
 />
```

L’élément est défini par l’élément [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Notes

L’élément **TLSExtensions** est facultatif.

## <a name="requirements"></a>Spécifications



| Role | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Éléments de schéma eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[**TLSExtensions (TLSExtensionsType)**](eaptlsconnectionpropertiesv2schema-performservervalidation-eaptype-element.md)
</dt> </dl>

 

 





