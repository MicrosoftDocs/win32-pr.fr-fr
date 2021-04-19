---
title: Événement CurrentMediaItemAvailable de l’objet AxWindowsMediaPlayer
description: L’événement CurrentMediaItemAvailable se produit lorsqu’un élément de métadonnées graphiques de l’élément multimédia actuel devient disponible. | Événement CurrentMediaItemAvailable de l’objet AxWindowsMediaPlayer
ms.assetid: 7db62e6a-5f20-441a-801f-147ac386c5f8
keywords:
- Événement CurrentMediaItemAvailable de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547622424194e63733cec6166d813d42ebf577ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535347"
---
# <a name="currentmediaitemavailable-event-of-the-axwindowsmediaplayer-object"></a>Événement CurrentMediaItemAvailable de l’objet AxWindowsMediaPlayer

L’événement CurrentMediaItemAvailable se produit lorsqu’un élément de métadonnées graphiques de l’élément multimédia actuel devient disponible.

``` syntax
[C#]
private void player_CurrentMediaItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentMediaItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentMediaItemAvailable(
  sender As Object,  
  e As _WMPOCXEvents_CurrentMediaItemAvailableEvent
) Handles player.CurrentMediaItemAvailable
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEvent**, qui contient la propriété suivante associée à cet événement.



| Propriété     | Description                                                 |
|--------------|-------------------------------------------------------------|
| bstrItemName | Nom System. StringThe de l’élément multimédia actuel.<br/> |



 

## <a name="remarks"></a>Notes

Dans la mesure où la lecture peut commencer avant le téléchargement complet d’un élément multimédia, les graphiques de métadonnées contenus dans l’élément multimédia (par exemple, les jaquettes de la couverture de l’album) peuvent ne pas être disponibles au début de la lecture. Cet événement vous avertit à la fin du téléchargement d’un élément de graphique de métadonnées. Vous pouvez ensuite récupérer l’interface **IWMPMedia** en passant la valeur de **bstrItemName** au *IWMPMediaCollection*. méthode **GetByName** , après laquelle vous pouvez accéder à l’élément de graphique de métadonnées à l’aide de *IWMPMedia3*. **getItemInfoByType** et en spécifiant **WM/image** comme nom d’attribut.

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

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB et C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection. getByName (VB et C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





