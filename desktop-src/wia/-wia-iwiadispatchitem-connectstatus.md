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
ms.openlocfilehash: 88cd81d149c57e5e69f8f48f47f539e2c57c970ba1f8f8d4157ff844c3c3b6e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669772"
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

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




