---
title: IWMPClosedCaption propriété SAMIFileName
description: La propriété SAMIFileName obtient ou définit le nom d’un fichier contenant les informations nécessaires pour le sous-titrage.
ms.assetid: c3162c5f-9d66-41d4-920c-ed9840742d9d
keywords:
- Lecteur Windows Media de la propriété SAMIFileName
- Lecteur Windows Media de la propriété SAMIFileName, interface IWMPClosedCaption
- Lecteur Windows Media de l’interface IWMPClosedCaption, propriété SAMIFileName
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIFileName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d251f2bbf0c8839ab9a0005c69e1869c47af16ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193079"
---
# <a name="iwmpclosedcaptionsamifilename-property"></a>IWMPClosedCaption :: SAMIFileName, propriété

La propriété **SAMIFileName** obtient ou définit le nom d’un fichier contenant les informations nécessaires pour le sous-titrage.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String SAMIFileName {get; set;}
```


```VB

Public Property SAMIFileName As System.String
```





## <a name="property-value"></a>Valeur de la propriété

**System. String** qui est le nom du fichier sami (Synchronized Accessible Media Interchange).

## <a name="remarks"></a>Notes

Le fichier SAMI doit utiliser une extension de nom de fichier. SMI ou. sami.

Si vous ne définissez pas de valeur à l’aide de **SAMIFileName**, cette propriété obtient une **chaîne** contenant le nom de fichier ou l’URL par défaut associés à l’élément multimédia en cours. Cette association peut se produire lorsqu’un fichier SAMI est spécifié à l’aide du paramètre d’URL *sami* , ou automatiquement lorsque le fichier sami porte le même nom que le fichier multimédia numérique (à l’exception de l’extension de nom de fichier). Si aucun fichier SAMI par défaut n’est associé au média actuel, cette propriété obtient une chaîne de longueur nulle ("").

Une fois que vous avez défini une valeur à l’aide de **SAMIFileName**, cette valeur persiste jusqu’à ce que vous ayez défini une nouvelle valeur (ou jusqu’à ce qu’un nouvel élément multimédia soit ouvert à l’aide du paramètre URL sami). Par conséquent, vous devez définir une nouvelle valeur pour cette propriété avant de lire chaque nouvel élément multimédia. De cette façon, la nouvelle valeur pour **SAMIFileName** prend effet lors de l’ouverture de l’élément multimédia suivant (ou lors de l’appel de **AxWindowsMediaPlayer. Close** ). La spécification d’une nouvelle valeur pour **SAMIFileName** n’a aucun effet sur le média actuel.

pour que Lecteur Windows Media utilise le fichier SAMI par défaut associé à un élément multimédia particulier, définissez **SAMIFileName** sur une chaîne de longueur nulle ("") avant de lire l’élément multimédia suivant.

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

[**AxWindowsMediaPlayer. Close**](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[**Interface IWMPClosedCaption (VB et C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interface IWMPClosedCaption2 (VB et C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





