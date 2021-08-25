---
description: récupère le mode Windows sécurisé actuel. Windows peut être en mode verrouillé, en mode normal déverrouillé ou en mode d’évaluation.
ms.assetid: FD280818-C6DE-4CEA-A772-E239A8DB891F
title: WldpQueryWindowsLockdownMode, fonction (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryWindowsLockdownMode
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 94dc1665dcfa98b27fc15f68a799792b57f428875fefb88c6d35de57bad71b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911289"
---
# <a name="wldpquerywindowslockdownmode-function"></a>WldpQueryWindowsLockdownMode fonction)

récupère le mode Windows sécurisé actuel. Windows peut être en mode verrouillé, en mode normal déverrouillé ou en mode d’évaluation.

## <a name="syntax"></a>Syntaxe


```C++
 WINAPI WldpQueryWindowsLockdownMode(
  _Out_ PWLDP_WINDOWS_LOCKDOWN_MODE lockdownMode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lockdownMode* \[ à\]
</dt> <dd>

en cas de réussite, retourne un [**\_ \_ \_ mode de verrouillage WINDOWS PWLDP**](wldp-windows-lockdown-mode.md) qui indique le mode sécurisé pour l’appareil Windows 10 actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne **S \_ OK** en cas de réussite ou un code d’échec dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1803 \[ uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




