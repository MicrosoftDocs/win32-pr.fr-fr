---
title: Message LB_SETCOUNT (winuser. h)
description: Définit le nombre d’éléments dans une zone de liste créée avec le \_ style NoData et non créé avec le \_ style HASSTRINGS.
ms.assetid: 3ebc4237-24d3-443f-86d5-bdcd66a31baf
keywords:
- LB_SETCOUNT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_SETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2042bcf0e0cbe7f5daacfcf7f493a070860ac9a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999856"
---
# <a name="lb_setcount-message"></a>\_Message SETCOUNT lb

Définit le nombre d’éléments dans une zone de liste créée avec le style [**\_ NoData**](list-box-styles.md) et non créé avec le [**style \_ HASSTRINGS**](list-box-styles.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie le nouveau nombre d’éléments dans la zone de liste.

Windows 95/Windows 98/Windows Millennium edition (Windows) : le paramètre *wParam* est limité aux valeurs 16 bits. Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments. Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si une erreur se produit, la valeur de retour est LB \_ Err. Si la mémoire est insuffisante pour stocker les éléments, la valeur de retour est LB \_ ERRSPACE.

## <a name="remarks"></a>Notes

Le **message \_ SETCOUNT lb** est pris en charge uniquement par les zones de liste créées avec le style de [**\_ données**](list-box-styles.md) de la lbs et non créées avec le style [**\_ HASSTRINGS**](list-box-styles.md) . Toutes les autres zones de liste renvoient l' \_ erreur lb.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LB \_ GETCOUNT**](lb-getcount.md)
</dt> </dl>

 

 





