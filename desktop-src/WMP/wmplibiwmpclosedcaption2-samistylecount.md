---
title: IWMPClosedCaption2 propriété SAMIStyleCount
description: La propriété SAMIStyleCount obtient le nombre de styles pris en charge par le fichier SAMI actuel.
ms.assetid: e2a0d194-6fa2-48c9-9fc7-0b60029d2e5d
keywords:
- Lecteur Windows Media de la propriété SAMIStyleCount
- Lecteur Windows Media de la propriété SAMIStyleCount, interface IWMPClosedCaption2
- Lecteur Windows Media de l’interface IWMPClosedCaption2, propriété SAMIStyleCount
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMIStyleCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f73ab4e252386f790f74741053012239d0219b1e296e392146894f906e1556f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115916"
---
# <a name="iwmpclosedcaption2samistylecount-property"></a>IWMPClosedCaption2 :: SAMIStyleCount, propriété

La propriété **SAMIStyleCount** obtient le nombre de styles pris en charge par le fichier sami actuel.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 SAMIStyleCount {get; set;}
```


```VB

Public ReadOnly Property SAMIStyleCount As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui correspond au nombre de styles.

## <a name="remarks"></a>Remarques

Cette propriété retourne la valeur 0, sauf si un fichier multimédia numérique est ouvert (AxWindowsMediaPlayer. openState est égal à 13).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Ajout de sous-titres à des médias numériques**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interface IWMPClosedCaption (VB et C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption. SAMIStyle (VB et C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[**Interface IWMPClosedCaption2 (VB et C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2. getSAMIStyleName (VB et C#)**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamistylename--vb-and-c.md)
</dt> </dl>

 

 





