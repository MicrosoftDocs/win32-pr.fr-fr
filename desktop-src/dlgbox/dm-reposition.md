---
title: Message DM_REPOSITION (winuser. h)
description: Repositionne une boîte de dialogue de niveau supérieur de façon à ce qu’elle s’ajuste à la zone du bureau. Une application peut envoyer ce message à une boîte de dialogue après l’avoir redimensionnée pour s’assurer que la boîte de dialogue entière reste visible.
ms.assetid: 8386d23e-06ea-4ea7-adde-ac97fc97861d
keywords:
- Boîtes de dialogue de DM_REPOSITION message
topic_type:
- apiref
api_name:
- DM_REPOSITION
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19425d4d77a62117f3fadfdd98f0629b81bf334c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192008"
---
# <a name="dm_reposition-message"></a>\_Message de repositionnement DM

Repositionne une boîte de dialogue de niveau supérieur de façon à ce qu’elle s’ajuste à la zone du bureau. Une application peut envoyer ce message à une boîte de dialogue après l’avoir redimensionnée pour s’assurer que la boîte de dialogue entière reste visible.


```C++
#define WM_USER              0x0400
#define DM_REPOSITION       (WM_USER+2)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Ce message n’a pas de valeur de retour.

## <a name="remarks"></a>Notes

Ce message n’a aucun effet si la boîte de dialogue est une fenêtre enfant.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d'ensemble des boîtes de dialogue](dialog-boxes.md)
</dt> </dl>

 

 





