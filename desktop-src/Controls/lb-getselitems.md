---
title: Message LB_GETSELITEMS (winuser. h)
description: Remplit une mémoire tampon avec un tableau d’entiers qui spécifient les numéros d’élément des éléments sélectionnés dans une zone de liste à sélection multiple.
ms.assetid: 95dd72ef-76a5-4188-b2c8-d4c5eb2f34e3
keywords:
- LB_GETSELITEMS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_GETSELITEMS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a541c7efb0acb8d462cce42f0323393baff58e51d63e6a78a72a9d334c0eae81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085499"
---
# <a name="lb_getselitems-message"></a>\_Message GETSELITEMS lb

Remplit une mémoire tampon avec un tableau d’entiers qui spécifient les numéros d’élément des éléments sélectionnés dans une zone de liste à sélection multiple.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre maximal d’éléments sélectionnés dont les numéros d’élément doivent être placés dans la mémoire tampon.

Windows 95/Windows 98/Windows Millennium edition (Windows) : le paramètre *wParam* est limité aux valeurs 16 bits. Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments. Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une mémoire tampon suffisamment grand pour le nombre d’entiers spécifiés par le paramètre *wParam* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est le nombre d’éléments placés dans la mémoire tampon. Si la zone de liste est une zone de liste à sélection unique, la valeur de retour est LB \_ Err.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETSELCOUNT lb**](lb-getselcount.md)
</dt> </dl>

 

 





