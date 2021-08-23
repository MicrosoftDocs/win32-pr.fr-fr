---
description: Serveurs de distribution de plug-in
ms.assetid: 80ff713d-f704-40d3-9317-cbf33d932207
title: Serveurs de distribution de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70d253066fdde4f082a964c56a221331cfd127c0984db2a7b1933a0bb352425
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583659"
---
# <a name="plug-in-distributors"></a>Serveurs de distribution de plug-in

Les serveurs de distribution de plug-in (PID) permettent d’étendre les fonctionnalités du gestionnaire de graphes de filtre. Un serveur de distribution de plug-in est un objet COM que le gestionnaire de graphique de filtre agrège au moment de l’exécution. Les applications obtiennent l’accès au PID via le gestionnaire de graphes de filtre.

Lorsque le gestionnaire de graphique de filtre est interrogé pour une interface qu’il ne prend pas en charge, il recherche une clé dans le registre, sous la forme suivante :


```C++
HKEY_CLASSES_ROOT\Interface\IID\Distributor
```



`IID` chaîne contenant l’identificateur d’interface. Si l’entrée de Registre existe, la valeur de l’entrée définit l’identificateur de classe (CLSID) d’un PID qui prend en charge l’interface. Le gestionnaire de graphique de filtre agrège le PID et retourne un pointeur d’interface, agissant ainsi comme **IUnknown** externe pour le PID. Lorsque l’application appelle des méthodes sur l’interface, elle les appelle en fait sur le PID. Toutefois, l’existence du PID est transparente pour l’application.

Le terme « *distributeur* » vient du fait qu’un PID peut interroger son pointeur **IUnknown** externe pour les interfaces sur le gestionnaire de graphes de filtre. En appelant la méthode [**IFilterGraph :: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) , le PID peut énumérer les filtres dans le graphique et distribuer les appels de méthode à ces filtres. De cette façon, un PID peut servir de point de contrôle unique pour que l’application puisse appeler des méthodes sur des filtres.

Lorsque le gestionnaire de graphique de filtre agrège un PID, il interroge le PID de l’interface [**IDistributorNotify**](/windows/desktop/api/Strmif/nn-strmif-idistributornotify) . Si le PID prend en charge cette interface, le gestionnaire de graphes de filtres l’utilise pour informer le PID des modifications apportées au graphique :

-   Lorsque le graphique de filtre bascule entre les États d’exécution, suspendus et arrêtés, il appelle [**IDistributorNotify :: Run**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-run), [**IDistributorNotify ::P ause**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-pause)ou [**IDistributorNotify :: Stop**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-stop).
-   Quand une horloge de référence est définie, le gestionnaire de graphique de filtre appelle [**IDistributorNotify :: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-setsyncsource).
-   Lorsque vous ajoutez ou supprimez des filtres, ou si les connexions d’épinglage sont modifiées, le gestionnaire de graphique de filtre appelle [**IDistributorNotify :: NotifyGraphChange**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-notifygraphchange).

Pour implémenter un PID personnalisé, créez un objet COM qui prend en charge l’agrégation. Il doit prendre en charge une interface que le gestionnaire de graphique de filtre ne prend pas encore en charge. Le cas échéant, il peut prendre en charge l’interface **IDistributorNotify** .

Si le PID obtient des pointeurs d’interface à partir du gestionnaire de graphes de filtre, il doit les libérer immédiatement. Dans le cas contraire, il peut créer un nombre de références circulaires, ce qui peut empêcher la destruction du gestionnaire de graphique de filtre. Le maintien d’un décompte de références sur le gestionnaire de graphique de filtre n’est pas nécessaire dans tous les cas, car le gestionnaire de graphique de filtre contrôle la durée de vie du PID.

Comme un PID est conçu spécifiquement pour l’agrégation par le gestionnaire de graphes de filtre, vous souhaiterez peut-être l’appliquer dans la méthode du constructeur du PID. Vérifiez si le pointeur **IUnknown** externe a la **valeur null** et, si tel est le cas, retournez le code d’erreur VFW E a besoin d’un \_ \_ \_ propriétaire. (Voir [les codes d’erreur et de réussite](error-and-success-codes.md).) En outre, pour empêcher d’autres objets d’agréger le PID, vous pouvez interroger le pointeur **IUnknown** externe pour l’interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) . Retourne un code d’erreur si l’objet n’expose pas **IGraphBuilder**.

 

 



