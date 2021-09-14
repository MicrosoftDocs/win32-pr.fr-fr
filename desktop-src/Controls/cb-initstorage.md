---
title: Message CB_INITSTORAGE (winuser. h)
description: Une application envoie le \_ message CB INITSTORAGE avant l’ajout d’un grand nombre d’éléments à la partie zone de liste d’une zone de liste déroulante. Ce message alloue de la mémoire pour le stockage des éléments de zone de liste.
ms.assetid: fb289968-a95b-4ca0-977d-b8651166f357
keywords:
- CB_INITSTORAGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78c2ae2592d89ba7a0f6392666dac0404d52e39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124129"
---
# <a name="cb_initstorage-message"></a>Message de la CB- \_ INITSTORAGE

Une application envoie le message **CB \_ INITSTORAGE** avant l’ajout d’un grand nombre d’éléments à la partie zone de liste d’une zone de liste déroulante. Ce message alloue de la mémoire pour le stockage des éléments de zone de liste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre d’éléments à ajouter.

</dd> <dt>

*lParam* 
</dt> <dd>

Quantité de mémoire à allouer pour les chaînes d’élément, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si le message est réussi, la valeur de retour est le nombre total d’éléments pour lesquels la mémoire a été préallouée, c’est-à-dire le nombre total d’éléments ajoutés par tous les messages **CB \_ INITSTORAGE** réussis.

Si le message échoue, la valeur de retour est CB \_ ERRSPACE.

Le message alloue de la mémoire et retourne les valeurs de réussite et d’erreur décrites ci-dessus.

## <a name="remarks"></a>Notes

Le message **CB \_ INITSTORAGE** permet d’accélérer l’initialisation des zones de liste déroulante qui ont un grand nombre d’éléments (plus de 100). Il réserve la quantité de mémoire spécifiée afin que les messages [**CB \_ ADDSTRING**](cb-addstring.md), [**CB \_ INSERTSTRING**](cb-insertstring.md)et [**CB \_ dir**](cb-dir.md) suivants prennent le plus de temps possible. Vous pouvez utiliser des estimations pour les paramètres *wParam* et *lParam* . Si vous surestime, la mémoire supplémentaire est allouée, si vous sous-estimez que l’allocation normale est utilisée pour les éléments qui dépassent la quantité demandée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**$ \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**\_Rép.**](cb-dir.md)
</dt> <dt>

[**\_INSERTSTRING CB**](cb-insertstring.md)
</dt> </dl>

 

 





