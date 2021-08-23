---
description: La \_ structure FOLLOWENTRY de PF définit un protocole que Moniteur réseau ajoute au jeu suivant d’un analyseur.
ms.assetid: 931ae70f-8c5e-4b7a-aae6-64a33dac3b23
title: Structure de PF_FOLLOWENTRY (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 8fd7452a4db6318df0d4c23ea405d2cd4afcf6575c7abac34749a66bc88c2084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063729"
---
# <a name="pf_followentry-structure"></a>PF \_ FOLLOWENTRY, structure

La **structure \_ FOLLOWENTRY de PF** définit un protocole que Moniteur réseau ajoute au jeu suivant d’un analyseur.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PF_FOLLOWENTRY {
  char szProtocol[MAX_PROTOCOL_NAME_LEN];
} PF_FOLLOWENTRY, *PPF_FOLLOWENTRY;
```



## <a name="members"></a>Membres

<dl> <dt>

**szProtocol**
</dt> <dd>

Nom du protocole.

</dd> </dl>

## <a name="remarks"></a>Remarques

La [structure \_ FOLLOWSET de PF](pf-followset.md) utilise un tableau de structures **\_ FOLLOWENTRY PF** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[\_FOLLOWSET PF](pf-followset.md)
</dt> </dl>

 

 




