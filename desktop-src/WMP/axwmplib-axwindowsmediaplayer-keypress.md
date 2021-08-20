---
title: Événement KeyPress de l’objet AxWindowsMediaPlayer
description: L’événement KeyPress se produit lorsqu’une touche est enfoncée et libérée. | Événement KeyPress de l’objet AxWindowsMediaPlayer
ms.assetid: 73ecd6f9-1b58-4e28-ad1b-2d930a235e1d
keywords:
- événement keypress de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- KeyPress Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45b8022feacda910b28d68636c1abdcb2f6c1c9d3c2e799f762f25f5060b2b82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618789"
---
# <a name="keypress-event-of-the-axwindowsmediaplayer-object"></a>Événement KeyPress de l’objet AxWindowsMediaPlayer

L’événement KeyPress se produit lorsqu’une touche est enfoncée et libérée.

``` syntax
[C#]
private void player_KeyPressEvent(
  object sender,
  _WMPOCXEvents_KeyPressEvent e
)

[Visual Basic]
Private Sub player_KeyPressEvent(  
  sender As Object,  
  e As _WMPOCXEvents_KeyPressEvent
) Handles player.KeyPressEvent
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEvent**, qui contient la propriété suivante associée à cet événement.



| Propriété      | Description                                                                        |
|---------------|------------------------------------------------------------------------------------|
| **nKeyAscii** | System. Int16Specifies Code ANSI numérique standard pour le caractère.<br/> |



 

## <a name="remarks"></a>Remarques

Cet événement se produit lorsque la séquence de touches génère un caractère imprimable du clavier, la touche CTRL combinée à un caractère de l’alphabet standard ou l’un des quelques caractères spéciaux, et la touche entrée ou retour arrière.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





