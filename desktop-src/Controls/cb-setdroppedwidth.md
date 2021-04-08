---
title: Message CB_SETDROPPEDWIDTH (winuser. h)
description: Une application envoie le \_ message CB SETDROPPEDWIDTH pour définir la largeur minimale autorisée, en pixels, de la zone de liste d’une zone de liste déroulante avec la liste \_ déroulante CBS ou le \_ style DropDownList SCC.
ms.assetid: 89f44733-aebe-44ea-b62d-8bd988f1bd6f
keywords:
- CB_SETDROPPEDWIDTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_SETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c4f5ce64bfb1b48e9e811027792a11e4358edc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843561"
---
# <a name="cb_setdroppedwidth-message"></a>\_Message SETDROPPEDWIDTH CB

Une application envoie le message **CB \_ SETDROPPEDWIDTH** pour définir la largeur minimale autorisée, en pixels, de la zone de liste d’une zone de liste déroulante avec la liste [**\_ déroulante CBS**](combo-box-styles.md) ou le style [**\_ DropDownList SCC**](combo-box-styles.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Largeur minimale autorisée de la zone de liste, en pixels.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message est réussi, la valeur de retour est la nouvelle largeur de la zone de liste.

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

[**\_GETDROPPEDWIDTH CB**](cb-getdroppedwidth.md)
</dt> </dl>

 

 





