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
ms.openlocfilehash: fa38b55fdcd7c338102ed62bd9d7011ca4b7caf79fa81e834bcf915d8f934464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224265"
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

## <a name="remarks"></a>Remarques

Les modifications du système de fichiers provoquées par une extension sont détectées automatiquement par le gestionnaire de fichiers. Une extension ne doit utiliser ce message que dans les situations où des connexions de lecteur sont effectuées ou annulées.

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

 

 




