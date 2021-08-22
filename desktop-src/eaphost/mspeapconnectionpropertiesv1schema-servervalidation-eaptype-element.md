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
ms.openlocfilehash: 194057a8769f32902388e733731fb1e3d987ecafd0eff26ea62c15d4fc8555d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984019"
---
# <a name="servervalidation-eaptype-element-peap"></a>ServerValidation (EapType), élément (PEAP)

L’élément **ServerValidation (EapType)** contient des informations sur la façon d’effectuer la validation du serveur.

``` syntax
<xs:element name="ServerValidation"
    type="ServerValidationParameters"
 />
```

L’élément **ServerValidation** est défini par l’élément [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Remarques

L’élément **ServerValidation** est facultatif.

## <a name="requirements"></a>Configuration requise



| Role | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



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

 

 





