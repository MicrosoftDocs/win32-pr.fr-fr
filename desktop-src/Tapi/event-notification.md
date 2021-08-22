---
description: La notification d’événements est le principal moyen par lequel une application obtient des informations de la part de l’interface TAPI et des fournisseurs de services.
ms.assetid: 02160f10-dc3f-484c-9cd3-bcfb07ded822
title: Notification d'événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a83ed721ed22049baeaf3de15626ed8deecf2a7562d883658195eb1eb590f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003667"
---
# <a name="event-notification"></a>Notification d'événement

La notification d’événements est le principal moyen par lequel une application obtient des informations de la part de l’interface TAPI et des fournisseurs de services. Ces informations peuvent être l’état d’une opération asynchrone qui a été provoquée par l’application ou qui peut concerner un processus démarré en dehors de l’application, comme des notifications de nouveaux appels entrants.

**TAPI 2. x :** Les applications gèrent la notification de l’une des trois manières suivantes : fenêtre masquée, descripteur d’événement ou port de terminaison. Pour plus d’informations sur ces mécanismes de notification, consultez la section Notes pour [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa). Une application spécifie le mécanisme en définissant le membre **dwOptions** de la structure [**LINEINITIALIZEEXPARAMS**](/windows/win32/api/tapi/ns-tapi-lineinitializeexparams) avant d’appeler [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).

La fonction [**lineSetStatusMessages**](/windows/win32/api/tapi/nf-tapi-linesetstatusmessages) permet à une application de spécifier les messages de notification à recevoir pour les événements liés aux modifications d’État pour la ligne spécifiée ou l’une de ses adresses.

**TAPI 3. x :** Les applications gèrent la notification générale à l’aide d' [objets connectables](../com/events-in-com-and-connectable-objects.md)standard com. [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) est l’interface sortante qui doit être inscrite auprès de l’objet conteneur de l’interface TAPI et [**ITTAPIEventNotification :: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) est la méthode appelée par TAPI pour déterminer la réponse de l’application. La méthode [**ITTAPI ::p ut \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) indique à TAPI les événements qui présentent un intérêt pour l’application. Si aucun filtre d’événements n’est entré, l’application ne reçoit pas de notification de tous les événements. La méthode [**ITTAPI :: RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) indique à l’interface TAPI les types de média et les adresses pour lesquels l’application gère les sessions entrantes. Pour plus d’informations sur la gestion des événements TAPI 3, consultez la vue d’ensemble des [événements](events.md) ou l’exemple de code [Register Events](register-events.md) .

Les fournisseurs de services de téléphonie implémentent [**TSPI \_ LineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) et [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages). L’interface TAPI appelle ces fonctions pour indiquer l’ensemble des événements de ligne, d’adresse et de type de média demandés par les applications.

 

 
