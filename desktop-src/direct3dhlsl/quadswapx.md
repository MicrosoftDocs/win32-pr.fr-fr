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
ms.openlocfilehash: cd41b0bd84861d23153f02ba6328d17b70287866
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104102553"
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

## <a name="remarks"></a>Notes

Pour plus d’informations sur les Quad, reportez-vous à [vue d’ensemble du Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Cette fonction est prise en charge à partir du nuanceur modèle 6,0 uniquement dans les nuanceurs de pixels et de calcul.



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Shader, modèle 6](shader-model-6-0.md)
</dt> </dl>

 

 




