---
title: Message TBM_GETTIC (commctrl. h)
description: Récupère la position logique d’une graduation dans un TrackBar. La position logique peut être l’une des valeurs entières dans la plage de la plage de la barre de défilement minimale à la position de curseur maximale.
ms.assetid: 9d70c860-de97-4579-bb10-e9e9db7f1784
keywords:
- TBM_GETTIC les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TBM_GETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d534d5100e20cc544c31fca2fc9e49cda3bd976
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116430"
---
# <a name="tbm_gettic-message"></a>\_Message TBM GETTIC

Récupère la position logique d’une graduation dans un TrackBar. La position logique peut être l’une des valeurs entières dans la plage de la plage de la barre de défilement minimale à la position de curseur maximale.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro identifiant une graduation. Les index valides se trouvent dans la plage comprise entre zéro et deux moins que le nombre de cycles renvoyé par le message [**TBM \_ GETNUMTICS**](tbm-getnumtics.md) .

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la position logique de la graduation spécifiée, ou-1 si *wParam* ne spécifie pas d’index valide.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





