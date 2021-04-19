---
description: L’interface ITParticipant est implémentée par le MSP IPConf. Il permet à une application de récupérer des informations sur les participants aux conférences et d’obtenir des pointeurs vers les flux associés à ces participants.
ms.assetid: 8c3edfc1-3165-48b7-9d83-8892c192498b
title: Interface ITParticipant (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8b7aa9d845d8d2489be0850bcc3fcf3f93ccdac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544035"
---
# <a name="itparticipant-interface"></a>Interface ITParticipant

\[**ITParticipant** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **ITParticipant** est implémentée par le [MSP ipconf](ipconf-msp.md). Il permet à une application de récupérer des informations sur les participants aux conférences et d’obtenir des pointeurs vers les flux associés à ces participants.

Cette interface est exposée sur l’objet d’appel lorsqu’un appel utilise la conférence IP. Un pointeur peut être obtenu en appelant **QueryInterface** à l’aide d’un pointeur [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .

## <a name="members"></a>Membres

L’interface **ITParticipant** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITParticipant** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITParticipant** possède ces méthodes.



| Méthode                                                                      | Description                                                                                                                                                             |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumerateStreams**](itparticipant-enumeratestreams.md)                  | Énumère les flux associés au participant actuel.<br/>                                                                                                  |
| [**Obtient \_ MediaTypes**](itparticipant-get-mediatypes.md)                     | Obtient les [**types de média**](tapimediatype--constants.md) associés à un participant.<br/>                                                                      |
| [**Obtient \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) | Obtient une représentation BSTR du type d’information nécessaire, par exemple PTI \_ EMAILADDRESS.<br/>                                                                     |
| [**afficher l' \_ État**](itparticipant-get-status.md)                             | Obtient l’état du participant.<br/>                                                                                                                          |
| [**recevoir des \_ flux**](itparticipant-get-streams.md)                           | Crée une collection de flux associés au participant actuel. Fourni pour les applications clientes Automation, telles que celles écrites en Visual Basic.<br/> |
| [**Placer l' \_ État**](itparticipant-put-status.md)                             | Définit si un flux associé au participant est activé.<br/>                                                                                            |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|--------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MSP IPConf](ipconf-msp.md)
</dt> <dt>

[Interfaces MSP IPConf](ipconf-msp-interfaces.md)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> </dl>

 

