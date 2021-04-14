---
title: Message CQPM_HANDLERSPECIFIC (cmnquery. h)
description: Valeur de base utilisée pour les messages qui sont privés pour le gestionnaire de requêtes.
ms.assetid: c3badb89-ee4e-4317-97aa-15187b9bb3e8
ms.tgt_platform: multiple
keywords:
- Message de CQPM_HANDLERSPECIFIC Active Directory
topic_type:
- apiref
api_name:
- CQPM_HANDLERSPECIFIC
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed06d4bd2b33eaf6224bb72f4814dfdced5cce2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464554"
---
# <a name="cqpm_handlerspecific-message"></a>\_Message CQPM HANDLERSPECIFIC

Le message **CQPM \_ HANDLERSPECIFIC** est la valeur de base utilisée pour les messages qui sont privés pour le gestionnaire de requêtes. Le gestionnaire de requêtes doit ajouter cette valeur aux messages privés pour s’assurer que les collisions de message ne se produisent pas.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Contient des données de message supplémentaires. Le contenu de ce paramètre est défini par le gestionnaire de requêtes.

</dd> <dt>

*lParam* 
</dt> <dd>

Contient des données de message supplémentaires. Le contenu de ce paramètre est défini par le gestionnaire de requêtes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La signification de la valeur de retour est définie par le gestionnaire de requêtes.

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

 

 





