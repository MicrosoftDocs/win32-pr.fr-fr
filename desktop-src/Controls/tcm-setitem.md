---
title: Message TCM_SETITEM (commctrl. h)
description: Définit tout ou partie des attributs d’un onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetItem.
ms.assetid: 1d9c6607-d8ec-4644-a714-22bc2677aa78
keywords:
- TCM_SETITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TCM_SETITEM
- TCM_SETITEMA
- TCM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee86cd0737c3c50c89a97d3881e2cdfd3850f481
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116158"
---
# <a name="tcm_setitem-message"></a>\_Message SETITEM TCM

Définit tout ou partie des attributs d’un onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’élément.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) qui contient les nouveaux attributs d’élément. Le membre **Mask** spécifie les attributs à définir. Si le membre de **masque** spécifie la \_ valeur de texte TCIF, le membre **pszText** est l’adresse d’une chaîne terminée par le caractère null et le membre **cchTextMax** est ignoré.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TCM \_ SETITEMW** (Unicode) et **TCM \_ SETITEMA** (ANSI)<br/>                   |



 

 





