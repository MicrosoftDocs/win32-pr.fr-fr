---
title: ServerNames (ServerValidationParameters), élément (PEAP)
description: En savoir plus sur l’élément ServerNames (ServerValidationParameters). Cet élément représente une liste de noms de serveurs délimités par des points-virgules. | ServerNames (ServerValidationParameters), élément (PEAP)
ms.assetid: 2595daa1-9f1b-40cf-9219-0e7295fdd5c3
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
ms.openlocfilehash: f3f9de6ee28077b5206a9783ef7722864a479e1e5f26b78e4402ac79c6e4be5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984009"
---
# <a name="servernames-servervalidationparameters-element-peap"></a>ServerNames (ServerValidationParameters), élément (PEAP)

L’élément **serverNames (ServerValidationParameters)** représente une liste de noms de serveurs délimités par des points-virgules.

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

L’élément **serverNames** est défini par le type complexe [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

## <a name="remarks"></a>Remarques

Chaque nom de serveur est délimité par des points-virgules et peut être représenté par des expressions régulières. L’élément **serverNames** est facultatif.

## <a name="requirements"></a>Configuration requise



| Role | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Éléments parents immédiats possibles dans l’instance de schéma**
</dt> <dt>

[**ServerValidation (EapType)**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Éléments de schéma mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





