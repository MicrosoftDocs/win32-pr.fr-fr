---
title: Message TCM_GETITEM (commctrl. h)
description: Récupère des informations sur un onglet dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl GetItem.
ms.assetid: 41774f14-c4e9-4c98-bc25-3522b2125ed5
keywords:
- TCM_GETITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TCM_GETITEM
- TCM_GETITEMA
- TCM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5403bb85e1b2747d1ab6081d33c25ec20a3b2099fc83b2b15e66b014f558584
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876579"
---
# <a name="tcm_getitem-message"></a>\_Message TCM GETITEM

Récupère des informations sur un onglet dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’onglet.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) qui spécifie les informations à récupérer et à recevoir des informations à propos de l’onglet. Lorsque le message est envoyé, le membre **Mask** spécifie les attributs à retourner. Si le membre de **masque** spécifie la \_ valeur de texte TCIF, le membre **pszText** doit contenir l’adresse de la mémoire tampon qui reçoit le texte de l’élément, et le membre **cchTextMax** doit spécifier la taille de la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Si l' \_ indicateur de texte TCIF est défini dans le membre **Mask** de la structure [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) , le contrôle peut modifier le membre **pszText** de la structure afin qu’il pointe vers le nouveau texte au lieu de remplir la mémoire tampon avec le texte demandé. Le contrôle peut affecter la **valeur null** au membre **pszText** pour indiquer qu’aucun texte n’est associé à l’élément.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TCM \_ GETITEMW** (Unicode) et **TCM \_ GETITEMA** (ANSI)<br/>                   |



 

 





