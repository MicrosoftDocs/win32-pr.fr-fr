---
title: Message WM_CAP_FILE_SAVEAS (VFW. h)
description: Le \_ message WM Cap \_ file \_ SaveAs copie le contenu du fichier de capture dans un autre fichier. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capFileSaveAs.
ms.assetid: fab37bee-3160-4ebc-b58f-46021ed49b55
keywords:
- message WM_CAP_FILE_SAVEAS Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a200b8e73d81072961ec4e6aa7c8e1dd989bf2d8c3e0480c75908a8761ee93b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687009"
---
# <a name="wm_cap_file_saveas-message"></a>\_Message de \_ fichier \_ SaveAs de l’embout de fichier WM

Le message **WM \_ Cap \_ file \_ SaveAs** copie le contenu du fichier de capture dans un autre fichier. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) .


```C++
WM_CAP_FILE_SAVEAS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Pointeur vers la chaîne terminée par le caractère null qui contient le nom du fichier de destination utilisé pour copier le fichier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

Si une erreur se produit et qu’une fonction de rappel d’erreur est définie à l’aide du message d' [**\_ erreur WM Cap \_ Set \_ callback \_**](wm-cap-set-callback-error.md) , la fonction de rappel d’erreur est appelée.

## <a name="remarks"></a>Remarques

Ce message ne modifie pas le nom ou le contenu du fichier de capture actuel.

Si l’opération de copie échoue en raison d’une erreur de disque plein, le fichier de destination est automatiquement supprimé.

En règle générale, un fichier de capture est préalloué pour le plus grand segment de capture attendu et seule une partie de celui-ci peut être utilisée pour capturer des données. Ce message copie uniquement la partie du fichier contenant les données de capture.

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

 

 





