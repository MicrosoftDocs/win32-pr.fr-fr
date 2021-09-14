---
title: Message LVM_GETFOOTERRECT (commctrl. h)
description: Récupère les coordonnées du pied de page pour un contrôle d’affichage de liste. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetFooterRect.
ms.assetid: f8816f35-c1d2-4072-81d3-0a9a3df53d64
keywords:
- LVM_GETFOOTERRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETFOOTERRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31df3a1b7b29e5ad9191da9e990e04daec99e948
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999834"
---
# <a name="lvm_getfooterrect-message"></a>\_Message GETFOOTERRECT LVM

Récupère les coordonnées du pied de page pour un contrôle d’affichage de liste. Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetFooterRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé. Doit être égal à 0.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) pour recevoir les coordonnées. Le processus appelant est chargé d’allouer cette structure. Les coordonnées reçues sont exprimées en tant que coordonnées clientes.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

