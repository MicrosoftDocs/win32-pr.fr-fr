---
description: Pointeur vers une fonction qui est appelée à partir du point d’entrée de la DLL. Sa valeur peut être NULL.
ms.assetid: 0769f55b-6f0d-4a89-9d3f-64f211426342
title: 'CFactoryTemplate :: m_lpfnInit, membre (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnInit
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b44181f926f77ecc7cc22673622d4a0d3dcb7d26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234264"
---
# <a name="cfactorytemplatem_lpfninit-member"></a>CFactoryTemplate :: m \_ lpfnInit, membre

Pointeur vers une fonction qui est appelée à partir du point d’entrée de la DLL. Peut avoir la **valeur null**.

## <a name="syntax"></a>Syntaxe


```C++
LPFNInitRoutine m_lpfnInit;
```



## <a name="remarks"></a>Notes

Le type de pointeur de fonction est [**LPFNInitRoutine**](lpfninitroutine.md). Si vous fournissez cette fonction dans votre DLL, la fonction de point d’entrée DLL l’appelle avec les paramètres suivants :

-   *bLoading*: **true** lorsque la dll est chargée, **false** lorsque la dll est déchargée.
-   *rclsid*: pointeur vers CLISD de l’objet, spécifié dans la variable de membre [**CFactoryTemplate :: m \_ ClsID**](cfactorytemplate-m-clsid.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>combase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CFactoryTemplate, classe**](cfactorytemplate.md)
</dt> </dl>

 

 




