---
description: L’interface ITParticipantSubStreamControl est implémentée par le MSP IPConf.
ms.assetid: d5af0fb1-af18-4efb-9b68-1fa60c1272f6
title: Interface ITParticipantSubStreamControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e910022d45ca9f9516adbe8aeebbdb172d66f28ab1bf8cb23219c2eee80f56cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774599"
---
# <a name="itparticipantsubstreamcontrol-interface"></a>Interface ITParticipantSubStreamControl

\[**ITParticipantSubStreamControl** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **ITParticipantSubStreamControl** est implémentée par le MSP ipconf. Cette interface est exposée sur l’objet d’appel. Cette interface fournit des méthodes qui permettent à une application de découvrir ou de contrôler la correspondance entre le sous-flux et le participant. L’interface **ITParticipantSubStreamControl** est créée en appelant **QueryInterface** sur [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).

## <a name="members"></a>Membres

L’interface **ITParticipantSubStreamControl** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITParticipantSubStreamControl** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITParticipantSubStreamControl** possède ces méthodes.



| Méthode                                                                                              | Description                                                     |
|:----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [**Obtient \_ ParticipantFromSubStream**](itparticipantsubstreamcontrol-get-participantfromsubstream.md) | Obtient les participants associés à un sous-flux donné.<br/> |
| [**Obtient \_ SubStreamFromParticipant**](itparticipantsubstreamcontrol-get-substreamfromparticipant.md) | Obtient les sous-flux associés à un participant donné.<br/> |
| [**SwitchTerminalToSubStream**](itparticipantsubstreamcontrol-switchterminaltosubstream.md)        | Définit un participant sur un sous-flux.<br/>                   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

