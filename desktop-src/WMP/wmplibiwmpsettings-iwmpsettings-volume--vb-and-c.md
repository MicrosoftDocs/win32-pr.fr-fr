---
title: Propriété du volume IWMPSettings
description: La propriété volume obtient ou définit le volume de lecture actuel.
ms.assetid: cff4fe70-9ca2-4419-bfc3-d622e8c72756
keywords:
- propriété de volume lecteur Windows Media
- propriété de volume lecteur Windows Media, interface IWMPSettings
- Interface IWMPSettings lecteur Windows Media, propriété volume
topic_type:
- apiref
api_name:
- IWMPSettings.volume
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b21e50c9d3c52b7ce117d6c2ab681e592571c0f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541272"
---
# <a name="iwmpsettingsvolume-property"></a>IWMPSettings :: volume, propriété

La propriété **volume** obtient ou définit le volume de lecture actuel.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 volume {get; set;}
```


```VB

Public Property volume As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui est le niveau de volume, compris entre 0 et 100.

## <a name="remarks"></a>Notes

La valeur zéro spécifie aucun volume (muet). La valeur 100 spécifie le volume complet. Si aucune valeur n’est spécifiée pour cette propriété, la valeur par défaut est le dernier paramètre de volume défini pour le lecteur Windows Media.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPSettings (VB et C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





