---
title: Message MCIWNDM_VALIDATEMEDIA (VFW. h)
description: Le \_ message MCIWNDM VALIDATEMEDIA met à jour les emplacements de début et de fin du contenu, la position actuelle dans le contenu et le TrackBar en fonction du format d’heure actuel.
ms.assetid: 98ac6227-fc90-4276-8e26-2bd005e35dc6
keywords:
- message MCIWNDM_VALIDATEMEDIA Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_VALIDATEMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43cb6e6a4a7c320d4eb6472c3c72da2843d0814c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364339"
---
# <a name="mciwndm_validatemedia-message"></a>\_Message MCIWNDM VALIDATEMEDIA

Le message **MCIWNDM \_ VALIDATEMEDIA** met à jour les emplacements de début et de fin du contenu, la position actuelle dans le contenu et le TrackBar en fonction du format d’heure actuel. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) .


```C++
MCIWNDM_VALIDATEMEDIA 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

En règle générale, vous n’avez pas besoin d’utiliser cette macro. Toutefois, si votre application modifie le format d’heure d’un appareil sans utiliser MCIWnd ; les emplacements de début et de fin du contenu, ainsi que le TrackBar, continuent à utiliser l’ancien format. Vous pouvez utiliser cette macro pour mettre à jour ces valeurs.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia)
</dt> </dl>

 

 





