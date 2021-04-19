---
description: Contient des informations de format pour la recompression intelligente.
ms.assetid: 471a7b4a-e639-443b-a30e-870b747e072c
title: SCompFmt0, structure (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCompFmt0
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: ad5a5277718e8d414d64a86b9c31739cf576736a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532247"
---
# <a name="scompfmt0-structure"></a>SCompFmt0, structure

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

Contient des informations de format pour la recompression intelligente.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _SCompFmt0 {
  long          nFormatId;
  AM_MEDIA_TYPE MediaType;
} SCompFmt0;
```



## <a name="members"></a>Membres

<dl> <dt>

**nFormatId**
</dt> <dd>

Réservé doit être égal à zéro.

</dd> <dt>

**MediaType**
</dt> <dd>

[**Am \_ Structure du \_ type de média**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui décrit le format de compression.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAMTimelineGroup::GetSmartRecompressFormat**](iamtimelinegroup-getsmartrecompressformat.md)
</dt> <dt>

[**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)
</dt> </dl>

 

 




