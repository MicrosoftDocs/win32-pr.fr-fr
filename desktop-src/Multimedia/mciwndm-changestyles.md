---
title: Message MCIWNDM_CHANGESTYLES (VFW. h)
description: Le \_ message MCIWNDM CHANGESTYLES modifie les styles utilisés par la fenêtre MCIWnd. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndChangeStyles.
ms.assetid: 9074c21a-e49f-4089-a6d2-af8d513cb632
keywords:
- message MCIWNDM_CHANGESTYLES Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CHANGESTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2cea636c3c879da642da753c4fd084b06c4334
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364240"
---
# <a name="mciwndm_changestyles-message"></a>\_Message MCIWNDM CHANGESTYLES

Le message **MCIWNDM \_ CHANGESTYLES** modifie les styles utilisés par la fenêtre MCIWnd. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) .


```C++
MCIWNDM_CHANGESTYLES 
wParam = (WPARAM) (UINT) mask; 
lParam = (LPARAM) (LONG) value; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="mask"></span><span id="MASK"></span>*filtrage*
</dt> <dd>

Masque qui identifie les styles qui peuvent changer. Ce masque est l’opérateur or au niveau du bit de tous les styles qui seront autorisés à changer.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*ajoutée*
</dt> <dd>

Nouveaux paramètres de style pour la fenêtre. Spécifiez zéro pour ce paramètre pour désactiver tous les styles identifiés dans le masque. Pour obtenir la liste des styles disponibles, consultez la fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
</dt> <dt>

[**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> </dl>

 

 





