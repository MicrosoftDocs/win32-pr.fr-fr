---
title: Message LVM_REDRAWITEMS (commctrl. h)
description: Force un contrôle List-View à redessiner une plage d’éléments. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView RedrawItems.
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- LVM_REDRAWITEMS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_REDRAWITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53fbee43ff8cfcbb14ab357b6e76ab709df3e4a797143d5c4fa2c9b1179153af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261729"
---
# <a name="lvm_redrawitems-message"></a>\_Message REDRAWITEMS LVM

Force un contrôle List-View à redessiner une plage d’éléments. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ RedrawItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index du premier élément à redessiner.

</dd> <dt>

*lParam* 
</dt> <dd>

Index du dernier élément à redessiner.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Les éléments spécifiés ne sont pas réellement redessinés tant que la fenêtre de vue liste n’a pas reçu de message de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) à redessiner. Pour redessiner immédiatement, appelez la fonction [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) après avoir utilisé cette macro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

