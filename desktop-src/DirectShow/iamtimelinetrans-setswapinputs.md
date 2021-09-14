---
description: La méthode SetSwapInputs spécifie si les entrées de transition sont échangées.
ms.assetid: c7303302-dbc4-41b6-8049-5c4496ee9264
title: 'IAMTimelineTrans :: SetSwapInputs, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b2deecb393d6532015cf1490aacd1bd50501920
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012195"
---
# <a name="iamtimelinetranssetswapinputs-method"></a>IAMTimelineTrans :: SetSwapInputs, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `SetSwapInputs` méthode spécifie si les entrées de transition sont échangées.

Par défaut, une transition va du composite de toutes les couches de faible priorité à la couche où la transition réside. Vous pouvez inverser cette progression, de sorte que la transition va de la couche où elle réside vers l’composite des couches de faible priorité. Pour plus d’informations, consultez [direction de transition](transition-direction.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetSwapInputs(
   BOOL Val
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Val* 
</dt> <dd>

Spécifie si les entrées sont échangées. Si la **valeur est false**, la transition passe de l’composite de toutes les couches de faible priorité à la couche de transition. Si la **valeur est true**, la transition passe dans la direction opposée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Cette méthode ne modifie pas la direction de l’effet visuel. Par exemple, une réinitialisation de gauche à droite sera toujours de gauche à droite. Pour modifier la direction, définissez la propriété **Progress** à l’aide de l’interface [**IPropertySetter**](ipropertysetter.md) .

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

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




