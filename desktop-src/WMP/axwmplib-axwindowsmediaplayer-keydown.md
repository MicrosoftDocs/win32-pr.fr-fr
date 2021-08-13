---
title: Événement KeyOut de l’objet AxWindowsMediaPlayer
description: L’événement KeyOut se produit lorsqu’une touche est enfoncée. | Événement KeyOut de l’objet AxWindowsMediaPlayer
ms.assetid: e67b9628-6c53-4893-921a-9487ebfc1cd5
keywords:
- événement keyout de l’objet AxWindowsMediaPlayer Lecteur Windows Media
topic_type:
- apiref
api_name:
- KeyDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 054736007219021dbc0a4c1c968f61e1bbdb285fa416aae5f3c92c3880fb55de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469719"
---
# <a name="keydown-event-of-the-axwindowsmediaplayer-object"></a>Événement KeyOut de l’objet AxWindowsMediaPlayer

L’événement KeyOut se produit lorsqu’une touche est enfoncée.

``` syntax
[C#]
private void player_KeyDownEvent(
  object sender,
  _WMPOCXEvents_KeyDownEvent e
)

[Visual Basic]
Private Sub player_KeyDownEvent(  
  sender As Object, 
  e As _WMPOCXEvents_KeyDownEvent
) Handles player.KeyDownEvent
```

## <a name="event-data"></a>Données d'événements

Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ KeyDownEventHandler**. Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ KeyDownEvent**, qui contient les propriétés suivantes relatives à cet événement.



| Propriété    | Description                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nKeyCode    | System. Int16Specifies quelle touche physique est enfoncée. Pour connaître les valeurs possibles, consultez la section Notes.<br/>                                                                                                                                                                                                                                                                                    |
| nShiftState | Champ de bits System. Int16a avec les bits les moins significatifs correspondant à la touche Maj (bit 0), la touche CTRL (bit 1) et la touche ALT (bit 2). Ces bits correspondent respectivement aux valeurs 1, 2 et 4. L’argument Shift indique l’état de ces clés. Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée.<br/> |



 

## <a name="remarks"></a>Remarques

La propriété **nKeyCode** spécifie une clé physique. Les tableaux suivants indiquent les valeurs possibles pour les clés principales sur un clavier standard.

Valeurs pour les clés principales.



| Clé                     | Valeur   |
|-------------------------|---------|
| A-Z                     | 65-90   |
| 0-9                     | 48-56   |
| F1-F12                  | 112-123 |
| ÉCHAP                     | 27      |
| Tab                     | 9       |
| Verr. Maj               | 20      |
| SHIFT (gauche ou droite)   | 16      |
| CTRL (gauche ou droite)    | 17      |
| ALT (gauche ou droite)     | 18      |
| SPACE                   | 32      |
| Ret.arr               | 8       |
| ENTRÉE                   | 13      |
| touche Windows du logo, à gauche  | 91      |
| touche Windows du logo, droite | 92      |
| Clé de l'application         | 93      |



 

Valeurs des touches du pavé numérique.



| Clé               | Valeur  |
|-------------------|--------|
| 0-9               | 96-105 |
| VERR. NUM          | 144    |
| Division (/)        | 111    |
| MULTIPLIER ( \* )     | 106    |
| SOUSTRAIre (-)      | 109    |
| AJOUTER (+)           | 107    |
| SÉPARATEUR (entrée) | 108    |
| DÉCIMAL (.)       | 110    |



 

Valeurs des touches de navigation.



| Clé         | Valeur |
|-------------|-------|
| INSERT      | 45    |
| Suppression      | 46    |
| Origine        | 36    |
| FIN         | 35    |
| Pg. préc     | 33    |
| Pg. suiv   | 34    |
| Flèche haut    | 38    |
| Bas  | 40    |
| Gauche  | 37    |
| Flèche droite | 39    |



 

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

 

 





