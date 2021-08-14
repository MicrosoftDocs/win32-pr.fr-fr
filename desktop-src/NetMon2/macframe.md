---
description: La structure MACFRAME est une Union des protocoles initiaux les plus courants.
ms.assetid: ec7e3a54-a47f-4390-a137-9574c63c9a11
title: MACFRAME Union (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MACFRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: dcff7294d2800e797b43b3a05bd25c35418c6fb466c95130b97be73f25040d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364707"
---
# <a name="macframe-union"></a>MACFRAME Union

La structure **MACFRAME** est une Union des protocoles initiaux les plus courants.

## <a name="syntax"></a>Syntaxe


```C++
typedef union {
  LPBYTE      MacHeader;
  LPETHERNET  Ethernet;
  LPTOKENRING Tokenring;
  LPFDDI      Fddi;
} MACFRAME, *LPMACFRAME;
```



## <a name="members"></a>Membres

<dl> <dt>

**MacHeader**
</dt> <dd>

Pointeur générique vers un frame.

</dd> <dt>

**Ethernet**
</dt> <dd>

Pointeur Ethernet vers un frame.

</dd> <dt>

**Tokenring**
</dt> <dd>

Pointeur Token Ring vers un frame.

</dd> <dt>

**FDDI**
</dt> <dd>

Pointeur FDDI vers un frame.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure est le plus souvent utilisée comme une superposition. Pour rendre les propriétés du premier protocole accessibles, effectuez un cast du frame en tant que type identique au protocole.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




