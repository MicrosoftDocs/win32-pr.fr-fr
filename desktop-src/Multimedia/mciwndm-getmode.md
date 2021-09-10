---
title: Message MCIWNDM_GETMODE (VFW. h)
description: Le \_ message MCIWNDM GETMODE récupère le mode d’opération actuel d’un périphérique MCI. Les périphériques MCI disposent de plusieurs modes de fonctionnement, qui sont désignés par des constantes. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetMode.
ms.assetid: cc327281-434e-4047-9e15-c04a10953f47
keywords:
- message MCIWNDM_GETMODE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daefea2c550a1d0cf807ae03840c38ae8b2567c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364264"
---
# <a name="mciwndm_getmode-message"></a>\_Message MCIWNDM GETMODE

Le message **MCIWNDM \_ GETMODE** récupère le mode d’opération actuel d’un périphérique MCI. Les périphériques MCI disposent de plusieurs modes de fonctionnement, qui sont désignés par des constantes. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) .


```C++
MCIWNDM_GETMODE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Taille, en octets, de la mémoire tampon.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Aid*
</dt> <dd>

Pointeur vers la mémoire tampon définie par l’application utilisée pour retourner le mode.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne un entier correspondant à la constante MCI définissant le mode.

## <a name="remarks"></a>Remarques

Si la chaîne se terminant par un caractère null décrivant le mode est plus longue que la mémoire tampon, elle est tronquée.

Tous les appareils ne peuvent pas fonctionner dans chaque mode. Par exemple, l’appareil MCIAVI est un périphérique de lecture ; elle ne prend pas en charge le mode d’enregistrement. Les modes suivants peuvent être récupérés à l’aide de **MCIWNDM \_ GETMODE**.



| Mode d'opération | MCI, constante          |
|----------------|-----------------------|
| non prêt      | \_mode MCI \_ non \_ prêt |
| ouvert           | \_mode MCI \_ ouvert       |
| en pause         | \_pause en mode MCI \_      |
| lecture en cours        | \_lecture en mode MCI \_       |
| enregistrement      | \_enregistrement en mode MCI \_     |
| rechercher dans        | \_recherche en mode MCI \_       |
| stopped        | \_arrêt en mode MCI \_       |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)
</dt> </dl>

 

 





