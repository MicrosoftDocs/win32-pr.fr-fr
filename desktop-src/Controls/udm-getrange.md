---
title: Message UDM_GETRANGE (commctrl. h)
description: Récupère les positions minimale et maximale (plage) pour un contrôle up-up.
ms.assetid: fd42538a-8d96-4a9c-a1db-07c3e9afef84
keywords:
- UDM_GETRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- UDM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6fd8467ad4494bea92a4c1f9a68d675ef1471f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200588"
---
# <a name="udm_getrange-message"></a>\_Message GETRANGE UDM

Récupère les positions minimale et maximale (plage) pour un contrôle up-up.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est une valeur 32 bits qui contient les positions minimale et maximale. [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est la position maximale du contrôle et [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est la position minimale.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

