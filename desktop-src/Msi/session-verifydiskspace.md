---
description: La propriété VerifyDiskSpace est une propriété en lecture seule.
ms.assetid: 62f11f71-00b0-4e04-8c45-d6d670238886
title: Session. VerifyDiskSpace, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.VerifyDiskSpace
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4a50bb96088f2c52673fda9a9ddffd786657376bcb4e4a60d5c6d81cb4fbe5e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628759"
---
# <a name="sessionverifydiskspace-property"></a>Session. VerifyDiskSpace, propriété

La propriété **VerifyDiskSpace** est une propriété en lecture seule. Elle retourne true si l’espace disque disponible est suffisant et false si le disque est plein. Étant donné que cette propriété utilise les informations collectées par les actions d’évaluation, **VerifyDiskSpace** doit être appelé uniquement après l’action [CostInitialize](costinitialize-action.md), l’action [FileCost](filecost-action.md)et l' [action CostFinalize](costfinalize-action.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Session.VerifyDiskSpace
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




