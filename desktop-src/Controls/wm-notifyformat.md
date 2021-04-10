---
title: Message WM_NOTIFYFORMAT (winuser. h)
description: Détermine si une fenêtre accepte des structures ANSI ou Unicode dans le \_ message de notification WM Notify. Les \_ messages WM NOTIFYFORMAT sont envoyés à partir d’un contrôle commun à sa fenêtre parente et de la fenêtre parente au contrôle commun.
ms.assetid: 45ddef45-3300-448d-b609-5fe931b08336
keywords:
- WM_NOTIFYFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_NOTIFYFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e9c7d74b21d0f5785273d1b60d612a346f2d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942370"
---
# <a name="wm_notifyformat-message"></a>\_Message WM NOTIFYFORMAT

Détermine si une fenêtre accepte des structures ANSI ou Unicode dans le message de notification [**WM \_ Notify**](wm-notify.md) . **WM \_** Les messages NOTIFYFORMAT sont envoyés à partir d’un contrôle commun à sa fenêtre parente et de la fenêtre parente au contrôle commun.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre qui envoie le message **WM \_ NOTIFYFORMAT** . Si *lParam* est \_ une requête NF, ce paramètre est le handle d’un contrôle. Si *lParam* est NF \_ Requery, ce paramètre est le handle de la fenêtre parente d’un contrôle.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur de commande qui spécifie la nature du message **WM \_ NOTIFYFORMAT** . Il s’agit de l’une des valeurs suivantes :



| Valeur                                                                                                                                                | Signification                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NF_QUERY"></span><span id="nf_query"></span><dl> <dt>**\_requête NF**</dt> </dl>       | Le message est une requête qui détermine si les structures ANSI ou Unicode doivent être utilisées dans les messages de [**\_ notification WM**](wm-notify.md) . Cette commande est envoyée à partir d’un contrôle à sa fenêtre parente pendant la création d’un contrôle et en réponse à une \_ commande de REREQUÊTE NF.<br/>                                                                                                         |
| <span id="NF_REQUERY"></span><span id="nf_requery"></span><dl> <dt>**rerequête NF \_**</dt> </dl> | Le message est une demande pour qu’un contrôle envoie un \_ formulaire de requête NF de ce message à sa fenêtre parente. Cette commande est envoyée à partir de la fenêtre parente. La fenêtre parente demande au contrôle de le redemander sur le type de structures à utiliser dans les messages [**WM \_ Notify**](wm-notify.md) . Si *lParam* est NF \_ Requery, la valeur de retour est le résultat de l’opération de rerequête.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs suivantes.



| Code de retour                                                                                 | Description                                                                                                    |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ANSI NFR**</dt> </dl>    | Les structures ANSI doivent être utilisées dans les messages de [**\_ notification WM**](wm-notify.md) envoyés par le contrôle.<br/>     |
| <dl> <dt>**\_Unicode NFR**</dt> </dl> | Les structures Unicode doivent être utilisées dans les messages de [**\_ notification WM**](wm-notify.md) envoyés par le contrôle. <br/> |
| <dl> <dt>**0**</dt> </dl>            | Une erreur est survenue.<br/>                                                                                  |



 

## <a name="remarks"></a>Notes

Lorsqu’un contrôle commun est créé, le contrôle envoie un message **WM \_ NOTIFYFORMAT** à sa fenêtre parente pour déterminer le type de structures à utiliser dans les messages de [**\_ notification WM**](wm-notify.md) . Si la fenêtre parente ne gère pas ce message, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) répond en fonction du type de la fenêtre parente. Autrement dit, si la fenêtre parente est une fenêtre Unicode, **DefWindowProc** retourne des \_ Unicode NFR et, si la fenêtre parente est une fenêtre ANSI, **DefWindowProc** retourne NFR \_ ANSI. Si la fenêtre parente est une boîte de dialogue et ne gère pas ce message, la fonction [**DefDlgProc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) répond de la même manière en fonction du type de la boîte de dialogue (Unicode ou ANSI).

Une fenêtre parente peut modifier le type de structures qu’un contrôle commun utilise dans les messages de [**\_ notification WM**](wm-notify.md) en affectant à *lParam* la valeur NF \_ Requery et en envoyant un message **WM \_ NOTIFYFORMAT** au contrôle. Ainsi, le contrôle envoie un \_ formulaire de requête NF du message **WM \_ NOTIFYFORMAT** à la fenêtre parente.

Tous les contrôles communs vont envoyer les messages **WM \_ NOTIFYFORMAT** . Toutefois, ce n’est pas le cas des contrôles Windows standard (contrôles d’édition, zones de liste déroulante, zones de liste, boutons, barres de défilement et contrôles statiques).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

