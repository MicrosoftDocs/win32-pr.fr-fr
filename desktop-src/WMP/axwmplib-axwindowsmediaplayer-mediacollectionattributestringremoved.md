---
title: Événement MediaCollectionAttributeStringRemoved de l’objet AxWindowsMediaPlayer
description: L’événement MediaCollectionAttributeStringRemoved se produit lorsqu’une valeur d’attribut est supprimée de la bibliothèque. | Événement MediaCollectionAttributeStringRemoved de l’objet AxWindowsMediaPlayer
ms.assetid: 2f264416-0bc5-41d0-8863-32c284393082
keywords:
- événement MediaCollectionAttributeStringRemoved de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11b6b028a2a47585b06159ed46b986124583950
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855975"
---
# <a name="mediacollectionattributestringremoved-event-of-the-axwindowsmediaplayer-object"></a>Événement MediaCollectionAttributeStringRemoved de l’objet AxWindowsMediaPlayer

L’événement MediaCollectionAttributeStringRemoved se produit lorsqu’une valeur d’attribut est supprimée de la bibliothèque.

``` syntax
[C#]
private void player_MediaCollectionAttributeStringRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent
) Handles player.MediaCollectionAttributeStringRemoved
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEvent**, qui contient les propriétés suivantes relatives à cet événement.



| Propriété           | Description                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bstrAttribName** | System. StringSpecifies nom de l’attribut. pour plus d’informations sur les attributs pris en charge par Lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md).<br/> |
| bstrAttribVal      | System. StringSpecifies valeur de l’attribut.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Notes

Lorsqu’un élément multimédia est supprimé de la bibliothèque, ses métadonnées sont supprimées du **MediaCollection** et cet événement est déclenché pour chaque attribut supprimé.

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

 

 





