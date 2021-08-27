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
ms.openlocfilehash: a30d890fa5b6dcbbca1797a53722b97b2109cc9943ce07260c7f47514cfeb7b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036979"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




