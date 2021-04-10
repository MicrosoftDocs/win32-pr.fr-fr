---
title: Message EM_SETUNDOLIMIT (RichEdit. h)
description: Définit le nombre maximal d’actions qui peuvent être stockées dans la file d’attente d’annulation d’un contrôle RichEdit.
ms.assetid: 485dbcda-89f4-40de-ad55-cd524958e910
keywords:
- EM_SETUNDOLIMIT les contrôles de message Windows
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
ms.openlocfilehash: c5b668d047f1de6d8720f09af5baf23e7cfc9cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942292"
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

## <a name="remarks"></a>Notes

Par défaut, le nombre maximal d’actions dans la file d’attente d’annulation est 100. Si vous augmentez ce nombre, la mémoire disponible doit être suffisante pour accueillir le nouveau nombre. Pour de meilleures performances, définissez la limite à la plus petite valeur possible.

La définition de la limite à zéro désactive la fonctionnalité d' **annulation** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
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

 

 





