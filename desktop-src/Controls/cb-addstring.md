---
title: Message CB_ADDSTRING (winuser. h)
description: Ajoute une chaîne à la zone de liste d’une zone de liste déroulante. Si la zone de liste déroulante n’a pas le \_ style de tri CBS, la chaîne est ajoutée à la fin de la liste. Dans le cas contraire, la chaîne est insérée dans la liste et la liste est triée.
ms.assetid: 201bcb7b-e7d1-41e6-8eb7-a5864b659a52
keywords:
- CB_ADDSTRING les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda16367ec24e869f6cb664e89751d7a13efec3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942669"
---
# <a name="cb_addstring-message"></a>\_Message CB ADDSTRING

Ajoute une chaîne à la zone de liste d’une zone de liste déroulante. Si la zone de liste déroulante n’a pas le style de [**\_ Tri CBS**](combo-box-styles.md) , la chaîne est ajoutée à la fin de la liste. Dans le cas contraire, la chaîne est insérée dans la liste et la liste est triée.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur **LPCTSTR** vers la chaîne terminée par le caractère null à ajouter. Si vous créez la zone de liste déroulante avec un style owner-drawn mais sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , la valeur du paramètre *lParam* est stockée en tant que données d’élément et non pas en tant que chaîne vers laquelle pointe. Les données d’élément peuvent être récupérées ou modifiées en envoyant le message [**CB \_ GETITEMDATA**](cb-getitemdata.md) ou [**CB \_ SETITEMDATA**](cb-setitemdata.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est l’index de base zéro de la chaîne dans la zone de liste de la zone de liste déroulante. Si une erreur se produit, la valeur de retour est CB \_ Err. Si l’espace disponible est insuffisant pour stocker la nouvelle chaîne, il s’agit de CB \_ ERRSPACE.

## <a name="remarks"></a>Notes

Si vous créez une zone de liste déroulante owner-drawn avec le style de [**\_ Tri CBS**](combo-box-styles.md) mais sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , le message [**WM \_ COMPAREITEM**](wm-compareitem.md) est envoyé une ou plusieurs fois au propriétaire de la zone de liste déroulante afin que le nouvel élément puisse être placé correctement dans la liste.

Pour insérer une chaîne à un emplacement spécifique de la liste, utilisez le message [**CB \_ INSERTSTRING**](cb-insertstring.md) .

Si la zone de liste déroulante a le style [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) et que vous ajoutez une chaîne plus grande que la zone de liste déroulante, envoyez un message [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) pour vous assurer que la barre de défilement horizontale s’affiche.

**Comclt32.dll version 5,0 ou ultérieure :** Si les [**\_ majuscules**](combo-box-styles.md) CBS ou les majuscules CBS sont définies, la version Unicode de **CB \_ ADDSTRING** modifie la chaîne. [**\_**](combo-box-styles.md) En cas d’utilisation de la mémoire globale en lecture seule, cela provoque l’échec de l’application.

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

[**\_Rép.**](cb-dir.md)
</dt> <dt>

[**\_INSERTSTRING CB**](cb-insertstring.md)
</dt> <dt>

[**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md)
</dt> <dt>

[**\_COMPAREITEM WM**](wm-compareitem.md)
</dt> </dl>

 

