---
title: Message MCM_GETMINREQRECT (commctrl. h)
description: Récupère la taille minimale requise pour afficher un mois complet dans un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetMinReqRect.
ms.assetid: f0378338-4809-48e9-9387-ed8b79356f95
keywords:
- MCM_GETMINREQRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- MCM_GETMINREQRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 575636837b1485de62dd5e603a0dea38455c4c99926c13f3bd05101fe2a27eca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062049"
---
# <a name="mcm_getminreqrect-message"></a>\_Message GETMINREQRECT MCM

Récupère la taille minimale requise pour afficher un mois complet dans un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui recevra les informations de rectangle englobant. Ce paramètre doit être une adresse valide et ne peut pas avoir la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro et *lParam* reçoit les informations de limite applicables en cas de réussite. Dans le cas contraire, le message retourne la valeur zéro.

## <a name="remarks"></a>Remarques

La taille de fenêtre minimale requise pour un contrôle de calendrier mensuel dépend de la police actuellement sélectionnée, des styles de contrôle, des métriques système et des paramètres régionaux. Lorsqu’une application modifie tout ce qui affecte la taille de fenêtre minimale, ou traite un message [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) , il doit envoyer des **\_ GETMINREQRECT MCM** pour déterminer la nouvelle taille minimale.

> [!Note]  
> Le rectangle retourné par **MCM \_ GETMINREQRECT** n’inclut pas la largeur de la chaîne « Today », si elle est présente. Si le style [**MCS \_ notoday**](month-calendar-control-styles.md) n’est pas défini, votre application doit également récupérer le rectangle qui définit la largeur de chaîne « aujourd’hui » en envoyant un message [**\_ GETMAXTODAYWIDTH MCM**](mcm-getmaxtodaywidth.md) . Utilisez le plus grand des deux rectangles pour vous assurer que la chaîne « aujourd’hui » n’est pas découpée.

 

Les membres **supérieurs** et **gauches** de la structure vers laquelle pointe *lParam* seront toujours nuls. Les membres **droits** et **inférieurs** représentent la valeur minimale pour *CX* et *CY* requis pour le contrôle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

