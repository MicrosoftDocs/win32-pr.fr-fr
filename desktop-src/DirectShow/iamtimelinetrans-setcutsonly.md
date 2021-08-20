---
description: La méthode SetCutsOnly spécifie si la transition est rendue sous la forme d’une coupe. Si c’est le cas, la transition se produit instantanément au point de coupe. Si le rendu d’une transition prend beaucoup de temps, vous souhaiterez peut-être l’afficher en mode d’affichage couper pour accélérer l’affichage.
ms.assetid: 9ccff624-e37b-422e-9cb2-c472e6c8b2bb
title: 'IAMTimelineTrans :: SetCutsOnly, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3b008e0aef31548dcba71f3b2a2940009c0cd0c71786bd9bd733c206c1d68ee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154724"
---
# <a name="iamtimelinetranssetcutsonly-method"></a>IAMTimelineTrans :: SetCutsOnly, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `SetCutsOnly` méthode spécifie si la transition est rendue sous la forme d’une coupe. Si c’est le cas, la transition se produit instantanément au point de coupe. Si le rendu d’une transition prend beaucoup de temps, vous souhaiterez peut-être l’afficher en mode d’affichage couper pour accélérer l’affichage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetCutsOnly(
   BOOL Val
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Val* 
</dt> <dd>

Spécifie s’il faut restituer la transition comme une coupe. Si la **valeur est true**, la transition est rendue sous la forme d’une coupe instantanée. Si la **valeur est false**, la transition est rendue sur sa durée normale.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Le rendu d’une transition en tant que coupe n’est pas compatible avec la permutation des entrées. (Voir [**IAMTimelineTrans :: SetSwapInputs**](iamtimelinetrans-setswapinputs.md).) Si vous appelez `SetCutsOnly` avec la valeur **true**, il remplace temporairement le paramètre **SetSwapInputs** . Toutefois, le paramètre de coupe uniquement est prévu pour l’aperçu. par conséquent, cette limitation n’affecte pas la sortie du fichier. n’oubliez pas d’appeler `SetCutsOnly` avec la valeur **false** avant d’écrire le fichier.

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

[**Interface IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




