---
title: Message HDM_GETITEM (commctrl. h)
description: Obtient des informations sur un élément dans un contrôle header. Vous pouvez envoyer ce message explicitement ou utiliser la macro Header \_ GetItem.
ms.assetid: fb1330d3-fd28-490c-9caa-4b2b5ff86ba0
keywords:
- HDM_GETITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- HDM_GETITEM
- HDM_GETITEMA
- HDM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 566f8b8e3bdf4e92abfb1fdd5874b8514814792e1d7aae169cc2aca4b2e8d101
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436189"
---
# <a name="hdm_getitem-message"></a>\_Message HDM GETITEM

Obtient des informations sur un élément dans un contrôle header. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**header \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’élément pour lequel les informations doivent être récupérées.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) . Lorsque le message est envoyé, le membre **Mask** indique le type d’informations demandées. Lorsque le message est renvoyé, les autres membres reçoivent les informations demandées. Si le membre de **masque** spécifie zéro, le message retourne la **valeur true** , mais aucune information n’est copiée dans la structure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Si l' \_ indicateur de texte hdi est défini dans le membre **Mask** de la structure [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) , le contrôle peut modifier le membre **pszText** de la structure afin qu’il pointe vers le nouveau texte au lieu de remplir la mémoire tampon avec le texte demandé. Les applications ne doivent pas supposer que le texte sera toujours placé dans la mémoire tampon demandée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **HDM \_ GETITEMW** (Unicode) et **HDM \_ GETITEMA** (ANSI)<br/>                   |



 

 





