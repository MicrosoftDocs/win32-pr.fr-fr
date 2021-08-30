---
description: Identifie une propriété qui doit être définie sur une transition ou un effet, ainsi que le nombre de valeurs distinctes que la propriété suppose sur la durée de la transition ou de l’effet.
ms.assetid: 3b1c35cf-f1f7-4f2c-8d94-1aaae4116833
title: Structure DEXTER_VALUE (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_VALUE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: e8e76636a28f1eaa8f3bd948c29e4ab6b2440c75bb4265f6d3c1bf281599bbf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051949"
---
# <a name="dexter_value-structure"></a>Structure de valeur DEXTERity \_

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

Identifie une propriété qui doit être définie sur une transition ou un effet, ainsi que le nombre de valeurs distinctes que la propriété suppose sur la durée de la transition ou de l’effet.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  VARIANT        v;
  REFERENCE_TIME rt;
  DWORD          dwInterp;
} DEXTER_VALUE;
```



## <a name="members"></a>Membres

<dl> <dt>

**v**
</dt> <dd>

Valeur de la propriété.

</dd> <dt>

**t**
</dt> <dd>

Heure à laquelle la propriété assume la valeur, par rapport au début de la transition ou de l’effet.

</dd> <dt>

**dwInterp**
</dt> <dd>

Indicateur qui spécifie la façon dont la propriété progresse de la valeur précédente à cette valeur. Doit prendre l'une des valeurs suivantes :



| Valeur                                                                                                                                                                           | Signification                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="DEXTERF_JUMP"></span><span id="dexterf_jump"></span><dl> <dt>**DEXTERF \_ saut**</dt> </dl>                      | La propriété passe instantanément à la nouvelle valeur à l’heure spécifiée.<br/>     |
| <span id="DEXTERF_INTERPOLATE"></span><span id="dexterf_interpolate"></span><dl> <dt>**\_interpolation DEXTERF**</dt> </dl> | La propriété est interpolée de façon linéaire dans le temps à partir de la valeur précédente.<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[**\_paramètre Dexter**](dexter-param.md)
</dt> </dl>

 

 




