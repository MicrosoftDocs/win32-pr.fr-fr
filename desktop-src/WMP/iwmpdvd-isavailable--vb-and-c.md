---
title: IWMPDVD. isAvailable (VB et C)
description: La propriété isAvailable (la \_ méthode obtenir IsAvailable dans C \) obtient une valeur qui indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée.
ms.assetid: 55690783-df2f-473d-a6f2-a4907b7e8a78
keywords:
- IWMPDVD. isAvailable (VB et C) Lecteur Windows Media
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
ms.openlocfilehash: c78c9dda7bff764752dc55524000ccd3695863afe69dcf45c2ed971c9c0373fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415915"
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

## <a name="remarks"></a>Remarques

les fonctionnalités de dvd de Lecteur Windows Media ne fonctionnent pas sur les ordinateurs sur lesquels aucun décodeur de DVD n’est installé. Vous pouvez déterminer si un décodeur est disponible en appelant la propriété **isAvailable** (la méthode « **obtenir \_ IsAvailable** » en C#) et en passant la valeur **System. String** « dvdDecoder ».

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

[**IWMPDVD. back (VB et C#)**](wmplibiwmpdvd-iwmpdvd-back--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. resume (VB et C#)**](wmplibiwmpdvd-iwmpdvd-resume--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. titleMenu (VB et C#)**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> <dt>

[**menu IWMPDVD. (VB et C#)**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





