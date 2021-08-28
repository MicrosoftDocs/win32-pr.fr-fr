---
title: IWMPControls. isAvailable (VB et C)
description: La propriété isAvailable (la \_ méthode obtenir IsAvailable dans C \) obtient une valeur indiquant si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée.
ms.assetid: 00812d5c-513e-49d5-93ba-750b81a852dd
keywords:
- IWMPControls. isAvailable (VB et C) Lecteur Windows Media
topic_type:
- apiref
api_name:
- IWMPControls.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73562fb4f96731216c30ada33db8e13d1468b31fb6fcefe7eedef6dd7892348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054847"
---
# <a name="iwmpcontrolsisavailable-vb-and-c"></a>IWMPControls. isAvailable (VB et C#)

La propriété **isAvailable** (la méthode **obtenir \_ isAvailable** en C#) obtient une valeur indiquant si un type d’informations spécifié est disponible ou si une action spécifiée peut être exécutée.


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
bool get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a>Paramètres

*bstrItem*

System. String qui est l’une des valeurs suivantes.



| Valeur           | Description                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| currentItem     | Découvre si l’utilisateur peut définir la propriété **IWMPControls. CurrentItem** .                                                                                     |
| currentMarker   | Découvre si l’utilisateur peut effectuer une recherche sur un marqueur spécifique.                                                                                                         |
| currentPosition | Découvre si l’utilisateur peut rechercher une position spécifique dans le fichier. Certains fichiers ne prennent pas en charge la recherche.                                                        |
| fastForward     | Détecte si le fichier prend en charge le transfert rapide et si cette fonctionnalité peut être appelée. De nombreux types de fichiers (et flux en direct) ne prennent pas en charge fastForward. |
| fastReverse     | Détecte si le fichier prend en charge fastReverse et si cette fonctionnalité peut être appelée. De nombreux types de fichiers (et flux en direct) ne prennent pas en charge fastReverse.     |
| Suivant            | Détecte si l’utilisateur peut Rechercher l’entrée suivante dans une sélection.                                                                                              |
| pause           | Détecte si la méthode **IWMPControls. pause** est disponible.                                                                                                 |
| répétition            | Détecte si la méthode **IWMPControls. Play** est disponible.                                                                                                  |
| previous        | Détecte si l’utilisateur peut Rechercher l’entrée précédente dans une sélection.                                                                                          |
| étape            | Détecte si la méthode **IWMPControls2. Step** est disponible pendant la lecture.                                                                                 |
| stop            | Détecte si la méthode **IWMPControls. Stop** est disponible.                                                                                                  |



 

## <a name="property-value"></a>Valeur de propriété

**System.Boolean**

**System. Boolean** qui indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée.

## <a name="remarks"></a>Remarques

**IWMPControls. isAvailable** est une propriété dans Visual Basic qui accepte un paramètre. En C#, on parle de la méthode **IWMPControls. obten \_ isAvailable** .

## <a name="examples"></a>Exemples

L’exemple suivant utilise la propriété **isAvailable** (méthode d’extraction de l’élément **\_ IsAvailable** en C#) pour vérifier que l’élément multimédia en cours prend en charge la propriété **CurrentPosition** . L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// If the currentPosition property is supported, seek to position 0.
if (player.Ctlcontrols.get_isAvailable("currentPosition"))
{
    player.Ctlcontrols.currentPosition = 0;
}
```


```VB

' If the currentPosition property is supported, seek to position 0.
If (player.Ctlcontrols.isAvailable(&quot;currentPosition&quot;)) Then

    player.Ctlcontrols.currentPosition = 0

End If
```





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPControls (VB et C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls. currentItem (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**IWMPControls. pause (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[**IWMPControls. play (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls. stop (VB et C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPControls2. step (VB et C#)**](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md)
</dt> </dl>

 

 





