---
title: Message TDM_CLICK_BUTTON (commctrl. h)
description: Simule l’action d’un clic sur un bouton dans une boîte de dialogue de tâche.
ms.assetid: cc8a8252-3418-4a28-bfb7-11d6e3fee903
keywords:
- TDM_CLICK_BUTTON les contrôles de message Windows
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
ms.openlocfilehash: 5e5933668eca907f36414113091b8901bfb9c110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510965"
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

## <a name="remarks"></a>Notes

L’ID de bouton spécifié par *wParam* est envoyé à la fonction de rappel [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) dans le cadre d’un [ \_ \_ clic sur](tdn-button-clicked.md) le code de notification du bouton TDN. Une fois que la fonction de rappel a été retournée, la boîte de dialogue de tâche est fermée si l’opération \_ a été retournée à partir de la fonction de rappel. Si S \_ false a été retourné à partir de la fonction de rappel, la boîte de dialogue de tâche reste active.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

