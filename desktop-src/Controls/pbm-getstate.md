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
ms.openlocfilehash: 07d4f7029fca46a046545efd1cea8e0eab99c757
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117722"
---
# <a name="pbm_getstate-message"></a>\_Message PBM GETSTATE

Obtient l’état de la barre de progression.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’état actuel de la barre de progression. Une des valeurs suivantes.



| Code de retour                                                                                 | Description             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**PBST \_ normal**</dt> </dl> | En cours.<br/> |
| <dl> <dt>**\_erreur PBST**</dt> </dl>  | Erreur.<br/>       |
| <dl> <dt>**PBST \_ suspendu**</dt> </dl> | Suspendu.<br/>      |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





