---
title: Message LB_ADDFILE (winuser. h)
description: Ajoute le nom de fichier spécifié à une zone de liste qui contient une liste de répertoires.
ms.assetid: 60426293-779b-4a4b-95a2-4901b5f6a13b
keywords:
- LB_ADDFILE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_ADDFILE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8077bda3015fef36d6383f37f272ddaf25469fcb6930bb38bd0fa8122efc5b55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434479"
---
# <a name="lb_addfile-message"></a>\_Message ADDFILE lb

Ajoute le nom de fichier spécifié à une zone de liste qui contient une liste de répertoires.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une mémoire tampon qui spécifie le nom du fichier à ajouter.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est l’index de base zéro du fichier qui a été ajouté ou LB \_ Err si une erreur se produit.

## <a name="remarks"></a>Remarques

La zone de liste à laquelle *lParam* est ajouté doit avoir été remplie par la fonction [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) .

Le message [**lb \_ INITSTORAGE**](lb-initstorage.md) permet d’accélérer l’initialisation des zones de liste qui comportent un grand nombre d’éléments (plus de 100). Il réserve la quantité de mémoire spécifiée afin que les **messages \_ ADDFILE** suivants prennent le plus rapidement possible. Vous pouvez utiliser des estimations pour les paramètres *wParam* et *lParam* . Si vous surestime, la mémoire supplémentaire est allouée. Si vous sous-estimez, l’allocation normale est utilisée pour les éléments qui dépassent la quantité demandée.

Pour une application ANSI, le système convertit le texte d’une zone de liste en Unicode à l’aide de CP \_ ACP. Cela peut entraîner des problèmes. par exemple, les caractères romains accentués dans une zone de liste non Unicode en japonais Windows sont tronqués. Pour résoudre ce problème, compilez l’application en Unicode ou utilisez une zone de liste owner-drawn.

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

[**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> </dl>

 

 





