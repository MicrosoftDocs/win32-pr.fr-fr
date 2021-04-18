---
description: La méthode VTrackGetCount récupère le nombre de pistes virtuelles contenues dans la composition.
ms.assetid: a8117b06-4f42-45da-9b93-f547cb70aa5d
title: 'IAMTimelineComp :: VTrackGetCount, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackGetCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 36800381ce50ea60d5252841d9731b2657fc22cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526634"
---
# <a name="iamtimelinecompvtrackgetcount-method"></a>IAMTimelineComp :: VTrackGetCount, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `VTrackGetCount` méthode récupère le nombre de pistes virtuelles contenues dans la composition.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT VTrackGetCount(
   long *pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVal* 
</dt> <dd>

Reçoit le nombre de pistes virtuelles.

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

[**Interface IAMTimelineComp**](iamtimelinecomp.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




