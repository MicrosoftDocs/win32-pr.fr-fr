---
title: Message LB_GETSEL (winuser. h)
description: Obtient l’état de sélection d’un élément.
ms.assetid: f92c02e7-3c6d-4649-8798-42eb4a0c51b6
keywords:
- LB_GETSEL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43e27a1bcec021d7416e32d1bae4047f7b2705e347cc396a07dcf6c377ccb48f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085509"
---
# <a name="lb_getsel-message"></a>\_Message GETSEL lb

Obtient l’état de sélection d’un élément.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de l'élément.

Windows 95/Windows 98/Windows Millennium edition (Windows) : le paramètre *wParam* est limité aux valeurs 16 bits. Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments. Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si un élément est sélectionné, la valeur de retour est supérieure à zéro ; dans le cas contraire, il est égal à zéro. Si une erreur se produit, la valeur de retour est LB \_ Err.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETSEL lb**](lb-setsel.md)
</dt> </dl>

 

 





