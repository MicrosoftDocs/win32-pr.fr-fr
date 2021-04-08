---
title: Message MCIWNDM_GETERROR (VFW. h)
description: Le \_ message MCIWNDM GETERROR récupère la dernière erreur MCI rencontrée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetError.
ms.assetid: f110a9b3-5b05-4bf0-85d1-b49ce7396222
keywords:
- Message MCIWNDM_GETERROR Windows Multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843194"
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

## <a name="remarks"></a>Notes

Si *LP* est un pointeur valide, une chaîne se terminant par un caractère null qui correspond à l’erreur est retournée dans sa mémoire tampon. Si la chaîne d’erreur est plus longue que la mémoire tampon, MCIWnd la tronque.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
</dt> </dl>

 

 





