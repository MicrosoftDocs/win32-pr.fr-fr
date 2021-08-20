---
title: Message CBEM_SETITEM (commctrl. h)
description: Définit les attributs d’un élément dans un contrôle ComboBoxEx.
ms.assetid: 752df8ea-fd5e-47fa-b729-d019bdde0904
keywords:
- CBEM_SETITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CBEM_SETITEM
- CBEM_SETITEMA
- CBEM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b1010c090283a47404ee93ef5f3bc1cf2d5ffe71a646d6d734cb443152bdd64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527929"
---
# <a name="cbem_setitem-message"></a>\_Message CBEM SETITEM

Définit les attributs d’un élément dans un contrôle ComboBoxEx.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) qui contient les informations d’élément à définir. Lorsque le message est envoyé, le membre de **masque** de la structure doit être défini pour indiquer les attributs qui sont valides et le membre **iItem** doit spécifier l’index de base zéro de l’élément à modifier. L’affectation de la valeur-1 au membre **iItem** modifie l’élément affiché dans le contrôle d’édition.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **CBEM \_ SETITEMW** (Unicode) et **CBEM \_ SETITEMA** (ANSI)<br/>                 |



 

 





