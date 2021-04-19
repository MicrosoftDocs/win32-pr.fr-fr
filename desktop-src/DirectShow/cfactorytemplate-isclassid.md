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
ms.openlocfilehash: 94564d7e9db52f8be22717a10f73fffb7fb6fa14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530989"
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
| En-tête<br/>  | <dl> <dt>ComBase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CFactoryTemplate, classe**](cfactorytemplate.md)
</dt> </dl>

 

 




