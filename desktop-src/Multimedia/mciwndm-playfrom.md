---
title: Message MCIWNDM_PLAYFROM (VFW. h)
description: Le \_ message MCIWNDM PLAYFROM lit le contenu d’un périphérique MCI à partir de l’emplacement spécifié jusqu’à la fin du contenu ou jusqu’à ce qu’une autre commande arrête la lecture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndPlayFrom.
ms.assetid: 1c47f8eb-2a1b-4671-a9f8-fd6d59a5c7c6
keywords:
- message MCIWNDM_PLAYFROM Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYFROM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0fa1b3f4b3359e1609b3ba12009fe5879c304a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364304"
---
# <a name="mciwndm_playfrom-message"></a>\_Message MCIWNDM PLAYFROM

Le message **MCIWNDM \_ PLAYFROM** lit le contenu d’un périphérique MCI à partir de l’emplacement spécifié jusqu’à la fin du contenu ou jusqu’à ce qu’une autre commande arrête la lecture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) .


```C++
MCIWNDM_PLAYFROM 
wParam = 0; 
lParam = (LPARAM) (LONG) lPos; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*lPos*
</dt> <dd>

Emplacement de départ. Les unités de l’emplacement de départ dépendent du format d’heure actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Vous pouvez également spécifier un emplacement de départ et un emplacement de fin pour la lecture à l’aide de la macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
</dt> <dt>

[**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> </dl>

 

 





