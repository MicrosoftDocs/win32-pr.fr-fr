---
title: interface IWMPMediaCollection (VB et C) (Wmp. h)
description: Fournit des méthodes qui peuvent être utilisées pour organiser une grande collection d’éléments multimédias.
ms.assetid: a9e3d466-7dcf-4f1b-ba6f-9d166a35f03d
keywords:
- interface IWMPMediaCollection (VB et C) Lecteur Windows Media
- Lecteur Windows Media de l’interface IWMPMediaCollection (VB et C), description
topic_type:
- apiref
api_name:
- IWMPMediaCollection (VB and C )
- IWMPMediaCollection (VB and C ).isDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce15616b2059802610360b52d5af9bfa8d56b56b7ed06129bb849de567e22e26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468449"
---
# <a name="iwmpmediacollection-vb-and-c-interface"></a>interface IWMPMediaCollection (VB et C#)

Fournit des méthodes qui peuvent être utilisées pour organiser une grande collection d’éléments multimédias.

## <a name="members"></a>Membres

l’interface **IWMPMediaCollection (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

l’interface **IWMPMediaCollection (VB et C#)** possède ces méthodes.



| Méthode                                                                                                                       | Description                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**add**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)                                                   | Ajoute un nouvel élément multimédia ou une nouvelle sélection à la bibliothèque.<br/>                                                                                  |
| [**getAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md)                                             | Retourne une interface **IWMPPlaylist** qui correspond à la sélection qui contient tous les éléments multimédias de la bibliothèque.<br/>               |
| [**getAttributeStringCollection**](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md) | Retourne une interface **IWMPStringCollection** qui représente le jeu de toutes les valeurs pour un attribut spécifié dans un type de média.<br/> |
| [**getByAlbum**](wmplibiwmpmediacollection-iwmpmediacollection-getbyalbum--vb-and-c.md)                                     | Retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias à partir de l’album spécifié.<br/>                                |
| [**getByAttribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md)                             | Retourne une interface **IWMPPlaylist** qui correspond à l’attribut spécifié ayant la valeur spécifiée.<br/>                      |
| [**getByAuthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md)                                   | Retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias par l’auteur spécifié.<br/>                             |
| [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md)                                     | Retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias du genre spécifié.<br/>                                  |
| [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)                                       | Retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias avec le nom spécifié.<br/>                                 |
| [**getMediaAtom**](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)                                 | Retourne l’index d’un attribut spécifié.<br/>                                                                                        |
| **isDeleted**                                                                                                                | N'est plus pris en charge.<br/>                                                                                                               |
| [**Installez**](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)                                             | Supprime l’élément multimédia spécifié de la collection de supports.<br/>                                                                        |
| [**setDeleted**](wmplibiwmpmediacollection-iwmpmediacollection-setdeleted--vb-and-c.md)                                     | Déplace l’élément multimédia spécifié vers le dossier éléments supprimés.<br/>                                                                        |



 

Procurez-vous une interface **IWMPMediaCollection** en utilisant les propriétés suivantes accessibles via l’objet ou l’interface suivant.



| Objet ou interface                                               | Propriété                                                                           |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**mediaCollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) |
| [**IWMPLibrary**](iwmplibrary--vb-and-c.md)                      | [**mediaCollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .net et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPMediaCollection2**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interface IWMPStringCollection (VB et C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





