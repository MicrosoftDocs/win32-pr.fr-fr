---
description: 'Cartes une seule fonction membre et un ensemble facultatif de paramètres à un jeu correspondant d’identificateurs de dispatch entier (dispid), qui peuvent être utilisés lors des appels suivants à la fonction membre CMediaControl :: Invoke.'
ms.assetid: 9ce1b1aa-ea03-4a65-bff7-e46771cd0772
title: CMediaControl. GetIDsOfNames, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d328a4311746f6fdab9cf7eaa3376c7ba49c2b13b9db1d3aaac19142d2d583d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055171"
---
# <a name="cmediacontrolgetidsofnames-method"></a>CMediaControl. GetIDsOfNames, méthode

Cartes une seule fonction membre et un ensemble facultatif de paramètres à un jeu correspondant d’identificateurs de dispatch entier (dispid), qui peuvent être utilisés lors des appels suivants à la fonction membre [**CMediaControl :: Invoke**](cmediacontrol-invoke.md) .

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
| <dl> <dt>**\_OK**</dt> </dl>                   | Réussite.<br/>                                                                                                                                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaControl, classe**](cmediacontrol.md)
</dt> </dl>

 

 




