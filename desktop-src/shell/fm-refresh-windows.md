---
description: Envoyé par une extension du gestionnaire de fichiers pour faire en sorte que le gestionnaire de fichiers redessine la fenêtre active ou l’ensemble de ses fenêtres.
title: Message FM_REFRESH_WINDOWS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_REFRESH_WINDOWS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 210168c6-d83b-4ffd-93d4-d22fa748cef2
ms.openlocfilehash: 386fdee5c7a8b56899fa7e13282445c57eccff08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201144"
---
# <a name="fm_refresh_windows-message"></a>\_Message Windows d’actualisation FM \_

Envoyé par une extension du gestionnaire de fichiers pour faire en sorte que le gestionnaire de fichiers redessine la fenêtre active ou l’ensemble de ses fenêtres.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*fRepaint* 
</dt> <dd>

Valeur qui indique si le gestionnaire de fichiers redessine sa fenêtre active ou toutes ses fenêtres. Si ce paramètre a la **valeur true**, le gestionnaire de fichiers redessine toutes ses fenêtres. Dans le cas contraire, le gestionnaire de fichiers redessine uniquement sa fenêtre active.

</dd> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Les modifications du système de fichiers provoquées par une extension sont détectées automatiquement par le gestionnaire de fichiers. Une extension ne doit utiliser ce message que dans les situations où des connexions de lecteur sont effectuées ou annulées.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




