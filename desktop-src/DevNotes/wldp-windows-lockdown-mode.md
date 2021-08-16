---
description: décrit les modes sécurisés pour un appareil Windows.
ms.assetid: CE50AC56-0295-477C-93CB-ABAB92482A59
title: Énumération WLDP_WINDOWS_LOCKDOWN_MODE (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_WINDOWS_LOCKDOWN_MODE
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 93a3ae8ef00c306d93995a3a97236fc9086185147144c4314726c507d8b52e57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911339"
---
# <a name="wldp_windows_lockdown_mode-enumeration"></a>WLDP \_ \_ énumération du mode de verrouillage Windows \_

décrit les modes sécurisés pour un appareil Windows. Utilisé principalement dans [**WldpQueryWindowsLockdownMode**](wldpquerywindowslockdownmode.md).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _WLDP_WINDOWS_LOCKDOWN_MODE { 
  WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED  = 0,
  WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL     = 1,
  WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED    = 2,
  WLDP_WINDOWS_LOCKDOWN_MODE_MAX       = 3
} WLDP_WINDOWS_LOCKDOWN_MODE, *PWLDP_WINDOWS_LOCKDOWN_MODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**\_mode de \_ verrouillage Windows WLDP \_ \_ déverrouillé**
</dt> <dd>

Déverrouillé. principalement utilisé pour les appareils Windows sans le mode S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**WLDP \_ \_ \_ essai en mode de verrouillage Windows \_**
</dt> <dd>

Evaluation. utilisé principalement pour un appareil d’essai Windows 10 avec le mode S. le mode d’évaluation est un cas particulier pour les appareils Windows 10 avec le mode S : les stratégies sont appliquées, mais il n’existe aucune protection anti-restauration pour l’application de la stratégie.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**WLDP \_ \_ mode de verrouillage Windows \_ \_ verrouillé**
</dt> <dd>

Fermée. utilisé principalement pour un appareil Windows 10 avec le mode S. un appareil verrouillé applique les stratégies device Guard signées fournies avec l’image du système d’exploitation Windows 10 avec le mode S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**WLDP \_ \_ mode de verrouillage Windows \_ \_ maximal**
</dt> <dd>

Valeur d’énumération maximale.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wldp. h</dt> </dl> |



 

 




