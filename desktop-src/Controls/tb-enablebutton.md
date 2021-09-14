---
title: Message TB_ENABLEBUTTON (commctrl. h)
description: Active ou désactive le bouton spécifié dans une barre d’outils.
ms.assetid: d73851ee-f909-4b70-9514-c45cd3a7e999
keywords:
- TB_ENABLEBUTTON les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_ENABLEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caf2fe865d49f9c89e31b1701abfcbf7991ae72e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116821"
---
# <a name="tb_enablebutton-message"></a>TO \_ ENABLEBUTTON message

Active ou désactive le bouton spécifié dans une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur de commande du bouton à activer ou à désactiver.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est un **booléen** qui indique s’il faut activer ou désactiver le bouton spécifié. Si la **valeur est true**, le bouton est activé. Si la **valeur est false**, le bouton est désactivé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Lorsqu’un bouton a été activé, il peut être appuyé et activé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

