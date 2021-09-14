---
title: Message LVM_FINDITEM (commctrl. h)
description: Recherche un élément de vue liste avec les caractéristiques spécifiées. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView FindItem.
ms.assetid: 3b18c8ad-97e6-4f4d-bf89-afb95f925ed1
keywords:
- LVM_FINDITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_FINDITEM
- LVM_FINDITEMA
- LVM_FINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f7dfc19e263a6ab7ad29b5e514fa4e52c1a9ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999841"
---
# <a name="lvm_finditem-message"></a>\_Message FINDITEM LVM

Recherche un élément de vue liste avec les caractéristiques spécifiées. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ FindItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_finditem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’élément à partir duquel commencer la recherche ou-1 pour démarrer à partir du début. L’élément spécifié est lui-même exclu de la recherche.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) qui contient des informations sur les éléments à rechercher.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’index de l’élément en cas de réussite, ou-1 dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVM \_ FINDITEMW** (Unicode) et **LVM \_ FINDITEMA** (ANSI)<br/>                 |



 

 





