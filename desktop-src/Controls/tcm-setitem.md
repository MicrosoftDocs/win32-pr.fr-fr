---
title: Message TCM_SETITEM (commctrl. h)
description: Définit tout ou partie des attributs d’un onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetItem.
ms.assetid: 1d9c6607-d8ec-4644-a714-22bc2677aa78
keywords:
- TCM_SETITEM les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739885"
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

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TCM \_ SETITEMW** (Unicode) et **TCM \_ SETITEMA** (ANSI)<br/>                   |



 

 





