---
title: Message BCM_GETTEXTMARGIN (commctrl. h)
description: Obtient les marges utilisées pour dessiner du texte dans un contrôle bouton. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ GetTextMargin macro.
ms.assetid: 6c141752-e636-41c4-9d05-df8b320ff59f
keywords:
- BCM_GETTEXTMARGIN les contrôles de message Windows
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
ms.openlocfilehash: d6a7d809207c21c74a36c796a9035ed0e3772481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942029"
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

## <a name="remarks"></a>Notes

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

