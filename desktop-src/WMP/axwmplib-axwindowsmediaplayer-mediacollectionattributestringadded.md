---
title: Événement MediaCollectionAttributeStringAdded de l’objet AxWindowsMediaPlayer
description: L’événement MediaCollectionAttributeStringAdded se produit lorsqu’une valeur d’attribut est ajoutée à la bibliothèque. | Événement MediaCollectionAttributeStringAdded de l’objet AxWindowsMediaPlayer
ms.assetid: b14db0ce-bd78-4e28-a42c-1a231c29da2b
keywords:
- événement MediaCollectionAttributeStringAdded de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6712b6caa8f014ec75bf2b031e2d3f6db429dbd2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855981"
---
# <a name="mediacollectionattributestringadded-event-of-the-axwindowsmediaplayer-object"></a>Événement MediaCollectionAttributeStringAdded de l’objet AxWindowsMediaPlayer

L’événement MediaCollectionAttributeStringAdded se produit lorsqu’une valeur d’attribut est ajoutée à la bibliothèque.

``` syntax
[C#]
private void player_MediaCollectionAttributeStringAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent
) Handles player.MediaCollectionAttributeStringAdded
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringAddedEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringAddedEvent**, qui contient les propriétés suivantes relatives à cet événement.



| Propriété           | Description                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bstrAttribName** | System. StringSpecifies nom de l’attribut. pour plus d’informations sur les attributs pris en charge par Lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md).<br/> |
| bstrAttribVal      | System. StringSpecifies valeur de l’attribut.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Notes

Lorsqu’un élément multimédia est ajouté à la bibliothèque, ses métadonnées sont ajoutées à la collection de supports et cet événement est déclenché pour chaque attribut ajouté.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. mediaCollection (VB et C#)**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMediaCollection (VB et C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





