---
description: Envoyé à une DLL d’extension lors du déchargement de la DLL par le gestionnaire de fichiers.
title: Message FMEVENT_UNLOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_UNLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 15ffcd46-602f-4ad0-9c58-0b8056b9cac4
ms.openlocfilehash: 5d18d72a43ac1fca6906bb1e3f7a14468dbd02933d801dc3c20e2a933bc18f1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860364"
---
# <a name="fmevent_unload-message"></a>FMEVENT \_ décharger le message

Envoyé à une DLL d’extension lors du déchargement de la DLL par le gestionnaire de fichiers.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une DLL d’extension doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Remarques

Les valeurs *HWND* et **HMENU** transmises avec les messages [**FMEVENT \_ Load**](fmevent-load.md) et [**FMEVENT \_ INITMENU**](fmevent-initmenu.md) peuvent ne pas être valides au moment de l’envoi de ce message.

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

 

 




