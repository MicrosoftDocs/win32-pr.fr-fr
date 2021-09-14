---
title: Message TBM_SETTHUMBLENGTH (commctrl. h)
description: Définit la longueur du curseur dans un TrackBar. Ce message est ignoré si le TrackBar n’a pas le \_ style tbs multiple.
ms.assetid: 027fe341-a60a-4dbe-a48a-5ddaadef0b4a
keywords:
- TBM_SETTHUMBLENGTH les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TBM_SETTHUMBLENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d4ac33d2df43a267766e14ab95fb9729692bbee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116369"
---
# <a name="tbm_setthumblength-message"></a>\_Message TBM SETTHUMBLENGTH

Définit la longueur du curseur dans un TrackBar. Ce message est ignoré si le TrackBar n’a pas le style [**tbs \_ multiple**](trackbar-control-styles.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Longueur, en pixels, du curseur.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TBM \_ GETTHUMBLENGTH**](tbm-getthumblength.md)
</dt> </dl>

 

 





