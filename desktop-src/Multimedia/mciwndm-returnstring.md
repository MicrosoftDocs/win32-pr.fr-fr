---
title: Message MCIWNDM_RETURNSTRING (VFW. h)
description: Le \_ message MCIWNDM RETURNSTRING récupère la réponse à la commande de chaîne MCI la plus récente envoyée à un périphérique MCI.
ms.assetid: 36a5222c-a63c-4b8c-ad0c-a00477e95b96
keywords:
- message MCIWNDM_RETURNSTRING Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_RETURNSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b99307bd7d61a70db594d0a696cceccd6d246a3
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364316"
---
# <a name="mciwndm_returnstring-message"></a>\_Message MCIWNDM RETURNSTRING

Le message **MCIWNDM \_ RETURNSTRING** récupère la réponse à la commande de chaîne MCI la plus récente envoyée à un périphérique MCI. Les informations contenues dans la réponse sont fournies sous la forme d’une chaîne terminée par le caractère null. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) .


```C++
MCIWNDM_RETURNSTRING 
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

Pointeur vers une mémoire tampon définie par l’application devant contenir la chaîne terminée par le caractère null.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne un entier correspondant à la chaîne MCI.

## <a name="remarks"></a>Remarques

Si la chaîne se terminant par un caractère NULL est plus longue que la mémoire tampon, la chaîne est tronquée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
</dt> </dl>

 

 





