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
ms.openlocfilehash: 7447e0ba8e13a593af6ac346ad47f8fe992b4a3187f0c46e8ee8fc28ddeb5646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910949"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




