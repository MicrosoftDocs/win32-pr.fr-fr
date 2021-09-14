---
description: Un frame réel du pilote.
ms.assetid: 867082c1-196a-4580-ba24-187b0752f6f8
title: Structure de FRAMEs (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b4ff8d66f88b18988cbb33bbcd8196cc01177b73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021105"
---
# <a name="frame-structure"></a>Structure de FRAME

La structure du **Frame** est un cadre réel du pilote.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _FRAME {
  __int64 TimeStamp;
  DWORD   FrameLength;
  DWORD   nBytesAvail;
  BYTE    MacFrame[];
} FRAME, *LPFRAME, *ULPFRAME;
```



## <a name="members"></a>Membres

<dl> <dt>

**Confirmé**
</dt> <dd>

Temps écoulé, en microsecondes, entre le début de la capture et le moment où le frame a été capturé.

</dd> <dt>

**FrameLength**
</dt> <dd>

Longueur du cadre MAC.

</dd> <dt>

**nBytesAvail**
</dt> <dd>

Longueur de trame réelle copiée.

</dd> <dt>

**MacFrame**
</dt> <dd>

Données de frame.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




