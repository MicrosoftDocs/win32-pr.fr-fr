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
ms.openlocfilehash: 9229291113f034924cf9ce8112c0e99376d37932
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117706"
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

## <a name="return-value"></a>Valeur de retour

Retourne toujours la **valeur true**.

## <a name="remarks"></a>Notes

Utilisez ce message lorsque vous ne connaissez pas la progression vers l’achèvement, mais que vous souhaitez indiquer la progression.

Envoyez le message **PBM \_ SETMARQUEE** pour démarrer ou arrêter l’animation.

> [!Note]  
> Vous devez définir le style du contrôle [**sur \_ PBS**](progress-bar-control-styles.md) pour tenter de démarrer l’animation.

 

> [!Note]  
> Ce message requiert ComCtl32.dll version 6,00 ou ultérieure.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





