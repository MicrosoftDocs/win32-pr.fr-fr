---
title: IWMPClosedCaption2 propriété SAMILangCount
description: La propriété SAMILangCount obtient le nombre de langues prises en charge par le fichier SAMI actuel.
ms.assetid: e3c7203d-66cb-49e2-9204-795c0f27248f
keywords:
- Lecteur Windows Media de la propriété SAMILangCount
- Lecteur Windows Media de la propriété SAMILangCount, interface IWMPClosedCaption2
- Lecteur Windows Media de l’interface IWMPClosedCaption2, propriété SAMILangCount
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMILangCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea01357de508dea319389cd14ab85ebafe0329e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413313"
---
# <a name="iwmpclosedcaption2samilangcount-property"></a>IWMPClosedCaption2 :: SAMILangCount, propriété

La propriété **SAMILangCount** obtient le nombre de langues prises en charge par le fichier sami actuel.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 SAMILangCount {get; set;}
```


```VB

Public ReadOnly Property SAMILangCount As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui correspond au nombre de langues prises en charge.

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

[**IWMPClosedCaption. SAMILang (VB et C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[**Interface IWMPClosedCaption2 (VB et C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2. getSAMILangName (VB et C#)**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)
</dt> </dl>

 

 





