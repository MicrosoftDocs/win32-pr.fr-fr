---
description: La propriété FeatureCost de l’objet session retourne la quantité totale d’espace disque (en unités de 512 octets) requise par la fonctionnalité spécifiée et ses fonctionnalités parentes (jusqu’à la racine du tableau des fonctionnalités).
ms.assetid: 5df9912a-2722-41c8-991b-256a009e85df
title: Session. FeatureCost, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCost
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 617d1695b8b472952f22737ba3f677d9320f9b4214afc3dea5a9cc5010e2b1a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629289"
---
# <a name="sessionfeaturecost-property"></a>Session. FeatureCost, propriété

La propriété **FeatureCost** de l’objet [**session**](session-object.md) retourne la quantité totale d’espace disque (en unités de 512 octets) requise par la fonctionnalité spécifiée et ses fonctionnalités parentes (jusqu’à la racine du tableau des fonctionnalités). Pour chaque fonctionnalité, le coût total est constitué des coûts de disque attribués à chaque composant lié à la fonctionnalité.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Session.FeatureCost
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

Si la propriété échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




