---
title: Message TB_SETLISTGAP (commctrl. h)
description: Définit la distance entre les boutons de la barre d’outils dans une barre d’outils spécifique.
ms.assetid: ca8ba6e4-cf70-41ca-ac61-cd13671d4010
keywords:
- TB_SETLISTGAP les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETLISTGAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 224a709b7beefcfdf49ea7838f905977487aca8d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116541"
---
# <a name="tb_setlistgap-message"></a>TO \_ SETLISTGAP message

Définit la distance entre les boutons de la barre d’outils dans une barre d’outils spécifique.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Intervalle, en pixels, entre les boutons de la barre d’outils.

</dd> <dt>

*lParam* 
</dt> <dd>

Ignoré.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

L’intervalle entre les boutons s’applique uniquement à la fenêtre de contrôle de barre d’outils qui reçoit ce message. La réception de ce message déclenche une redessine de la barre d’outils, si la barre d’outils est actuellement visible.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





