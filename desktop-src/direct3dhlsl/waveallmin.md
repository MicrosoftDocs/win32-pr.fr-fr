---
title: WaveActiveMin fonction)
description: Retourne la valeur minimale de l’expression sur tous les couloirs actifs de l’onde actuelle pour la répliquer à tous les couloirs actifs.
ms.assetid: BA762C02-894C-4AF9-A226-C1E3AAC286FF
keywords:
- WaveActiveMin fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91555df354ab2b7ffc447a9422c4811ae23e6e0c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104032090"
---
# <a name="waveactivemin-function"></a>WaveActiveMin fonction)

Retourne la valeur minimale de l’expression sur tous les couloirs actifs de l’onde actuelle pour la répliquer à tous les couloirs actifs.

## <a name="syntax"></a>Syntaxe

``` syntax
<type> WaveActiveMin(
   <type> expr
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*expr* 
</dt> <dd>

Expression à évaluer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Valeur minimale.

## <a name="remarks"></a>Notes

L’ordre des opérations n’est pas défini.

Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur. 



 

## <a name="examples"></a>Exemples

``` syntax
 float3 minPos = WaveActiveMin( myPoint.position );
    BoundingBox.min = min( minPos, BoundingBox.min );
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du modèle de nuanceur 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader, modèle 6](shader-model-6-0.md)
</dt> </dl>

 

 




