---
title: Message MCIWNDM_GETSTART (VFW. h)
description: Le \_ message MCIWNDM GETSTART récupère l’emplacement du début du contenu d’un périphérique ou d’un fichier MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetStart.
ms.assetid: 2350616c-2aac-4ff6-b074-bb785a97cdfb
keywords:
- message MCIWNDM_GETSTART Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTART
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbe88df006f1f98854e42259074d82bbd87dc1
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364276"
---
# <a name="mciwndm_getstart-message"></a>\_Message MCIWNDM GETSTART

Le message **MCIWNDM \_ GETSTART** récupère l’emplacement du début du contenu d’un périphérique ou d’un fichier MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) .


```C++
MCIWNDM_GETSTART 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne l’emplacement au format d’heure actuel.

## <a name="remarks"></a>Remarques

En règle générale, la valeur de retour est zéro ; Toutefois, certains appareils utilisent un emplacement de départ différent de zéro. La recherche de cet emplacement définit l’appareil au début du support.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
</dt> </dl>

 

 





