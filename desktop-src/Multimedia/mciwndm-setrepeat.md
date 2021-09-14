---
title: Message MCIWNDM_SETREPEAT (VFW. h)
description: Le \_ message MCIWNDM SETREPEAT définit l’indicateur de répétition associé à la lecture continue.
ms.assetid: 9a8da201-9ce8-4b6c-8b76-cd9e1356c75d
keywords:
- message MCIWNDM_SETREPEAT Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeae2ac3cb57f8ddbb2343ee3f42d30fa8def370
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218537"
---
# <a name="mciwndm_setrepeat-message"></a>\_Message MCIWNDM SETREPEAT

Le message **MCIWNDM \_ SETREPEAT** définit l’indicateur de répétition associé à la lecture continue. Le message **MCIWNDM \_ SETREPEAT** fonctionne conjointement avec la commande [MCI \_ Play](mci-play.md) pour fournir une boucle de lecture continue. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) .


```C++
MCIWNDM_SETREPEAT 
wParam = 0; 
lParam = (LPARAM) (BOOL) f; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="f"></span><span id="F"></span>*FA*
</dt> <dd>

Nouvel état de l’indicateur de répétition. Spécifiez **true** pour activer la lecture continue.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro.

## <a name="remarks"></a>Notes

À l’heure actuelle, MCIAVI est le seul périphérique qui prend en charge la lecture continue.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[\_lecture MCI](mci-play.md)
</dt> <dt>

[**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)
</dt> </dl>

 

 





