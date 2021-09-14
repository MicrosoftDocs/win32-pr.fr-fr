---
title: Message TB_GETIDEALSIZE (commctrl. h)
description: Obtient la taille idéale de la barre d’outils.
ms.assetid: d3b5ea4d-fd80-4f07-be4f-89b53a8bdf4d
keywords:
- TB_GETIDEALSIZE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59b8701a4f4debcfb8e43f37068e7e7a4ef4f11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116770"
---
# <a name="tb_getidealsize-message"></a>TO \_ GETIDEALSIZE message

Obtient la taille idéale de la barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Valeur **booléenne** qui indique s’il faut récupérer la hauteur ou la largeur idéale de la barre d’outils. Utilisez **true** pour récupérer la hauteur idéale, **false** pour récupérer la largeur idéale.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure de [**taille**](/previous-versions//dd145106(v=vs.85)) qui reçoit la hauteur ou la largeur d’affichage de tous les boutons. Si *wParam* a la **valeur true**, seul le membre **CY** (Height) est valide. Si *wParam* a la **valeur false**, seul le membre **CX** (Width) est valide.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

