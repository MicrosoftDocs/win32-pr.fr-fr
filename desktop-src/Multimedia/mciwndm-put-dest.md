---
title: Message MCIWNDM_PUT_DEST (VFW. h)
description: Le \_ message MCIWNDM put \_ dest redéfinit les coordonnées du rectangle de destination utilisé pour le zoom ou l’étirement des images d’un fichier AVI lors de la lecture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndPutDest.
ms.assetid: 0b13d473-ef93-41a2-bbb2-09fbf264493e
keywords:
- message MCIWNDM_PUT_DEST Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba150f450f71c3593976f98c9935233918becd70
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218617"
---
# <a name="mciwndm_put_dest-message"></a>MCIWNDM \_ put \_ dest message

Le message **MCIWNDM \_ put \_ dest** redéfinit les coordonnées du rectangle de destination utilisé pour le zoom ou l’étirement des images d’un fichier AVI lors de la lecture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) .


```C++
MCIWNDM_PUT_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*République*
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) contenant les coordonnées du rectangle de destination.

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

[**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)
</dt> </dl>

 

