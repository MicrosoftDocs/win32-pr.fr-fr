---
description: La méthode GetNextTrans récupère la première transition qui apparaît à l’heure spécifiée ou une version ultérieure.
ms.assetid: 40598d8d-ce74-4a6f-83d0-ea409b0a858c
title: 'IAMTimelineTransable :: GetNextTrans, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cc8f7c88dab2b8c0dfece6f2799b6648c0b9da2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543780"
---
# <a name="iamtimelinetransablegetnexttrans-method"></a>IAMTimelineTransable :: GetNextTrans, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `GetNextTrans` méthode récupère la première transition qui apparaît à l’heure spécifiée ou une version ultérieure.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNextTrans(
  [out] IAMTimelineObj **ppTrans,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppTrans* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’objet de transition.

</dd> <dt>

*pInOut* 
</dt> <dd>

Pointeur vers une variable qui spécifie le temps en unités de 100 nanosecondes. En entrée, cette valeur spécifie l’heure à partir de laquelle la transition doit être trouvée. En sortie, si une transition est récupérée, cette valeur est définie sur l’heure d’arrêt de la transition.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne \_ la valeur OK si la méthode récupère une transition ou la \_ valeur false si elle ne trouve pas de transition. Sinon, retourne une valeur **HRESULT** indiquant la cause de l’échec.

## <a name="remarks"></a>Notes

L’heure de début de la transition peut être inférieure à l’heure que vous spécifiez dans *pInOut*, si la transition s’étend sur l’heure spécifiée.

Si la méthode retourne la valeur \_ OK, l’interface [**IAMTimelineObj**](iamtimelineobj.md) qu’elle retourne a un nombre de références en attente. Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IAMTimelineTransable**](iamtimelinetransable.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




