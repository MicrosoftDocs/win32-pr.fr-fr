---
title: AxWindowsMediaPlayer. enableContextMenu, propriété
description: La propriété enableContextMenu obtient ou définit une valeur indiquant s’il faut activer le menu contextuel qui apparaît lorsque l’utilisateur clique sur le bouton droit de la souris.
ms.assetid: 6096cab7-c1fa-4b71-804b-e84facab2229
keywords:
- Lecteur Windows Media de la propriété enableContextMenu
- Lecteur Windows Media de la propriété enableContextMenu, classe AxWindowsMediaPlayer
- Lecteur Windows Media de la classe AxWindowsMediaPlayer, propriété enableContextMenu
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.enableContextMenu
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5603762ec9823f7e9896c5c22c1dee33f2399bb02301921057f8502046bcc002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582338"
---
# <a name="axwindowsmediaplayerenablecontextmenu-property"></a>AxWindowsMediaPlayer. enableContextMenu, propriété

La propriété enableContextMenu obtient ou définit une valeur indiquant s’il faut activer le menu contextuel qui apparaît lorsque l’utilisateur clique sur le bouton droit de la souris.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Boolean enableContextMenu {get; set;}
```


```VB

Public Property enableContextMenu As System.Boolean
```





## <a name="property-value"></a>Valeur de la propriété

Valeur System. Boolean qui indique s’il faut activer le menu contextuel. La valeur par défaut est true.

## <a name="remarks"></a>Notes

pendant la lecture en plein écran, Lecteur Windows Media masque le curseur de la souris quand **enableContextMenu** est égal à false et **uiMode** est égal à « none ».

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

 

 





