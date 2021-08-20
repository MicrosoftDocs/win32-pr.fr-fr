---
title: Message CBEM_GETITEM (commctrl. h)
description: Obtient des informations sur les éléments d’un élément ComboBoxEx donné.
ms.assetid: 2df07ae8-fa84-487c-a4a7-90244dfdb40e
keywords:
- CBEM_GETITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CBEM_GETITEM
- CBEM_GETITEMA
- CBEM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcf4dadf72a9f1fab679599c01c8fd0c6ca3541f2f77a5e8c52a740828966034
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528059"
---
# <a name="cbem_getitem-message"></a>\_Message CBEM GETITEM

Obtient des informations sur les éléments d’un élément ComboBoxEx donné.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) qui reçoit les informations de l’élément.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

Lorsque le message est envoyé, les membres **iItem** et **Mask** de la structure doivent être définis pour indiquer l’index de l’élément cible et le type d’informations à récupérer. D’autres membres sont définis en fonction des besoins. Par exemple, pour récupérer du texte, vous devez définir l' \_ indicateur de texte CBEIF dans le **masque** et assigner une valeur à **cchTextMax**. La définition du membre **iItem** sur-1 permet de récupérer l’élément affiché dans le contrôle d’édition.

Si l' \_ indicateur de texte CBEIF est défini dans le membre **Mask** de la structure [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) , le contrôle peut modifier le membre **pszText** de la structure afin qu’il pointe vers le nouveau texte au lieu de remplir la mémoire tampon avec le texte demandé. Les applications ne doivent pas supposer que le texte sera toujours placé dans la mémoire tampon demandée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **CBEM \_ GETITEMW** (Unicode) et **CBEM \_ GETITEMA** (ANSI)<br/>                 |



 

 





