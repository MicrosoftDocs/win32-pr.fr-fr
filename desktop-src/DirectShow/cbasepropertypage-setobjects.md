---
description: 'La méthode SetObjects fournit des pointeurs IUnknown pour les objets associés à la page de propriétés. Cette méthode implémente la méthode IPropertyPage :: SetObjects.'
ms.assetid: 11ca1e70-772c-414e-9647-7e4c4084c0d3
title: Méthode CBasePropertyPage. SetObjects (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetObjects
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 197c5eb82de76fb5a5f606d8a161e853b0c1e8f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539291"
---
# <a name="cbasepropertypagesetobjects-method"></a>Méthode CBasePropertyPage. SetObjects

La `SetObjects` méthode fournit des pointeurs **IUnknown** pour les objets associés à la page de propriétés. Cette méthode implémente la méthode **IPropertyPage :: SetObjects** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetObjects(
   ULONG     cObjects,
   LPUNKNOWN *ppUnk
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cObjects* 
</dt> <dd>

Spécifie le nombre de pointeurs **IUnknown** dans le tableau spécifié par *ppUnk*.

</dd> <dt>

*ppUnk* 
</dt> <dd>

Spécifie un tableau de pointeurs **IUnknown** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                  | Description                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Opération réussie.<br/>                   |
| <dl> <dt>**\_pointeur E**</dt> </dl>    | Argument de pointeur **null** .<br/> |
| <dl> <dt>**E \_ inattendu**</dt> </dl> | Erreur inattendue.<br/>        |



 

## <a name="remarks"></a>Notes

Bien que *ppUnk* spécifie un tableau de pointeurs **IUnknown** , la classe **CBasePropertyPage** est conçue uniquement pour prendre en charge un objet associé. Si *CObjects* est supérieur à 1, la méthode retourne E \_ inattendue.

Si *CObjects* est égal à 1, cette méthode appelle la méthode [**CBasePropertyPage :: OnConnect**](cbasepropertypage-onconnect.md) . Si *CObjects* est égal à 0, cette méthode appelle la méthode [**CBasePropertyPage :: OnDisconnect**](cbasepropertypage-ondisconnect.md) . La classe dérivée doit substituer ces deux méthodes ; Pour plus d’informations, consultez les notes relatives à ces méthodes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Cprop. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePropertyPage, classe**](cbasepropertypage.md)
</dt> </dl>

 

 




