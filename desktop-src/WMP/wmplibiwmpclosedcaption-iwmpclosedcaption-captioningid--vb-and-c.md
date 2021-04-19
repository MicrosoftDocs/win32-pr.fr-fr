---
title: IWMPClosedCaption propriété captioningId
description: La propriété IWMPClosedCaption obtient ou définit le nom de l’élément HTML affichant le sous-titrage.
ms.assetid: b09bb7c7-c3b6-4e0d-962f-24b06a04f6d1
keywords:
- propriété captioningId lecteur Windows Media
- propriété captioningId lecteur Windows Media, interface IWMPClosedCaption
- Interface IWMPClosedCaption lecteur Windows Media, propriété captioningId
topic_type:
- apiref
api_name:
- IWMPClosedCaption.captioningId
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343234fce2b93ac02255731a38025f6d7b9fac6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540516"
---
# <a name="iwmpclosedcaptioncaptioningid-property"></a>IWMPClosedCaption :: captioningId, propriété

La propriété **IWMPClosedCaption** obtient ou définit le nom de l’élément HTML affichant le sous-titrage.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String captioningId {get; set;}
```


```VB

Public Property captioningId As System.String
```





## <a name="property-value"></a>Valeur de la propriété

**System. String** qui correspond à l’ID de l’élément HTML.

## <a name="remarks"></a>Notes

Le nom d’élément spécifié peut être n’importe quel élément HTML dans la page Web, à condition qu’il prenne en charge l’attribut **InnerHtml** . Si la page Web contient plusieurs frames, le nom de l’élément ne peut faire référence qu’à un élément dans le même frame que le contrôle du lecteur Windows Media.

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

 

 





