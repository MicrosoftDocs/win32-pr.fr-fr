---
description: CMediaPosition. GetIDsOfNames, méthode-la méthode GetIDsOfNames mappe un ensemble de noms à un ensemble correspondant de DISPID.
ms.assetid: 4d3780ff-905f-4166-86d4-32395090b5cb
title: CMediaPosition. GetIDsOfNames, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26a348e58fa84aa4134ce9f2ea756874b9ce2724
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095527"
---
# <a name="cmediapositiongetidsofnames-method"></a>CMediaPosition. GetIDsOfNames, méthode

La `GetIDsOfNames` méthode mappe un ensemble de noms à un ensemble correspondant de DISPID.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*riid* 
</dt> <dd>

Réservé. Utilisez l’IID \_ null.

</dd> <dt>

*rgszNames* 
</dt> <dd>

Adresse d’un tableau de chaînes de caractères larges qui contiennent les noms à mapper.

</dd> <dt>

*Enregistrements CNAME* 
</dt> <dd>

Taille du tableau donnée par le paramètre *rgszNames* .

</dd> <dt>

*lcid* 
</dt> <dd>

Contexte des paramètres régionaux dans lequel interpréter les noms. Peut avoir la **valeur null**.

</dd> <dt>

*rgdispid* 
</dt> <dd>

Pointeur vers un tableau qui reçoit les DISPID. Chaque élément de reçoit un identificateur qui correspond à l’un des noms transmis dans le paramètre *rgszNames* .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                         | Description                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | Réussite.<br/>                                 |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>       | Mémoire insuffisante.<br/>                     |
| <dl> <dt>**\_UNKNOWNNAME DISP \_**</dt> </dl> | Un ou plusieurs noms sont inconnus.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaPosition, classe**](cmediaposition.md)
</dt> </dl>

 

 




