---
description: La \_ structure du descripteur de Frame fournit des informations descriptives sur les frames bruts.
ms.assetid: f2fc256e-8e64-49c1-b2ad-ef656762d5c7
title: Structure de FRAME_DESCRIPTOR (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c327ce1568eec07aabe3334013dae8b720ab7446
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021106"
---
# <a name="frame_descriptor-structure"></a>\_Structure du descripteur de frame

La structure du **\_ descripteur de frame** fournit des informations descriptives sur les frames bruts.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _FRAME_DESCRIPTOR {
  LPBYTE       FramePointer;
  __int64      TimeStamp;
  DWORD        FrameLength;
  DWORD        nBytesAvail;
  WORD         Etype;
  BYTE         Sap;
  BYTE         LowProtocol;
  WORD         LowProtocolOffset;
  GENERIC_PORT HighPort;
  WORD         HighProtocolOffset;
} FRAME_DESCRIPTOR, *LPFRAME_DESCRIPTOR;
```



## <a name="members"></a>Membres

<dl> <dt>

**FramePointer**
</dt> <dd>

Pointeur vers les données de frame.

</dd> <dt>

**Confirmé**
</dt> <dd>

Heure système, en microsecondes, à laquelle le frame a été capturé. Cette durée est généralement utilisée pour déterminer l’intervalle entre les deux frames capturés.

</dd> <dt>

**FrameLength**
</dt> <dd>

Longueur du frame.

</dd> <dt>

**nBytesAvail**
</dt> <dd>

Longueur de trame réelle copiée.

</dd> <dt>

**ETYPE**
</dt> <dd>

Nom ETYPE.

</dd> <dt>

**SAP**
</dt> <dd>

Valeur SAP.

</dd> <dt>

**LowProtocol**
</dt> <dd>

Index du protocole trouvé.

</dd> <dt>

**LowProtocolOffset**
</dt> <dd>

Décalage des données de protocole obtenues à partir de **LowProtocol**.

</dd> <dt>

**HighPort**
</dt> <dd>

Port de protocole élevé identifié dans **LowProtocol**.

</dd> <dt>

**HighProtocolOffset**
</dt> <dd>

Décalage des données de protocole obtenues à partir de **HighPort**.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




