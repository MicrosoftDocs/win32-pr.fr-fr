---
title: Événement MediaCollectionAttributeStringChanged de l’objet AxWindowsMediaPlayer
description: L’événement MediaCollectionAttributeStringChanged se produit lorsqu’une valeur d’attribut de la bibliothèque est modifiée. | Événement MediaCollectionAttributeStringChanged de l’objet AxWindowsMediaPlayer
ms.assetid: f5b91399-42b7-4202-9b65-caa9b15847b9
keywords:
- Événement MediaCollectionAttributeStringChanged de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringChanged Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b83d8036ca0dca7f79e2a9ba721830447f9c5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526831"
---
# <a name="mediacollectionattributestringchanged-event-of-the-axwindowsmediaplayer-object"></a>Événement MediaCollectionAttributeStringChanged de l’objet AxWindowsMediaPlayer

L’événement MediaCollectionAttributeStringChanged se produit lorsqu’une valeur d’attribut de la bibliothèque est modifiée.

``` syntax
[C#]
private void player_MediaCollectionAttributeStringChanged(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringChanged(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent
) Handles player.MediaCollectionAttributeStringChanged
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringChangedEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringChangedEvent**, qui contient les propriétés suivantes relatives à cet événement.



| Propriété         | Description                                                                                                                                                                                  |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| bstrAttribName   | System. StringSpecifies nom de l’attribut. Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md).<br/> |
| bstrOldAttribVal | System. StringSpecifies l’ancienne valeur de l’attribut.<br/>                                                                                                                            |
| bstrNewAttribVal | System. StringSpecifies nouvelle valeur de l’attribut.<br/>                                                                                                                            |



 

## <a name="remarks"></a>Notes

Quand un utilisateur modifie des métadonnées de bibliothèque, la collection de supports est mise à jour et cet événement se déclenche pour chaque attribut modifié.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. mediaCollection (VB et C#)**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMediaCollection (VB et C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





