---
title: Message CQPM_ENABLE (cmnquery. h)
description: Envoyé à la fonction de rappel CQPageProc d’une page d’extension de formulaire de requête pour activer ou désactiver la page.
ms.assetid: dc75fab7-6de7-4138-86df-84d44e774120
ms.tgt_platform: multiple
keywords:
- Message de CQPM_ENABLE Active Directory
topic_type:
- apiref
api_name:
- CQPM_ENABLE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0252c5e1ec7fd9633241416fbf01bb4ead52c45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032499"
---
# <a name="cqpm_enable-message"></a>CQPM \_ activer le message

Le message d' **\_ activation de CQPM** est envoyé à la fonction de rappel [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) d’une page d’extension de formulaire de requête pour activer ou désactiver la page.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Contient zéro pour désactiver la page ou une valeur différente de zéro pour activer la page.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé.

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
</dt> </dl>

 

 





