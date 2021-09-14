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
ms.openlocfilehash: 4ea7e8c36ad05e2f9a4573d8e2433d705f354239
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193331"
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

## <a name="remarks"></a>Notes

Les valeurs contenues dans cette propriété sont sujettes à modification à tout moment et doivent être utilisées à des fins d’affichage uniquement.

AxWindowsMediaPlayer. L’événement **statuschange** est déclenché à chaque modification de la valeur de cette propriété.

## <a name="requirements"></a>Spécifications



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

 

 





