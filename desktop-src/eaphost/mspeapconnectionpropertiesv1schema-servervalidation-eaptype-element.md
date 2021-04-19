---
title: ServerValidation (EapType), élément (PEAP)
description: En savoir plus sur l’élément ServerValidation (EapType). Cet élément contient des informations sur la façon d’effectuer la validation du serveur. | ServerValidation (EapType), élément (PEAP)
ms.assetid: 5b213853-7161-456c-bbba-d3b1118f1786
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
ms.openlocfilehash: 1495da3f1a1f5e69e7a6af9c64e69aa1ea354abc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106541246"
---
# <a name="servervalidation-eaptype-element-peap"></a>ServerValidation (EapType), élément (PEAP)

L’élément **ServerValidation (EapType)** contient des informations sur la façon d’effectuer la validation du serveur.

``` syntax
<xs:element name="ServerValidation"
    type="ServerValidationParameters"
 />
```

L’élément **ServerValidation** est défini par l’élément [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

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

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Éléments de schéma mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





