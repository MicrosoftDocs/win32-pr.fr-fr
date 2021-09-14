---
title: Message HDM_INSERTITEM (commctrl. h)
description: Insère un nouvel élément dans un contrôle header. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro en-tête \_ InsertItem.
ms.assetid: aececf32-090d-4cd4-a239-4435a322f72e
keywords:
- HDM_INSERTITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- HDM_INSERTITEM
- HDM_INSERTITEMA
- HDM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9cabf86fea79fd437b3e9fb7e32890b3ba1a780
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006280"
---
# <a name="hdm_insertitem-message"></a>\_Message HDM INSERTITEM

Insère un nouvel élément dans un contrôle header. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**en-tête \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’élément après lequel le nouvel élément doit être inséré. Le nouvel élément est inséré à la fin du contrôle header si *wParam* est supérieur ou égal au nombre d’éléments dans le contrôle. Si *wParam* est égal à zéro, le nouvel élément est inséré au début du contrôle header.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) qui contient des informations sur le nouvel élément.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’index du nouvel élément en cas de réussite, ou-1 dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **HDM \_ INSERTITEMW** (Unicode) et **HDM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





