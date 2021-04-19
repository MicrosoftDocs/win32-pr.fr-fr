---
description: Récupère l’état de la connexion de l’appareil. Cette propriété s’applique uniquement aux éléments de type périphérique (éléments racines). Les valeurs possibles sont &\# 0034 ; connected&\# 0034 ;, &\# 0034 ; disconnected&\# 0034 ; ou null (si cette propriété ne s’applique pas à l’élément). Lecture seule.
ms.assetid: 44b1713a-5859-4973-8495-e8a67f2344b2
title: Item. ConnectStatus, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.ConnectStatus
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 48e12c35ad98746f5a263680e74a09c814bbc65a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517719"
---
# <a name="itemconnectstatus-property"></a>Item. ConnectStatus, propriété

Récupère l’état de la connexion de l’appareil. Cette propriété s’applique uniquement aux éléments de type périphérique (éléments racines). Les valeurs possibles sont « connected », « Disconnected » ou **null** (si cette propriété ne s’applique pas à l’élément). Lecture seule.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Item.ConnectStatus
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne qui reçoit l’état de la connexion.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




