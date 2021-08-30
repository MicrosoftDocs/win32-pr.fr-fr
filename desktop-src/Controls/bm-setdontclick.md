---
title: Message BM_SETDONTCLICK (winuser. h)
description: Définit un indicateur sur une case d’option qui contrôle la génération de \_ messages sur lesquels un clic a été effectué lorsque le bouton reçoit le focus.
ms.assetid: 91d98bce-abea-4afc-a995-0f426ba7a518
keywords:
- BM_SETDONTCLICK les contrôles de Windows de message
topic_type:
- apiref
api_name:
- BM_SETDONTCLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a118b0e9ed3e1ea797cdd0b690aee0fe3c4cc067b72990d884fdd121fcb80c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921239"
---
# <a name="bm_setdontclick-message"></a>\_Message SETDONTCLICK BM

Définit un indicateur sur une case d’option qui contrôle la génération de messages [ \_ sur lesquels un clic a été effectué](bn-clicked.md) lorsque le bouton reçoit le focus.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Valeur **booléenne** qui spécifie l’État. **True** pour définir l’indicateur, sinon **false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé. Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



 

 





