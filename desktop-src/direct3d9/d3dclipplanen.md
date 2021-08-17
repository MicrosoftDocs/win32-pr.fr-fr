---
description: Définit des modèles binaires qui permettent des plans de découpage définis par l’utilisateur. Ces macros sont définies comme pratiques lors de la définition de valeurs pour l' \_ État de rendu D3DRS CLIPPLANEENABLE.
ms.assetid: 5bca2401-a3fb-4b1c-bb59-621b15da10f1
title: D3DCLIPPLANEn macro (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPPLANEn
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 315f1cdd8f8835b869f04edd9869243f3e05a9c2c9a08a41eeffc014727b3fc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805466"
---
# <a name="d3dclipplanen-macro"></a>D3DCLIPPLANEn macro)

Définit des modèles binaires qui permettent des plans de découpage définis par l’utilisateur. Ces macros sont définies comme pratiques lors de la définition de valeurs pour l' \_ État de rendu D3DRS CLIPPLANEENABLE.

## <a name="syntax"></a>Syntaxe


```C++
void D3DCLIPPLANEn(void);
```



## <a name="parameters"></a>Paramètres

Cette macro n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette macro ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Les plans de découpage définis par l’utilisateur sont activés lorsque la valeur définie dans l' \_ État de rendu D3DRS CLIPPLANEENABLE contient un ou plusieurs bits Set (autrement dit, n’est pas 0). La valeur de l’État Render n’est pas importante. le système n’interprète pas la valeur comme un nombre. Au lieu de cela, la valeur active le plan de découpage dont le bit correspondant est défini. Le bit 0 contrôle l’état du premier plan de découpage (au niveau de l’index 0), le bit 1 le deuxième plan, et ainsi de suite.

Les modèles de bits créés par ces macros peuvent être combinés à l’aide d’une opération OR logique pour activer simultanément plusieurs plans de découpage. L’omission de l’une de ces macros dans la combinaison désactive efficacement le plan de découpage au niveau de cet index.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




