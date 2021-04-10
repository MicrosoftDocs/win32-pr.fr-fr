---
title: Message PBM_SETMARQUEE (commctrl. h)
description: Définit la barre de progression en mode texte défilant. La barre de progression se déplace alors comme un texte défilant.
ms.assetid: 6501bcb9-a711-470f-874f-f3484d3613b6
keywords:
- PBM_SETMARQUEE les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942471"
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

## <a name="remarks"></a>Notes

Utilisez ce message lorsque vous ne connaissez pas la progression vers l’achèvement, mais que vous souhaitez indiquer la progression.

Envoyez le message **PBM \_ SETMARQUEE** pour démarrer ou arrêter l’animation.

> [!Note]  
> Vous devez définir le style du contrôle [**sur \_ PBS**](progress-bar-control-styles.md) pour tenter de démarrer l’animation.

 

> [!Note]  
> Ce message requiert ComCtl32.dll version 6,00 ou ultérieure.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





