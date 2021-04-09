---
title: Message RB_SIZETORECT (commctrl. h)
description: Tente de trouver la meilleure disposition des bandes pour le rectangle donné.
ms.assetid: c6242b54-bd65-489b-b417-9680cc39b64a
keywords:
- RB_SIZETORECT les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106252"
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

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro si une modification de disposition s’est produite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Notes

Les bandes rebar sont organisées et encapsulées si nécessaire pour s’ajuster au rectangle. Les bandes qui ont le \_ style RBBS VARIABLEHEIGHT sont redimensionnées aussi uniformément que possible pour s’adapter au rectangle. La hauteur d’un Rebar horizontal ou la largeur d’un Rebar vertical peut changer en fonction de la nouvelle disposition.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

