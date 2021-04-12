---
title: Message CB_SHOWDROPDOWN (winuser. h)
description: Une application envoie un \_ message CB SHOWDROPDOWN pour afficher ou masquer la zone de liste d’une zone de liste déroulante avec le \_ style déroulant CBS ou le \_ style DropDownList SCC.
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- CB_SHOWDROPDOWN les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_SHOWDROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb66e9a0ecf3b6680fce9aca7f680fd6e6fd13e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105604"
---
# <a name="cb_showdropdown-message"></a>\_Message SHOWDROPDOWN CB

Une application envoie un message **CB \_ SHOWDROPDOWN** pour afficher ou masquer la zone de liste d’une zone de liste déroulante avec le style [**\_ déroulant CBS**](combo-box-styles.md) ou le style [**\_ DropDownList SCC**](combo-box-styles.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur **booléenne** qui spécifie si la zone de liste déroulante doit être affichée ou masquée. La valeur **true** affiche la zone de liste ; la valeur **false** le masque.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est toujours **true**.

## <a name="remarks"></a>Notes

Ce message n’a aucun effet sur une zone de liste déroulante créée avec le style [**\_ simple CBS**](combo-box-styles.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETDROPPEDSTATE CB**](cb-getdroppedstate.md)
</dt> </dl>

 

 





