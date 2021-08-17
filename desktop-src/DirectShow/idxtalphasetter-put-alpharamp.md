---
description: La \_ méthode put AlphaRamp spécifie la propriété de rampe alpha. La rampe alpha est le pourcentage d’ajustement des valeurs alpha dans l’image d’origine. Par exemple, si la rampe alpha est 0,5, les valeurs alpha de l’image sont réduites à 50%.
ms.assetid: 19ea5828-54fc-43a1-be7c-f6c12cf84648
title: IDxtAlphaSetter ::p ut_AlphaRamp, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 88661c40ea0824d643909f688a7d86251c434e0e3dcc88d8a3aec97dcb6b40c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952728"
---
# <a name="idxtalphasetterput_alpharamp-method"></a>IDxtAlphaSetter ::p ut \_ AlphaRamp, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `put_AlphaRamp` méthode spécifie la propriété de rampe alpha. La rampe alpha est le pourcentage d’ajustement des valeurs alpha dans l’image d’origine. Par exemple, si la rampe alpha est 0,5, les valeurs alpha de l’image sont réduites à 50%.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_AlphaRamp(
  [in] double Alpha
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Alpha* \[ dans\]
</dt> <dd>

Rampe alpha sous la forme d’un pourcentage. Par exemple, 1,0 est 100%. Pour désactiver cette propriété, définissez une valeur négative.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Si vous affectez une valeur non négative à cette propriété, vous devez également désactiver la propriété alpha en appelant **put \_ alpha** avec une valeur négative. Dans le cas contraire, l’effet ne sera pas correctement rendu.

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

[**Interface IDxtAlphaSetter**](idxtalphasetter.md)
</dt> <dt>

[**IDxtAlphaSetter ::p ut \_ alpha**](idxtalphasetter-put-alpha.md)
</dt> </dl>

 

 




