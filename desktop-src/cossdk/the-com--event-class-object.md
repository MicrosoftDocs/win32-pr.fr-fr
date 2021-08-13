---
description: Le service d’événements COM+ utilise un objet de classe d’événements pour gérer la connexion entre le serveur de publication et l’abonné.
ms.assetid: 877c5890-588d-4978-8fb2-b4ecf4134068
title: Objet de classe d’événements COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5650969895cdfa63f07e6ba77e617a962335101d4f56aeb21a5b439b27daaf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546151"
---
# <a name="the-com-event-class-object"></a>Objet de classe d’événements COM+

Le service d’événements COM+ utilise un *objet de classe d’événements* pour gérer la connexion entre le serveur de publication et l’abonné. L’objet de classe d’événements est un composant COM+ géré et stocké par le système d’événements COM+ et qui contient les interfaces et les méthodes utilisées par un serveur de publication pour déclencher des événements. Il s’agit d’un objet persistant qui indique les événements qui peuvent se produire et, éventuellement, identifie le serveur de publication. Vous spécifiez les interfaces et les méthodes que vous souhaitez qu’une classe d’événements contienne en fournissant une bibliothèque de types.

pour déclencher un événement, le serveur de publication instancie l’objet de classe d’événements en appelant [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou la méthode Microsoft Visual Basic **CreateObject** et en demandant que l’interface d’événement soit retournée. L’objet de classe d’événements instancié contient l’implémentation du système d’événements de l’interface demandée. Un abonné intéressé doit également implémenter l’interface de la classe d’événements pour recevoir les événements d’un serveur de publication donné. Lorsque l’objet de classe d’événements est instancié, le système d’événements l’associe aux abonnés appropriés. La liste des abonnés est conservée pendant la durée de vie de l’objet de classe d’événements. Un événement peut être remis à plusieurs abonnés en série ou en parallèle.

Lorsque vous implémentez un objet de classe d’événements, vous devez fournir une DLL à inscription automatique qui exporte les fonctions [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) et [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) . La fonction **DllRegisterServer** inscrit une classe com et la fonction **DllUnregisterServer** annule l’inscription du composant. Les objets de la classe d’événements sont stockés dans le catalogue COM+, soit à l’aide de l’outil d’administration Services de composants, soit par programme à l’aide des méthodes des interfaces [**ICOMAdminCatalog :: InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass) ou [**ICOMAdminCatalog :: InstallMultipleEventClasses**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installmultipleeventclasses) . Pour plus d’informations sur l’inscription des objets de classe d’événements, consultez [inscription d’une classe d’événements](registering-an-event-class.md).

Étant donné que les objets de classe d’événements sont des composants configurés, d’autres attributs, tels que la mise en file d’attente, les transactions, la sécurité, etc., peuvent être configurés pour eux à l’aide de l’outil d’administration Services de composants ou des fonctions du SDK d’administration COM+.

> [!Note]  
> Le service d’événements COM+ utilise le marshaling de bibliothèque de types. Cela place des restrictions sur les interfaces de classes d’événements. Par exemple, le marshaleur de bibliothèque de types ne prend pas en charge la taille des attributs MIDL et la [**longueur \_ est**](/windows/desktop/Midl/length-is). [**\_**](/windows/desktop/Midl/size-is)

 

Un objet de classe d’événements possède des attributs de publication qui déterminent la façon dont les événements sont publiés, ainsi que les propriétés suivantes :

-   **EventCLSID**. Identificateur unique qui spécifie le CLSID du composant.
-   **Événements**. Identificateur unique qui spécifie le PROGID du composant.
-   **TypeLibrary**. Fournit la liste des interfaces offertes par l’objet de classe d’événements. Il n’est pas nécessaire d’implémenter les interfaces de déclenchement spécifiées dans la bibliothèque de types.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Considérations sur la sécurité des événements COM+](com--events-security-considerations.md)
</dt> <dt>

[Filtrage des événements dans COM+](filtering-events-in-com-.md)
</dt> <dt>

[Publication et diffusion d’événements dans COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Abonnements](subscriptions.md)
</dt> <dt>

[Utilisation d’événements COM+ avec des composants en file d’attente COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 
