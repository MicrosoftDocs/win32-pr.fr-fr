---
title: Message LM_GETIDEALSIZE (commctrl. h)
description: 'LM_GETIDEALSIZE message : récupère la hauteur par défaut d’un lien pour la largeur actuelle du contrôle.'
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- LM_GETIDEALSIZE les contrôles de Windows de message
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
ms.openlocfilehash: 035a919aabeb5d07587c7d9e4fc97e5edc728de4ec8fc476448dca62658f1ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958371"
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

## <a name="remarks"></a>Remarques

> [!Note]  
> Pour utiliser cette API, vous devez fournir un manifeste qui spécifie Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

