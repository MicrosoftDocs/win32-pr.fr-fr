---
title: Windows Constantes de mouvements tactiles (winuser. h)
description: cette section répertorie les constantes utilisées pour Windows les gestes tactiles.
ms.assetid: C5C3C533-A781-47EF-8209-2D94A94C9097
topic_type:
- apiref
api_name:
- GESTURECONFIGMAXCOUNT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/18/2020
ms.openlocfilehash: 3e980619a4f0f2a0df83ebfbe2fb8e8a767ef5f988e2bb3b769bde64e714eb80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435225"
---
# <a name="windows-touch-gestures-constants"></a>Windows Constantes de mouvements tactiles

cette section répertorie les constantes utilisées pour Windows les gestes tactiles.

<dl> <dt>

**GESTURECONFIGMAXCOUNT**
</dt> <dd> <dl> <dt>

256
</dt> <dt>

Définit le nombre maximal de configurations de mouvement qui peuvent être incluses dans un seul appel à [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) ou [**GetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig).

</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[**GetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig), [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig), [Windows les gestes tactiles](multi-touch-gestures.md)
