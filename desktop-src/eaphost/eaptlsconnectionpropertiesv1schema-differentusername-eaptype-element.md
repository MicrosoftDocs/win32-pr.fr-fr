---
title: Élément DifferentUsername (EapType)
description: En savoir plus sur l’élément DifferentUsername (EapType). Cet élément détermine le nom d’utilisateur EAP-TLS à utiliser.
ms.assetid: f0ce41a9-c774-4d12-8a5a-a8eb1eb84cb0
keywords:
- Élément DifferentUsername EAPHost
topic_type:
- apiref
api_name:
- DifferentUsername
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 505e23c74d4c1c8c74a50906809d0acc9ce06c42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294282"
---
# <a name="differentusername-eaptype-element"></a>Élément DifferentUsername (EapType)

L’élément **DifferentUsername (EapType)** détermine le nom d’utilisateur EAP-TLS à utiliser.

``` syntax
<xs:element name="DifferentUsername"
    type="boolean"
 />
```

L’élément **DifferentUsername** est défini par l’élément [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Notes

Si l’élément **DifferentUserName** a la valeur true, EAP-TLS doit utiliser un nom d’utilisateur différent du nom qui s’affiche sur le certificat. Si l’élément **DifferentUserName** a la valeur false, EAP-TLS utilise le nom d’utilisateur qui apparaît sur le certificat.

L’élément **DifferentUserName** est facultatif.

## <a name="requirements"></a>Spécifications



| Role | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



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
</dt> </dl>

 

 





