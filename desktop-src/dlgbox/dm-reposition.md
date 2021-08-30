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
ms.openlocfilehash: 52fd3978df92e379f4750b4140c137b915d0d1ae21ac0a5124d3e9d87e62d5c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117809"
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

## <a name="return-value"></a>Valeur retournée

Ce message n’a pas de valeur de retour.

## <a name="remarks"></a>Remarques

Ce message n’a aucun effet si la boîte de dialogue est une fenêtre enfant.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d'ensemble des boîtes de dialogue](dialog-boxes.md)
</dt> </dl>

 

 





