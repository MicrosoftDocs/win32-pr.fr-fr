---
description: La propriété Item est une propriété en lecture seule qui retourne une chaîne dans la collection d’objets StringList.
ms.assetid: 5c654927-41cf-4e47-9d4f-76524f8bbc97
title: StringList. Item, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ebd32af433fd932cb05d062fbc515a3245113343
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541423"
---
# <a name="stringlistitem-property"></a>StringList. Item, propriété

La propriété **Item** est une propriété en lecture seule qui retourne une chaîne dans la collection d' [**objets StringList**](stringlist-object.md) .

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = StringList.Item
```



## <a name="property-value"></a>Valeur de la propriété

Numéro d’index de l’élément avec la collection de chaînes. Ce paramètre est obligatoire.

## <a name="remarks"></a>Notes

Le client doit vérifier que l' [**objet StringList**](stringlist-object.md) existe et n’est pas vide avant de référencer la propriété **Item** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IStringList est défini en tant que 000C1095-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 




