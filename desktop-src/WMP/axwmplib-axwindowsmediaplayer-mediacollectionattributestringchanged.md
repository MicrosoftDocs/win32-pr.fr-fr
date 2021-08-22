---
title: Événement MediaCollectionAttributeStringChanged de l’objet AxWindowsMediaPlayer
description: L’événement MediaCollectionAttributeStringChanged se produit lorsqu’une valeur d’attribut de la bibliothèque est modifiée. | Événement MediaCollectionAttributeStringChanged de l’objet AxWindowsMediaPlayer
ms.assetid: f5b91399-42b7-4202-9b65-caa9b15847b9
keywords:
- événement MediaCollectionAttributeStringChanged de l’objet AxWindowsMediaPlayer Lecteur Windows Media
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
ms.openlocfilehash: 5dcc755d1a183525923b91ce2de7937860582c3cf795d13cbf4a8c22d7c9c37f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618779"
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
| bstrAttribName   | System. StringSpecifies nom de l’attribut. pour plus d’informations sur les attributs pris en charge par Lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md).<br/> |
| bstrOldAttribVal | System. StringSpecifies l’ancienne valeur de l’attribut.<br/>                                                                                                                            |
| bstrNewAttribVal | System. StringSpecifies nouvelle valeur de l’attribut.<br/>                                                                                                                            |



 

## <a name="remarks"></a>Remarques

Quand un utilisateur modifie des métadonnées de bibliothèque, la collection de supports est mise à jour et cet événement se déclenche pour chaque attribut modifié.

## <a name="requirements"></a>Configuration requise



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

 

 





