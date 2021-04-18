---
title: Méthode AxWindowsMediaPlayer. newMedia
description: La méthode newMedia retourne une interface IWMPMedia pour un nouvel élément multimédia.
ms.assetid: d10a517e-b4da-4f0b-9d51-9d387578d7dd
keywords:
- méthode newMedia lecteur Windows Media
- méthode newMedia lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, méthode newMedia
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093a4e2b8181aac9148686108ad2c5c318a4d0cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540333"
---
# <a name="axwindowsmediaplayernewmedia-method"></a>Méthode AxWindowsMediaPlayer. newMedia

La méthode newMedia retourne une interface IWMPMedia pour un nouvel élément multimédia.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPMedia newMedia(
  System.String bstrURL
);
```


```VB

Public Function newMedia( _
  ByVal bstrURL As System.String _
) As IWMPMedia
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrURL* 
</dt> <dd>

**System. String** qui est l’URL du fichier multimédia numérique utilisé pour initialiser le nouvel élément multimédia.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Interface WMPLib. IWMPMedia qui représente l’élément multimédia nouvellement créé.

## <a name="remarks"></a>Notes

Le paramètre *du bstrURL* ne doit pas être une chaîne de longueur nulle ("") ou null.

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
</dt> </dl>

 

 





