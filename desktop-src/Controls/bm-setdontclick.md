---
title: Message BM_SETDONTCLICK (winuser. h)
description: Définit un indicateur sur une case d’option qui contrôle la génération de \_ messages sur lesquels un clic a été effectué lorsque le bouton reçoit le focus.
ms.assetid: 91d98bce-abea-4afc-a995-0f426ba7a518
keywords:
- BM_SETDONTCLICK les contrôles de message Windows
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
ms.openlocfilehash: c8596ec679ff07b87b3433d5b5a7805698f56f84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513583"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



 

 





