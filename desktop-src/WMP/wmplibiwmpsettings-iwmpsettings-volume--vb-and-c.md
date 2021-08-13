---
title: Propriété du volume IWMPSettings
description: La propriété volume obtient ou définit le volume de lecture actuel.
ms.assetid: cff4fe70-9ca2-4419-bfc3-d622e8c72756
keywords:
- Lecteur Windows Media de propriétés de volume
- Lecteur Windows Media de propriétés de volume, interface IWMPSettings
- Lecteur Windows Media de l’interface IWMPSettings, propriété volume
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
ms.openlocfilehash: a2077547dd00b5c75b6ca77a966190db2bb3bb1bcde61d1f5c5b84c794af84e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568396"
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

## <a name="remarks"></a>Remarques

La valeur zéro spécifie aucun volume (muet). La valeur 100 spécifie le volume complet. si aucune valeur n’est spécifiée pour cette propriété, la valeur par défaut est le dernier paramètre de volume établi pour Lecteur Windows Media.

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

 

 





