---
title: AxWindowsMediaPlayer. stretchToFit, propriété
description: La propriété stretchToFit obtient ou définit une valeur qui indique si la vidéo affichée par le contrôle du lecteur Windows Media se redimensionne automatiquement pour s’adapter à la fenêtre vidéo, lorsque la fenêtre vidéo est plus grande que les dimensions de l’image vidéo.
ms.assetid: 02e2bcba-4975-4ddd-996b-9bd40774ebc1
keywords:
- propriété stretchToFit lecteur Windows Media
- propriété stretchToFit lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, propriété stretchToFit
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.stretchToFit
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd6937ffa556817a80f0b21dfaed6d270c2e351
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545569"
---
# <a name="axwindowsmediaplayerstretchtofit-property"></a>AxWindowsMediaPlayer. stretchToFit, propriété

La propriété stretchToFit obtient ou définit une valeur qui indique si la vidéo affichée par le contrôle du lecteur Windows Media se redimensionne automatiquement pour s’adapter à la fenêtre vidéo, lorsque la fenêtre vidéo est plus grande que les dimensions de l’image vidéo.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Boolean stretchToFit {get; set;}
```


```VB

Public Property stretchToFit As System.Boolean
```





## <a name="property-value"></a>Valeur de la propriété

Valeur System. Boolean qui indique si la vidéo sera étirée pour s’ajuster à la fenêtre. La valeur par défaut est false.

## <a name="remarks"></a>Notes

Quand **stretchToFit** a la valeur true, le contrôle du lecteur Windows Media conserve les proportions d’origine de la vidéo. Si les proportions de la vidéo ne correspondent pas aux proportions de la fenêtre vidéo, les zones de masque noires peuvent apparaître en haut et en bas, ou à gauche et à droite de l’image vidéo.

Cette propriété s’applique au contrôle du lecteur Windows Media uniquement lorsqu’il est incorporé dans une page Web.

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

 

 





