---
title: Propriété d’État ITsSbSession
description: Récupère ou spécifie l’état de session.
ms.assetid: 4e769ff7-2bd5-4fcb-b2d7-4dedc853482b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriété d’État
- Propriété State Services Bureau à distance, interface ITsSbSession
- Services Bureau à distance de l’interface ITsSbSession, propriété d’État
topic_type:
- apiref
api_name:
- ITsSbSession.State
- ITsSbSession.get_State
- ITsSbSession.put_State
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 308d8eef2a19ff9b92f7d860bb17662e84e4028eb21a5a228819b90b0af31ba3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128169"
---
# <a name="itssbsessionstate-property"></a>ITsSbSession :: State, propriété

Récupère ou spécifie l’état de session.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_State(
  [in]          TSSESSION_STATE State
);

HRESULT get_State(
  [out, retval] TSSESSION_STATE *pState
);
```



## <a name="property-value"></a>Valeur de la propriété

Valeur de l’énumération d' [**\_ État TSSESSION**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state) qui indique l’état d’une session.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                       |
| MIDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dt>

[**État de TSSESSION \_**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state)
</dt> </dl>

 

 





