---
description: Méthode de constructeur.
ms.assetid: a64c3e29-91f2-455f-aac1-1e4ecce6958d
title: Constructeur CTransformFilter. CTransformFilter (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39569dff69c2ab1ebb635cb69a4c71602a7400d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525295"
---
# <a name="ctransformfilterctransformfilter-constructor"></a>Constructeur CTransformFilter. CTransformFilter

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CTransformFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   CLSID     clsid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pObjectName* 
</dt> <dd>

Chaîne contenant le nom de débogage du filtre. Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*lpUnk* 
</dt> <dd>

Pointeur vers le propriétaire de cet objet. Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation. Sinon, affectez la valeur **null** à ce paramètre.

</dd> <dt>

*identificateur* 
</dt> <dd>

Identificateur de classe du filtre.

</dd> </dl>

## <a name="remarks"></a>Notes

Le constructeur ne crée pas les codes confidentiels du filtre. Cela se produit lors du premier appel à la méthode [**GetPin**](ctransformfilter-getpin.md) . Le constructeur initialise les variables de membre [**m \_ pInput**](ctransformfilter-m-pinput.md) et [**m \_ pOutput**](ctransformfilter-m-poutput.md) à la **valeur null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




