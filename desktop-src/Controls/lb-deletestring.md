---
title: Message LB_DELETESTRING (winuser. h)
description: Supprime une chaîne dans une zone de liste.
ms.assetid: 3f360e07-b70d-4bfc-89d4-18d3b18b0fcf
keywords:
- LB_DELETESTRING les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3329f82babea73a6392f7c360623fdeadec843dfcfd62e70106e7fb1cb0367ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671674"
---
# <a name="lb_deletestring-message"></a>\_Message DELETESTRING lb

Supprime une chaîne dans une zone de liste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la chaîne à supprimer.

Windows 95/Windows 98/Windows Millennium edition (Windows) : le paramètre *wParam* est limité aux valeurs 16 bits. Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments. Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est le nombre de chaînes restantes dans la liste. La valeur de retour est LB \_ Err si le paramètre *wParam* spécifie un index supérieur au nombre d’éléments de la liste.

## <a name="remarks"></a>Remarques

Si une application crée la zone de liste avec un style owner-drawn, mais sans le style [**\_ HASSTRINGS kg**](list-box-styles.md) , le système envoie un message [**WM \_ DELETEITEM**](wm-deleteitem.md) au propriétaire de la zone de liste afin que l’application puisse libérer toutes les données supplémentaires associées à l’élément.

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

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**\_INSERTSTRING lb**](lb-insertstring.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





