---
description: La structure ADDRESSTABLE contient une table de paires d’adresses.
ms.assetid: 84577b6c-9d43-4e53-9f8d-33685329b11d
title: ADDRESSTABLE, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c1c766e29033136954abab69755e1231e610983314cdaa01da3957889af5eb33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064279"
---
# <a name="addresstable-structure"></a>ADDRESSTABLE, structure

La structure **ADDRESSTABLE** contient une table de paires d’adresses.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _ADDRESSTABLE {
  DWORD       nAddressPairs;
  DWORD       nNonMacAddressPairs;
  ADDRESSPAIR AddressPair[MAX_ADDRESS_PAIRS];
} ADDRESSTABLE, *LPADDRESSTABLE;
```



## <a name="members"></a>Membres

<dl> <dt>

**nAddressPairs**
</dt> <dd>

Nombre de paires d’adresses dans le tableau **AddressPair** .

</dd> <dt>

**nNonMacAddressPairs**
</dt> <dd>

Nombre de paires d’adresses non-MAC.

</dd> <dt>

**AddressPair**
</dt> <dd>

Tableau de paires d’adresses. Notez que vous ne pouvez stocker que huit paires d’adresses par structure ADDRESSTABLE.

</dd> </dl>

## <a name="remarks"></a>Remarques

Utilisez cette structure dans le cadre du processus de construction de filtre de capture. Pour plus d’informations sur l’implémentation de cette structure, consultez [filtres de capture](capture-filters.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ADDRESSPAIR](addresspair.md)
</dt> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




