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
ms.openlocfilehash: 930b828e1b715cfcb53275192ed76a7df7d116ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012226"
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

**rt**
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[**\_paramètre Dexter**](dexter-param.md)
</dt> </dl>

 

 




