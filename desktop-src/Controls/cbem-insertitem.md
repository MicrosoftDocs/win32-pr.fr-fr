---
title: Message CBEM_INSERTITEM (commctrl. h)
description: Insère un nouvel élément dans un contrôle ComboBoxEx.
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- CBEM_INSERTITEM les contrôles de message Windows
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
ms.openlocfilehash: 23e6cb26a575472e53703d65e407a94a024dcfac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516297"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **CBEM \_ INSERTITEMW** (Unicode) et **CBEM \_ INSERTITEMA** (ANSI)<br/>           |



 

 





