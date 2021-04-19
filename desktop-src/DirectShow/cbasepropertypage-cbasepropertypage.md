---
description: Méthode de constructeur.
ms.assetid: 5d9863e7-fdd9-4df2-a603-34a240a2286c
title: Constructeur CBasePropertyPage. CBasePropertyPage (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 915bc42cfb7f152cc061dab76caede6c998edf8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539177"
---
# <a name="cbasepropertypagecbasepropertypage-constructor"></a>Constructeur CBasePropertyPage. CBasePropertyPage

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CBasePropertyPage(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   int       DialogId,
   int       TitleId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pName* 
</dt> <dd>

Chaîne qui contient le nom de l’objet, à des fins de débogage. Pour plus d’informations, consultez [**CBaseObject :: CBaseObject**](cbaseobject-cbaseobject.md).

</dd> <dt>

*pUnk* 
</dt> <dd>

Pointeur vers l’interface **IUnknown** d’agrégation.

</dd> <dt>

*DialogId* 
</dt> <dd>

ID de ressource de la boîte de dialogue.

</dd> <dt>

*TitleId* 
</dt> <dd>

ID de ressource pour la chaîne qui contient le titre de la boîte de dialogue.

</dd> </dl>

## <a name="examples"></a>Exemples


```C++
CMyProp::CMyProp(IUnknown *pUnk) : 
    CBasePropertyPage(NAME("MyPropPage"), pUnk, IDD_PROPPAGE, IDS_TITLE),
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Cprop. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePropertyPage, classe**](cbasepropertypage.md)
</dt> </dl>

 

 




