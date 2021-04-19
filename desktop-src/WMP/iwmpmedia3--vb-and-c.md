---
title: Interface IWMPMedia3 (VB et C) (WMP. h)
description: Fournit des méthodes supplémentaires pour accéder aux propriétés d’un élément multimédia.
ms.assetid: e16aa5e2-ae44-41c2-8c61-fb688c2e89e2
keywords:
- IWMPMedia3 (VB et C) interface Windows Media Player
- Interface IWMPMedia3 (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPMedia3 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb5438ad4d80031d5b45c738c6b6cc9335018af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527989"
---
# <a name="iwmpmedia3-vb-and-c-interface"></a>Interface IWMPMedia3 (VB et C#)

Fournit des méthodes supplémentaires pour accéder aux propriétés d’un élément multimédia.

## <a name="members"></a>Membres

L’interface **IWMPMedia3 (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWMPMedia3 (VB et C#)** possède ces méthodes.



| Méthode                                                                                           | Description                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**getAttributeCountByType**](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md) | Retourne le nombre d’attributs associés au type d’attribut spécifié.<br/>              |
| [**getItemInfoByType**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)             | Retourne la valeur de l’attribut correspondant au type d’attribut et à l’index spécifiés.<br/> |



 

Obtient une interface **IWMPMedia3** en effectuant un cast de la valeur retournée par l’une des propriétés ou méthodes suivantes accessibles par le biais de l’objet ou de l’interface suivant.



| Objet ou interface                                               | Propriété ou méthode                                                                                                                |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [IWMPControls](iwmpcontrols--vb-and-c.md)                        | [currentItem](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                          |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md) |
| [IWMPPlaylist](iwmpplaylist--vb-and-c.md)                        | [Item](iwmpplaylist-item--vb-and-c.md) ( **recevoir un \_ élément** en C#)                                                                   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .NET et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia2 (VB et C#)**](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





