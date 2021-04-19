---
title: IWMPDVD. isAvailable (VB et C)
description: La propriété isAvailable (la \_ méthode obtenir IsAvailable dans C \) obtient une valeur qui indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée.
ms.assetid: 55690783-df2f-473d-a6f2-a4907b7e8a78
keywords:
- Lecteur Windows Media IWMPDVD. isAvailable (VB et C)
topic_type:
- apiref
api_name:
- IWMPDVD.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e3409da619f337b61606baaf546cebbb438087c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531021"
---
# <a name="iwmpdvdisavailable-vb-and-c"></a>IWMPDVD. isAvailable (VB et C#)

La propriété **isAvailable** (la méthode **obtenir \_ isAvailable** en C#) obtient une valeur qui indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée.


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
)
```



## <a name="parameters"></a>Paramètres

*bstrItem*

System. String qui est l’une des valeurs suivantes.



| Valeur      | Description                                                                                   |
|------------|-----------------------------------------------------------------------------------------------|
| Retour       | Détecte si la méthode **IWMPDVD. Back** est disponible.                                   |
| DVD        | Détecte si le DVD est chargé.                                                          |
| dvdDecoder | Détecte si le décodeur DVD est installé sur le système.                                     |
| resume     | Détecte si la méthode **IWMPDVD. Resume** est disponible.                                 |
| titleMenu  | Détecte si la méthode **IWMPDVD. titleMenu** est disponible.                              |
| Menu de la    | Détecte si la méthode de **menu IWMPDVD.** est disponible. Communément appelé menu racine. |



 

## <a name="property-value"></a>Valeur de propriété

**System.Boolean**

**System. Boolean** qui indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée.

## <a name="remarks"></a>Notes

Les fonctionnalités DVD du lecteur Windows Media ne fonctionneront pas sur les ordinateurs sur lesquels aucun décodeur de DVD n’est installé. Vous pouvez déterminer si un décodeur est disponible en appelant la propriété **isAvailable** (la méthode « **obtenir \_ IsAvailable** » en C#) et en passant la valeur **System. String** « dvdDecoder ».

Chaque DVD est créé différemment. Les méthodes disponibles pendant la lecture et la navigation sur DVD dépendent de la façon dont le DVD est créé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPDVD (VB et C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. Back (VB et C#)**](wmplibiwmpdvd-iwmpdvd-back--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. Resume (VB et C#)**](wmplibiwmpdvd-iwmpdvd-resume--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. titleMenu (VB et C#)**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> <dt>

[**Menu IWMPDVD. (VB et C#)**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





