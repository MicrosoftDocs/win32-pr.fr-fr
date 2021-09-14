---
description: Envoyé à une DLL d’extension lorsque l’utilisateur choisit la commande Actualiser dans le menu Affichage du gestionnaire de fichiers. L’extension peut utiliser cette notification pour mettre à jour son menu.
title: Message FMEVENT_USER_REFRESH (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_USER_REFRESH
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b8fb4ce8-d284-4558-82a4-488d4d833bcb
ms.openlocfilehash: 16f75f562149b50237a6b41bf2023d1f694741e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295303"
---
# <a name="fmevent_user_refresh-message"></a>Message d’actualisation de l' \_ utilisateur FMEVENT \_

Envoyé à une DLL d’extension lorsque l’utilisateur choisit la commande **Actualiser** dans le menu **affichage** du gestionnaire de fichiers. L’extension peut utiliser cette notification pour mettre à jour son menu.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Une DLL d’extension doit retourner zéro si elle traite ce message.

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

 

 




