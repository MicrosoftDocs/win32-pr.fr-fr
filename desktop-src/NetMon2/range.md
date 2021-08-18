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
ms.openlocfilehash: 0e0135a6210aebbca38bfdede00231315dd2680461f366930b24925eda830604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063719"
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

## <a name="remarks"></a>Remarques

La structure **Range** est utilisée pour spécifier une plage de nombres valide pour une propriété de protocole. Si le membre **DataQualifier** de la structure **PropertyInfo** a la valeur **prop \_ Qualys \_ Range**, le membre **lpRange** de la structure [PropertyInfo](propertyinfo.md) doit fournir un pointeur vers une structure **Range** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> </dl>

 

 




