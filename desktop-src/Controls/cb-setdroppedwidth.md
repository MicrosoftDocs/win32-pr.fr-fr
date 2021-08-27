---
title: Message CB_SETDROPPEDWIDTH (winuser. h)
description: Une application envoie le \_ message CB SETDROPPEDWIDTH pour définir la largeur minimale autorisée, en pixels, de la zone de liste d’une zone de liste déroulante avec la liste \_ déroulante CBS ou le \_ style DropDownList SCC.
ms.assetid: 89f44733-aebe-44ea-b62d-8bd988f1bd6f
keywords:
- CB_SETDROPPEDWIDTH les contrôles de Windows de message
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
ms.openlocfilehash: 05d59aee89c4be18ba8e5013fa1a1e685a56b727d293c833c7f99140b683efeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089049"
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

## <a name="remarks"></a>Remarques

Par défaut, la largeur minimale autorisée de la zone de liste déroulante est égale à zéro. La largeur de la zone de liste est la largeur minimale autorisée ou la largeur de zone de liste déroulante, selon la valeur la plus grande.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETDROPPEDWIDTH CB**](cb-getdroppedwidth.md)
</dt> </dl>

 

 





