---
title: AxWindowsMediaPlayer. windowlessVideo, propriété
description: La propriété windowlessVideo obtient ou définit une valeur indiquant si le contrôle du lecteur Windows Media affiche la vidéo en mode sans fenêtre.
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- propriété windowlessVideo lecteur Windows Media
- propriété windowlessVideo lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, propriété windowlessVideo
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.windowlessVideo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22ecc0f39b03201809877fe8ebc667d62e16d0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526491"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a>AxWindowsMediaPlayer. windowlessVideo, propriété

La propriété windowlessVideo obtient ou définit une valeur indiquant si le contrôle du lecteur Windows Media affiche la vidéo en mode sans fenêtre.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a>Valeur de la propriété

Valeur System. Boolean indiquant si le contrôle du lecteur Windows Media affiche la vidéo en mode sans fenêtre. La valeur par défaut est false.

## <a name="remarks"></a>Notes

Par défaut, un contrôle du lecteur Windows Media incorporé affiche la vidéo dans sa propre fenêtre au sein de la zone cliente. Quand **windowlessVideo** a la valeur true, l’objet lecteur Windows Media affiche la vidéo directement dans la zone cliente, ce qui vous permet d’appliquer des effets spéciaux ou de coucher la vidéo avec du texte.

Dans Windows Vista, le rendu de la vidéo en mode sans fenêtre peut dégrader les performances.

L’obtention d’une valeur pour cette propriété n’est pas prise en charge pour Netscape Navigator. La définition d’une valeur pour cette propriété dans Netscape Navigator peut donner des résultats inattendus.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





