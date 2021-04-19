---
title: Interface IWMPMediaCollection2 (VB et C) (WMP. h)
description: Fournit des méthodes qui complètent l’interface IWMPMediaCollection.
ms.assetid: 204f336c-ea78-43d4-9686-bcab72362bc9
keywords:
- IWMPMediaCollection2 (VB et C) interface Windows Media Player
- Interface IWMPMediaCollection2 (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPMediaCollection2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58175e80fbf0f706a9ae6c6b3b69afbd26d52af3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533110"
---
# <a name="iwmpmediacollection2-vb-and-c-interface"></a>Interface IWMPMediaCollection2 (VB et C#)

Fournit des méthodes qui complètent l’interface **IWMPMediaCollection** .

## <a name="members"></a>Membres

L’interface **IWMPMediaCollection2 (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWMPMediaCollection2 (VB et C#)** possède ces méthodes.



| Méthode                                                                                                                     | Description                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**createQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)                               | Retourne une interface **IWMPQuery** qui représente une nouvelle requête.<br/>                                                                                               |
| [**getByAttributeAndMediaType**](wmplibiwmpmediacollection2-iwmpmediacollection2-getbyattributeandmediatype--vb-and-c.md) | Retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias qui ont un attribut et un type de média spécifiés.<br/>                                     |
| [**getPlaylistByQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)                 | Retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias qui correspondent aux conditions de requête.<br/>                                                    |
| [**getStringCollectionByQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md) | Retourne une interface **IWMPStringCollection** qui fournit l’accès à l’ensemble de toutes les valeurs de chaîne pour un attribut spécifié qui correspondent aux conditions de requête.<br/> |



 

Obtient une interface **IWMPMediaCollection2** en effectuant un cast de la valeur retournée par la propriété [**AxWindowsMediaPlayer. mediaCollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) ou de la valeur retournée par la propriété [**IWMPLibrary. mediaCollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .NET et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPMediaCollection (VB et C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





