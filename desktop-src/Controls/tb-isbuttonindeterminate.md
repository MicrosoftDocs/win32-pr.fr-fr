---
title: Message TB_ISBUTTONINDETERMINATE (commctrl. h)
description: Détermine si le bouton spécifié dans une barre d’outils est indéterminé.
ms.assetid: b4d759b3-cdbc-417b-9da4-4ed9edc38c0e
keywords:
- TB_ISBUTTONINDETERMINATE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_ISBUTTONINDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29fc024efcad9f0f48ae4882b019269903c249bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116649"
---
# <a name="tb_isbuttonindeterminate-message"></a>TO \_ ISBUTTONINDETERMINATE message

Détermine si le bouton spécifié dans une barre d’outils est indéterminé.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur de commande du bouton.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur différente de zéro si le bouton est indéterminé, ou zéro dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





