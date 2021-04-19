---
title: Interface IWMPMedia2 (VB et C) (WMP. h)
description: Fournit l’accès à une propriété d’élément multimédia supplémentaire.
ms.assetid: 7d9f8304-ae26-4175-b9d4-9f272861ef87
keywords:
- IWMPMedia2 (VB et C) interface Windows Media Player
- Interface IWMPMedia2 (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPMedia2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1a77322e0e6649d9a286c920ccd9ddc77890f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525343"
---
# <a name="iwmpmedia2-vb-and-c-interface"></a>Interface IWMPMedia2 (VB et C#)

Fournit l’accès à une propriété d’élément multimédia supplémentaire.

En plus des propriétés et des méthodes héritées de **IWMPMedia**, l’interface **IWMPMedia2** expose la propriété suivante.



| Propriété                                                 | Description                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------|
| [Error](wmplibiwmpmedia2-iwmpmedia2-error--vb-and-c.md) | Obtient une interface **IWMPErrorItem** si l’élément multimédia a une condition d’erreur. |



 

Obtient une interface **IWMPMedia2** en effectuant un cast de la valeur retournée par l’une des propriétés ou méthodes suivantes accessibles par le biais de l’objet ou de l’interface suivant.



| Objet ou interface                                               | Propriété ou méthode                                                                                                                |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [IWMPControls](iwmpcontrols--vb-and-c.md)                        | [currentItem](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                          |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md) |
| [IWMPPlaylist](iwmpplaylist--vb-and-c.md)                        | [Item](iwmpplaylist-item--vb-and-c.md) ( **recevoir un \_ élément** en C#)                                                                   |



 

## <a name="members"></a>Membres

L’interface **IWMPMedia2 (VB et C#)** ne définit aucun membre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .NET et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPErrorItem (VB et C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia3 (VB et C#)**](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





