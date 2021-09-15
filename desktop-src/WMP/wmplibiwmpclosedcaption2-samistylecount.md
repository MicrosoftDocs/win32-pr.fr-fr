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
ms.openlocfilehash: ff361b4c6d34f63e86e3d8458bff4d3308cae29f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413310"
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

## <a name="remarks"></a>Notes

Cette propriété retourne la valeur 0, sauf si un fichier multimédia numérique est ouvert (AxWindowsMediaPlayer. openState est égal à 13).

## <a name="requirements"></a>Spécifications



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

 

 





