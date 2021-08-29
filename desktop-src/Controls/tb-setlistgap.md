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
ms.openlocfilehash: 6192a002fcc2aec52c6c294b9eaad3fc55af3bfa3d01a092ae44f5c6d4087559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078173"
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

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

L’intervalle entre les boutons s’applique uniquement à la fenêtre de contrôle de barre d’outils qui reçoit ce message. La réception de ce message déclenche une redessine de la barre d’outils, si la barre d’outils est actuellement visible.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





