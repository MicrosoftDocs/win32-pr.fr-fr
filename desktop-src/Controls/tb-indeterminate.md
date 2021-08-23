---
title: Message TB_INDETERMINATE (commctrl. h)
description: Définit ou efface l’état indéterminé du bouton spécifié dans une barre d’outils.
ms.assetid: 6a0f2b82-8241-4c2e-b349-606975ba1a24
keywords:
- TB_INDETERMINATE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_INDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90845f269d0af1e690d5ddeb02f2a8ec2a2f63ff4f698f1dd0f3e2729d98b72c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078263"
---
# <a name="tb_indeterminate-message"></a>TO \_ message indéterminé

Définit ou efface l’état indéterminé du bouton spécifié dans une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur de commande du bouton dont l’état indéterminé doit être défini ou effacé.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est un **booléen** qui indique s’il faut définir ou désélectionner l’état indéterminé. Si la **valeur est true**, l’état indéterminé est défini. Si la **valeur est false**, l’État est effacé.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

