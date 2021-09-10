---
title: Message MCIWNDM_SETZOOM (VFW. h)
description: Le \_ message MCIWNDM SETZOOM redimensionne une image vidéo en fonction d’un facteur de zoom. Ce Marco ajuste la taille d’une fenêtre MCIWnd tout en conservant les proportions constantes. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndSetZoom.
ms.assetid: c899b678-5ba7-4f0a-9ef9-c5370b3b4ea8
keywords:
- message MCIWNDM_SETZOOM Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80ecb513735c4e62266892e8ad55c7bf5daca151
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364287"
---
# <a name="mciwndm_setzoom-message"></a>\_Message MCIWNDM SETZOOM

Le message **MCIWNDM \_ SETZOOM** redimensionne une image vidéo en fonction d’un facteur de zoom. Ce Marco ajuste la taille d’une fenêtre MCIWnd tout en conservant les proportions constantes. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) .


```C++
MCIWNDM_SETZOOM 
wParam = 0; 
lParam = (LPARAM) (UINT) iZoom; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*iZoom*
</dt> <dd>

Facteur de zoom exprimé sous la forme d’un pourcentage de l’image d’origine. Spécifiez 100 pour afficher l’image à sa taille d’auteur, 200 pour afficher l’image au double de sa taille normale, ou 50 pour afficher l’image à la moitié de sa taille normale.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)
</dt> </dl>

 

 





