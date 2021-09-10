---
title: Message MCIWNDM_GETERROR (VFW. h)
description: Le \_ message MCIWNDM GETERROR récupère la dernière erreur MCI rencontrée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetError.
ms.assetid: f110a9b3-5b05-4bf0-85d1-b49ce7396222
keywords:
- message MCIWNDM_GETERROR Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c2977bb079351824b48da21f4ba3cc2dc5afe7e
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364259"
---
# <a name="mciwndm_geterror-message"></a>\_Message MCIWNDM GETERROR

Le message **MCIWNDM \_ GETERROR** récupère la dernière erreur MCI rencontrée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) .


```C++
MCIWNDM_GETERROR 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Taille, en octets, de la mémoire tampon d’erreur.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Aid*
</dt> <dd>

Pointeur vers une mémoire tampon définie par l’application utilisée pour retourner la chaîne d’erreur.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la valeur d’erreur entière en cas de réussite.

## <a name="remarks"></a>Remarques

Si *LP* est un pointeur valide, une chaîne se terminant par un caractère null qui correspond à l’erreur est retournée dans sa mémoire tampon. Si la chaîne d’erreur est plus longue que la mémoire tampon, MCIWnd la tronque.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
</dt> </dl>

 

 





