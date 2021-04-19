---
description: Méthode de constructeur.
ms.assetid: 20c3c4af-b22f-4b74-a6b6-5ee309de4eef
title: Constructeur CBaseObject. CBaseObject (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b13fe906af1900dbf067e8aa9273d811b3c1ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545348"
---
# <a name="cbaseobjectcbaseobject-constructor"></a>Constructeur CBaseObject. CBaseObject

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pName* 
</dt> <dd>

Chaîne qui contient le nom de l’objet, à des fins de débogage.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette méthode incrémente le nombre d’objets actifs. (Voir [**CBaseObject :: ObjectsActive**](cbaseobject-objectsactive.md).)

Allouez le paramètre *pname* dans la mémoire statique :


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



La macro de [**nom**](name.md) compile en **valeur null** dans les versions commerciales, afin que les chaînes statiques apparaissent uniquement dans les versions Debug. Pour plus d’informations, consultez [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>ComBase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseObject, classe**](cbaseobject.md)
</dt> </dl>

 

 




