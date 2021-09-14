---
title: Message CB_SETEDITSEL (winuser. h)
description: Une application envoie un \_ message CB SETEDITSEL pour sélectionner des caractères dans le contrôle d’édition d’une zone de liste déroulante.
ms.assetid: 25a07341-a21c-42a9-a220-62650997757b
keywords:
- CB_SETEDITSEL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_SETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54e09697e266b4e0c4260104e90f454a5e3edfb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120065"
---
# <a name="cb_seteditsel-message"></a>\_Message SETEDITSEL CB

Une application envoie un message **CB \_ SETEDITSEL** pour sélectionner des caractères dans le contrôle d’édition d’une zone de liste déroulante.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de *lParam* spécifie la position de départ. Si le **LOWORD** est-1, la sélection, le cas échéant, est supprimée.

Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) de *lParam* spécifie la position de fin. Si **HIWORD** a la valeur-1, tout le texte de la position de départ jusqu’au dernier caractère dans le contrôle d’édition est sélectionné.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si le message est correctement exécuté, la valeur de retour est **true**. Si le message est envoyé à une zone de liste déroulante avec le style de [**\_ DropDownList SCC**](combo-box-styles.md) , il s’agit de CB \_ Err.

## <a name="remarks"></a>Notes

Les positions sont de base zéro. Le premier caractère du contrôle d’édition est dans la position zéro. Le premier caractère après le dernier caractère sélectionné se trouve à la position de fin. Par exemple, pour sélectionner les quatre premiers caractères du contrôle d’édition, utilisez une position de départ de 0 et une position de fin de 4.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETEDITSEL CB**](cb-geteditsel.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

