---
description: Récupère le mode sécurisé Windows actuel. Les fenêtres peuvent être en mode verrouillé, en mode normal déverrouillé ou en mode d’évaluation.
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
ms.openlocfilehash: fc746270a0634525154417cfba7e1529bee7edfb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201080"
---
# <a name="wldpquerywindowslockdownmode-function"></a>WldpQueryWindowsLockdownMode fonction)

Récupère le mode sécurisé Windows actuel. Les fenêtres peuvent être en mode verrouillé, en mode normal déverrouillé ou en mode d’évaluation.

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

En cas de réussite, retourne un [**\_ \_ \_ mode de verrouillage Windows PWLDP**](wldp-windows-lockdown-mode.md) qui indique le mode sécurisé pour l’appareil Windows 10 actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne **S \_ OK** en cas de réussite ou un code d’échec dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1803 \[ uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




