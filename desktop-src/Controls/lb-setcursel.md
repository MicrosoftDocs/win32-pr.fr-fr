---
title: Message LB_SETCURSEL (winuser. h)
description: Sélectionne une chaîne et la fait défiler en vue, si nécessaire. Lorsque la nouvelle chaîne est sélectionnée, la zone de liste supprime la mise en surbrillance de la chaîne précédemment sélectionnée.
ms.assetid: 28d81f9d-a926-400c-8803-dcdb0e8f193d
keywords:
- LB_SETCURSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77d1305ccece9c220d6a20e72e0ee54a428f8b13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511794"
---
# <a name="lb_setcursel-message"></a>\_Message SETCURSEL lb

Sélectionne une chaîne et la fait défiler en vue, si nécessaire. Lorsque la nouvelle chaîne est sélectionnée, la zone de liste supprime la mise en surbrillance de la chaîne précédemment sélectionnée.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie l’index de base zéro de la chaîne sélectionnée. Si ce paramètre a la valeur-1, la zone de liste est définie sur ne pas sélectionner.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits. Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments. Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une erreur se produit, la valeur de retour est LB \_ Err. Si le paramètre *wParam* est-1, la valeur de retour est lb \_ Err même si aucune erreur ne s’est produite.

## <a name="remarks"></a>Notes

Utilisez ce message uniquement avec les zones de liste à sélection unique. Vous ne pouvez pas l’utiliser pour définir ou supprimer une sélection dans une zone de liste à sélection multiple.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETCURSEL lb**](lb-getcursel.md)
</dt> </dl>

 

 





