---
title: interface IWMPControls (VB et C) (Wmp. h)
description: fournit un moyen de manipuler la lecture d’un élément multimédia en représentant les contrôles de transport de Lecteur Windows Media, tels que lecture, arrêt et Pause. l’interface IWMPControls expose les propriétés suivantes.
ms.assetid: 46603d98-c7dd-4c20-a4ae-1472b3af8d52
keywords:
- interface IWMPControls (VB et C) Lecteur Windows Media
- Lecteur Windows Media de l’interface IWMPControls (VB et C), description
topic_type:
- apiref
api_name:
- IWMPControls (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b96f79b8942935d9722bf38dbd1ae946b03d16496664b4c069552819785c1f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119308"
---
# <a name="iwmpcontrols-vb-and-c-interface"></a>interface IWMPControls (VB et C#)

fournit un moyen de manipuler la lecture d’un élément multimédia en représentant les contrôles de transport de Lecteur Windows Media, tels que lecture, arrêt et Pause.

L’interface **IWMPControls** expose les propriétés suivantes.

## <a name="members"></a>Membres

l’interface **IWMPControls (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

l’interface **IWMPControls (VB et C#)** possède ces méthodes.



| Méthode                                                                       | Description                                                                                 |
|:-----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**fastForward**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md) | Démarre la lecture rapide de l’élément multimédia dans le sens avant.<br/>                     |
| [**fastReverse**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md) | Démarre la lecture rapide de l’élément multimédia dans le sens inverse.<br/>                     |
| [**Situé**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)               | Définit l’élément suivant dans la sélection en tant qu’élément actuel.<br/>                          |
| [**suspen**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)             | Suspend la lecture de l’élément multimédia.<br/>                                               |
| [**répétition**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)               | Commence la lecture de l’élément multimédia en cours ou reprend la lecture d’un élément suspendu.<br/> |
| [**playItem**](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)       | Lit l’élément multimédia spécifié.<br/>                                                  |
| [**premier**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)       | Définit l’élément précédent dans la sélection en tant qu’élément actuel.<br/>                      |
| [**erreur**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)               | Arrête la lecture de l’élément multimédia.<br/>                                                |



 

### <a name="properties"></a>Propriétés

l’interface **IWMPControls (VB et C#)** a ces propriétés.



| Propriété                                                                                                    | Type d’accès           | Description                                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**currentItem**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)<br/>                     | Lecture/écriture<br/> | Obtient ou définit l’élément multimédia actuel dans une sélection.<br/>                                                                                                                    |
| [**currentMarker**](wmplibiwmpcontrols-iwmpcontrols-currentmarker--vb-and-c.md)<br/>                 | Lecture/écriture<br/> | Obtient ou définit le numéro de marqueur actuel.<br/>                                                                                                                               |
| [**currentPosition**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)<br/>             | Lecture/écriture<br/> | Obtient ou définit la position actuelle dans l’élément multimédia, en secondes, à partir du début.<br/>                                                                                    |
| [**currentPositionString**](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)<br/> | Lecture seule<br/>  | Obtient la position actuelle dans l’élément multimédia en tant que **System. String**.<br/>                                                                                                   |
| [**isAvailable**](iwmpcontrols-isavailable--vb-and-c.md)<br/>                                        | Lecture seule<br/>  | Obtient une valeur indiquant si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée. En C#, il s’agit de la méthode d' **extraction de \_ isAvailable** .<br/> |



 

Procurez-vous une interface **IWMPControls** à l’aide de la propriété suivante.



| Object                                                                   | Propriété                                                                   |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Objet AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .net et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPControls2 (VB et C#)**](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[**Interface IWMPControls3 (VB et C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





