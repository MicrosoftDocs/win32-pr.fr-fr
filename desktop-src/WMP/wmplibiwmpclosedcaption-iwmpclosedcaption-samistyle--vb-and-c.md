---
title: IWMPClosedCaption propriété SAMIStyle
description: La propriété SAMIStyle obtient ou définit le style de sous-titrage.
ms.assetid: 0b1f92c6-b659-4ade-90c8-62a06e475f5c
keywords:
- Lecteur Windows Media de la propriété SAMIStyle
- Lecteur Windows Media de la propriété SAMIStyle, interface IWMPClosedCaption
- Lecteur Windows Media de l’interface IWMPClosedCaption, propriété SAMIStyle
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIStyle
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e147b48ffb80e1114133b59018cef514eefd2ae7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193075"
---
# <a name="iwmpclosedcaptionsamistyle-property"></a>IWMPClosedCaption :: SAMIStyle, propriété

La propriété **SAMIStyle** obtient ou définit le style de sous-titrage.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String SAMIStyle {get; set;}
```


```VB

Public Property SAMIStyle As System.String
```





## <a name="property-value"></a>Valeur de la propriété

**System. String** qui est le nom spécifié dans l’identificateur de style d’un fichier sami.

## <a name="remarks"></a>Notes

Un fichier SAMI peut contenir plusieurs définitions de style de format. Les styles SAMI sont définis entre le &lt; style &gt; et les </STYLE> balises dans le fichier sami. Un style est défini avec une chaîne de texte précédée d’un \# caractère. Par exemple :


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}
```



Cela spécifie un style qui produit une police particulière.

Si aucun style SAMI n’est spécifié, le premier style défini dans le fichier SAMI est utilisé par défaut.

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

[**Interface IWMPClosedCaption2 (VB et C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





