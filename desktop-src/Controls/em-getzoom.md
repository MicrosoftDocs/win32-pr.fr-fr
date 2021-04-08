---
title: Message EM_GETZOOM (RichEdit. h)
description: Obtient le rapport de zoom actuel. Le taux de zoom est toujours compris entre 1/64 et 64. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: d4a1daee-4af7-44d1-80d6-0fcaaf3672a8
keywords:
- EM_GETZOOM les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a88aa96787e1fda5cdeb8f77f478a4d51635cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740293"
---
# <a name="em_getzoom-message"></a>\_Message GETZOOM em

Obtient le taux de zoom actuel pour un contrôle d’édition multiligne ou un contrôle RichEdit. Le taux de zoom est toujours compris entre 1/64 et 64.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Reçoit le numérateur du rapport de zoom.

</dd> <dt>

*lParam* 
</dt> <dd>

Reçoit le dénominateur du rapport de zoom.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Le message retourne la **valeur true** si le message est traité, ce qui est le cas si *wParam* et *lParam* n’ont pas la **valeur null**.

## <a name="remarks"></a>Notes

**Modifier :** Pris en charge dans Windows 10 1809 et versions ultérieures. Le contrôle d’édition doit avoir le jeu de styles étendus **es \_ ex \_ zoomable** . pour que ce message ait un effet, consultez [modifier les styles étendus de contrôle](edit-control-window-extended-styles.md). Pour plus d’informations sur le contrôle d’édition, consultez [modifier des contrôles](edit-controls.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | Édition enrichie 3,0<br/>                                                              |
| En-tête<br/>                   | <dl> <dt>RichEdit. h/commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETZOOM em**](em-setzoom.md)
</dt> </dl>

 

 





