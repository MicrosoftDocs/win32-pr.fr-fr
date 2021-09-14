---
title: Message MCIWNDM_OPENINTERFACE (VFW. h)
description: Le \_ message MCIWNDM OPENINTERFACE joint le flux de données ou le fichier associé à l’interface spécifiée à une fenêtre MCIWnd. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndOpenInterface.
ms.assetid: 73cbd637-d315-4b39-a978-2b72aed1f303
keywords:
- message MCIWNDM_OPENINTERFACE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_OPENINTERFACE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c40453f4d587429508a5aae19bc432fc46088ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218652"
---
# <a name="mciwndm_openinterface-message"></a>\_Message MCIWNDM OPENINTERFACE

Le message **MCIWNDM \_ OPENINTERFACE** joint le flux de données ou le fichier associé à l’interface spécifiée à une fenêtre MCIWnd. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) .


```C++
MCIWNDM_OPENINTERFACE 
wParam = 0; 
lParam = (LPARAM) (LPUNKNOWN) pUnk; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*pUnk*
</dt> <dd>

Pointeur vers une interface IAVI qui pointe vers un fichier ou un flux de données dans un fichier.

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

[**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface)
</dt> </dl>

 

 





