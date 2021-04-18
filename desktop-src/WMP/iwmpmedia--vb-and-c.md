---
title: Interface IWMPMedia (VB et C) (WMP. h)
description: Fournit un moyen de définir et de récupérer les propriétés d’un élément multimédia. L’interface IWMPMedia expose les propriétés suivantes.
ms.assetid: 4f67336e-d1d3-4f18-b063-086edf9d9094
keywords:
- IWMPMedia (VB et C) interface Windows Media Player
- Interface IWMPMedia (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPMedia (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c60a3396710ea4c426bd41c96db34e1e59cc690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540619"
---
# <a name="iwmpmedia-vb-and-c-interface"></a>Interface IWMPMedia (VB et C#)

Fournit un moyen de définir et de récupérer les propriétés d’un élément multimédia.

L’interface **IWMPMedia** expose les propriétés suivantes.

## <a name="members"></a>Membres

L’interface **IWMPMedia (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IWMPMedia (VB et C#)** possède ces méthodes.



| Méthode                                                                             | Description                                                                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**getAttributeName**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)   | Retourne le nom de l’attribut correspondant à l’index spécifié.<br/>                            |
| [**getItemInfo**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)             | Retourne la valeur de l’attribut spécifié pour l’élément multimédia.<br/>                                   |
| [**getItemInfoByAtom**](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md) | Retourne la valeur de l’attribut avec le numéro d’index spécifié.<br/>                                |
| [**getMarkerName**](wmplibiwmpmedia-iwmpmedia-getmarkername--vb-and-c.md)         | Retourne le nom du marqueur à l’index spécifié.<br/>                                             |
| [**getMarkerTime**](wmplibiwmpmedia-iwmpmedia-getmarkertime--vb-and-c.md)         | Retourne l’heure du marqueur au niveau de l’index spécifié.<br/>                                             |
| [**isMemberOf**](wmplibiwmpmedia-iwmpmedia-ismemberof--vb-and-c.md)               | Retourne une valeur indiquant si l’élément multimédia spécifié est membre de la sélection spécifiée.<br/> |
| [**isReadOnlyItem**](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)       | Retourne une valeur indiquant si les attributs de l’élément multimédia spécifié peuvent être modifiés.<br/>       |
| [**setItemInfo**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)             | Définit la valeur de l’attribut spécifié pour l’élément multimédia.<br/>                                      |



 

### <a name="properties"></a>Propriétés

L’interface **IWMPMedia (VB et C#)** a ces propriétés.



| Propriété                                                                                      | Type d’accès          | Description                                                                                                                                          |
|:----------------------------------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attributeCount**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)<br/>       | Lecture seule<br/> | Obtient le nombre d’attributs qui peuvent être interrogés et/ou définis pour l’élément multimédia.<br/>                                                          |
| [**Macauley**](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)<br/>                   | Lecture seule<br/> | Obtient la durée en secondes de l’élément multimédia actuel.<br/>                                                                                   |
| [**durationString**](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)<br/>       | Lecture seule<br/> | Obtient une valeur indiquant la durée de l’élément multimédia actuel au format HH : MM : SS.<br/>                                                        |
| [**imageSourceHeight**](wmplibiwmpmedia-iwmpmedia-imagesourceheight--vb-and-c.md)<br/> | Lecture seule<br/> | Obtient la hauteur, en pixels, de l’élément multimédia actuel.<br/>                                                                                      |
| [**imageSourceWidth**](wmplibiwmpmedia-iwmpmedia-imagesourcewidth--vb-and-c.md)<br/>   | Lecture seule<br/> | Obtient la largeur en pixels de l’élément multimédia actuel.<br/>                                                                                       |
| [**isIdentical**](iwmpmedia-isidentical--vb-and-c.md)<br/>                             | Lecture seule<br/> | Obtient une valeur indiquant si l’élément multimédia spécifié est le même que celui actuel. En C#, il s’agit de la méthode **\_ isIdentical** .<br/> |
| [**markerCount**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)<br/>             | Lecture seule<br/> | Obtient le nombre de marqueurs dans l’élément multimédia.<br/>                                                                                             |
| [**nomme**](wmplibiwmpmedia-iwmpmedia-name--vb-and-c.md)<br/>                           | Lecture seule<br/> | Obtient ou définit le nom de l’élément multimédia.<br/>                                                                                                  |
| [**sourceURL**](wmplibiwmpmedia-iwmpmedia-sourceurl--vb-and-c.md)<br/>                 | Lecture seule<br/> | Obtient l’URL de l’élément multimédia.<br/>                                                                                                           |



 

Procurez-vous une interface **IWMPMedia** en utilisant les propriétés ou méthodes suivantes accessibles via l’objet ou l’interface suivant.



| Objet ou interface                                               | Propriété ou méthode                                                                                                                       |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMPControls**](iwmpcontrols--vb-and-c.md)                    | [**CurrentItem**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                             |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md), [ **newMedia**](axwmplib-axwindowsmediaplayer-newmedia.md) |
| [**IWMPPlaylist**](iwmpplaylist--vb-and-c.md)                    | [**Item**](iwmpplaylist-item--vb-and-c.md) (recevoir un \_ élément en C#)                                                                           |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .NET et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPMedia2 (VB et C#)**](iwmpmedia2--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia3 (VB et C#)**](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





