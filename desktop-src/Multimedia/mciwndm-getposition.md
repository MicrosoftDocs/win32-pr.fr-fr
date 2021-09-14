---
title: Message MCIWNDM_GETPOSITION (VFW. h)
description: Le \_ message GETPOSITION MCIWNDM récupère la valeur numérique de la position actuelle dans le contenu de l’appareil MCI.
ms.assetid: 6dc5d3bd-8515-4514-a2a5-c1bee07f7acf
keywords:
- message MCIWNDM_GETPOSITION Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETPOSITION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e7468b0e3698a72d3dce82bbd1591d59940d9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009507"
---
# <a name="mciwndm_getposition-message"></a>\_Message MCIWNDM GETPOSITION

Le **message \_ GETPOSITION MCIWNDM** récupère la valeur numérique de la position actuelle dans le contenu de l’appareil MCI. Cette macro fournit également la position actuelle sous forme de chaîne dans une mémoire tampon définie par l’application. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) ou [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) .


```C++
MCIWNDM_GETPOSITION 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPTSTR) lp; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Taille, en octets, de la mémoire tampon. Si la chaîne se terminant par un caractère NULL est plus longue que la mémoire tampon, elle est tronquée. Utilisez zéro pour empêcher la récupération de la position comme une chaîne.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Aid*
</dt> <dd>

Pointeur vers une mémoire tampon définie par l’application utilisée pour retourner la position. Utilisez zéro pour empêcher la récupération de la position comme une chaîne. Si l’appareil prend en charge les suivis, les informations de position de la chaîne sont retournées sous la forme TT : MM : SS : FF où TT correspond aux suivis, MM et SS correspondent aux minutes et aux secondes, et FF correspond aux frames.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne un entier correspondant à la position actuelle. Les unités pour la valeur de position dépendent du format d’heure actuel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
</dt> <dt>

[**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
</dt> </dl>

 

 





