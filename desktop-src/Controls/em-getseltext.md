---
title: Message EM_GETSELTEXT (RichEdit. h)
description: Récupère le texte actuellement sélectionné dans un contrôle RichEdit.
ms.assetid: 56af77c3-f2d7-4b5d-895f-a67c141459e3
keywords:
- EM_GETSELTEXT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETSELTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 540567f1b52c936ad085acac8e0374fdb0a912bae06480632263f9676f2948e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019497"
---
# <a name="em_getseltext-message"></a>\_Message GETSELTEXT em

Récupère le texte actuellement sélectionné dans un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit le texte sélectionné. L’application appelante doit s’assurer que la mémoire tampon est suffisamment grande pour contenir le texte sélectionné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message retourne le nombre de caractères copiés, à l’exclusion du caractère null de fin.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





