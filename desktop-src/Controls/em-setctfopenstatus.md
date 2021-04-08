---
title: Message EM_SETCTFOPENSTATUS (RichEdit. h)
description: Ouvre ou ferme le clavier Text Services Framework (TSF).
ms.assetid: 9bdabf5a-93db-4b0e-9528-807d262de866
keywords:
- EM_SETCTFOPENSTATUS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf4163a415f129dfc5d3f98aa06578d13bb462e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033151"
---
# <a name="em_setctfopenstatus-message"></a>\_Message SETCTFOPENSTATUS em

Ouvre ou ferme le clavier Text Services Framework (TSF).

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Pour activer le clavier TSF, utilisez **true**. Pour désactiver le clavier TSF, utilisez **false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, ce message retourne la **valeur true**. En cas d’échec, ce message retourne **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP1 uniquement\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETCTFOPENSTATUS em**](em-getctfopenstatus.md)
</dt> </dl>

 

 





