---
title: Élément InnerEapOptional (EapType)
description: En savoir plus sur l’élément InnerEapOptional (EapType). Cet élément indique s’il faut effectuer l’accès invité.
ms.assetid: 2d314c89-5415-407f-84c3-c4c5c8957b39
keywords:
- Élément InnerEapOptional EAPHost
topic_type:
- apiref
api_name:
- InnerEapOptional
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 372163b39ea788b5c03bd25aedcc44aee172d58080fb94e3333a029a514962a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404589"
---
# <a name="innereapoptional-eaptype-element"></a>Élément InnerEapOptional (EapType)

L’élément **InnerEapOptional (EapType)** indique s’il faut effectuer l’accès invité.

``` syntax
<xs:element name="InnerEapOptional"
    type="boolean"
 />
```

L’élément **InnerEapOptional** est défini par l’élément [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Remarques

Si l’élément **InnerEapOptional** a la valeur true, l’élément [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) doit être présent et décrire la méthode interne et sa configuration. Si la valeur est FALSe, PEAP effectue un accès invité. L’élément **InnerEapOptional** est facultatif.

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


</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Éléments de schéma mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





