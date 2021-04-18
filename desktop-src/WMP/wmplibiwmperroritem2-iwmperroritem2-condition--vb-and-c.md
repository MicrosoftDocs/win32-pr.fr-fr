---
title: Propriété de condition IWMPErrorItem2
description: La propriété condition obtient une valeur indiquant la condition de l’erreur.
ms.assetid: 68800d75-8341-40d1-b699-ffe27bb1f38a
keywords:
- propriété condition lecteur Windows Media
- propriété condition lecteur Windows Media, interface IWMPErrorItem2
- Interface IWMPErrorItem2 lecteur Windows Media, propriété condition
topic_type:
- apiref
api_name:
- IWMPErrorItem2.condition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be53e7467f741371867b2c0d1dd66c3f68d22ec8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533447"
---
# <a name="iwmperroritem2condition-property"></a>IWMPErrorItem2 :: condition, propriété

La propriété **condition** obtient une valeur indiquant la condition de l’erreur.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 condition {get; set;}
```


```VB

Public ReadOnly Property condition As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui est le code de condition.

## <a name="remarks"></a>Notes

Le code de condition est une valeur utilisée par Microsoft pour fournir des informations supplémentaires au personnel du support technique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPErrorItem2 (VB et C#)**](iwmperroritem2--vb-and-c.md)
</dt> </dl>

 

 





