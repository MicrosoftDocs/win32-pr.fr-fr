---
description: La \_ structure de mappage PID contient identifie le contenu d’un ID de paquet de flux de transport MPEG-2.
ms.assetid: c247ec75-483d-4587-a82f-07bbf6d277b4
title: Structure PID_MAP (Bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PID_MAP
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 98b238c61ccfcfb93e4ddcc0a051d9084228f604
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007478"
---
# <a name="pid_map-structure"></a>Structure de la \_ carte PID

La `PID_MAP` structure contient identifie le contenu d’un ID de paquet de flux de transport MPEG-2.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  ULONG                ulPID;
  MEDIA_SAMPLE_CONTENT MediaSampleContent;
} PID_MAP;
```



## <a name="members"></a>Membres

<dl> <dt>

**ulPID**
</dt> <dd>

Spécifie l’ID de paquet (PID)

</dd> <dt>

**MediaSampleContent**
</dt> <dd>

Spécifie le contenu de la charge utile du paquet, sous la forme d’un exemple de type d’énumération de [**\_ \_ contenu multimédia**](media-sample-content.md) .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Bdatypes. h (inclure Bdaiface. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[DirectShow Celles](directshow-structures.md)
</dt> <dt>

[**Interface IEnumPIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-ienumpidmap)
</dt> </dl>

 

 




