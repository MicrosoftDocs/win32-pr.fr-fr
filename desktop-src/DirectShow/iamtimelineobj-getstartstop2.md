---
description: 'La méthode GetStartStop2 récupère les heures de début et de fin de l’objet par rapport au parent de l’objet. Cette méthode est équivalente à IAMTimelineObj :: GetStartStop, mais prend des valeurs REFTIME.'
ms.assetid: 140842f5-3a24-4947-a360-ef97cba414ee
title: 'IAMTimelineObj :: GetStartStop2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 211bd54ee755a08d3e592a856c792eba6e3d4e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528087"
---
# <a name="iamtimelineobjgetstartstop2-method"></a>IAMTimelineObj :: GetStartStop2, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `GetStartStop2` méthode récupère les heures de début et de fin de l’objet par rapport au parent de l’objet. Cette méthode est équivalente à [**IAMTimelineObj :: GetStartStop**](iamtimelineobj-getstartstop.md), mais prend des valeurs [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetStartStop2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStart* 
</dt> <dd>

Reçoit l’heure de début, en secondes.

</dd> <dt>

*pStop* 
</dt> <dd>

Reçoit l’heure d’arrêt, en secondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

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

[**Interface IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




