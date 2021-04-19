---
title: Méthode AxWindowsMediaPlayer. openPlayer
description: La méthode openPlayer ouvre le lecteur Windows Media à l’aide de l’URL spécifiée. | Méthode AxWindowsMediaPlayer. openPlayer
ms.assetid: 9a9d8200-f427-42ff-b49f-d973cf86014f
keywords:
- méthode openPlayer lecteur Windows Media
- méthode openPlayer lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, méthode openPlayer
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openPlayer
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58416a1f20969b0bd223f653f44b5633f19cb096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535899"
---
# <a name="axwindowsmediaplayeropenplayer-method"></a>Méthode AxWindowsMediaPlayer. openPlayer

La méthode **openPlayer** ouvre le lecteur Windows Media à l’aide de l’URL spécifiée.

## <a name="syntax"></a>Syntaxe


```CSharp
public void openPlayer(
  System.String bstrURL
);
```


```VB

Public Sub openPlayer( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrURL* 
</dt> <dd>

**System. String** qui est l’URL de l’élément multimédia à lire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode lance le lecteur Windows Media avec l’URL spécifiée définie en tant qu’élément multimédia actuel. Si le joueur a été précédemment fermé en mode apparence, il s’ouvre en utilisant la dernière apparence choisie par l’utilisateur. Dans le cas contraire, le joueur s’ouvre en mode complet.

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

 

 





