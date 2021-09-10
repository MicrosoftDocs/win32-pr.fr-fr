---
title: Message MCIWNDM_GET_SOURCE (VFW. h)
description: Le \_ \_ message source MCIWNDM obtient les coordonnées du rectangle source utilisé pour le rognage des images d’un fichier AVI lors de la lecture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndGetSource.
ms.assetid: d5f25926-5a3d-412e-8248-fbf307583757
keywords:
- message MCIWNDM_GET_SOURCE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GET_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85147182d06386efed73229fcdd6c75372244fd6
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364272"
---
# <a name="mciwndm_get_source-message"></a>MCIWNDM \_ recevoir le \_ message source

Le **message \_ \_ source MCIWNDM obtient** les coordonnées du rectangle source utilisé pour le rognage des images d’un fichier AVI lors de la lecture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) .


```C++
MCIWNDM_GET_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*République*
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) pour contenir les coordonnées du rectangle source.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)
</dt> </dl>

 

