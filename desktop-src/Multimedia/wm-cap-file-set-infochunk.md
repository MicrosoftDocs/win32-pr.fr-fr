---
title: Message WM_CAP_FILE_SET_INFOCHUNK (VFW. h)
description: Le \_ jeu de fichiers WM Cap définit les \_ \_ \_ jeux de messages INFOCHUNK et efface les segments d’informations.
ms.assetid: 67d11a05-a2b4-45d2-ba66-83a198745303
keywords:
- Message WM_CAP_FILE_SET_INFOCHUNK Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_INFOCHUNK
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 067ba00563a5ca511f13b23615fc4542090ba397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032386"
---
# <a name="wm_cap_file_set_infochunk-message"></a>\_ \_ \_ Message INFOCHUNK du jeu de fichiers \_ de la casquette WM

Le **jeu de fichiers WM Cap définit les jeux de messages \_ \_ \_ \_ INFOCHUNK** et efface les segments d’informations. Des blocs d’informations peuvent être insérés dans un fichier AVI au cours de la capture pour incorporer des chaînes de texte ou des données personnalisées. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) .


```C++
WM_CAP_FILE_SET_INFOCHUNK 
wParam = (WPARAM)0; 
lParam = (LPARAM) (LPCAPINFOCHUNK) (lpInfoChunk); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*
</dt> <dd>

Pointeur vers une structure [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) définissant le segment d’informations à créer ou à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

Si une erreur se produit et qu’une fonction de rappel d’erreur est définie à l’aide du message d' [**\_ erreur WM Cap \_ Set \_ callback \_**](wm-cap-set-callback-error.md) , la fonction de rappel d’erreur est appelée.

## <a name="remarks"></a>Notes

Plusieurs segments d’informations inscrits peuvent être ajoutés à un fichier AVI. Une fois qu’un segment d’informations est défini, il continue à être ajouté aux fichiers de capture suivants jusqu’à ce que l’entrée soit effacée ou que toutes les entrées de segment d’information soient effacées. Pour effacer une entrée unique, spécifiez le segment d’informations dans le membre **fccInfoID** et la **valeur null** dans le membre **lpData** de la structure [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) . Pour effacer toutes les entrées, spécifiez **null** dans **fccInfoID**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Capture vidéo](video-capture.md)
</dt> <dt>

[Messages de capture vidéo](video-capture-messages.md)
</dt> </dl>

 

 





