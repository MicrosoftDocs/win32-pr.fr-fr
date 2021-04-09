---
title: Message PBM_DELTAPOS (commctrl. h)
description: Avance la position actuelle d’une barre de progression d’un incrément spécifié et redessine la barre pour refléter la nouvelle position.
ms.assetid: 92c89434-d50b-45e7-b686-42e9297518b9
keywords:
- PBM_DELTAPOS les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033051"
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

## <a name="return-value"></a>Valeur retournée

Retourne la position précédente.

## <a name="remarks"></a>Notes

Si l’incrément produit une valeur en dehors de la plage du contrôle, la position est définie sur la limite la plus proche.

Le comportement de ce message n’est pas défini s’il est envoyé à un contrôle dont le style [**PBS est \_ défilant**](progress-bar-control-styles.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





