---
description: La propriété Property de l’objet session est une propriété en lecture-écriture qui représente la valeur de chaîne d’une propriété de programme d’installation nommée, telle qu’elle est gérée par l’objet de session.
ms.assetid: 15ce8264-2573-428c-98d9-690cfaae5144
title: Session. Property, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9635d5b9ee093f270e4ee7993f78609d60caa13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528835"
---
# <a name="sessionproperty-property"></a>Session. Property, propriété

La propriété **Property** de l’objet [**session**](session-object.md) est une propriété en lecture-écriture qui représente la valeur de chaîne d’une propriété de programme d’installation nommée, telle qu’elle est gérée par l’objet de **session** dans la table de propriétés en mémoire ou, si elle est précédée d’un signe de pourcentage (%), de la valeur d’une variable d’environnement système pour le processus en cours. Des valeurs de type chaîne ou entier peuvent être fournies. Une variable d’environnement ou une propriété inexistante équivaut à une valeur null.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Session.Property
Session.Property = propVal 
```



## <a name="property-value"></a>Valeur de la propriété

Nom de propriété obligatoire qui respecte la casse ou un nom qui ne respecte pas la casse d’une variable d’environnement préfixée par un signe de pourcentage (%).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




