---
description: La structure ADDRESSPAIR construit un filtre de capture.
ms.assetid: 0dd2bcaa-5e0f-448f-969e-14b923a01a2f
title: ADDRESSPAIR, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSPAIR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7960a8bb1c3ed1b2fc86c93f371b2f05d299b97b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021126"
---
# <a name="addresspair-structure"></a>ADDRESSPAIR, structure

La structure **ADDRESSPAIR** construit un filtre de capture.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _ADDRESSPAIR {
  WORD    AddressFlags;
  WORD    NalReserved;
  ADDRESS DstAddress;
  ADDRESS SrcAddress;
} ADDRESSPAIR, *LPADDRESSPAIR;
```



## <a name="members"></a>Membres

<dl> <dt>

**AddressFlags**
</dt> <dd>

Indicateurs qui décrivent les adresses utilisées par un filtre de capture. Pour plus d'informations, consultez la section Notes.



| Valeur                                                                                                                                                                                                         | Signification                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="ADDRESS_FLAGS_MATCH_DST"></span><span id="address_flags_match_dst"></span><dl> <dt>**indicateurs d’adresse \_ \_ correspondant à l' \_ heure d’été**</dt> </dl>                 | Correspond à l’adresse de destination.<br/>                              |
| <span id="ADDRESS_FLAGS_MATCH_SRC"></span><span id="address_flags_match_src"></span><dl> <dt>**indicateurs d’adresse \_ \_ correspondant à \_ src**</dt> </dl>                 | Correspond à l’adresse source.<br/>                                   |
| <span id="ADDRESS_FLAGS_EXCLUDED"></span><span id="address_flags_excluded"></span><dl> <dt>**indicateurs d’adresse \_ \_ exclus**</dt> </dl>                     | Exclut le frame si cette adresse est trouvée.<br/>                  |
| <span id="ADDRESS_FLAGS_DST_GROUP_ADDR"></span><span id="address_flags_dst_group_addr"></span><dl> <dt>**\_identificateurs d’adresse \_ ADR du \_ groupe DST \_**</dt> </dl> | Correspond au bit de groupe uniquement. À utiliser pour les messages de type diffusion.<br/> |
| <span id="ADDRESS_FLAGS_MATCH_BOTH"></span><span id="address_flags_match_both"></span><dl> <dt>**\_les indicateurs d’adresse \_ correspondent à la \_ fois**</dt> </dl>              | Correspond aux adresses de destination et sources.<br/>                     |



 

</dd> <dt>

**NalReserved**
</dt> <dd>

Cela est réservé.

</dd> <dt>

**DstAddress**
</dt> <dd>

Adresse de destination de l’élément de la paire d’adresses.

</dd> <dt>

**SrcAddress**
</dt> <dd>

Adresse source de l’élément de la paire d’adresses.

</dd> </dl>

## <a name="remarks"></a>Notes

Les indicateurs du membre **AddressFlags** peuvent être combinés. Par exemple, le paramètre suivant exclut le frame si l’adresse source spécifiée est détectée.

``` syntax
ADDRESS_FLAGS_MATCH_SOURCE|ADDRESS_FLAGS_EXCLUDED
```

Pour plus d’informations sur l’implémentation de cette structure, consultez [filtres de capture](capture-filters.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




