---
title: QuadReadAcrossX fonction)
description: Retourne la valeur locale spécifiée lue à partir de l’autre Lane dans ce Quad sur l’axe X.
ms.assetid: 7A7E0623-30EC-4167-90A5-D79E10A394CC
keywords:
- QuadReadAcrossX fonction HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 86a2f525a79fa2458e4f7e0ef44379053e03128782d2625e1bdceb23ec518b16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672439"
---
# <a name="quadreadacrossx-function"></a>QuadReadAcrossX fonction)

Retourne la valeur locale spécifiée lue à partir de l’autre Lane dans ce Quad sur l’axe X.

## <a name="syntax"></a>Syntaxe

``` syntax
<type> QuadReadAcrossX(
   <type> localValue
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*localValue* 
</dt> <dd>

Type demandé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Valeur locale spécifiée. Si le couloir source est inactif, les résultats ne sont pas définis.

## <a name="remarks"></a>Remarques

Pour plus d’informations sur les Quad, reportez-vous à [vue d’ensemble du Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Cette fonction est prise en charge à partir du nuanceur modèle 6,0 uniquement dans les nuanceurs de pixels et de calcul.



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Shader, modèle 6](shader-model-6-0.md)
</dt> </dl>

 

 




