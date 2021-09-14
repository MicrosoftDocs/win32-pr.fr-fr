---
title: AxWindowsMediaPlayer. windowlessVideo, propriété
description: la propriété windowlessVideo obtient ou définit une valeur indiquant si le contrôle Lecteur Windows Media restitue la vidéo en mode sans fenêtre.
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- Lecteur Windows Media de la propriété windowlessVideo
- Lecteur Windows Media de la propriété windowlessVideo, classe AxWindowsMediaPlayer
- Lecteur Windows Media de la classe AxWindowsMediaPlayer, propriété windowlessVideo
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192104"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a>AxWindowsMediaPlayer. windowlessVideo, propriété

la propriété windowlessVideo obtient ou définit une valeur indiquant si le contrôle Lecteur Windows Media restitue la vidéo en mode sans fenêtre.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a>Valeur de la propriété

valeur System. Boolean indiquant si le contrôle Lecteur Windows Media restitue la vidéo en mode sans fenêtre. La valeur par défaut est false.

## <a name="remarks"></a>Notes

par défaut, un contrôle de Lecteur Windows Media incorporé affiche la vidéo dans sa propre fenêtre au sein de la zone cliente. quand **windowlessVideo** a la valeur true, l’objet Lecteur Windows Media restitue la vidéo directement dans la zone cliente, ce qui vous permet d’appliquer des effets spéciaux ou de coucher la vidéo avec du texte.

dans Windows Vista, le rendu de la vidéo en mode sans fenêtre peut dégrader les performances.

L’obtention d’une valeur pour cette propriété n’est pas prise en charge pour Netscape Navigator. La définition d’une valeur pour cette propriété dans Netscape Navigator peut donner des résultats inattendus.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





