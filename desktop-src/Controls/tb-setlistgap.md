---
title: Message TB_SETLISTGAP (commctrl. h)
description: Définit la distance entre les boutons de la barre d’outils dans une barre d’outils spécifique.
ms.assetid: ca8ba6e4-cf70-41ca-ac61-cd13671d4010
keywords:
- TB_SETLISTGAP les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843053"
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

## <a name="remarks"></a>Notes

L’intervalle entre les boutons s’applique uniquement à la fenêtre de contrôle de barre d’outils qui reçoit ce message. La réception de ce message déclenche une redessine de la barre d’outils, si la barre d’outils est actuellement visible.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





