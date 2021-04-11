---
title: Message LVM_SETITEM (commctrl. h)
description: Définit tout ou partie des attributs d’un élément d’affichage de liste. Vous pouvez également envoyer \_ des SETITEM LVM pour définir le texte d’un sous-élément. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetItem.
ms.assetid: f1189b5d-bce7-4569-b4b9-bd750d7ef505
keywords:
- LVM_SETITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETITEM
- LVM_SETITEMA
- LVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623339c3d1ecc7a74cf20b5e52fb621666391bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032623"
---
# <a name="lvm_setitem-message"></a>\_Message SETITEM LVM

Définit tout ou partie des attributs d’un élément d’affichage de liste. Vous pouvez également envoyer \_ des SETITEM LVM pour définir le texte d’un sous-élément. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) qui contient les nouveaux attributs d’élément. Les membres **iItem** et **iSubItem** identifient l’élément ou le sous-élément, et le membre **Mask** spécifie les attributs à définir. Si le membre de **masque** spécifie la \_ valeur de texte LVIF, le membre **pszText** est l’adresse d’une chaîne terminée par le caractère null et le membre **cchTextMax** est ignoré. Si le membre de **masque** spécifie la \_ valeur d’État LVIF, le membre **stateMask** spécifie les États à modifier et le membre d' **État** contient les valeurs de ces États.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Pour définir les attributs d’un élément de vue de liste, définissez le membre **iItem** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) sur l’index de l’élément et définissez le membre **iSubItem** sur zéro. Pour un élément, vous pouvez définir les membres **State**, **pszText**, **IImage** et **lParam** de la structure **LVITEM** .

Pour définir le texte d’un sous-élément, définissez les membres **iItem** et **iSubItem** pour indiquer le sous-élément spécifique, puis utilisez le membre **pszText** pour spécifier le texte. Vous pouvez également utiliser la macro [**ListView \_ SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) pour définir le texte d’un sous-élément. Vous ne pouvez pas définir les membres **State** ou **lParam** pour les sous-éléments, car les sous-éléments ne possèdent pas ces attributs. Dans la version 4,70 et les versions ultérieures, vous pouvez définir le membre **IImage** pour les sous-éléments. L’image de sous-élément sera affichée si le contrôle List-View a le style étendu [**LVS \_ ex \_ SUBITEMIMAGES**](extended-list-view-styles.md) . Les versions précédentes ignorent l’image de sous-élément.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVM \_ SETITEMW** (Unicode) et **LVM \_ SETITEMA** (ANSI)<br/>                   |



 

 





