---
title: Message RB_SIZETORECT (commctrl. h)
description: Tente de trouver la meilleure disposition des bandes pour le rectangle donné.
ms.assetid: c6242b54-bd65-489b-b417-9680cc39b64a
keywords:
- RB_SIZETORECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- RB_SIZETORECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3db5727ee8c94d2473b503c9a81b7669bb829a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117197"
---
# <a name="rb_sizetorect-message"></a>\_Message SIZETORECT RB

Tente de trouver la meilleure disposition des bandes pour le rectangle donné.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui spécifie le rectangle vers lequel le contrôle rebar doit être dimensionné.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur différente de zéro si une modification de disposition s’est produite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Notes

Les bandes rebar sont organisées et encapsulées si nécessaire pour s’ajuster au rectangle. Les bandes qui ont le \_ style RBBS VARIABLEHEIGHT sont redimensionnées aussi uniformément que possible pour s’adapter au rectangle. La hauteur d’un Rebar horizontal ou la largeur d’un Rebar vertical peut changer en fonction de la nouvelle disposition.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

