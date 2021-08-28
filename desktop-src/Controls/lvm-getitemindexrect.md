---
title: Message LVM_GETITEMINDEXRECT (commctrl. h)
description: Récupère le rectangle englobant pour l’intégralité ou une partie d’un sous-élément dans l’affichage actuel d’un contrôle List View. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetItemIndexRect.
ms.assetid: 17704d24-c029-4d41-b198-04d1e78698e0
keywords:
- LVM_GETITEMINDEXRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETITEMINDEXRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91aa3e6d0420bfddb974d13f210c84241cefc5d79f0ee5a82920bdc2961879dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770369"
---
# <a name="lvm_getitemindexrect-message"></a>\_Message GETITEMINDEXRECT LVM

Récupère le rectangle englobant pour l’intégralité ou une partie d’un sous-élément dans l’affichage actuel d’un contrôle List View. Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetItemIndexRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) pour l’élément parent du sous-élément. Le processus appelant est responsable de l’allocation de cette structure et de la définition de ses membres. *wParam* ne doit pas être **null**.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) pour recevoir les coordonnées. Le processus appelant est chargé d’allouer cette structure. *lParam* ne doit pas avoir la **valeur null**. Définissez le membre **supérieur** sur l’index du sous-élément. Définissez le membre de **gauche** sur l’une des valeurs suivantes, indiquant la partie du sous-élément pour laquelle le rectangle englobant doit être récupéré.



| Valeur                                                                                                                                                   | Signification                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <dt>**\_limites LVIR**</dt> </dl> | Retourne le rectangle englobant du sous-élément entier, y compris l’icône et l’étiquette.<br/> |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <dt>**\_icône LVIR**</dt> </dl>       | Retourne le rectangle englobant de l’icône ou de la petite icône du sous-élément.<br/>            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <dt>**\_étiquette LVIR**</dt> </dl>    | Retourne le rectangle englobant du texte du sous-élément.<br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

