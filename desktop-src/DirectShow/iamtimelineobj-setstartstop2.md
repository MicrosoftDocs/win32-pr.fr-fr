---
description: 'La méthode SetStartStop2 définit les heures de début et de fin de l’objet par rapport au parent de l’objet. Cette méthode est équivalente à IAMTimelineObj :: SetStartStop, mais prend des valeurs REFTIME.'
ms.assetid: 0fc79c82-d8e1-4b87-9e59-6d9e6ca614f3
title: 'IAMTimelineObj :: SetStartStop2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 30e7f9e6ce54cb86e2eee486937841842311dd498b42ec42e101128612bf16d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086829"
---
# <a name="iamtimelineobjsetstartstop2-method"></a>IAMTimelineObj :: SetStartStop2, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `SetStartStop2` méthode définit les heures de début et de fin de l’objet par rapport au parent de l’objet. Cette méthode est équivalente à [**IAMTimelineObj :: SetStartStop**](iamtimelineobj-setstartstop.md), mais prend des valeurs [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetStartStop2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Start* 
</dt> <dd>

Nouvelle heure de début, en secondes, ou-1 pour conserver l’heure de début existante.

</dd> <dt>

*Stop* 
</dt> <dd>

Nouvelle heure d’arrêt, en secondes, ou-1 pour conserver l’heure d’arrêt existante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                                  | Description                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Réussite.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argument non valide.<br/> |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>    | Non implémenté.<br/>  |



 

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

 

 




