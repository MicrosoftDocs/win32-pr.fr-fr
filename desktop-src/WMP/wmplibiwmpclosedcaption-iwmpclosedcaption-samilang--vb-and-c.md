---
title: IWMPClosedCaption propriété SAMILang
description: La propriété SAMILang obtient ou définit la langue affichée pour le sous-titrage.
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- Propriété SAMILang lecteur Windows Media
- Propriété SAMILang lecteur Windows Media, interface IWMPClosedCaption
- Interface IWMPClosedCaption lecteur Windows Media, propriété SAMILang
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMILang
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe29defa3736795c88613ee7ab2ef11a914a3f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521730"
---
# <a name="iwmpclosedcaptionsamilang-property"></a>IWMPClosedCaption :: SAMILang, propriété

La propriété **SAMILang** obtient ou définit la langue affichée pour le sous-titrage.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a>Valeur de la propriété

**System. String** qui est le nom spécifié dans l’identificateur de langue d’un fichier sami.

## <a name="remarks"></a>Notes

Un fichier SAMI peut contenir du texte pour une ou plusieurs langues. Les langues disponibles pour le sous-titrage sont définies entre les balises <STYLE> et </STYLE> dans le fichier sami. Un identificateur de langue est spécifié avec une chaîne alphanumérique unique précédée d’un point (.). Le nom spécifié pour une langue peut être n’importe quelle chaîne. Par exemple, les éléments suivants peuvent être utilisés pour définir l’anglais des États-Unis :


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



Si aucune langue SAMI n’est spécifiée, la première langue définie dans le fichier SAMI est utilisée par défaut.

La chaîne que vous définissez à l’aide de **SAMILang** doit correspondre à l’attribut **Name** dans le spécificateur de langage.

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

[**Interface IWMPClosedCaption2 (VB et C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





