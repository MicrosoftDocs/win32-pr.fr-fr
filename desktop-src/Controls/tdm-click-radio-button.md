---
title: Message TDM_CLICK_RADIO_BUTTON (commctrl. h)
description: Simule l’action d’un clic sur une case d’option dans une boîte de dialogue de tâche.
ms.assetid: ad1616fc-f64d-4575-8bd1-7ce63185d725
keywords:
- TDM_CLICK_RADIO_BUTTON les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_CLICK_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b76d465b1b937359a3d312a401914d497f9c9b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942759"
---
# <a name="tdm_click_radio_button-message"></a>Message de case d' \_ option de clic TDM \_ \_

Simule l’action d’un clic sur une case d’option dans une boîte de dialogue de tâche.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Valeur **int** qui spécifie l’ID de la case d’option sur laquelle cliquer.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="remarks"></a>Notes

L’ID de case d’option spécifié est envoyé à la fonction de rappel [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) dans le cadre d’un [ \_ \_ \_ clic sur](tdn-radio-button-clicked.md) le code de notification de TDN. Une fois la fonction de rappel retournée, la case d’option est sélectionnée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

