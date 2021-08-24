---
title: AxWindowsMediaPlayer. Status, propriété
description: la propriété status obtient une valeur indiquant l’état de Lecteur Windows Media.
ms.assetid: fefed54d-1fae-4599-8efc-eb2efdbd8ebd
keywords:
- Lecteur Windows Media de la propriété status
- Lecteur Windows Media de propriété status, classe AxWindowsMediaPlayer
- Lecteur Windows Media de la classe AxWindowsMediaPlayer, propriété status
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.status
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac46eeef411e1d728994d829d95727cdaf4020c2ef1b7511391b6ca0d2e31ff7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864559"
---
# <a name="axwindowsmediaplayerstatus-property"></a>AxWindowsMediaPlayer. Status, propriété

la propriété status obtient une valeur indiquant l’état de Lecteur Windows Media.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String status {get;}
```


```VB

Public ReadOnly Property status As System.String
```





## <a name="property-value"></a>Valeur de la propriété

System. String qui est l’État.

## <a name="remarks"></a>Remarques

Les valeurs contenues dans cette propriété sont sujettes à modification à tout moment et doivent être utilisées à des fins d’affichage uniquement.

AxWindowsMediaPlayer. L’événement **statuschange** est déclenché à chaque modification de la valeur de cette propriété.

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

[**événement AxWindowsMediaPlayer. StatusChange (VB et C#)**](axwmplib-axwindowsmediaplayer-statuschange.md)
</dt> </dl>

 

 





