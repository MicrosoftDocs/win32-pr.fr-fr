---
description: La propriété StringData de l’objet record est une propriété en lecture-écriture qui transfère les données de chaîne vers ou à partir d’un champ spécifié dans l’enregistrement. Si un entier ou un objet a été stocké, sa valeur de chaîne est retournée.
ms.assetid: ffa163eb-41b3-47ae-b01d-39a3890990a3
title: Record. StringData, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.StringData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 21f72c35795696875aa55f2d5d791564c6f1fee5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530539"
---
# <a name="recordstringdata-property"></a>Record. StringData, propriété

La propriété **StringData** de l’objet [**Record**](record-object.md) est une propriété en lecture-écriture qui transfère les données de chaîne vers ou à partir d’un champ spécifié dans l’enregistrement. Si un entier ou un objet a été stocké, sa valeur de chaîne est retournée.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Record.StringData
Record.StringData = propVal 
```



## <a name="property-value"></a>Valeur de la propriété

Numéro de champ obligatoire de la valeur dans l’enregistrement, de base 1.

## <a name="remarks"></a>Notes

La valeur retournée d’un champ inexistant est une chaîne vide. Pour définir un champ de chaîne d’enregistrement sur null, utilisez un variant vide ou une chaîne vide. Toute tentative de stockage d’une valeur dans un champ inexistant génère une erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iRecord est défini en tant que 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




