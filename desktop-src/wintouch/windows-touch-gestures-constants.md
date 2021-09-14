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
ms.openlocfilehash: be1d8fe9354c7160643dcefb2d35938453ad5b07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196055"
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

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[**GetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig), [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig), [Windows les gestes tactiles](multi-touch-gestures.md)
