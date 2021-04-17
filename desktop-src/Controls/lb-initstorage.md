---
title: Message LB_INITSTORAGE (winuser. h)
description: Alloue de la mémoire pour le stockage des éléments de zone de liste. Ce message est utilisé avant qu’une application ajoute un grand nombre d’éléments à une zone de liste.
ms.assetid: abc49049-3424-46c6-981a-b858afe88883
keywords:
- LB_INITSTORAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28216705dd0446aeb11adad9d45f9e604171e62c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465374"
---
# <a name="lb_initstorage-message"></a>Message (LB) \_ INITSTORAGE

Alloue de la mémoire pour le stockage des éléments de zone de liste. Ce message est utilisé avant qu’une application ajoute un grand nombre d’éléments à une zone de liste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre d’éléments à ajouter.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits. Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments. Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Quantité de mémoire, en octets, à allouer pour les chaînes d’élément.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message est réussi, la valeur de retour est le nombre total d’éléments pour lesquels la mémoire a été allouée de façon préallouée, c’est-à-dire le nombre total d’éléments ajoutés par tous les messages de l' **équilibrage \_** de charge de la mémoire.

Si le message échoue, la valeur de retour est LB \_ ERRSPACE.

Microsoft Windows NT 4,0 : ce message n’alloue pas la quantité de mémoire spécifiée. Toutefois, elle retourne toujours la valeur spécifiée dans le paramètre *wParam* .

## <a name="remarks"></a>Notes

Le message **lb \_ INITSTORAGE** permet d’accélérer l’initialisation des zones de liste qui comportent un grand nombre d’éléments (plus de 100). Il réserve la quantité de mémoire spécifiée, de sorte que les messages [**lb \_ ADDSTRING**](lb-addstring.md), [**lb \_ INSERTSTRING**](lb-insertstring.md), [**lb \_ dir**](lb-dir.md)et [**\_ ADDFILE lb**](lb-addfile.md) peuvent durer le plus rapidement possible. Vous pouvez utiliser des estimations pour les paramètres *wParam* et *lParam* . Si vous surestime, la mémoire supplémentaire est allouée. Si vous sous-estimez, l’allocation normale est utilisée pour les éléments qui dépassent la quantité demandée.

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

[**\_ADDFILE lb**](lb-addfile.md)
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**direction \_ lb**](lb-dir.md)
</dt> <dt>

[**\_INSERTSTRING lb**](lb-insertstring.md)
</dt> </dl>

 

 





