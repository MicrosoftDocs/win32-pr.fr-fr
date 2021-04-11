---
description: Une file d’attente d’appels ou un point de routage est une adresse spéciale dans le commutateur dans laquelle les appels sont temporairement détenus en attente.
ms.assetid: 1c801401-be05-4b5f-bc4f-628dde0f3cf7
title: Appels aux files d’attente et points de route
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66895101b72ca8e16810d3766edf897efcfedddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202710"
---
# <a name="call-queues-and-route-points"></a>Appels aux files d’attente et points de route

Une file d’attente d’appels ou un point de routage est une adresse spéciale dans le commutateur dans laquelle les appels sont temporairement détenus en attente. Cette caractéristique est représentée par la \_ file d’attente LINEADDRCAPFLAGS bits et LINEADDRCAPFLAGS \_ ROUTEPOINT dans le membre **dwAddrCapFlags** de [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps). Tous les appels apparaissant sur une telle adresse attendent une action de l’application, et il peut y avoir des actions par défaut qui se produisent (par exemple, un transfert vers un agent ou un Trunk) si l’application n’effectue aucune action dans un laps de temps défini. L’application doit être configurée par l’administrateur système afin de connaître les actions qu’il doit prendre en ce qui concerne les appels apparaissant sur chaque adresse de file d’attente ou de point de routage, ainsi que la durée nécessaire pour décider de l’action à entreprendre.

Les applications peuvent déterminer le nombre d’appels en attente dans une file d’attente ou un point d’itinéraire à l’aide de [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus). La fonction [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) peut être utilisée pour obtenir des informations telles que l’ID appelant, l’ID, l’origine entrante ou sortante, etc. et utilisée par l’application pour prendre des décisions sur la gestion des appels. les appels peuvent être redirigés, en aveugle, supprimés, etc., ou simplement autorisés à passer automatiquement de la file d’attente à une destination. Un appel passe à LINECALLSTATE \_ Disconnected s’il est abandonné. Les appels passent *inactifs* lorsqu’ils laissent la file d’attente ; **lineGetCallInfo** peut être utilisé pour lire l’identificateur de redirection afin de déterminer où ils ont été transférés.

Certains commutateurs autorisent les appels dans une file d’attente ou en attente pour recevoir un traitement particulier, tel que le silence, le rappel, le signal occupé, la musique ou l’écoute d’une annonce enregistrée. La fonction [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) permet à l’application de contrôler le traitement. La structure délimitée par les membres **dwCallTreatmentListSize** et **dwCallTreatmentListOffset** dans [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) permet aux applications de déterminer les traitements pris en charge. Le membre **dwCallTreatment** dans [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) indique le traitement actuel, et un message de [**ligne \_ CALLINFO**](line-callinfo.md) avec \_ traitement LINECALLINFOSTATE indique le moment où cette modification est apportée. Le \_ bit LINECALLFEATURE SETTREATMENT dans le membre **DwCallFeatures** de [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) indique le moment où l’application est autorisée à modifier le traitement. L' \_ ensemble de constantes LINECALLTREATMENT définit un ensemble limité de traitements d’appels prédéfinis ; les fournisseurs de services peuvent en définir beaucoup plus.

 

 



