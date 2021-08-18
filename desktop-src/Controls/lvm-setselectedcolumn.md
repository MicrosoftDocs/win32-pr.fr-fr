---
title: Message LVM_SETSELECTEDCOLUMN (commctrl. h)
description: Définit l’index de la colonne sélectionnée.
ms.assetid: 11b0838e-24a7-4c1c-b67d-0912b5a6442a
keywords:
- LVM_SETSELECTEDCOLUMN les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6564e1fda50d11b3d4c520f85184439b0465f1cf5767e7926e6e1c9476f786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019169"
---
# <a name="lvm_setselectedcolumn-message"></a>\_Message SETSELECTEDCOLUMN LVM

Définit l’index de la colonne sélectionnée.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Valeur de type **int** qui spécifie l’index de colonne.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour n’est pas utilisée.

## <a name="remarks"></a>Remarques

Les index de colonne sont stockés dans un tableau **int** . Consultez le membre **puColumns** de [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema).

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





