---
title: IWMPPlaylist (VB et C), interface (Wmp.h)
description: Fournit des propriétés et des méthodes pour organiser, gérer et manipuler des éléments multimédias dans une sélection. L’interface IWMPPlaylist expose les propriétés suivantes.
ms.assetid: c3f4f9dd-eb5f-493a-b8d0-22e70c63a2d1
keywords:
- interface IWMPPlaylist (VB et C) Lecteur Windows Media
- Lecteur Windows Media de l’interface IWMPPlaylist (VB et C), description
topic_type:
- apiref
api_name:
- IWMPPlaylist (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3fc1d8be09596d89dd87748811846d6dee1e8af8f28bebec56fa852c42ed6bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119001"
---
# <a name="iwmpplaylist-vb-and-c-interface"></a>interface IWMPPlaylist (VB et C#)

Fournit des propriétés et des méthodes pour organiser, gérer et manipuler des éléments multimédias dans une sélection.

L’interface **IWMPPlaylist** expose les propriétés suivantes.

## <a name="members"></a>Membres

l’interface **IWMPPlaylist (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

l’interface **IWMPPlaylist (VB et C#)** possède ces méthodes.



| Méthode                                                                       | Description                                                             |
|:-----------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**appendItem**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)   | Ajoute un élément multimédia à la fin de la sélection.<br/>                |
| [**effacé**](iwmpplaylist-iwmpplaylist-clear--vb-and-c.md)                   | Réservé pour un usage futur.<br/>                                     |
| [**getItemInfo**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) | Retourne la valeur d’un attribut playlist spécifié par Name.<br/> |
| [**insertItem**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)   | Insère un élément multimédia à un emplacement spécifié dans une sélection.<br/>  |
| [**moveItem**](wmplibiwmpplaylist-iwmpplaylist-moveitem--vb-and-c.md)       | Modifie l’emplacement d’un élément multimédia dans la sélection.<br/>        |
| [**removeItem**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)   | Supprime l’élément multimédia spécifié de la sélection.<br/>          |
| [**setItemInfo**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md) | Définit la valeur d’un attribut playlist.<br/>                      |



 

### <a name="properties"></a>Propriétés

l’interface **IWMPPlaylist (VB et C#)** a ces propriétés.



| Propriété                                                                                      | Type d’accès           | Description                                                                                                                                         |
|:----------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attributeCount**](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)<br/> | Lecture seule<br/>  | Obtient le nombre d’attributs associés à une sélection.<br/>                                                                                |
| [**attributeName**](iwmpplaylist-attributename--vb-and-c.md)<br/>                      | Lecture seule<br/>  | Obtient le nom d’un attribut de sélection spécifié par un index. En C#, il s’agit de la méthode d’extraction de \_ AttributeName.<br/>                               |
| [**saut**](wmplibiwmpplaylist-iwmpplaylist-count--vb-and-c.md)<br/>                   | Lecture seule<br/>  | Obtient le nombre d’éléments multimédias dans une sélection.<br/>                                                                                            |
| [**isIdentical**](iwmpplaylist-isidentical--vb-and-c.md)<br/>                          | Lecture seule<br/>  | Obtient une valeur indiquant si la sélection spécifiée est identique à la sélection actuelle. En C#, il s’agit de la \_ méthode isIdentical.<br/> |
| [**Élément**](iwmpplaylist-item--vb-and-c.md)<br/>                                        | Lecture seule<br/>  | Obtient une interface pour l’élément multimédia à l’index spécifié. En C#, il s’agit de la méthode d’extraction d' \_ élément.<br/>                                         |
| [**nomme**](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)<br/>                     | Lecture/écriture<br/> | Obtient ou définit le nom de la sélection.<br/>                                                                                                   |



 

Procurez-vous une interface **IWMPPlaylist** en utilisant les propriétés ou méthodes suivantes accessibles via l’objet ou l’interface suivant.



| Objet ou interface                                                | Propriété ou méthode                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMPCdrom**](iwmpcdrom--vb-and-c.md)                           | [**Sélection**](wmplibiwmpcdrom-iwmpcdrom-playlist--vb-and-c.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**IWMPMediaCollection**](iwmpmediacollection--vb-and-c.md)       | [**GetAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md), [**getByAlbum**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum), [**getByAttribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md), [**getByAuthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md), [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md), [**GetByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md) |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md)  | [**currentPlaylist**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md), [ **newPlaylist**](axwmplib-axwindowsmediaplayer-newplaylist.md)                                                                                                                                                                                                                                                                                                                                                                   |
| [**IWMPPlaylistArray**](iwmpplaylistarray--vb-and-c.md)           | [**Élément**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistarray-item)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**IWMPPlaylistCollection**](iwmpplaylistcollection--vb-and-c.md) | [**newPlaylist**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-newplaylist)                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .net et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





