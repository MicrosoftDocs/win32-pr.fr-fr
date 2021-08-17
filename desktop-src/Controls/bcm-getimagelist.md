---
title: Message BCM_GETIMAGELIST (commctrl. h)
description: Obtient la \_ structure IMAGELIST du bouton qui décrit la liste d’images assignée à un contrôle bouton. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ GetImageList macro.
ms.assetid: 79383758-53d4-4955-b472-befd338cbec6
keywords:
- BCM_GETIMAGELIST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- BCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba74f358e80871ffad4822fd8088ca6aeb58521d8878254ed920356db5a6daf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117833910"
---
# <a name="bcm_getimagelist-message"></a>\_Message GETIMAGELIST BCM

Obtient la [**structure \_ IMAGELIST du bouton**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) qui décrit la liste d’images assignée à un contrôle bouton. Vous pouvez envoyer ce message de manière explicite ou utiliser le [**bouton \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) macro.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**\_ IMAGELIST de bouton**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) qui contient des informations sur la liste d’images.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message est correctement exécuté, la méthode retourne la **valeur true**. Sinon, elle retourne **false**.

## <a name="remarks"></a>Remarques

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





