---
title: Message IPM_SETFOCUS (commctrl. h)
description: Définit le focus clavier sur le champ spécifié dans le contrôle d’adresse IP. Tout le texte de ce champ est sélectionné.
ms.assetid: 4b975eb2-85e1-4e33-a803-99b48d2ff5e8
keywords:
- IPM_SETFOCUS les contrôles de message Windows
topic_type:
- apiref
api_name:
- IPM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d713e0a8b7eb838a2db5c4738c801d4fb76b782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104461"
---
# <a name="ipm_setfocus-message"></a>\_Message IPM SetFocus

Définit le focus clavier sur le champ spécifié dans le contrôle d’adresse IP. Tout le texte de ce champ est sélectionné.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de champ de base zéro auquel le focus doit être défini. Si cette valeur est supérieure au nombre de champs, le focus est défini sur le premier champ vide. Si tous les champs ne sont pas vides, le focus est défini sur le premier champ.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





