---
title: Message MCIWNDM_SETTIMEFORMAT (VFW. h)
description: Le \_ message MCIWNDM SETTIMEFORMAT définit le format d’heure d’un appareil MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndSetTimeFormat.
ms.assetid: 7de82094-6d35-44fd-88e7-ebd18a558cfd
keywords:
- Message MCIWNDM_SETTIMEFORMAT Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcec1f0db5accad93211bf1eb6f1c9297e2b9f33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508333"
---
# <a name="mciwndm_settimeformat-message"></a>\_Message MCIWNDM SETTIMEFORMAT

Le message **MCIWNDM \_ SETTIMEFORMAT** définit le format d’heure d’un appareil MCI. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) .


```C++
MCIWNDM_SETTIMEFORMAT 
wParam = 0; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lp"></span><span id="LP"></span>*Aid*
</dt> <dd>

Pointeur vers une mémoire tampon contenant la chaîne terminée par le caractère null qui indique le format d’heure. Spécifiez « frames » pour définir le format d’heure sur frames, ou « MS » pour définir le format d’heure sur millisecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Une application peut spécifier des formats d’heure autres que des images ou des millisecondes tant que les formats sont pris en charge par l’appareil MCI. Les formats incontinus, tels que Tracks et SMPTE, peuvent entraîner un comportement erratique du TrackBar. Pour ces formats d’heure, vous souhaiterez peut-être désactiver la barre d’outils à l’aide de la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) et en spécifiant le \_ style de fenêtre NOPLAYBAR MCIWNDF.

Si vous souhaitez définir le format d’heure sur des images ou des millisecondes, vous pouvez également utiliser la macro [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) ou [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) . Pour obtenir la liste des formats d’heure, consultez la macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> <dt>

[**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> <dt>

[**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)
</dt> <dt>

[**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)
</dt> <dt>

[**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime)
</dt> </dl>

 

 





