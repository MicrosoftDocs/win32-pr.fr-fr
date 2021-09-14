---
description: 'La méthode GetNextTrans2 récupère la première transition qui apparaît à l’heure spécifiée ou une version ultérieure. Cette méthode est équivalente à IAMTimelineTransable :: GetNextTrans, mais prend une valeur REFTIME.'
ms.assetid: e6910e94-f289-4a5d-9976-1e8f7373c882
title: 'IAMTimelineTransable :: GetNextTrans2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2c5f79ff20507247fbcac3badceaf2c3e28f0303
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012192"
---
# <a name="iamtimelinetransablegetnexttrans2-method"></a>IAMTimelineTransable :: GetNextTrans2, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetNextTrans2` méthode récupère la première transition qui apparaît à l’heure spécifiée ou une version ultérieure. Cette méthode est équivalente à [**IAMTimelineTransable :: GetNextTrans**](iamtimelinetransable-getnexttrans.md), mais prend une valeur [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNextTrans2(
  [out] IAMTimelineObj **ppTrans,
        REFTIME        *pInOut
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

Pointeur vers une variable qui spécifie la durée en secondes. En entrée, cette valeur spécifie l’heure à partir de laquelle la transition doit être trouvée. En sortie, si une transition est récupérée, cette valeur est définie sur l’heure d’arrêt de la transition.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne \_ la valeur OK si la méthode récupère une transition ou la \_ valeur false si elle ne trouve pas de transition. Sinon, retourne une valeur **HRESULT** indiquant la cause de l’échec.

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Spécifications



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

 

 




