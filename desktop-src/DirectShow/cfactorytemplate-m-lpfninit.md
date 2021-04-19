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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534768"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>ComBase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CFactoryTemplate, classe**](cfactorytemplate.md)
</dt> </dl>

 

 




