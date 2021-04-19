---
description: La méthode GetIDsOfNames mappe un ensemble de noms à un ensemble correspondant de DISPID.
ms.assetid: 0c0a2726-e89a-4eaf-aab0-e7e9e82e3c34
title: CBaseDispatch. GetIDsOfNames, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf11e4aa298f924b69c299c2f411dde88e28e5b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520805"
---
# <a name="cbasedispatchgetidsofnames-method"></a>CBaseDispatch. GetIDsOfNames, méthode

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

Référence à un identificateur d’interface (IID) qui spécifie l’interface.

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

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                         | Description                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | Opération réussie.<br/>                                 |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>       | Mémoire insuffisante.<br/>                     |
| <dl> <dt>**\_UNKNOWNNAME DISP \_**</dt> </dl> | Un ou plusieurs noms sont inconnus.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode se comporte comme la méthode **IDispatch :: GetIDsOfNames** , mais le paramètre *riid* spécifie l’interface sur laquelle récupérer les DISPID. (Dans la version **IDispatch** , le paramètre *riid* est réservé.)

Si la méthode retourne DISP \_ E \_ UNKNOWNNAME, les DISPID retournés contiennent DISPID \_ Unknown pour chaque entrée correspondant à un nom inconnu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseDispatch, classe**](cbasedispatch.md)
</dt> </dl>

 

 




