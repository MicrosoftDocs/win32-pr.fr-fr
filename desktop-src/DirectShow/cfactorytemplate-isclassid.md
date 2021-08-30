---
description: La méthode IsClassID détermine si un CLSID correspond à ce modèle de classe.
ms.assetid: de560f7a-2ccb-44e2-ac32-3b0fea0d80b8
title: Méthode CFactoryTemplate. IsClassID (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.IsClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38714c6c6a97c46a14d1e381fdf49ddbc723d04ee217a09c9554b39d4eb22491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055789"
---
# <a name="cfactorytemplateisclassid-method"></a>Méthode CFactoryTemplate. IsClassID

La `IsClassID` méthode détermine si un CLSID correspond à ce modèle de classe.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsClassID(
   REFCLSID rclsid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*rclsid* 
</dt> <dd>

Référence à un CLSID.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si le paramètre *rclsid* est le même CLSID que la variable membre [**CFactoryTemplate :: m \_ CLSID**](cfactorytemplate-m-clsid.md) , ou sinon retourne **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>combase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CFactoryTemplate, classe**](cfactorytemplate.md)
</dt> </dl>

 

 




