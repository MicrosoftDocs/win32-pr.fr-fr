---
title: Message MCIWNDM_PLAYTO (VFW. h)
description: Le \_ message MCIWNDM point lit le contenu d’un périphérique MCI de la position actuelle à l’emplacement de fin spécifié ou jusqu’à ce qu’une autre commande arrête la lecture.
ms.assetid: ed940ee7-7b96-47da-99d3-6697f8a2e3d5
keywords:
- Message MCIWNDM_PLAYTO Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYTO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf0104204dc0306615ead91be036459cdf3c11d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105430"
---
# <a name="mciwndm_playto-message"></a>\_Message MCIWNDM point

Le message **MCIWNDM \_ point** lit le contenu d’un périphérique MCI de la position actuelle à l’emplacement de fin spécifié ou jusqu’à ce qu’une autre commande arrête la lecture. Si l’emplacement de fin spécifié se situe au-delà de la fin du contenu, la lecture s’arrête à la fin du contenu. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) .


```C++
MCIWNDM_PLAYTO 
wParam = 0; 
lParam = (LPARAM) (LONG) lEnd; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*Prêter*
</dt> <dd>

Emplacement de fin. Les unités de l’emplacement de fin dépendent du format d’heure actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Cette macro est définie à l’aide des macros [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) et [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) , qui à leur tour utilisent la commande [MCI \_ Seek](mci-seek.md) et le message **MCIWNDM \_ point** .

Vous pouvez également spécifier un emplacement de départ et un emplacement de fin pour la lecture à l’aide de la macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[\_recherche MCI](mci-seek.md)
</dt> <dt>

[**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> <dt>

[**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
</dt> <dt>

[**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
</dt> </dl>

 

 





