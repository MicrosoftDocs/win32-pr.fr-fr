---
description: 'La méthode FixTimes2 arrondit les heures de démarrage et d’arrêt spécifiées aux limites de frame les plus proches, comme défini par le paramètre de fréquence d’images du groupe parent. Cette méthode est équivalente à IAMTimelineObj :: FixTimes, mais prend des valeurs REFTIME.'
ms.assetid: bdb3d999-2c91-4108-9286-c6e1f3362c09
title: 'IAMTimelineObj :: FixTimes2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 74890c2b094172ac3ced0c9fd192a755d051b56df22301b4d64d9003eaa74e9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400904"
---
# <a name="iamtimelineobjfixtimes2-method"></a>IAMTimelineObj :: FixTimes2, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

La `FixTimes2` méthode arrondit les heures de démarrage et d’arrêt spécifiées aux limites de frame les plus proches, comme défini par le paramètre de fréquence d’images du groupe parent. Cette méthode est équivalente à [**IAMTimelineObj :: FixTimes**](iamtimelineobj-fixtimes.md), mais prend des valeurs [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FixTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStart* 
</dt> <dd>

Pointeur vers une variable qui contient l’heure de début, en secondes. Si l’appel a échoué, cette variable est définie sur le temps arrondi.

</dd> <dt>

*pStop* 
</dt> <dd>

Pointeur vers une variable qui contient l’heure d’arrêt, en secondes. Si l’appel a échoué, cette variable est définie sur le temps arrondi.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou E \_ NOTINTREE si l’objet ne fait pas partie d’un groupe.

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

[**Interface IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




