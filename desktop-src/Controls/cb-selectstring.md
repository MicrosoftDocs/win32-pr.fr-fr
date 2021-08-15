---
title: Message CB_SELECTSTRING (winuser. h)
description: Recherche dans la liste d’une zone de liste déroulante un élément qui commence par les caractères d’une chaîne spécifiée. Si un élément correspondant est trouvé, il est sélectionné et copié dans le contrôle d’édition.
ms.assetid: c08dff72-7e44-40ed-8b64-513359292829
keywords:
- CB_SELECTSTRING les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bedef20646664e37405c97a97f9e49147cad8acc08c05e33172e44a34298f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019967"
---
# <a name="cb_selectstring-message"></a>\_Message SELECTSTRING CB

Recherche dans la liste d’une zone de liste déroulante un élément qui commence par les caractères d’une chaîne spécifiée. Si un élément correspondant est trouvé, il est sélectionné et copié dans le contrôle d’édition.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de l’élément qui précède le premier élément dans lequel effectuer la recherche. Lorsque la recherche atteint le bas de la liste, elle continue à partir du haut de la liste jusqu’à l’élément spécifié par le paramètre *wParam* . Si *wParam* est-1, la liste entière est recherchée à partir du début.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la chaîne terminée par le caractère null qui contient les caractères à rechercher. La recherche ne respecte pas la casse, par conséquent, cette chaîne peut contenir n’importe quelle combinaison de lettres majuscules et minuscules.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la chaîne est trouvée, la valeur de retour est l’index de l’élément sélectionné. Si la recherche échoue, la valeur de retour est CB \_ Err et la sélection actuelle n’est pas modifiée.

## <a name="remarks"></a>Remarques

Une chaîne est sélectionnée uniquement si les caractères à partir du point de départ correspondent aux caractères de la chaîne de préfixe.

Si vous créez la zone de liste déroulante avec un style owner-drawn mais sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , ce que fait le message **\_ SELECTSTRING CB** varie selon que vous utilisez le style de [**\_ Tri CBS**](combo-box-styles.md) . Si le style de **\_ Tri CBS** est utilisé, le système envoie des messages [**WM \_ COMPAREITEM**](wm-compareitem.md) au propriétaire de la zone de liste déroulante pour déterminer l’élément qui correspond à la chaîne spécifiée. Si vous n’utilisez pas le style de **\_ Tri CBS** , **CB \_ SELECTSTRING** tente de faire correspondre la valeur **DWORD** à la valeur du paramètre *lParam* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_FindString CB**](cb-findstring.md)
</dt> <dt>

[**\_FINDEXACTSTRING CB**](cb-findstringexact.md)
</dt> <dt>

[**\_SETCURSEL CB**](cb-setcursel.md)
</dt> <dt>

[**\_COMPAREITEM WM**](wm-compareitem.md)
</dt> </dl>

 

 





