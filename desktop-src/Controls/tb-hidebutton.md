---
title: Message TB_HIDEBUTTON (commctrl. h)
description: Masque ou affiche le bouton spécifié dans une barre d’outils.
ms.assetid: 57941a40-279a-426e-baf9-115429c62839
keywords:
- TB_HIDEBUTTON les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_HIDEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e198a48ae65f13be699b76a20c9f423cdb0da197
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941948"
---
# <a name="tb_hidebutton-message"></a>TO \_ HIDEBUTTON message

Masque ou affiche le bouton spécifié dans une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur de commande du bouton à masquer ou afficher.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est un **booléen** qui indique s’il faut masquer ou afficher le bouton spécifié. Si la **valeur est true**, le bouton est masqué. Si la **valeur est false**, le bouton est affiché.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

