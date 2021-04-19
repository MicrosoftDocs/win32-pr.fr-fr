---
description: La méthode ModifyStopTime définit l’heure d’arrêt, par rapport à la chronologie.
ms.assetid: 0d9b6cf7-d029-4c35-9045-82cbeff1e3ae
title: 'IAMTimelineSrc :: ModifyStopTime, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5e0f3ac58df4e74926d2163705261ffad4551e69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533458"
---
# <a name="iamtimelinesrcmodifystoptime-method"></a>IAMTimelineSrc :: ModifyStopTime, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `ModifyStopTime` méthode définit l’heure d’arrêt, par rapport à la chronologie.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ModifyStopTime(
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Stop* 
</dt> <dd>

Nouvelle heure d’arrêt, en unités de 100 nanosecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK ou E \_ INVALIDARG si l’heure spécifiée n’est pas valide.

## <a name="remarks"></a>Notes

Cette méthode équivaut à appeler [**IAMTimelineObj :: SetStartStop**](iamtimelineobj-setstartstop.md) avec l’heure de début d’origine et une nouvelle heure d’arrêt.

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

[**Interface IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




