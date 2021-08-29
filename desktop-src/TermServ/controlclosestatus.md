---
title: Énumération ControlCloseStatus
description: Indique si l’application contenant le contrôle peut fermer le contrôle immédiatement.
ms.assetid: ac2e1c68-81b1-4b51-aa7e-0ff703e619a2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’énumération ControlCloseStatus
topic_type:
- apiref
api_name:
- ControlCloseStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e663ce5f6b8fd4536942bd9426c230255aa5132c04a3e2ed0133d6d32d4e6272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119401619"
---
# <a name="controlclosestatus-enumeration"></a>Énumération ControlCloseStatus

Indique si l’application contenant le contrôle peut fermer le contrôle immédiatement.

## <a name="syntax"></a>Syntaxe


```C++
enum ControlCloseStatus {
  controlCloseCanProceed     = 0x0000, 
  controlCloseWaitForEvents  = 0x0001 

};
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed**
</dt> <dd>

Le conteneur peut continuer immédiatement. Cela peut se produire si le contrôle n’est pas connecté.

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents**
</dt> <dd>

Le conteneur doit attendre les événements [**IMsTscAxEvents :: OnDisconnected**](imstscaxevents-ondisconnected.md) ou [**IMsTscAxEvents :: OnConfirmClose**](imstscaxevents-onconfirmclose.md).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                      |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md)
</dt> <dt>

[**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





