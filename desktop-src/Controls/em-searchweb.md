---
title: Message EM_SEARCHWEB (commctrl. h)
description: Ouvre le navigateur et effectue une recherche sur le Web avec le texte sélectionné comme terme de recherche.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- EM_SEARCHWEB les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SEARCHWEB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e83c18db47d18648797ee3d58fe12567af941b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006427"
---
# <a name="em_searchweb-message"></a>\_Message SEARCHWEB em

Ouvre le navigateur et effectue une recherche sur le Web avec le texte sélectionné comme terme de recherche.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si la fonctionnalité « Rechercher sur le Web » est désactivée à l’aide du message [**\_ ENABLESEARCHWEB em**](em-enablesearchweb.md) , ce message n’a aucun effet.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, 1809 \[ applications de bureau uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2019 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ENABLESEARCHWEB em**](em-enablesearchweb.md)
</dt> </dl>

 

 





