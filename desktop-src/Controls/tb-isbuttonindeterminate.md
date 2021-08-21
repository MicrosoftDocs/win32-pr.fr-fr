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
ms.openlocfilehash: 8d1209147993b770dde4fa5f67078ff16f68dcc213c3ae1fc780f01b7d615b06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503749"
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

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro si le bouton est indéterminé, ou zéro dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





