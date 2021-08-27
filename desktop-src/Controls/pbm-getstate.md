---
title: Message PBM_GETSTATE (commctrl. h)
description: Obtient l’état de la barre de progression.
ms.assetid: ff240160-7db6-4711-8d4e-25a77dfba118
keywords:
- PBM_GETSTATE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PBM_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cd157ccb6ab8a1fe4cd4a31bf1f8a033f0e591288338e21cc322a8ac10bfc41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047009"
---
# <a name="pbm_getstate-message"></a>\_Message PBM GETSTATE

Obtient l’état de la barre de progression.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’état actuel de la barre de progression. Une des valeurs suivantes.



| Code de retour                                                                                 | Description             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**PBST \_ normal**</dt> </dl> | En cours.<br/> |
| <dl> <dt>**\_erreur PBST**</dt> </dl>  | Erreur.<br/>       |
| <dl> <dt>**PBST \_ suspendu**</dt> </dl> | Suspendu.<br/>      |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





