---
description: Envoyé à une DLL d’extension lorsque l’utilisateur sélectionne un nom de fichier dans la fenêtre répertoire du gestionnaire de fichiers ou dans la fenêtre des résultats de la recherche.
title: Message FMEVENT_SELCHANGE (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_SELCHANGE
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0773aa74-adf2-4e90-aead-2a9a981be3cb
ms.openlocfilehash: befc217eeb24453d7db726cf68d233fa57e5a7971fd148406cf90810b52b070d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459036"
---
# <a name="fmevent_selchange-message"></a>\_Message FMEVENT selChange

Envoyé à une DLL d’extension lorsque l’utilisateur sélectionne un nom de fichier dans la fenêtre répertoire du gestionnaire de fichiers ou dans la fenêtre des résultats de la recherche.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une DLL d’extension doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Remarques

Les modifications apportées à la partie de l’arborescence de la fenêtre de répertoire ne génèrent pas ce message.

Étant donné que l’utilisateur peut modifier la sélection plusieurs fois, la DLL d’extension doit retourner promptement après le traitement de ce message pour éviter de ralentir le processus de sélection de l’utilisateur.

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

 

 




