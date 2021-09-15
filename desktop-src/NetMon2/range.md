---
description: La structure RANGE définit une plage de valeurs de propriété valides.
ms.assetid: 7bd14410-f5c1-487b-8776-405567991e5a
title: Structure de plage (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RANGE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: bf465636f315e60e43350bb370e2002b8a96e635
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311877"
---
# <a name="range-structure"></a>Structure de plage

La structure **Range** définit une plage de valeurs de propriété valides.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct range {
  DWORD MinValue;
  DWORD MaxValue;
} RANGE, *LPRANGE;
```



## <a name="members"></a>Membres

<dl> <dt>

**MinValue**
</dt> <dd>

Valeur la plus basse possible dans une plage.

</dd> <dt>

**MaxValue**
</dt> <dd>

Valeur la plus élevée possible dans une plage.

</dd> </dl>

## <a name="remarks"></a>Notes

La structure **Range** est utilisée pour spécifier une plage de nombres valide pour une propriété de protocole. Si le membre **DataQualifier** de la structure **PropertyInfo** a la valeur **prop \_ Qualys \_ Range**, le membre **lpRange** de la structure [PropertyInfo](propertyinfo.md) doit fournir un pointeur vers une structure **Range** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> </dl>

 

 




