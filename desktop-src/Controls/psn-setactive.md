---
title: PSN_SETACTIVE le code de notification (Prsht. h)
description: Avertit une page qu’elle va être activée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0cf918b7-9f0d-4dec-8df1-a1d2d8ac6463
keywords:
- PSN_SETACTIVE les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- PSN_SETACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e7b656f5497065378af87408fa87fc16cf9ca2cef3cc710f52a1cd643c2927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409731"
---
# <a name="psn_setactive-notification-code"></a>\_Code de notification PSN

Avertit une page qu’elle va être activée. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
PSN_SETACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) qui contient des informations sur le code de notification. Cette structure contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de cette structure **NMHDR** contient le handle de la feuille de propriétés. Le membre **lParam** de la structure **PSHNOTIFY** ne contient aucune information.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur zéro pour accepter l’activation, ou-1 pour activer la page suivante ou précédente (selon que l’utilisateur a cliqué sur le bouton **suivant** ou **précédent** ). Pour définir l’activation sur une page particulière, retournez l’identificateur de ressource de la page.

## <a name="remarks"></a>Remarques

Le \_ Code de notification PSN est envoyé avant que la page ne soit visible. Une application peut utiliser ce code de notification pour initialiser des données dans la page.

> [!Note]  
> La feuille de propriétés se trouve dans le processus de manipulation de la liste de pages lorsque le \_ Code de notification PSN est envoyé. N’essayez pas d’ajouter, de supprimer ou d’insérer des pages lors de la gestion de ce code de notification. Vous obtiendrez des résultats imprévisibles.

 

Pour définir la valeur de retour, la procédure de la boîte de dialogue de la page doit utiliser la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec la valeur MSGRESULT de la boîte de \_ dialogue, et la procédure de boîte de dialogue doit retourner **true**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

