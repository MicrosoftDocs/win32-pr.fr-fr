---
title: Message MCIWNDM_GETDEVICE (VFW. h)
description: Le \_ message MCIWNDM GETDEVICE récupère le nom de l’appareil MCI actuellement ouvert. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetDevice.
ms.assetid: e69a73a6-a927-4536-98c7-ee7d5b16668a
keywords:
- message MCIWNDM_GETDEVICE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32664508a577db9d5a077e3cb4fd00aab34fbdf3
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364251"
---
# <a name="mciwndm_getdevice-message"></a>\_Message MCIWNDM GETDEVICE

Le message **MCIWNDM \_ GETDEVICE** récupère le nom de l’appareil MCI actuellement ouvert. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) .


```C++
MCIWNDM_GETDEVICE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Taille, en octets, de la mémoire tampon.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Aid*
</dt> <dd>

Pointeur vers une mémoire tampon définie par l’application pour retourner le nom de l’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une valeur différente de zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

Si la chaîne se terminant par un caractère NULL contenant le nom de l’appareil est plus longue que la mémoire tampon, MCIWnd la tronque.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





