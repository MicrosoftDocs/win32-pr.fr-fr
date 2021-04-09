---
title: Message CB_GETDROPPEDWIDTH (winuser. h)
description: Obtient la largeur minimale autorisée, en pixels, de la zone de liste d’une zone de liste déroulante avec la \_ liste déroulante CBS ou le \_ style DropDownList SCC.
ms.assetid: d7f37a6c-a623-4b15-8ef7-4b64d85c15fa
keywords:
- CB_GETDROPPEDWIDTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299b360348a6bf7378fdfc9bc9f0959b01366642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032858"
---
# <a name="cb_getdroppedwidth-message"></a>\_Message GETDROPPEDWIDTH CB

Obtient la largeur minimale autorisée, en pixels, de la zone de liste d’une zone de liste déroulante avec la [**\_ liste déroulante CBS**](combo-box-styles.md) ou le style [**\_ DropDownList SCC**](combo-box-styles.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message est correctement exécuté, la valeur de retour est la largeur, en pixels.

Si le message échoue, la valeur de retour est CB \_ Err.

## <a name="remarks"></a>Notes

Par défaut, la largeur minimale autorisée de la zone de liste déroulante est égale à zéro. La largeur de la zone de liste est la largeur minimale autorisée ou la largeur de zone de liste déroulante, selon la valeur la plus grande.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETDROPPEDWIDTH CB**](cb-setdroppedwidth.md)
</dt> </dl>

 

 





