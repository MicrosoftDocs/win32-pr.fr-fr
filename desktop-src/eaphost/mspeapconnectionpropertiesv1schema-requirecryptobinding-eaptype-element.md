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
ms.openlocfilehash: 63ee456f87205346a935ad047cb8db9828febba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385084"
---
# <a name="requirecryptobinding-eaptype-element"></a>Élément RequireCryptoBinding (EapType)

L’élément **RequireCryptoBinding (EapType)** indique s’il faut s’authentifier auprès des serveurs qui prennent en charge TLV.

``` syntax
<xs:element name="RequireCryptoBinding"
    type="boolean"
 />
```

L’élément **RequireCryptoBinding** est défini par l’élément [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Notes

Si l’élément **RequireCryptoBinding** a la valeur true, PEAP s’authentifie auprès des serveurs qui ne prennent pas en charge TLV ; Si la valeur est FALSe, PEAP s’authentifie uniquement avec les serveurs qui prennent en charge TLV. L’élément **RequireCryptoBinding** est facultatif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



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

 

 





