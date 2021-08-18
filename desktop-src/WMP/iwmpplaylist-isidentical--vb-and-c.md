---
title: IWMPPlaylist. isIdentical (VB et C)
description: La propriété isIdentical (méthode obtenir \_ isIdentical dans C \) obtient une valeur indiquant si la sélection spécifiée est identique à la sélection actuelle.
ms.assetid: 0e5520ee-3d41-4e36-98f4-7bc2ec45fcb8
keywords:
- IWMPPlaylist. isIdentical (VB et C) Lecteur Windows Media
topic_type:
- apiref
api_name:
- IWMPPlaylist.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca62b1667250b049cf47e797d59bdddea0444c6ea8803ca0fc8daf526289eb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119006"
---
# <a name="iwmpplaylistisidentical-vb-and-c"></a>IWMPPlaylist. isIdentical (VB et C#)

La propriété **isIdentical** (méthode **obtenir \_ isIdentical** en C#) obtient une valeur indiquant si la sélection spécifiée est identique à la sélection actuelle.


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPPlaylist As IWMPPlaylist
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPPlaylist pIWMPPlaylist
);
```



## <a name="parameters"></a>Paramètres

*pIWMPPlaylist*

Interface **wmplib. IWMPPlaylist** pour la sélection que cette méthode compare à la sélection actuelle.

## <a name="property-value"></a>Valeur de propriété

**System. Boolean** qui indique si les sélections comparées sont identiques.

## <a name="remarks"></a>Remarques

**IWMPPlaylist. isIdentical** est une propriété de Visual Basic qui accepte un paramètre, tandis que en C#, elle est appelée méthode **IWMPPlaylist. obtenir \_ isIdentical** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





