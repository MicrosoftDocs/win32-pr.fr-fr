---
title: Interface IWMPLibrary (VB et C) (WMP. h)
description: Représente une bibliothèque. L’interface IWMPLibrary expose les propriétés suivantes.
ms.assetid: 956b2da1-5f01-48d6-8faa-e360c225afda
keywords:
- IWMPLibrary (VB et C) interface Windows Media Player
- Interface IWMPLibrary (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPLibrary (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9749d3a2363c3863180639f249d7261ec1b9694
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539984"
---
# <a name="iwmplibrary-vb-and-c-interface"></a>Interface IWMPLibrary (VB et C#)

Représente une bibliothèque.

L’interface **IWMPLibrary** expose les propriétés suivantes.

## <a name="members"></a>Membres

L’interface **IWMPLibrary (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IWMPLibrary (VB et C#)** possède ces méthodes.



| Méthode                                                                     | Description                                                                                           |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**isIdentical**](wmplibiwmplibrary-iwmplibrary-isidentical--vb-and-c.md) | Retourne une valeur qui indique si l’objet fourni est identique à l’objet actuel.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IWMPLibrary (VB et C#)** a ces propriétés.



| Propriété                                                                                      | Type d’accès          | Description                                                                   |
|:----------------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [**mediaCollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)<br/> | Lecture seule<br/> | Obtient une interface **IWMPMediaCollection** pour la bibliothèque actuelle.<br/> |
| [**nomme**](wmplibiwmplibrary-iwmplibrary-name--vb-and-c.md)<br/>                       | Lecture seule<br/> | Obtient le nom complet de la bibliothèque actuelle.<br/>                      |
| [**entrer**](wmplibiwmplibrary-iwmplibrary-type--vb-and-c.md)<br/>                       | Lecture seule<br/> | Obtient une valeur qui indique le type de bibliothèque.<br/>                      |



 

Procurez-vous une interface **IWMPLibrary** à l’aide de la méthode suivante.



| Object                                                   | Propriété                                                         |
|----------------------------------------------------------|------------------------------------------------------------------|
| [IWMPLibraryServices](iwmplibraryservices--vb-and-c.md) | [**getLibraryByType**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getlibrarybytype) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .NET et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPLibraryServices. getLibraryByType (VB et C#)**](wmplibiwmplibraryservices-iwmplibraryservices-getlibrarybytype--vb-and-c.md)
</dt> </dl>

 

 





