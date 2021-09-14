---
description: La méthode GetCutsOnly détermine si la transition est rendue sous la forme d’une coupe. Si c’est le cas, la transition se produit instantanément au point de coupe.
ms.assetid: d7959816-1152-4bc4-b3f8-bed69b450530
title: 'IAMTimelineTrans :: GetCutsOnly, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d3bbec55ddfe77c053135054fde9b64efce516a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012210"
---
# <a name="iamtimelinetransgetcutsonly-method"></a>IAMTimelineTrans :: GetCutsOnly, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetCutsOnly` méthode détermine si la transition est rendue sous la forme d’une coupe. Si c’est le cas, la transition se produit instantanément au point de coupe.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCutsOnly(
   BOOL *pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVal* 
</dt> <dd>

Reçoit une valeur booléenne spécifiant si la transition est rendue sous la forme d’une coupe. Si la **valeur est true**, la transition est une coupe instantanée. Si la **valeur est false**, la transition se produit sur sa durée normale.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

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

[**Interface IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[**IAMTimelineTrans::SetCutsOnly**](iamtimelinetrans-setcutsonly.md)
</dt> <dt>

[**IAMTimelineTrans::GetCutPoint**](iamtimelinetrans-getcutpoint.md)
</dt> <dt>

[**IAMTimeline::TransitionsEnabled**](iamtimeline-transitionsenabled.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




