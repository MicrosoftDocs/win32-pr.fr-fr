---
description: L’interface ITParticipantEvent contient des méthodes qui récupèrent la description des événements participant.
ms.assetid: 1199ec91-ee06-4e6c-8d8f-1585a3da3db0
title: Interface ITParticipantEvent (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac6e2b43a528bc041a71962e84b4e1be62152a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525500"
---
# <a name="itparticipantevent-interface"></a>Interface ITParticipantEvent

\[**ITParticipantEvent** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **ITParticipantEvent** contient des méthodes qui récupèrent la description des événements participant. Lorsque l’implémentation de l’application de la méthode [**ITTAPIEventNotification :: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) indique qu’un [**\_ événement TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) est égal à **te \_ Private**, le paramètre *pEvent* de la méthode est un pointeur **IDispatch** pour l’interface **ITParticipantEvent** . Les méthodes de cette interface peuvent être utilisées pour récupérer des informations concernant une modification de participant qui s’est produite.

> [!Note]  
> Vous devez appeler la méthode [**ITTAPI ::p ut \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) et définir un masque de filtre d’événement qui comprend l’événement **\_ Private te** pour activer la réception des événements participant. Si vous n’appelez pas **ITTAPI ::p ut \_ EventFilter**, votre application ne recevra aucun événement. Pour plus d’informations, consultez la vue d’ensemble des [événements](events.md) .

 

## <a name="members"></a>Membres

L’interface **ITParticipantEvent** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITParticipantEvent** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITParticipantEvent** possède ces méthodes.



| Méthode                                                         | Description                                                                                                                                     |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**recevoir un \_ événement**](itparticipantevent-get-event.md)             | Obtient le descripteur d' [**\_ événement participant**](participant-event.md) de l’événement.<br/>                                                    |
| [**recevoir un \_ participant**](itparticipantevent-get-participant.md) | Obtient un pointeur vers un tableau d’interfaces [**ITParticipant**](itparticipant.md) représentant les participants impliqués dans l’événement.<br/> |
| [**extraire le sous- \_ flux**](itparticipantevent-get-substream.md)     | Obtient un pointeur vers un tableau d’interfaces [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) représentant les sous-flux impliqués dans l’événement.<br/>       |



 

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
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**\_événement participant**](participant-event.md)
</dt> <dt>

[**ITTAPIEventNotification :: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
</dt> <dt>

[**\_événement TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
</dt> <dt>

[Enregistrer l’extrait de code des événements](register-events.md)
</dt> </dl>

 

