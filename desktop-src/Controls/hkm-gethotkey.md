---
title: Message HKM_GETHOTKEY (commctrl. h)
description: Obtient le code de touche virtuel et les indicateurs de modificateur d’une touche d’accès rapide à partir d’un contrôle de touche d’accès rapide.
ms.assetid: 8b061411-604d-46ea-a082-3eca2d47d992
keywords:
- HKM_GETHOTKEY les contrôles de Windows de message
topic_type:
- apiref
api_name:
- HKM_GETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79bfbad1eb5e9a6679a1b3e419a0877e61cd90247ef0cf91b0a30c655f755a57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672267"
---
# <a name="hkm_gethotkey-message"></a>\_Message hkm GETHOTKEY

Obtient le code de touche virtuel et les indicateurs de modificateur d’une touche d’accès rapide à partir d’un contrôle de touche d’accès rapide.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le code de touche virtuel et les indicateurs de modificateur. Le [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) du [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est le code de la touche virtuelle de la touche d’accès rapide. Le [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) du **LOWORD** est le modificateur de clé qui spécifie les clés qui définissent une combinaison de touches d’accès rapide. Les indicateurs de modificateur peuvent être une combinaison des valeurs suivantes.



| Valeur            | Signification      |
|------------------|--------------|
| HOTKEYF \_ ALT     | touche ALT      |
| \_contrôle HOTKEYF | Clé de contrôle  |
| HOTKEYF \_ ext     | Clé étendue |
| HOTKEYF \_ Shift   | Touche Maj    |



 

## <a name="remarks"></a>Remarques

La valeur 16 bits retournée par ce message peut être utilisée comme paramètre *wParam* dans le message [**WM \_ SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

