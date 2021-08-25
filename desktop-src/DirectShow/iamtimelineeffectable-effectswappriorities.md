---
description: La méthode EffectSwapPriorities bascule les niveaux de priorité de deux effets.
ms.assetid: ff5ab294-3963-4df7-9299-ee7c7165e72f
title: 'IAMTimelineEffectable :: EffectSwapPriorities, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6e79f3f83422290600b4b6e75dbf15daff161f5e913a0300645254cdf94e7c37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928229"
---
# <a name="iamtimelineeffectableeffectswappriorities-method"></a>IAMTimelineEffectable :: EffectSwapPriorities, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `EffectSwapPriorities` méthode bascule les niveaux de priorité de deux effets.

Étant donné deux valeurs de priorité, cette méthode permute les effets à ces priorités. Lorsque la méthode retourne, l’effet qui se trouvait au premier niveau de priorité est le deuxième niveau de priorité, et vice versa.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EffectSwapPriorities(
   long PriorityA,
   long PriorityB
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Prioritéa* 
</dt> <dd>

Premier niveau de priorité auquel permuter les effets.

</dd> <dt>

*PriorityB* 
</dt> <dd>

Deuxième niveau de priorité auquel permuter les effets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IAMTimelineEffectable**](iamtimelineeffectable.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




