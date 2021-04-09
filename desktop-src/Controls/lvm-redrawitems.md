---
title: Message LVM_REDRAWITEMS (commctrl. h)
description: Force un contrôle List-View à redessiner une plage d’éléments. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView RedrawItems.
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- LVM_REDRAWITEMS les contrôles de message Windows
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
ms.openlocfilehash: 42568a9ab78361a28a99eee372674287a24d03cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032841"
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

## <a name="remarks"></a>Notes

Les éléments spécifiés ne sont pas réellement redessinés tant que la fenêtre de vue liste n’a pas reçu de message de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) à redessiner. Pour redessiner immédiatement, appelez la fonction [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) après avoir utilisé cette macro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

