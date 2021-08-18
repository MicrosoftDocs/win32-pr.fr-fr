---
description: La propriété FeatureCurrentState de l’objet session est une propriété en lecture seule qui retourne l’état installé actuel de la fonctionnalité désignée. Pour les valeurs d’État, consultez la propriété FeatureRequestState.
ms.assetid: c4c325dc-6e7e-4009-8707-952c04574170
title: Session. FeatureCurrentState, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3738a33d2c7a855abe6cc60139286b3e9c4d586bc6c2d9d436390fc5e52f4fd1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629229"
---
# <a name="sessionfeaturecurrentstate-property"></a>Session. FeatureCurrentState, propriété

La propriété **FeatureCurrentState** de l’objet [**session**](session-object.md) est une propriété en lecture seule qui retourne l’état installé actuel de la fonctionnalité désignée. Pour les valeurs d’État, consultez la propriété [**FeatureRequestState**](session-featurerequeststate.md) .

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Session.FeatureCurrentState
```



## <a name="property-value"></a>Valeur de la propriété

Nom de chaîne requis pour la fonctionnalité demandée et une clé primaire dans la [table des fonctionnalités](feature-table.md).

## <a name="remarks"></a>Remarques

Si la propriété échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**session**](session-object.md)
</dt> <dt>

[**Propriété FeatureRequestState**](session-featurerequeststate.md)
</dt> </dl>

 

 




