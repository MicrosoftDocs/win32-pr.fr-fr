---
title: Message LVM_GETITEM (commctrl. h)
description: Récupère une partie ou la totalité des attributs d’un élément d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetItem.
ms.assetid: 684ad96a-2c3b-4148-b66c-41f8322500bb
keywords:
- LVM_GETITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETITEM
- LVM_GETITEMA
- LVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c19632567db5e37059b1b028a8ec1fc9385268cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742996"
---
# <a name="lvm_getitem-message"></a>Message de LVM. \_

Récupère une partie ou la totalité des attributs d’un élément d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) qui spécifie les informations pour récupérer et recevoir des informations sur l’élément de vue de liste.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Lorsque le **message \_ LVM de LVM** est envoyé, les membres **iItem** et **iSubItem** identifient l’élément ou le sous-élément pour lequel récupérer des informations et le membre **Mask** spécifie les attributs à récupérer. Pour obtenir la liste des valeurs possibles, consultez la description de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .

Si l' \_ indicateur de texte LVIF est défini dans le membre **Mask** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , le membre **pszText** doit pointer vers une mémoire tampon valide et le membre **cchTextMax** doit avoir pour valeur le nombre de caractères de cette mémoire tampon. Les applications ne doivent pas supposer que le texte sera nécessairement placé dans la mémoire tampon spécifiée. Le contrôle peut à la place modifier le membre **pszText** de la structure pour pointer vers le nouveau texte, au lieu de le placer dans la mémoire tampon.

Si le membre de **masque** spécifie la \_ valeur d’État LVIF, le membre **stateMask** doit spécifier les bits d’état d’élément à récupérer. Lors de la sortie, le membre d' **État** contient les valeurs des bits d’état spécifiés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVM \_ GETITEMW** (Unicode) et **LVM \_ GETITEMA** (ANSI)<br/>                   |



 

 





