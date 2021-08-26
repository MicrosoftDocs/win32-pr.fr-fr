---
description: Avertit un appbar lorsqu’un événement qui peut affecter la taille et la position du appbar.
ms.assetid: 1016a362-4d2b-410e-aec9-c1cc8f497778
title: Message ABN_POSCHANGED (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92528de38b60c1f4705873427616b1ed7a5be6be5875a21e352d2136313c84df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943599"
---
# <a name="abn_poschanged-message"></a>Message d’ABN \_ POSCHANGED

Avertit un appbar lorsqu’un événement qui peut affecter la taille et la position du appbar. Les événements incluent les modifications de la taille, de la position et de l’état de visibilité de la barre des tâches, ainsi que l’ajout, la suppression ou le redimensionnement d’un autre appbar sur le même côté de l’écran.


```C++
ABN_POSCHANGED
```



## <a name="parameters"></a>Paramètres

Ce message n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Un appbar doit répondre à ce message de notification en envoyant les messages [**ABM \_ QUERYPOS**](abm-querypos.md) et [**ABM \_ SetPos**](abm-setpos.md) . Si sa position a changé, appbar doit appeler la fonction [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) pour se déplacer vers la nouvelle position.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

