---
description: 'Non pris en charge. Appelez la méthode IAMTimelineComp :: GetRecursiveLayerOfType à la place.'
ms.assetid: 857f57e2-6123-43c3-bb74-62afd0fc0b52
title: 'IAMTimelineComp :: GetRecursiveLayerOfTypeI, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfTypeI
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dc62c0813aa38af450e2f5351390ec958dddd533cc203f52b3bfb70ff45344b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756419"
---
# <a name="iamtimelinecompgetrecursivelayeroftypei-method"></a>IAMTimelineComp :: GetRecursiveLayerOfTypeI, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

Non pris en charge. Appelez la méthode [**IAMTimelineComp :: GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md) à la place.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRecursiveLayerOfTypeI(
   IAMTimelineObj      **ppVirtualTrack,
   long                **pWhichLayer,
   TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppVirtualTrack* 
</dt> <dd>

Réservé.

</dd> <dt>

*pWhichLayer* 
</dt> <dd>

Réservé.

</dd> <dt>

*Type* 
</dt> <dd>

Réservé.

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

[**Interface IAMTimelineComp**](iamtimelinecomp.md)
</dt> </dl>

 

 




