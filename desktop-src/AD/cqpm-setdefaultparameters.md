---
title: Message CQPM_SETDEFAULTPARAMETERS (cmnquery. h)
description: Envoyé à la fonction de rappel CQPageProc d’une page d’extension de formulaire de requête pour définir d’autres paramètres par défaut pour la page.
ms.assetid: 4d7f1c03-5c67-4f4c-b381-034a142251fe
ms.tgt_platform: multiple
keywords:
- Message de CQPM_SETDEFAULTPARAMETERS Active Directory
topic_type:
- apiref
api_name:
- CQPM_SETDEFAULTPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4df77b9068c23a0eeac30181d131cb8469dc53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465158"
---
# <a name="cqpm_setdefaultparameters-message"></a>\_Message CQPM SETDEFAULTPARAMETERS

Le message **CQPM \_ SETDEFAULTPARAMETERS** est envoyé à la fonction de rappel [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) d’une page d’extension de formulaire de requête pour définir d’autres paramètres par défaut pour la page.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Contient une valeur différente de zéro si la page est la page par défaut ou zéro dans le cas contraire.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**OPENQUERYWINDOW**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow) qui contient des données sur la boîte de dialogue requête de service d’annuaire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message est ignorée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>Cmnquery. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[**OPENQUERYWINDOW**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow)
</dt> </dl>

 

 





