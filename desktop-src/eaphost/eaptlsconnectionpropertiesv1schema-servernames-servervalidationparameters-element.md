---
title: Élément ServerNames (ServerValidationParameters) (TLS)
description: En savoir plus sur l’élément ServerNames (ServerValidationParameters). Cet élément représente une liste de noms de serveurs délimités par des points-virgules. | Élément ServerNames (ServerValidationParameters) (TLS)
ms.assetid: c6cfcc67-4e6a-4bf0-87d9-37cc1d504598
keywords:
- Élément ServerNames EAPHost
topic_type:
- apiref
api_name:
- ServerNames
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef94bc650432c4fb87abf00a93841d0d4d42e965
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523155"
---
# <a name="servernames-servervalidationparameters-element-tls"></a>Élément ServerNames (ServerValidationParameters) (TLS)

L’élément **serverNames (ServerValidationParameters)** représente une liste de noms de serveurs délimités par des points-virgules.

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

L’élément **serverNames** est défini par le type complexe [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

## <a name="remarks"></a>Notes

Chaque nom de serveur est délimité par des points-virgules et peut être représenté par des expressions régulières. L’élément **serverNames** est facultatif.

## <a name="requirements"></a>Configuration requise



| Role | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Éléments parents immédiats possibles dans l’instance de schéma**
</dt> <dt>

[**ServerValidation (EapType)**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Éléments de schéma eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





