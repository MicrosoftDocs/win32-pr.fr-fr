---
title: Message CB_INSERTSTRING (winuser. h)
description: Insère une chaîne ou des données d’élément dans la liste d’une zone de liste déroulante. Contrairement au \_ message CB ADDSTRING, le \_ message CB INSERTSTRING n’entraîne pas le tri d’une liste avec le \_ style de tri CBS.
ms.assetid: b9067b4e-afca-4c78-9ca2-c717b99c7459
keywords:
- CB_INSERTSTRING les contrôles de message Windows
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
ms.openlocfilehash: 14d050980137bc34652cb2fce39b9f188f4d5cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465263"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
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

 

