---
title: Message TVM_GETITEM (commctrl. h)
description: Récupère une partie ou la totalité des attributs d’un élément d’affichage d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TreeView GetItem.
ms.assetid: e26ec000-967d-46de-8f71-6ebc36fefe5e
keywords:
- TVM_GETITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_GETITEM
- TVM_GETITEMA
- TVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dff96f4721a3c50eda54792b2b1c003cd808bf11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115693"
---
# <a name="tvm_getitem-message"></a>TVM ( \_ message GETITEM)

Récupère une partie ou la totalité des attributs d’un élément d’affichage d’arborescence. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TreeView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui spécifie les informations pour récupérer et recevoir des informations sur l’élément. Avec la [version 4,71](common-control-versions.md) et les versions ultérieures, vous pouvez utiliser une structure [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) à la place.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Lorsque le message est envoyé, le membre **hitem** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) ou [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifie l’élément sur lequel les informations doivent être récupérées, et le membre **Mask** spécifie les attributs à récupérer.

Si l' \_ indicateur de texte TVIF est défini dans le membre **Mask** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) ou [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) , le membre **pszText** doit pointer vers une mémoire tampon valide et le membre **cchTextMax** doit avoir pour valeur le nombre de caractères de cette mémoire tampon.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVM \_ GETITEMW** (Unicode) et **TVM \_ GETITEMA** (ANSI)<br/>                   |



 

 





