---
title: Message MCIWNDM_GETTIMEFORMAT (VFW. h)
description: Le \_ message MCIWNDM GETTIMEFORMAT récupère le format d’heure actuel d’un appareil MCI sous deux formes, sous la forme d’une valeur numérique et sous forme de chaîne. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetTimeFormat.
ms.assetid: 01844872-5444-4f3b-92a3-64f80b94d3a0
keywords:
- message MCIWNDM_GETTIMEFORMAT Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a09f969c009ff23bc0951ed2efbc0dbf7aa95dda
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009494"
---
# <a name="mciwndm_gettimeformat-message"></a>\_Message MCIWNDM GETTIMEFORMAT

Le message **MCIWNDM \_ GETTIMEFORMAT** récupère le format d’heure actuel d’un appareil MCI sous deux formes : une valeur numérique et une chaîne. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .


```C++
MCIWNDM_GETTIMEFORMAT 
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

Pointeur vers une mémoire tampon destinée à contenir la forme de chaîne terminée par le caractère null du format d’heure.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne un entier correspondant à la constante MCI définissant le format d’heure.

## <a name="remarks"></a>Notes

Si la chaîne de format d’heure est plus longue que la mémoire tampon de retour, MCIWnd tronque la chaîne.

Un périphérique MCI peut prendre en charge un ou plusieurs des formats d’heure suivants.



| Format de l’heure                      | MCI, constante               |
|----------------------------------|----------------------------|
| Octets                            | \_octets au format MCI \_         |
| Frame                           | \_images au format MCI \_        |
| Heures, minutes, secondes          | \_format MCI \_ HMS           |
| Millisecondes                     | FORMAT MCI en \_ \_ millisecondes  |
| Minutes, secondes, frames         | FORMAT MCI ( \_ \_ MSF)           |
| Exemples                          | \_exemples de format MCI \_       |
| SMPTE 24                         | \_Format MCI \_ SMPTE \_ 24     |
| SMPTE 25                         | \_Format MCI \_ SMPTE \_ 25     |
| Suppression SMPTE 30                    | \_Format MCI \_ \_ 30DROP SMPTE |
| SMPTE 30 (non-Drop)              | FORMAT MCI, \_ \_ SMPTE \_ 30     |
| Pistes, minutes, secondes, frames | \_format MCI \_ TMSF          |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> </dl>

 

 





