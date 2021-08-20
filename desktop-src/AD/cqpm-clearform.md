---
title: Message CQPM_CLEARFORM (cmnquery. h)
description: Envoyé à la fonction de rappel CQPageProc d’une page de requête pour l’extension lorsque le contenu de la page doit être réinitialisé sur les valeurs par défaut.
ms.assetid: 0fd3ec82-0566-43de-a7a1-4b6b76bf2050
ms.tgt_platform: multiple
keywords:
- Message de CQPM_CLEARFORM Active Directory
topic_type:
- apiref
api_name:
- CQPM_CLEARFORM
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f900542c631193057985ca70d81dbfa7d3e53c6602f81a69b4e61a7cd107641a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021365"
---
# <a name="cqpm_clearform-message"></a>\_Message CQPM CLEARFORM

Le message **CQPM \_ CLEARFORM** est envoyé à la fonction de rappel [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) d’une page de requête pour l’extension lorsque le contenu de la page doit être réinitialisé sur les valeurs par défaut.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** en cas de réussite ou un code d’erreur **HRESULT** standard dans le cas contraire.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>Cmnquery. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





