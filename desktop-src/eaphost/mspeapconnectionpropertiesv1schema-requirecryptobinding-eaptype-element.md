---
title: Élément RequireCryptoBinding (EapType)
description: Indique s’il faut s’authentifier auprès des serveurs qui prennent en charge TLV.
ms.assetid: 6b6a131d-8fce-4a5c-a649-891c4617b0f2
keywords:
- Élément RequireCryptoBinding EAPHost
topic_type:
- apiref
api_name:
- RequireCryptoBinding
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c4f4169e6ac0af123085795374b06de854b261b5f22004bd726ad47488bc11d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067219"
---
# <a name="requirecryptobinding-eaptype-element"></a>Élément RequireCryptoBinding (EapType)

L’élément **RequireCryptoBinding (EapType)** indique s’il faut s’authentifier auprès des serveurs qui prennent en charge TLV.

``` syntax
<xs:element name="RequireCryptoBinding"
    type="boolean"
 />
```

L’élément **RequireCryptoBinding** est défini par l’élément [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Remarques

Si l’élément **RequireCryptoBinding** a la valeur true, PEAP s’authentifie auprès des serveurs qui ne prennent pas en charge TLV ; Si la valeur est FALSe, PEAP s’authentifie uniquement avec les serveurs qui prennent en charge TLV. L’élément **RequireCryptoBinding** est facultatif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



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

 

 





