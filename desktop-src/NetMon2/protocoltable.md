---
description: La structure PROTOCOLTABLE contient une liste de protocoles.
ms.assetid: dad2b228-5916-44fe-b78e-ebc6507dc555
title: PROTOCOLTABLE, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3ad79beca7ce79611747a02704ffc05da5fc3d4b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311897"
---
# <a name="protocoltable-structure"></a>PROTOCOLTABLE, structure

La structure **PROTOCOLTABLE** contient une liste de protocoles.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PROTOCOLTABLE {
  DWORD     nProtocols;
  HPROTOCOL hProtocol[1];
} PROTOCOLTABLE;
```



## <a name="members"></a>Membres

<dl> <dt>

**nProtocols**
</dt> <dd>

Nombre de protocoles activés.

</dd> <dt>

**hProtocol**
</dt> <dd>

Tableau de handles vers les Protocoles activés.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




