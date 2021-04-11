---
title: PSN_QUERYINITIALFOCUS le code de notification (Prsht. h)
description: Envoyé par une feuille de propriétés pour permettre à une page de feuille de propriétés de spécifier quel contrôle de boîte de dialogue doit recevoir le focus initial. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 29b5e598-75b2-4b6f-acdb-171b1f7a1850
keywords:
- Contrôles Windows de code de notification PSN_QUERYINITIALFOCUS
topic_type:
- apiref
api_name:
- PSN_QUERYINITIALFOCUS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc542332440009f6564f384b415657e725edda00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102973"
---
# <a name="psn_queryinitialfocus-notification-code"></a>\_Code de notification PSN QUERYINITIALFOCUS

Envoyé par une feuille de propriétés pour permettre à une page de feuille de propriétés de spécifier quel contrôle de boîte de dialogue doit recevoir le focus initial. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
PSN_QUERYINITIALFOCUS

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) . Effectuez un cast du membre **lParam** de cette structure en un type **HWND** , pour récupérer le handle du contrôle qui reçoit le focus par défaut. La structure contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de cette structure **NMHDR** contient le handle de la feuille de propriétés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour spécifier le contrôle qui doit recevoir le focus, retournez le handle du contrôle. Sinon, retournez zéro et le focus sera placé dans le contrôle par défaut. Pour définir la valeur de retour, la procédure de la boîte de dialogue doit appeler la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec une valeur **\_ MSGRESULT DWL** et retourner **true**.

## <a name="remarks"></a>Notes

Une application ne doit pas appeler la fonction [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) lors de la gestion de ce code de notification. Retourne le handle du contrôle qui doit recevoir le focus, et le gestionnaire de feuille de propriétés gère la modification du focus.

Le \_ Code de notification PSN QUERYINITIALFOCUS n’est pas envoyé si le gestionnaire de feuille de propriétés détermine qu’aucun contrôle de la page ne doit recevoir le focus.

Ce fragment de code implémente un gestionnaire simple pour PSN \_ QUERYINITIALFOCUS. Elle demande que le focus initial soit donné au contrôle d’emplacement **( \_ emplacement IDC**).

``` syntax
case PSN_QUERYINITIALFOCUS :
    SetWindowLong(hDlg,DWL_MSGRESULT, (LPARAM)GetDlgItem(hDlg, IDC_LOCATION));
    return TRUE;
...
```

> [!Note]  
> Ce code de notification n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

