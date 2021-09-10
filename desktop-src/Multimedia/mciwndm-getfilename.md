---
title: Message MCIWNDM_GETFILENAME (VFW. h)
description: Le \_ message MCIWNDM GETFILENAME récupère le nom de fichier actuellement utilisé par un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetFileName.
ms.assetid: d61b1b6d-0fae-4732-993c-41e08a4e05be
keywords:
- message MCIWNDM_GETFILENAME Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETFILENAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 232a1d829b5cdd6da23e7dd3fb0294b95ca79f4b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364256"
---
# <a name="mciwndm_getfilename-message"></a>\_Message MCIWNDM GETFILENAME

Le message **MCIWNDM \_ GETFILENAME** récupère le nom de fichier actuellement utilisé par un périphérique MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) .


```C++
MCIWNDM_GETFILENAME 
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

Pointeur vers une mémoire tampon définie par l’application pour retourner le nom de fichier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou 1 dans le cas contraire.

## <a name="remarks"></a>Remarques

Si la chaîne se terminant par un caractère NULL contenant le nom de fichier est plus longue que la mémoire tampon, MCIWnd tronque le nom de fichier.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename)
</dt> </dl>

 

 





