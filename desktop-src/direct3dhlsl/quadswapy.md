---
title: QuadReadAcrossY fonction)
description: Retourne la valeur source spécifiée lue à partir de l’autre Lane dans ce Quad sur l’axe Y.
ms.assetid: 6C03D1E6-433F-4CCA-A5EA-C3F34BB2B93B
keywords:
- QuadReadAcrossY fonction HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f761a3588759e0c27143d16bd8fac5f674f05ae1819a0cdcebc55d6b4bdc6e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672399"
---
# <a name="quadreadacrossy-function"></a>QuadReadAcrossY fonction)

Retourne la valeur source spécifiée lue à partir de l’autre Lane dans ce Quad sur l’axe Y.

## <a name="syntax"></a>Syntaxe

``` syntax
<type> QuadReadAcrossY(
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

Valeur source spécifiée. Si le couloir source est inactif, les résultats ne sont pas définis.

## <a name="remarks"></a>Remarques

Pour plus d’informations sur les Quad, reportez-vous à [vue d’ensemble du Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Cette fonction est prise en charge à partir du nuanceur modèle 6,0 uniquement dans les nuanceurs de pixels et de calcul.



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Shader, modèle 6](shader-model-6-0.md)
</dt> </dl>

 

 




