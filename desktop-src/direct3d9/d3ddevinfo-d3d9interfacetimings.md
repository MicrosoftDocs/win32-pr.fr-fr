---
description: Pourcentage de temps de traitement des données dans le pilote. Ces statistiques peuvent aider à identifier les cas où le pilote attend d’autres ressources.
ms.assetid: 2c613349-61eb-44aa-aa7b-3161dd1fc95e
title: Structure D3DDEVINFO_D3D9INTERFACETIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9INTERFACETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d7261096ed373620b8438ccce2d353ccf21f1c236028e8c829951fc64ee3725a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989029"
---
# <a name="d3ddevinfo_d3d9interfacetimings-structure"></a>D3DDEVINFO \_ D3D9INTERFACETIMINGS, structure

Pourcentage de temps de traitement des données dans le pilote. Ces statistiques peuvent aider à identifier les cas où le pilote attend d’autres ressources.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DDEVINFO_D3D9INTERFACETIMINGS {
  FLOAT WaitingForGPUToUseApplicationResourceTimePercent;
  FLOAT WaitingForGPUToAcceptMoreCommandsTimePercent;
  FLOAT WaitingForGPUToStayWithinLatencyTimePercent;
  FLOAT WaitingForGPUExclusiveResourceTimePercent;
  FLOAT WaitingForGPUOtherTimePercent;
} D3DDEVINFO_D3D9INTERFACETIMINGS, *LPD3DDEVINFO_D3D9INTERFACETIMINGS;
```



## <a name="members"></a>Membres

<dl> <dt>

**WaitingForGPUToUseApplicationResourceTimePercent**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Pourcentage de temps passé par le pilote à attendre la fin du GPU à l’aide d’une ressource verrouillée (et [D3DLOCK \_ DONOTWAIT](d3dlock.md) n’a pas été spécifié).

</dd> <dt>

**WaitingForGPUToAcceptMoreCommandsTimePercent**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Pourcentage de temps passé par le pilote à attendre que le GPU termine le traitement de certaines commandes avant que le pilote puisse en envoyer davantage. Cela indique que le pilote n’a plus suffisamment de place pour envoyer des commandes au GPU.

</dd> <dt>

**WaitingForGPUToStayWithinLatencyTimePercent**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Pourcentage de temps passé par le pilote à attendre la latence du GPU pour réduire à moins de trois frames de rendu.

Si une application est limitée par GPU, le pilote doit bloquer l’UC jusqu’à ce que le GPU soit dans trois frames. Cela empêche une application de mettre en file d’attente de nombreuses secondes les appels de rendu, ce qui peut augmenter considérablement la latence entre le moment où l’utilisateur entre de nouvelles données et le moment où l’utilisateur voit les résultats de cette entrée. En général, le pilote peut effectuer le suivi du nombre de fois où l’élément [**présent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) est appelé pour empêcher la mise en file d’attente de plus de trois frames de travail de rendu.

</dd> <dt>

**WaitingForGPUExclusiveResourceTimePercent**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Pourcentage de temps passé par le pilote à attendre une ressource qui ne peut pas être canalisée (qui est exécutée en parallèle). Une application peut souhaiter éviter d’utiliser une ressource non pipeline pour des raisons de performances.

</dd> <dt>

**WaitingForGPUOtherTimePercent**
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Pourcentage de temps passé par le pilote à attendre un autre traitement GPU.

</dd> </dl>

## <a name="remarks"></a>Remarques

Ces mesures permettent d’identifier le moment où un pilote est en attente et ce qu’il attend. Les pourcentages élevés ne sont pas nécessairement un problème.

Ces métriques globales du système peuvent ou non être implémentées. En fonction du matériel spécifique, ces métriques peuvent ne pas prendre en charge plusieurs requêtes simultanément.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
