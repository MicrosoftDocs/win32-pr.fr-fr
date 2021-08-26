---
title: AxWindowsMediaPlayer. mediaCollection, propriété
description: La propriété mediaCollection obtient une interface IWMPMediaCollection qui fournit un moyen d’organiser une grande collection d’éléments multimédias.
ms.assetid: ec37e1da-a843-4b89-88fc-ec9255baa98a
keywords:
- Lecteur Windows Media de la propriété mediaCollection
- Lecteur Windows Media de la propriété mediaCollection, classe AxWindowsMediaPlayer
- Lecteur Windows Media de la classe AxWindowsMediaPlayer, propriété mediaCollection
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.mediaCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86ad0cc720c49926ddbd75fe71d47738a9e8af43fa97670a0b9915a50716ed0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902629"
---
# <a name="axwindowsmediaplayermediacollection-property"></a>AxWindowsMediaPlayer. mediaCollection, propriété

La propriété mediaCollection obtient une interface **IWMPMediaCollection** qui fournit un moyen d’organiser une grande collection d’éléments multimédias.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPMediaCollection mediaCollection {get;}
```


```VB

Public ReadOnly Property mediaCollection As IWMPMediaCollection
```





## <a name="property-value"></a>Valeur de la propriété

L’interface WMPLib. IWMPMediaCollection à une collection d’éléments multimédias.

## <a name="remarks"></a>Remarques

Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

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

[**Interface IWMPMediaCollection (VB et C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





