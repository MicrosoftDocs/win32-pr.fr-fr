---
description: La propriété Property de l’objet UIPreview est une propriété en lecture-écriture qui représente la valeur de chaîne d’une propriété de programme d’installation nommée ou, si elle est précédée d’un signe de pourcentage (%), de la valeur d’une variable d’environnement système pour le processus en cours.
ms.assetid: 92900426-8fb5-4a94-a982-438267ad756e
title: Propriété UIPreview. Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 430c6f75b03fe69f8054bb2b0a61bab59dcc4d58
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011810"
---
# <a name="uipreviewproperty-property"></a>Propriété UIPreview. Property

La propriété **Property** de l’objet [**UIPreview**](uipreview-object.md) est une propriété en lecture-écriture qui représente la valeur de chaîne d’une propriété de programme d’installation nommée ou, si elle est précédée d’un signe de pourcentage (%), de la valeur d’une variable d’environnement système pour le processus en cours. Cette valeur est exposée pour permettre l’affichage correct des boîtes de dialogue qui sont dépendantes des valeurs de propriété. Des valeurs de type chaîne ou entier peuvent être fournies. Une variable d’environnement ou une propriété inexistante équivaut à une valeur null.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = UIPreview.Property
UIPreview.Property = propVal 
```



## <a name="property-value"></a>Valeur de la propriété

Nom de propriété obligatoire qui respecte la casse ou un nom qui ne respecte pas la casse d’une variable d’environnement préfixée par un signe de pourcentage (%).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview est défini en tant que 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




