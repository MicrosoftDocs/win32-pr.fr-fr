---
title: ServerValidation (EapType), élément (TLS)
description: En savoir plus sur l’élément ServerValidation (EapType). Cet élément contient des informations sur la façon d’effectuer la validation du serveur. | ServerValidation (EapType), élément (TLS)
ms.assetid: f4ae1579-8c61-4187-8f5a-13aca3075af2
keywords:
- Élément ServerValidation EAPHost
topic_type:
- apiref
api_name:
- ServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c54905f35d673aee692efa6569eaddc6d18fc716
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531505"
---
# <a name="servervalidation-eaptype-element-tls"></a>ServerValidation (EapType), élément (TLS)

L’élément **ServerValidation (EapType)** contient des informations sur la façon d’effectuer la validation du serveur.

``` syntax
<xs:element name="ServerValidation"
    type="ServerValidationParameters"
 />
```

L’élément **ServerValidation** est défini par l’élément [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Notes

L’élément **ServerValidation** est facultatif.

## <a name="requirements"></a>Configuration requise



| Role | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



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

 

 





