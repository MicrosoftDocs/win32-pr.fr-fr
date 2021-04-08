---
title: Message LB_DELETESTRING (winuser. h)
description: Supprime une chaîne dans une zone de liste.
ms.assetid: 3f360e07-b70d-4bfc-89d4-18d3b18b0fcf
keywords:
- LB_DELETESTRING les contrôles de message Windows
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
ms.openlocfilehash: 557256484ad5c5fa698d787144a37ff619b02ef2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844037"
---
# <a name="lb_deletestring-message"></a>\_Message DELETESTRING lb

Supprime une chaîne dans une zone de liste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la chaîne à supprimer.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits. Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments. Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est le nombre de chaînes restantes dans la liste. La valeur de retour est LB \_ Err si le paramètre *wParam* spécifie un index supérieur au nombre d’éléments de la liste.

## <a name="remarks"></a>Notes

Si une application crée la zone de liste avec un style owner-drawn, mais sans le style [**\_ HASSTRINGS kg**](list-box-styles.md) , le système envoie un message [**WM \_ DELETEITEM**](wm-deleteitem.md) au propriétaire de la zone de liste afin que l’application puisse libérer toutes les données supplémentaires associées à l’élément.

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

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**\_INSERTSTRING lb**](lb-insertstring.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





