---
title: Message CQPM_HELP (cmnquery. h)
description: Envoyé à la fonction de rappel CQPageProc d’une page d’extension de formulaire de requête pour permettre à l’extension de page d’afficher l’aide contextuelle pour la page.
ms.assetid: 07f5bd24-bca2-4d87-8e1e-acce552a3bf2
ms.tgt_platform: multiple
keywords:
- Message de CQPM_HELP Active Directory
topic_type:
- apiref
api_name:
- CQPM_HELP
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a50be772a429a2eb2f87bf3cf1679dcfc68e811d80244f10dd4ec33f3f2b7d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021095"
---
# <a name="cqpm_help-message"></a>\_Message d’aide CQPM

Le message d' **\_ aide CQPM** est envoyé à la fonction de rappel [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) d’une page d’extension de formulaire de requête pour permettre à l’extension de page d’afficher l’aide contextuelle pour la page. Si possible, l’extension de la page de requête doit afficher l’aide contextuelle en réponse à cet événement.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) qui contient des données supplémentaires sur l’élément de menu, le contrôle, la boîte de dialogue ou la fenêtre pour laquelle une aide contextuelle est demandée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message est ignorée.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>Cmnquery. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo)
</dt> </dl>

 

