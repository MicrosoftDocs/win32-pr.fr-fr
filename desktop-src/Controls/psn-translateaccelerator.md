---
title: PSN_TRANSLATEACCELERATOR le code de notification (Prsht. h)
description: Avertit une feuille de propriétés qu’un message de clavier a été reçu. Elle offre la possibilité d’effectuer une traduction d’accélérateur de clavier privée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 04d67326-92f9-4b92-a27e-354815f3c1a8
keywords:
- Contrôles Windows de code de notification PSN_TRANSLATEACCELERATOR
topic_type:
- apiref
api_name:
- PSN_TRANSLATEACCELERATOR
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dc86866be1154bbd0ef1cf76b3535b7b02496e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510934"
---
# <a name="psn_translateaccelerator-notification-code"></a>\_Code de notification PSN TRANSLATEACCELERATOR

Avertit une feuille de propriétés qu’un message de clavier a été reçu. Elle offre la possibilité d’effectuer une traduction d’accélérateur de clavier privée. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
PSN_TRANSLATEACCELERATOR 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) qui contient des informations sur le code de notification. Cette structure contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de la structure **NMHDR** contient le handle de la feuille de propriétés. Le membre **lParam** de la structure **PSHNOTIFY** est un pointeur vers le [**MSG**](/windows/win32/api/winuser/ns-winuser-msg)du message. Elle peut être convertie en type **LPMSG** , pour accéder aux paramètres du message à traduire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne PSNRET \_ MESSAGEHANDLED pour indiquer qu’aucun traitement supplémentaire n’est nécessaire. Retourne une \_ erreur PSNRET pour demander un traitement normal.

## <a name="remarks"></a>Notes

Pour définir la valeur de retour, la procédure de la boîte de dialogue de la page doit utiliser la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec la valeur MSGRESULT de l’DWL \_ . La procédure de la boîte de dialogue doit retourner **true**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

