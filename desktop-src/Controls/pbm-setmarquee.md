---
title: Message PBM_SETMARQUEE (commctrl. h)
description: Définit la barre de progression en mode texte défilant. La barre de progression se déplace alors comme un texte défilant.
ms.assetid: 6501bcb9-a711-470f-874f-f3484d3613b6
keywords:
- PBM_SETMARQUEE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PBM_SETMARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f724f87faa6e989fddb17e8d6fb3b115dd04859ea426addb7d4c0b893aff407a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986139"
---
# <a name="pbm_setmarquee-message"></a>\_Message PBM SETMARQUEE

Définit la barre de progression en mode texte défilant. La barre de progression se déplace alors comme un texte défilant.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indique s’il faut activer ou désactiver le mode texte défilant.

</dd> <dt>

*lParam* 
</dt> <dd>Durée, en millisecondes, entre les mises à jour de l’animation de texte défilant. Si ce paramètre est égal à zéro, l’animation de texte défilant est mise à jour toutes les 30 millisecondes.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne toujours la **valeur true**.

## <a name="remarks"></a>Remarques

Utilisez ce message lorsque vous ne connaissez pas la progression vers l’achèvement, mais que vous souhaitez indiquer la progression.

Envoyez le message **PBM \_ SETMARQUEE** pour démarrer ou arrêter l’animation.

> [!Note]  
> Vous devez définir le style du contrôle [**sur \_ PBS**](progress-bar-control-styles.md) pour tenter de démarrer l’animation.

 

> [!Note]  
> Ce message requiert ComCtl32.dll version 6,00 ou ultérieure.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





