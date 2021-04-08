---
title: Message CB_GETCURSEL (winuser. h)
description: Une application envoie un \_ message CB GETCURSEL pour récupérer l’index de l’élément actuellement sélectionné, le cas échéant, dans la zone de liste d’une zone de liste déroulante.
ms.assetid: 47bf87f6-637f-48e9-849e-b2acbe5a6a7b
keywords:
- CB_GETCURSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fbc9aa1785738fb061696fbad64598747168269
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844498"
---
# <a name="cb_getcursel-message"></a>\_Message GETCURSEL CB

Une application envoie un message **CB \_ GETCURSEL** pour récupérer l’index de l’élément actuellement sélectionné, le cas échéant, dans la zone de liste d’une zone de liste déroulante.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est l’index de base zéro de l’élément actuellement sélectionné. Si aucun élément n’est sélectionné, il s’agit de CB \_ Err.

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

[**\_SELECTSTRING CB**](cb-selectstring.md)
</dt> <dt>

[**\_SETCURSEL CB**](cb-setcursel.md)
</dt> </dl>

 

 





