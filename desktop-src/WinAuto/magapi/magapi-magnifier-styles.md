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
ms.openlocfilehash: 212e079a59db9a85b6d232d1c11ac9f46eceb314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384692"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Agrandissement. h</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[Constantes](entry-magapi-constants.md)
