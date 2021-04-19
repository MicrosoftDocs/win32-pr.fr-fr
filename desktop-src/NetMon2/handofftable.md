---
description: La structure HANDOFFTABLE définit les protocoles d’une table de remise.
ms.assetid: 6bb7465b-c1ba-4ffe-aecf-8125993c309a
title: HANDOFFTABLE, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 842ef9fde56ff6b4c420034b861aa8c151e7e6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517444"
---
# <a name="handofftable-structure"></a>HANDOFFTABLE, structure

La structure **HANDOFFTABLE** définit les protocoles d’une table de remise.

Cette structure est renseignée par Moniteur réseau en fonction des informations contenues dans un fichier. ini fourni par l’utilisateur fourni lors de l’appel de la fonction [**CreateHandoffTable**](createhandofftable.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct HANDOFFTABLE {
  DWORD          hot_sig;
  DWORD          hot_NumEntries;
  LPHANDOFFENTRY hot_Entries;
} HANDOFFTABLE, *LPHANDOFFTABLE;
```



## <a name="members"></a>Membres

<dl> <dt>

**\_SIG chaud**
</dt> <dd>

Signature qui identifie cette table comme table de remise.

</dd> <dt>

**\_NumEntries chaud**
</dt> <dd>

Nombre d’entrées qui Moniteur réseau ajoutées à la table de remise.

</dd> <dt>

**entrées réactives \_**
</dt> <dd>

Table de remise.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure, ainsi que les structures HANDOFFENTRY associées, sont renseignées par Moniteur réseau lorsque Moniteur réseau crée une table de remise.

Les informations de protocole qui sont utilisées lors de la création d’une table de remise sont fournies dans un fichier. ini fourni par l’application lorsque [**CreateHandoffTable**](createhandofftable.md) est appelé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[HANDOFFENTRY](handoffentry.md)
</dt> <dt>

[CreateHandoffTable](createhandofftable.md)
</dt> </dl>

 

 




