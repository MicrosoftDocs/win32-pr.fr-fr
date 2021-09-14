---
title: Message PBM_SETBKCOLOR (commctrl. h)
description: Définit la couleur d’arrière-plan dans la barre de progression.
ms.assetid: e28af958-babb-4c2e-9202-89b608c22f8e
keywords:
- PBM_SETBKCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PBM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfaf84695221cf998275d76a9d2d67773150da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117710"
---
# <a name="pbm_setbkcolor-message"></a>\_Message PBM SETBKCOLOR

Définit la couleur d’arrière-plan dans la barre de progression.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur **COLORREF** qui spécifie la nouvelle couleur d’arrière-plan. Spécifiez la \_ valeur CLR par défaut pour faire en sorte que la barre de progression utilise sa couleur d’arrière-plan par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la couleur d’arrière-plan précédente ou la \_ valeur CLR par défaut si la couleur d’arrière-plan est la couleur par défaut.

## <a name="remarks"></a>Notes

Lorsque les styles visuels sont activés, ce message n’a aucun effet.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





