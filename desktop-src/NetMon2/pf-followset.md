---
description: La \_ structure FOLLOWSET de PF définit les protocoles qui peuvent précéder ou suivre un protocole.
ms.assetid: ef444af9-edae-4547-9548-8a682c279f08
title: Structure de PF_FOLLOWSET (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f5c286d3b137df24f7da7f0fc5ae269a7a3d946d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534340"
---
# <a name="pf_followset-structure"></a>PF \_ FOLLOWSET, structure

La **structure \_ FOLLOWSET de PF** définit les protocoles qui peuvent précéder ou suivre un protocole.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PF_FOLLOWSET {
  DWORD          nEntries;
  PF_FOLLOWENTRY Entry[];
} PF_FOLLOWSET, *PPF_FOLLOWSET;
```



## <a name="members"></a>Membres

<dl> <dt>

**nEntries**
</dt> <dd>

Nombre de protocoles dans la liste.

</dd> <dt>

**Entrée**
</dt> <dd>

Tableau de [structures \_ FOLLOWENTRY PF](pf-followentry.md) qui décrivent chaque protocole.

</dd> </dl>

## <a name="remarks"></a>Notes

La [structure \_ PARSERINFO de PF](pf-parserinfo.md) utilise la structure **\_ FOLLOWSET de PF** pour répertorier les protocoles qui peuvent précéder ou suivre le protocole détecté par l’analyseur.

Moniteur réseau utilise les informations de la **structure \_ FOLLOWSET de PF** pour mettre à jour les ensembles suivants d’analyseurs spécifiques. La **structure \_ FOLLOWSET de PF** doit être allouée à l’aide de **HeapAlloc**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[\_FOLLOWENTRY PF](pf-followentry.md)
</dt> <dt>

[\_PARSERINFO PF](pf-parserinfo.md)
</dt> </dl>

 

 




