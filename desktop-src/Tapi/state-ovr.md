---
description: L’état de la session ou de l’appel indique l’état actuel d’une session, par exemple &\# 0034 ; offre&\# 0034 ; ou &\# 0034 ; connecté. &\# 0034 ; La gestion correcte des informations d’État est essentielle au bon fonctionnement de la plupart des applications TAPI.
ms.assetid: a6a49b77-4e9b-4f23-bfe6-26f26549b18f
title: State
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88fb9c482fcb9e432b5bfb5d36f77cd09f538086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542021"
---
# <a name="state"></a>State

L’état de la session ou de l’appel indique l’état actuel d’une session, par exemple « offre » ou « connecté ». La gestion correcte des informations d’État est essentielle au bon fonctionnement de la plupart des applications TAPI. Par exemple, l’opération de réponse ne peut être effectuée que sur une session proposée, mais un transfert échoue si la session est dans cet État.

L’état d’une session change suite à des événements. Les événements peuvent être sollicités ou non. Les *événements sollicités* sont provoqués par l’application qui contrôle la session, par exemple lorsqu’elle appelle une opération de session TAPI. Les *événements non sollicités* sont provoqués par le commutateur, le réseau téléphonique, l’utilisateur qui appuie sur les boutons du téléphone local ou les actions du tiers distant.

Chaque fois qu’un fournisseur de services détecte un changement d’état de session, il signale la modification à l’interface TAPI et TAPI envoie une notification d’événement à toutes les applications propriétaire et moniteur. L’application doit réagir à ces notifications de manière appropriée. Pour plus d’informations sur le contrôle des événements signalés à une application, consultez notification d’événements sous [initialisation TAPI](tapi-initialization.md) .

Une application doit toujours traiter les notifications d’événements d’État. Les transitions d’état valides pour une configuration physique peuvent être non valides pour une autre. Par exemple, considérez une ligne qui se termine physiquement à la fois sur l’ordinateur et sur un autre ensemble de téléphones, en créant une configuration de ligne de tiers entre l’ordinateur et l’ensemble de téléphones. Une application en cours d’exécution sur l’ordinateur peut ne pas connaître les activités de l’ensemble de téléphones. Autrement dit, la ligne peut être utilisée sans que le fournisseur de services en ait connaissance. Une application qui tente d’effectuer un appel sortant aboutit à l’allocation d’une apparence d’appel à partir de l’interface TAPI, mais cela se traduit par le partage de l’appel actif sur la ligne. L’envoi aveugle d’une chaîne de numérotation DTMF sans vérification préalable d’une tonalité peut ne pas aboutir à un comportement intentionnel (ou poli).

Une application ne doit pas supposer une progression rigide d’un État à un autre. Les événements d’État arrivent et sont transférés de manière asynchrone et les notifications peuvent ne pas être reçues dans un ordre prévisible. Par conséquent, les notifications d’état d’appel doivent être affichées pour indiquer à l’application le nouvel état de l’appel au lieu de signaler les transitions entre deux États.

Tous les fournisseurs de services de téléphonie doivent fournir ces informations.

* * TAPI 2. x : * *[**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**\_ CALLSTATE**](./line-callstate.md) , LINECALLSTATE, [ \_ constantes](./linecallstate--constants.md)

**TAPI 3. x : **[**ITCallInfo :: obten \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** CIL \_ CALLID** membre de [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent) notification, [**Call \_ State**](/windows/desktop/api/Tapi3if/ne-tapi3if-call_state) Enumerator

 

 
