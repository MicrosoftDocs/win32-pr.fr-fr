---
description: Il s’agit de la propriété IntegerData de l’objet record. Cette propriété en lecture-écriture transfère les données de type entier 32 bits dans vers ou à partir d’un champ spécifié dans l’enregistrement. Si une valeur de champ ne peut pas être convertie en un entier, msiDatabaseNullInteger est retourné.
ms.assetid: abc291cd-31ba-409f-b010-8b3a71cbdc77
title: Record. IntegerData, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.IntegerData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ed816c75ab6adc98b3ac19984079d840a4a447b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526107"
---
# <a name="recordintegerdata-property"></a>Record. IntegerData, propriété

Il s’agit de la propriété **IntegerData** de l’objet [**Record**](record-object.md) . Cette propriété en lecture-écriture transfère les données de type entier 32 bits dans vers ou à partir d’un champ spécifié dans l’enregistrement. Si une valeur de champ ne peut pas être convertie en un entier, msiDatabaseNullInteger est retourné.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Record.IntegerData
Record.IntegerData = propVal 
```



## <a name="property-value"></a>Valeur de la propriété

Numéro de champ obligatoire de la valeur dans l’enregistrement, de base 1.

## <a name="remarks"></a>Notes

Pour définir un champ d’entier d’enregistrement sur null, utilisez msiDatabaseNullInteger. La valeur retournée d’un champ inexistant est msiDatabaseNullInteger. Toute tentative de stockage d’une valeur dans un champ inexistant génère une erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iRecord est défini en tant que 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




