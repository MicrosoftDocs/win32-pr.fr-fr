---
description: La \_ structure d’élément KSMULTIPLE décrit la taille et le nombre de propriétés de longueur variable sur les broches en mode noyau.
ms.assetid: aedbf7bc-393d-4ab5-afcd-d8822b925f07
title: KSMULTIPLE_ITEM, structure (KS. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSMULTIPLE_ITEM
api_type:
- HeaderDef
api_location:
- ks.h
ms.openlocfilehash: 62e26b1aa8804514588e66c1d02e1f0643e97bcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543253"
---
# <a name="ksmultiple_item-structure"></a>Structure de l' \_ élément KSMULTIPLE

La `KSMULTIPLE_ITEM` structure décrit la taille et le nombre de propriétés de longueur variable sur les broches en mode noyau.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  ULONG Size;
  ULONG Count;
} KSMULTIPLE_ITEM, *PKSMULTIPLE_ITEM;
```



## <a name="members"></a>Membres

<dl> <dt>

**Taille**
</dt> <dd>

Taille du bloc de mémoire retourné, en octets. La taille comprend la structure de l' **\_ élément KSMULTIPLE** et les éléments qui le suivent.

</dd> <dt>

**Count**
</dt> <dd>

Spécifie le nombre total d’éléments qui suivent cette structure.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>KS. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures DirectShow](directshow-structures.md)
</dt> <dt>

[**IKsPin::KsQueryMediums**](ikspin-ksquerymediums.md)
</dt> <dt>

[**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




