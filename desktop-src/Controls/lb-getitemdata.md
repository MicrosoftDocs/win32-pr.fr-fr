---
title: Message LB_GETITEMDATA (winuser. h)
description: Obtient la valeur définie par l’application associée à l’élément de zone de liste spécifié.
ms.assetid: 3a3f7fa5-ce04-4e95-86e1-5c7de796d1b6
keywords:
- LB_GETITEMDATA les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bbfdb091fb98c0cf448af1cf5f554f7d0db2b03f53826154f7d62f2f6b27b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019337"
---
# <a name="lb_getitemdata-message"></a>\_Message GETITEMDATA lb

Obtient la valeur définie par l’application associée à l’élément de zone de liste spécifié.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l'élément.

Windows 95/Windows 98/Windows Millennium edition (Windows) : le paramètre *wParam* est limité aux valeurs 16 bits. Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments. Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est la valeur associée à l’élément, ou LB \_ Err si une erreur se produit. Si l’élément se trouve dans une zone de liste owner-drawn et qu’il a été créé sans le style [**\_ HASSTRINGS**](list-box-styles.md) , cette valeur était dans le paramètre *lParam* du message [**lb \_ ADDSTRING**](lb-addstring.md) ou [**lb \_ INSERTSTRING**](lb-insertstring.md) qui a ajouté l’élément à la zone de liste. Dans le cas contraire, il s’agit de la valeur dans le *lParam* du message [**lb \_ SETITEMDATA**](lb-setitemdata.md) .

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

[**\_SETITEMDATA lb**](lb-setitemdata.md)
</dt> </dl>

 

 





