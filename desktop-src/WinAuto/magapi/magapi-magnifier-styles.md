---
title: Styles de la loupe
description: Cette rubrique décrit les styles utilisés avec le contrôle magnifier.
ms.assetid: B3C575AC-B8D3-40CF-AF09-BAC73E6C7B45
topic_type:
- apiref
api_name:
- MS_CLIPAROUNDCURSOR
- MS_INVERTCOLORS
- MS_SHOWMAGNIFIEDCURSOR
api_location:
- Magnification.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: ef65f736b50210ed52c542375aa340d5bd85ae38265a71858d82e069d830aa62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052577"
---
# <a name="magnifier-styles"></a>Styles de la loupe

Cette rubrique décrit les styles utilisés avec le contrôle magnifier. Pour créer un contrôle Magnifier, utilisez la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) et spécifiez la classe de fenêtre WC_MAGNIFIER, ainsi qu’une combinaison des styles de loupe suivants.

| Condition requise | Valeur |
|:---|:---|
| MS_CLIPAROUNDCURSOR 0x0002L | Découpe la zone de la fenêtre de la loupe qui entoure le curseur système. Ce style permet à l’utilisateur de voir le contenu de l’écran qui se trouve derrière la fenêtre Loupe. |
| MS_INVERTCOLORS 0x0004L | Affiche le contenu agrandi de l’écran à l’aide de couleurs inversées. |
| MS_SHOWMAGNIFIEDCURSOR 0x0001L | Affiche le curseur système agrandi ainsi que le contenu de l’écran agrandi. |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Agrandissement. h</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[Constantes](entry-magapi-constants.md)
