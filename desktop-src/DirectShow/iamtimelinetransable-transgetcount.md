---
description: La méthode TransGetCount récupère le nombre de transitions sur cet objet.
ms.assetid: f7fb4a99-c841-4680-b7f1-e4d887f12707
title: 'IAMTimelineTransable :: TransGetCount, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransGetCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e69724854e69b4139811b5afe2f3b516f592c17594650f585e576dea0f6c9894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399186"
---
# <a name="iamtimelinetransabletransgetcount-method"></a>IAMTimelineTransable :: TransGetCount, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

La `TransGetCount` méthode récupère le nombre de transitions sur cet objet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT TransGetCount(
   long *pCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCount* 
</dt> <dd>

Reçoit le nombre de transitions.

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

[**Interface IAMTimelineTransable**](iamtimelinetransable.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




