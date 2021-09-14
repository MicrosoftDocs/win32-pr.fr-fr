---
title: Message TCM_DELETEALLITEMS (commctrl. h)
description: Supprime tous les éléments d’un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl DeleteAllItems.
ms.assetid: 733494c4-38f4-44ba-98d2-c33a8d63c3b7
keywords:
- TCM_DELETEALLITEMS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TCM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b73a91cd6ec3b5472b6e7da2127f8224062cfbbc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116241"
---
# <a name="tcm_deleteallitems-message"></a>\_Message DELETEALLITEMS TCM

Supprime tous les éléments d’un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteallitems) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





