---
title: Message CBEM_INSERTITEM (commctrl. h)
description: Insère un nouvel élément dans un contrôle ComboBoxEx.
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- CBEM_INSERTITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CBEM_INSERTITEM
- CBEM_INSERTITEMA
- CBEM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4d9627efef4796554dfdbe1d7263747cc6b1c32b2cc00d5619a7cb7953024cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699304"
---
# <a name="cbem_insertitem-message"></a>\_Message CBEM INSERTITEM

Insère un nouvel élément dans un contrôle ComboBoxEx.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) qui contient des informations sur l’élément à insérer. Lorsque le message est envoyé, le membre **iItem** doit être défini pour indiquer l’index de base zéro au niveau duquel insérer l’élément. Pour insérer un élément à la fin de la liste, affectez la valeur-1 au membre **iItem** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index auquel le nouvel élément a été inséré en cas de réussite, ou-1 dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **CBEM \_ INSERTITEMW** (Unicode) et **CBEM \_ INSERTITEMA** (ANSI)<br/>           |



 

 





