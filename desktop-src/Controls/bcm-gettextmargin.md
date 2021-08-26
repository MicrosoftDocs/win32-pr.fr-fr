---
title: Message BCM_GETTEXTMARGIN (commctrl. h)
description: Obtient les marges utilisées pour dessiner du texte dans un contrôle bouton. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ GetTextMargin macro.
ms.assetid: 6c141752-e636-41c4-9d05-df8b320ff59f
keywords:
- BCM_GETTEXTMARGIN les contrôles de Windows de message
topic_type:
- apiref
api_name:
- BCM_GETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea871d0054558e1522011d4fdb00fdd3c82a0dd1562fe3420d3295bbab89a01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064409"
---
# <a name="bcm_gettextmargin-message"></a>\_Message GETTEXTMARGIN BCM

Obtient les marges utilisées pour dessiner du texte dans un contrôle bouton. Vous pouvez envoyer ce message de manière explicite ou utiliser le [**bouton \_ GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) macro.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contient les marges à utiliser pour dessiner du texte.

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



 

