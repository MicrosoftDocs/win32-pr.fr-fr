---
description: Envoyé par une extension du gestionnaire de fichiers (ou une autre application) pour faire en sorte que le gestionnaire de fichiers recharge toutes les dll d’extension listées dans la \[ section addons \] du fichier Winfile.ini.
ms.assetid: 5103a986-5f45-4deb-aaae-c6e87cb60051
title: Message FM_RELOAD_EXTENSIONS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_RELOAD_EXTENSIONS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: 9e4e632ac153a78e729ce0d3fcd65f49ae90781bd29cfe354d4571ba04e63be0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224173"
---
# <a name="fm_reload_extensions-message"></a>\_Message d’extensions de REchargement FM \_

Envoyé par une extension du gestionnaire de fichiers (ou une autre application) pour faire en sorte que le gestionnaire de fichiers recharge toutes les dll d’extension listées dans la \[ section addons \] du fichier Winfile.ini.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

D’autres applications peuvent utiliser la fonction [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) pour envoyer ce message au gestionnaire de fichiers. Pour obtenir le handle de fenêtre appropriée du gestionnaire de fichiers, une application peut spécifier « WFS \_ Frame » comme paramètre *lpszClassName* dans un appel à la fonction [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 
