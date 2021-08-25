---
title: Propriété IWMPSettings balance
description: La propriété balance obtient ou définit le solde stéréo actuel.
ms.assetid: 6b9b6305-3bab-418d-a172-d47ca4dbaba5
keywords:
- Lecteur Windows Media de la propriété de solde
- Lecteur Windows Media de propriété de solde, interface IWMPSettings
- Lecteur Windows Media de l’interface IWMPSettings, propriété de solde
topic_type:
- apiref
api_name:
- IWMPSettings.balance
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d519d656be6b4974e2b4dd2707aafb2bb153f6b26bafe75de948d5e50c67b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861081"
---
# <a name="iwmpsettingsbalance-property"></a>IWMPSettings :: balance, propriété

La propriété **balance** obtient ou définit le solde stéréo actuel.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 balance {get; set;}
```


```VB

Public Property balance As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui est la valeur de l’équilibre. Cette valeur peut être comprise entre 100 et 100. La valeur par défaut est zéro.

## <a name="remarks"></a>Remarques

La valeur zéro indique que le son est lu à un volume égal sur les canaux gauche et droit. Une valeur de 100 indique que l’audio est lu uniquement sur le canal de gauche. Une valeur de 100 indique que l’audio est lu uniquement sur le canal approprié.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                                                     |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPSettings (VB et C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





