---
title: AxWindowsMediaPlayer. Status, propriété
description: La propriété Status obtient une valeur indiquant l’état du lecteur Windows Media.
ms.assetid: fefed54d-1fae-4599-8efc-eb2efdbd8ebd
keywords:
- propriété d’État lecteur Windows Media
- propriété d’État lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, propriété Status
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525262"
---
# <a name="axwindowsmediaplayerstatus-property"></a>AxWindowsMediaPlayer. Status, propriété

La propriété Status obtient une valeur indiquant l’état du lecteur Windows Media.

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

[**Événement AxWindowsMediaPlayer. StatusChange (VB et C#)**](axwmplib-axwindowsmediaplayer-statuschange.md)
</dt> </dl>

 

 





