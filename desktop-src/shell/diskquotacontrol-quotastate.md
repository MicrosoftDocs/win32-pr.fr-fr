---
description: Définit ou obtient l’état des quotas de disque du volume.
title: DiskQuotaControl. QuotaState, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaState
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b0766ecf-6e22-4481-a6a7-df873a277bc2
ms.openlocfilehash: 460decc1068642ae797723b31f7350082f591d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485521"
---
# <a name="diskquotacontrolquotastate-property"></a>DiskQuotaControl. QuotaState, propriété

Définit ou obtient l’état des quotas de disque du volume.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
iQuotaState = DiskQuotaControl.QuotaState
DiskQuotaControl.QuotaState = iQuotaState
```



## <a name="property-value"></a>Valeur de la propriété

Cette propriété peut être définie sur l’une des valeurs suivantes.



| État          | Valeur | Description               |
|----------------|-------|---------------------------|
| dqStateDisable | 0     | Les quotas de disque sont désactivés. |
| dqStateTrack   | 1     | Les quotas de disque sont désactivés. |
| dqStateEnforce | 2     | Appliquer la limite de quota.      |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




