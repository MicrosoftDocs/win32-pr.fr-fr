---
title: Message EM_SETUNDOLIMIT (RichEdit. h)
description: Définit le nombre maximal d’actions qui peuvent être stockées dans la file d’attente d’annulation d’un contrôle RichEdit.
ms.assetid: 485dbcda-89f4-40de-ad55-cd524958e910
keywords:
- EM_SETUNDOLIMIT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETUNDOLIMIT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771e339e38437ea0299e5da6120fa555fd26148f72ff7da4e0287ed46cc4ad22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697519"
---
# <a name="em_setundolimit-message"></a>\_Message SETUNDOLIMIT em

Définit le nombre maximal d’actions qui peuvent être stockées dans la file d’attente d’annulation d’un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie le nombre maximal d’actions qui peuvent être stockées dans la file d’attente d’annulation.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est le nouveau nombre maximal d’actions d’annulation pour le contrôle RichEdit. Cette valeur peut être inférieure à *wParam* si la mémoire est limitée.

## <a name="remarks"></a>Remarques

Par défaut, le nombre maximal d’actions dans la file d’attente d’annulation est 100. Si vous augmentez ce nombre, la mémoire disponible doit être suffisante pour accueillir le nouveau nombre. Pour de meilleures performances, définissez la limite à la plus petite valeur possible.

La définition de la limite à zéro désactive la fonctionnalité d' **annulation** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**EM- \_ CANREDO**](em-canredo.md)
</dt> <dt>

[**\_GETREDONAME em**](em-getredoname.md)
</dt> <dt>

[**\_GETUNDONAME em**](em-getundoname.md)
</dt> <dt>

[**\_rétablissement em**](em-redo.md)
</dt> <dt>

[**\_Effacer em**](em-undo.md)
</dt> </dl>

 

 





