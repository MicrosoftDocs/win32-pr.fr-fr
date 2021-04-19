---
description: 'Mappe une fonction membre unique et un ensemble facultatif de paramètres à un jeu correspondant d’identificateurs de dispatch entier, qui peut être utilisé lors des appels suivants à la fonction membre CMediaEvent :: Invoke.'
ms.assetid: 04e607e6-0b68-4371-aacf-01af308a56a3
title: CMediaEvent. GetIDsOfNames, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 191fa85264e4e7e22aa67f409db20cebd68f4319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537860"
---
# <a name="cmediaeventgetidsofnames-method"></a>CMediaEvent. GetIDsOfNames, méthode

Mappe une fonction membre unique et un ensemble facultatif de paramètres à un jeu correspondant d’identificateurs de dispatch entier, qui peut être utilisé lors des appels suivants à la fonction membre [**CMediaEvent :: Invoke**](cmediaevent-invoke.md) .

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

Identificateur de référence. Réservé pour un usage futur. Doit avoir la **valeur null**.

</dd> <dt>

*rgszNames* 
</dt> <dd>

Adresse d’un pointeur vers un tableau de noms passé à mapper.

</dd> <dt>

*Enregistrements CNAME* 
</dt> <dd>

Compte des noms à mapper.

</dd> <dt>

*lcid* 
</dt> <dd>

Contexte des paramètres régionaux dans lequel interpréter les noms.

</dd> <dt>

*rgdispid* 
</dt> <dd>

Pointeur vers un tableau alloué par l’appelant, dont chaque élément contient un ID correspondant à l’un des noms transmis dans le tableau *rgszNames* . Le premier élément représente le nom du membre ; les éléments suivants représentent chacun des paramètres du membre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs suivantes.



| Code de retour                                                                                            | Description                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Impossible d’avoir un \_ \_ \_ CLSID inconnu**</dt> </dl> | Le CLSID n’a pas été reconnu.<br/>                                                                                                             |
| <dl> <dt>**\_UNKNOWNNAME DISP \_**</dt> </dl>    | Un ou plusieurs noms sont inconnus. Les DISPID retournés contiennent \_ un DISPID inconnu pour chaque entrée correspondant à un nom inconnu.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>          | Mémoire insuffisante.<br/>                                                                                                                            |
| <dl> <dt>**\_OK**</dt> </dl>                   | Opération réussie.<br/>                                                                                                                                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaEvent, classe**](cmediaevent.md)
</dt> </dl>

 

 




