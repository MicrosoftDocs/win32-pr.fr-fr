---
title: Message TCM_GETCURSEL (commctrl. h)
description: Détermine l’onglet actuellement sélectionné dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl GetCurSel.
ms.assetid: 1caa7fad-da5a-4b26-8e78-12110c126691
keywords:
- TCM_GETCURSEL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3103931e29d150412192a745f8dde7681cff0e94
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116230"
---
# <a name="tcm_getcursel-message"></a>\_Message GETCURSEL TCM

Détermine l’onglet actuellement sélectionné dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’index de l’onglet sélectionné en cas de réussite, ou-1 si aucun onglet n’est sélectionné.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





