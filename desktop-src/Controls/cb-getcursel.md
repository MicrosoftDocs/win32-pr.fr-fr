---
title: Message CB_GETCURSEL (winuser. h)
description: Une application envoie un \_ message CB GETCURSEL pour récupérer l’index de l’élément actuellement sélectionné, le cas échéant, dans la zone de liste d’une zone de liste déroulante.
ms.assetid: 47bf87f6-637f-48e9-849e-b2acbe5a6a7b
keywords:
- CB_GETCURSEL les contrôles de Windows de message
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
ms.openlocfilehash: e9bc51f43fd28563be4bc3f024bf6afd35c297648aa6c6cad677aca4582c3737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089259"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_SELECTSTRING CB**](cb-selectstring.md)
</dt> <dt>

[**\_SETCURSEL CB**](cb-setcursel.md)
</dt> </dl>

 

 





