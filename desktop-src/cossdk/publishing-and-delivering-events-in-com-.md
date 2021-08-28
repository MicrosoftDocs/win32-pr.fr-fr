---
description: Pour publier un événement, il vous suffit d’instancier un objet de classe d’événements et d’appeler la méthode souhaitée. pour obtenir des instructions détaillées sur la façon de procéder dans le code, consultez publication d’un événement.
ms.assetid: 835c3753-fdcc-4afe-94c3-c954aaf1c832
title: Publication et diffusion d’événements dans COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de1625d1e18340d71b3ad3a53c06d2db79b9fd1f913e7a49274644bc3a715c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118812860"
---
# <a name="publishing-and-delivering-events-in-com"></a>Publication et diffusion d’événements dans COM+

Pour publier un événement, il vous suffit d’instancier un objet de [classe d’événements](the-com--event-class-object.md) et d’appeler la méthode souhaitée. pour obtenir des instructions détaillées sur la façon de procéder dans le code, consultez [publication d’un événement](publishing-an-event.md).

Lorsqu’un serveur de publication déclenche un événement, le service d’événements COM+ recherche la base de données d’abonnement pour trouver tous les abonnés qui ont inscrit des abonnements à la classe d’événements instanciée. Il se connecte à ces abonnés (par la création directe, les monikers ou les composants mis en file d’attente) et appelle la méthode. Pour prendre en charge plusieurs notifications de l’abonné pour un événement, les méthodes peuvent contenir uniquement des paramètres in et doivent retourner uniquement des valeurs **HRESULT** de réussite ou d’échec.

> [!Note]  
> Cette version des événements COM+ ne prend pas en charge un magasin d’événements distribué. Un abonné doit s’abonner à un événement sur chaque ordinateur à partir duquel il souhaite recevoir une notification. Vous pouvez également enregistrer l’objet de classe d’événements et les abonnements sur un ordinateur central et instancier cet objet de classe d’événements à partir des ordinateurs distants sur lesquels vous publiez des événements. La remise des événements est fournie par DCOM ou par le service de composants en file d’attente COM+. Pour plus d’informations sur l’utilisation du service COM+ Queued Components, consultez [utilisation d’événements com+ avec des composants en file d’attente com+](using-com--events-with-com--queued-components.md).

 

Par défaut, le service événements COM+ déclenche un événement à la fois, sans ordre déterminé ou reproductible. Les serveurs de publication qui ont besoin de contrôler l’ordre dans lequel les abonnés reçoivent un événement peuvent implémenter un filtre de l’éditeur. (Pour plus d’informations, consultez [filtrage des événements dans com+](filtering-events-in-com-.md).)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtrage des événements dans COM+](filtering-events-in-com-.md)
</dt> <dt>

[Abonnements](subscriptions.md)
</dt> <dt>

[Objet de classe d’événements COM+](the-com--event-class-object.md)
</dt> <dt>

[Utilisation d’événements COM+ avec des composants en file d’attente COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



