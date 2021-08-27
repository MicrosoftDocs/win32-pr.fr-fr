---
title: Message CB_INSERTSTRING (winuser. h)
description: Insère une chaîne ou des données d’élément dans la liste d’une zone de liste déroulante. Contrairement au \_ message CB ADDSTRING, le \_ message CB INSERTSTRING n’entraîne pas le tri d’une liste avec le \_ style de tri CBS.
ms.assetid: b9067b4e-afca-4c78-9ca2-c717b99c7459
keywords:
- CB_INSERTSTRING les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcebd3ed5c52a40f3ca5d49031948f76edfa9d6d98974cec104c4b8e283c101a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089069"
---
# <a name="cb_insertstring-message"></a>\_Message INSERTSTRING CB

Insère une chaîne ou des données d’élément dans la liste d’une zone de liste déroulante. Contrairement au message [**CB \_ ADDSTRING**](cb-addstring.md) , le message **CB \_ INSERTSTRING** n’entraîne pas le tri d’une liste avec le style de [**\_ Tri CBS**](combo-box-styles.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la position à laquelle insérer la chaîne. Si ce paramètre a la valeur-1, la chaîne est ajoutée à la fin de la liste.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la chaîne terminée par le caractère null à insérer. Si vous créez la zone de liste déroulante avec un style owner-drawn, mais sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , la valeur du paramètre *lParam* est stockée au lieu de la chaîne dans laquelle elle pointe normalement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est l’index de la position à laquelle la chaîne a été insérée. Si une erreur se produit, la valeur de retour est CB \_ Err. Si l’espace disponible est insuffisant pour stocker la nouvelle chaîne, il s’agit de CB \_ ERRSPACE.

Si la zone de liste déroulante a le style [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) et que vous insérez une chaîne plus grande que la zone de liste modifiable, vous devez envoyer un message [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) pour vous assurer que la barre de défilement horizontale s’affiche.

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

[**$ \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md)
</dt> <dt>

[**\_Rép.**](cb-dir.md)
</dt> </dl>

 

