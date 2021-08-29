---
description: La structure FRAMETABLE, une mémoire tampon circulaire de pointeurs de frame, est remise aux applications attachées à l’interface ITRC du NPP.
ms.assetid: 6e2d4f8d-46f2-4d53-bc28-7b0706663490
title: FRAMETABLE, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAMETABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 214a9e947c7aba34f0cc65d1df8d56a57b9d1087e168824494f64e30bd8098e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890739"
---
# <a name="frametable-structure"></a>FRAMETABLE, structure

La structure **FRAMETABLE** , une mémoire tampon circulaire de pointeurs de frame, est remise aux applications attachées à l’interface **ITRC** du NPP.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _FRAMETABLE {
  DWORD            FrameTableLength;
  DWORD            StartIndex;
  DWORD            EndIndex;
  DWORD            FrameCount;
  FRAME_DESCRIPTOR Frames[1];
} FRAMETABLE, *LPFRAMETABLE;
```



## <a name="members"></a>Membres

<dl> <dt>

**FrameTableLength**
</dt> <dd>

Longueur totale de la table.

</dd> <dt>

**StartIndex**
</dt> <dd>

Premier index dans la table.

</dd> <dt>

**EndIndex**
</dt> <dd>

Dernier index dans la table.

</dd> <dt>

**FrameCount**
</dt> <dd>

Nombre de frames décrits dans ce tableau.

</dd> <dt>

**Frame**
</dt> <dd>

Tableau réel des descripteurs de frame.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




