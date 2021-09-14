---
title: Propriété d’erreur IWMPMedia2
description: La propriété Error obtient une interface IWMPErrorItem si l’élément multimédia a une condition d’erreur.
ms.assetid: 57dc8aef-5f22-43da-87bc-fdc0c8ebe49b
keywords:
- Lecteur Windows Media de propriétés d’erreur
- Lecteur Windows Media de propriété d’erreur, interface IWMPMedia2
- Lecteur Windows Media de l’interface IWMPMedia2, propriété Error
topic_type:
- apiref
api_name:
- IWMPMedia2.Error
- IWMPMedia2.get_Error
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2179b4604efd03574c78261575ce02311cd18a0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122673"
---
# <a name="iwmpmedia2error-property"></a>IWMPMedia2 :: Error, propriété

La propriété **Error** obtient une interface **IWMPErrorItem** si l’élément multimédia a une condition d’erreur.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPErrorItem Error {get;}
```


```VB

Public ReadOnly Property Error As IWMPErrorItem
```





## <a name="property-value"></a>Valeur de la propriété

Interface **wmplib. IWMPErrorItem** qui fournit l’accès aux informations sur la condition d’erreur.

## <a name="remarks"></a>Notes

Si l’élément multimédia ne peut pas être lu, cette propriété obtient une interface **IWMPErrorItem** qui contient des informations sur le problème rencontré.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWMPErrorItem (VB et C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia2 (VB et C#)**](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





