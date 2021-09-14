---
title: Message PBM_DELTAPOS (commctrl. h)
description: Avance la position actuelle d’une barre de progression d’un incrément spécifié et redessine la barre pour refléter la nouvelle position.
ms.assetid: 92c89434-d50b-45e7-b686-42e9297518b9
keywords:
- PBM_DELTAPOS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PBM_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d0c36bbfdf5a812c8a7ffb2b2cdda6720fb757
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117741"
---
# <a name="pbm_deltapos-message"></a>\_Message PBM DELTAPOS

Avance la position actuelle d’une barre de progression d’un incrément spécifié et redessine la barre pour refléter la nouvelle position.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Montant d’avance de la position.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la position précédente.

## <a name="remarks"></a>Notes

Si l’incrément produit une valeur en dehors de la plage du contrôle, la position est définie sur la limite la plus proche.

Le comportement de ce message n’est pas défini s’il est envoyé à un contrôle dont le style [**PBS est \_ défilant**](progress-bar-control-styles.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





