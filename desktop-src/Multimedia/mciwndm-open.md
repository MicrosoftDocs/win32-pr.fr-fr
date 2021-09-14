---
title: Message MCIWNDM_OPEN (VFW. h)
description: Le \_ message MCIWNDM Open ouvre un appareil MCI et l’associe à une fenêtre MCIWnd.
ms.assetid: ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057
keywords:
- message MCIWNDM_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2f232ea9076a1e0ff8c105d8c5cf94104e455c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218657"
---
# <a name="mciwndm_open-message"></a>MCIWNDM \_ ouvrir le message

Le message **MCIWNDM \_ Open** ouvre un appareil MCI et l’associe à une fenêtre MCIWnd. Pour les appareils MCI qui utilisent des fichiers de données, cette macro peut également ouvrir un fichier de données spécifié, nommer un nouveau fichier à créer ou afficher une boîte de dialogue qui permet à l’utilisateur de sélectionner un fichier à ouvrir. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) .


```C++
MCIWNDM_OPEN 
wParam = (WPARAM) (UINT) wFlags; 
lParam = (LPARAM) (LPVOID) szFile; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*
</dt> <dd>

Indicateurs associés à l’appareil ou au fichier à ouvrir. Le \_ nouvel indicateur MCIWNDOPENF spécifie qu’un nouveau fichier doit être créé avec le nom spécifié dans **szFile**.

</dd> <dt>

<span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null, identifiant le nom de fichier ou le nom du périphérique MCI à ouvrir. Spécifiez 1 pour que ce paramètre affiche la boîte de dialogue Ouvrir.

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

[**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
</dt> </dl>

 

 





