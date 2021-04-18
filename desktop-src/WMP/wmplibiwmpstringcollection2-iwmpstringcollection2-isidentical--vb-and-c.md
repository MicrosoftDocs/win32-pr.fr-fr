---
title: Méthode IWMPStringCollection2 isIdentical
description: La méthode isIdentical retourne une valeur indiquant si l’objet représenté par l’interface fournie est le même que celui en cours.
ms.assetid: 826e7fd8-88f8-4a2a-9ca0-82a500099272
keywords:
- méthode isIdentical lecteur Windows Media
- méthode isIdentical lecteur Windows Media, interface IWMPStringCollection2
- Interface IWMPStringCollection2 lecteur Windows Media, méthode isIdentical
topic_type:
- apiref
api_name:
- IWMPStringCollection2.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb760dae213f28d44fbc707b4430cb151cfe578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533423"
---
# <a name="iwmpstringcollection2isidentical-method"></a>IWMPStringCollection2 :: isIdentical, méthode

La méthode **isIdentical** retourne une valeur indiquant si l’objet représenté par l’interface fournie est le même que celui en cours.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Boolean isIdentical(
  IWMPStringCollection2 pIWMPStringCollection2
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPStringCollection2 As IWMPStringCollection2 _
) As System.Boolean
Implements IWMPStringCollection2.isIdentical
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*pIWMPStringCollection2* \[ dans\]
</dt> <dd>

Interface **wmplib. IWMPStringCollection2** qui représente l’objet à comparer avec l’objet actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**System. Boolean** qui est le résultat de la comparaison. La valeur **true** indique que les objets de collection de chaînes sont identiques.

## <a name="remarks"></a>Notes

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11.<br/>                                                                                    |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPStringCollection2 (VB et C#)**](iwmpstringcollection2--vb-and-c.md)
</dt> </dl>

 

 





