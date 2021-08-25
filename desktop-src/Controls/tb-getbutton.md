---
title: Message TB_GETBUTTON (commctrl. h)
description: Récupère des informations sur le bouton spécifié dans une barre d’outils.
ms.assetid: d90d053c-0daf-4a5a-b7ca-b9b4472c65a3
keywords:
- TB_GETBUTTON les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e36d8cd4e382570884b0cb30f7c95615e2342544cab0970e9864e9fde7882f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919029"
---
# <a name="tb_getbutton-message"></a>TO \_ GETBUTTON message

Récupère des informations sur le bouton spécifié dans une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro du bouton pour lequel des informations doivent être récupérées.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) qui reçoit les informations sur le bouton.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





