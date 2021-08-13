---
description: La propriété ComponentRequestState de l’objet de session obtient ou demande une modification de l’état d’action d’une ligne dans la table des composants.
ms.assetid: d0b50c25-dca6-4bdf-8ee9-490e436fcc5b
title: Session. ComponentRequestState, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3cef17ab3a4781f925e92968bd50dfedddd9a0df8e1781a2f209712fc447ef10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625235"
---
# <a name="sessioncomponentrequeststate-property"></a>Session. ComponentRequestState, propriété

La propriété **ComponentRequestState** de l’objet de [**session**](session-object.md) obtient ou demande une modification de l’état d’action d’une ligne dans la [table des composants](component-table.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Session.ComponentRequestState
```



## <a name="property-value"></a>Valeur de la propriété

Nom de chaîne requis de l’élément de composant, clé primaire de la table des composants.

## <a name="remarks"></a>Remarques



| État de sélection        | Valeur | Description                                                    |
|------------------------|-------|----------------------------------------------------------------|
| Null                   | Null  | Demande qu’aucune action ne soit effectuée pour cet élément.                |
| msiInstallStateAbsent  | 2     | L’élément doit être supprimé.                                         |
| msiInstallStateLocal   | 3     | L’élément doit être installé localement.                               |
| msiInstallStateSource  | 4     | L’élément doit être installé et exécuté à partir du média source.         |
| msiInstallStateDefault | 5     | S’il est installé, l’élément doit être réinstallé dans le même État. |



 

Si la propriété échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




