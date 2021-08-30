---
title: Message LB_SETANCHORINDEX (winuser. h)
description: Définit l’élément d’ancrage \ 8212 ; autrement dit, l’élément à partir duquel une sélection multiple démarre. Une sélection multiple s’étend sur tous les éléments de l’élément d’ancrage à l’élément du signe insertion.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setanchorindex.htm
keywords:
- LB_SETANCHORINDEX les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_SETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d8e1eba4168cfd6dd9a7e18a5b82b252c08908e9e49ce7059ed8fdef5ea95d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085349"
---
# <a name="lb_setanchorindex-message"></a>\_Message SETANCHORINDEX lb

Définit l’élément d’ancrage qui est l’élément à partir duquel commence une sélection multiple. Une sélection multiple s’étend sur tous les éléments de l’élément d’ancrage à l’élément du signe insertion.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie l’index du nouvel élément d’ancrage.

Windows 95/Windows 98/Windows Millennium edition (Windows) : le paramètre *wParam* est limité aux valeurs 16 bits. Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments. Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message est correctement exécuté, la valeur de retour est zéro.

Si le message échoue, la valeur de retour est LB \_ Err.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETANCHORINDEX lb**](lb-getanchorindex.md)
</dt> </dl>

 

 





