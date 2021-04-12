---
title: Message LM_GETIDEALSIZE (commctrl. h)
description: Récupère la hauteur par défaut d’un lien pour la largeur actuelle du contrôle.
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- LM_GETIDEALSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c138e22982116a3b7173f586d96c70cfc91194c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464302"
---
# <a name="lm_getidealsize-message"></a>\_Message LM GETIDEALSIZE

Récupère la hauteur par défaut d’un lien pour la largeur actuelle du contrôle.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Largeur maximale du lien, en pixels.</dd> <dt>

*lParam* \[ à\]
</dt> <dd>Lorsque ce message est retourné, contient un pointeur vers une structure de <a href="/previous-versions//dd145106(v=vs.85)">**taille**</a> . Le membre **CY** de cette structure indique la hauteur idéale du contrôle pour la largeur donnée. Il ajuste le membre **CX** en fonction de la quantité d’espace réellement nécessaire.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Entier qui représente la hauteur préférée du texte du lien, en pixels.

## <a name="remarks"></a>Notes

> [!Note]  
> Pour utiliser cette API, vous devez fournir un manifeste qui spécifie Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

