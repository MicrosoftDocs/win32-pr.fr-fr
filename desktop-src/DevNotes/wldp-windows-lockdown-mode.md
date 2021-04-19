---
description: Décrit les modes sécurisés (S) pour un appareil Windows.
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
ms.openlocfilehash: 438a44bec0745ea67b2b40c3f8aa9c0dd6bd0072
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534869"
---
# <a name="wldp_windows_lockdown_mode-enumeration"></a>WLDP \_ \_ énumération du mode de verrouillage Windows \_

Décrit les modes sécurisés (S) pour un appareil Windows. Utilisé principalement dans [**WldpQueryWindowsLockdownMode**](wldpquerywindowslockdownmode.md).

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

Déverrouillé. Utilisé principalement pour les appareils Windows sans le mode S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**WLDP \_ \_ \_ essai en mode de verrouillage Windows \_**
</dt> <dd>

Evaluation. Utilisé principalement pour un appareil d’évaluation Windows 10 avec le mode S. Le mode d’évaluation est un cas particulier pour les appareils Windows 10 avec le mode S : les stratégies sont appliquées, mais il n’existe aucune protection anti-restauration pour l’application de la stratégie.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**WLDP \_ \_ mode de verrouillage Windows \_ \_ verrouillé**
</dt> <dd>

Fermée. Utilisé principalement pour un appareil Windows 10 avec le mode S. Un appareil verrouillé applique les stratégies Device Guard signées fournies avec l’image du système d’exploitation Windows 10 avec le mode S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**WLDP \_ \_ mode de verrouillage Windows \_ \_ maximal**
</dt> <dd>

Valeur d’énumération maximale.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wldp. h</dt> </dl> |



 

 




