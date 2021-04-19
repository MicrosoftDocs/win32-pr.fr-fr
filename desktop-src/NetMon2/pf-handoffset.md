---
description: La \_ structure HANDOFFSET de PF définit les protocoles qui sont confiés à l’analyseur, ou les protocoles que l’analyseur transmet.
ms.assetid: 2fda399d-a09e-47b4-bb2e-95996de9f950
title: Structure de PF_HANDOFFSET (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1b5dc9620f3b1860b27af973432aa4218c05b63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541216"
---
# <a name="pf_handoffset-structure"></a>PF \_ HANDOFFSET, structure

La **structure \_ HANDOFFSET de PF** définit les protocoles qui sont confiés à l’analyseur, ou les protocoles que l’analyseur transmet.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PF_HANDOFFSET {
  DWORD           nEntries;
  PF_HANDOFFENTRY Entry[];
} PF_HANDOFFSET, *PPF_HANDOFFSET;
```



## <a name="members"></a>Membres

<dl> <dt>

**nEntries**
</dt> <dd>

Nombre de protocoles.

</dd> <dt>

**Entrée**
</dt> <dd>

Tableau de structures [ \_ HANDOFFENTRY PF](pf-handoffentry.md) qui définissent chaque protocole.

</dd> </dl>

## <a name="remarks"></a>Notes

La [structure \_ PARSERINFO de PF](pf-parserinfo.md) utilise la structure **\_ HANDOFFSET de PF** pour répertorier les éléments suivants :

-   Les protocoles qui sont confiés à l’analyseur.
-   Les protocoles que l’analyseur transmet.

La **structure \_ HANDOFFSET de PF** doit être allouée à l’aide de **HeapAlloc**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[\_PARSERINFO PF](pf-parserinfo.md)
</dt> <dt>

[\_HANDOFFENTRY PF](pf-handoffentry.md)
</dt> </dl>

 

 




