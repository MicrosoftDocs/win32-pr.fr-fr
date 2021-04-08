---
title: Constantes de mouvements tactiles Windows (winuser. h)
description: Cette section répertorie les constantes utilisées pour les gestes tactiles Windows.
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
ms.openlocfilehash: be1d8fe9354c7160643dcefb2d35938453ad5b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942173"
---
# <a name="windows-touch-gestures-constants"></a>Constantes de mouvements tactiles Windows

Cette section répertorie les constantes utilisées pour les gestes tactiles Windows.

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[**GetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig), [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig), [entrées tactiles Windows](multi-touch-gestures.md)
