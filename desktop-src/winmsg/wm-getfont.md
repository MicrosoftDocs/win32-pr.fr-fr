---
description: Récupère la police avec laquelle le contrôle dessine actuellement son texte.
ms.assetid: a6d05ef5-9933-4d03-a677-a8328bf1cb7d
title: Message WM_GETFONT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f9d3dbd4a34557459fa0f31f6e2a96eba9d0cab36d54cf2bddaa353343a18b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200470"
---
# <a name="wm_getfont-message"></a>\_Message WM GETFONT

Récupère la police avec laquelle le contrôle dessine actuellement son texte.


```C++
#define WM_GETFONT                      0x0031
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

Tapez : **Hfont**

La valeur de retour est un handle de la police utilisée par le contrôle, ou **null** si le contrôle utilise la police système.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_SetFont WM**](wm-setfont.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 




