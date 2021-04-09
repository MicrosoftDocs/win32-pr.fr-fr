---
title: Configuration de la file d’attente des demandes
description: Configuration de la file d’attente des demandes
ms.assetid: ab03089c-2ef1-457d-a5f5-a4d400f3a7f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ed397ffbcb42d887d519bc4492bd167dd98c57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840013"
---
# <a name="configuring-the-request-queue"></a>Configuration de la file d’attente des demandes

Lorsque la file d’attente de demandes est ouverte ou créée, l’application appelante reçoit un descripteur qui peut être utilisé pour envoyer des demandes ou configurer la file d’attente de demandes. L’appel de [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) avec **HttpServerBindingProperty** et la spécification du descripteur de la file d’attente des demandes dans la structure des [**\_ \_ informations de liaison http**](/windows/desktop/api/Http/ns-http-http_binding_info) , spécifiée dans le paramètre *pPropertyInformation* , associe le groupe d’URL à la file d’attente de demandes. Les propriétés de la file d’attente des demandes sont définies uniquement par l’application qui crée la file d’attente des demandes. Par exemple, pour définir la propriété longueur de la file d’attente du serveur, l’application Creator appelle [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) en spécifiant **HttpServerQueueLengthProperty** dans le paramètre *Property* .

 

 




