---
title: Message TTM_UPDATETIPTEXT (commctrl. h)
description: Définit le texte d’info-bulle d’un outil.
ms.assetid: 2a7432dd-76f9-42b4-b639-178dce1d89ef
keywords:
- TTM_UPDATETIPTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_UPDATETIPTEXT
- TTM_UPDATETIPTEXTA
- TTM_UPDATETIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c94b14ec83c190ce019ecba1413d2fa05f0103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104434"
---
# <a name="ttm_updatetiptext-message"></a>\_Message atténuation UPDATETIPTEXT

Définit le texte d’info-bulle d’un outil.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . Les membres **HINST** et **lpszText** doivent spécifier le handle d’instance et l’adresse du texte. Les membres **HWND** et **UID** identifient l’outil à mettre à jour. Le membre **cbSize** de cette structure doit être rempli avant l’envoi de ce message.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **Atténuation \_ UPDATETIPTEXTW** (Unicode) et **atténuation \_ UPDATETIPTEXTA** (ANSI)<br/>       |



 

 





