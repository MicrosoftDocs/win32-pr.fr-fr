---
title: Message TDM_CLICK_BUTTON (commctrl. h)
description: Simule l’action d’un clic sur un bouton dans une boîte de dialogue de tâche.
ms.assetid: cc8a8252-3418-4a28-bfb7-11d6e3fee903
keywords:
- TDM_CLICK_BUTTON les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TDM_CLICK_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7758385699a0d280f808a21db4c56487c466c716b3ae0236f77130847cea3aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876169"
---
# <a name="tdm_click_button-message"></a>Message de bouton de \_ clic TDM \_

Simule l’action d’un clic sur un bouton dans une boîte de dialogue de tâche.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

**Entier** qui spécifie l’ID du bouton sur lequel un clic a été effectué.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="remarks"></a>Remarques

L’ID de bouton spécifié par *wParam* est envoyé à la fonction de rappel [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) dans le cadre d’un [ \_ \_ clic sur](tdn-button-clicked.md) le code de notification du bouton TDN. Une fois que la fonction de rappel a été retournée, la boîte de dialogue de tâche est fermée si l’opération \_ a été retournée à partir de la fonction de rappel. Si S \_ false a été retourné à partir de la fonction de rappel, la boîte de dialogue de tâche reste active.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

