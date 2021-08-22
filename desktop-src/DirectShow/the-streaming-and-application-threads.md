---
description: Threads de diffusion en continu et d’application
ms.assetid: 954f7abd-fe06-430a-b6f7-d60852826bc9
title: Threads de diffusion en continu et d’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a90916c14395a21aa5c53481c96b03fb6bbb2a8d4162cf996ef18ac15ce5e856
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583119"
---
# <a name="the-streaming-and-application-threads"></a>Threads de diffusion en continu et d’application

toute application DirectShow contient au moins deux threads importants : le thread d’application et un ou plusieurs threads de streaming. Les exemples sont fournis sur les threads de streaming, et les modifications d’État se produisent sur le thread d’application. Le thread de streaming principal est créé par un filtre de source ou d’analyseur. D’autres filtres peuvent créer des threads de travail qui fournissent des exemples. ceux-ci sont également considérés comme des threads de diffusion en continu.

Certaines méthodes sont appelées sur le thread d’application, tandis que d’autres sont appelées sur un thread de streaming. Par exemple :

-   Thread (s) de diffusion en continu : [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**IMemInputPin :: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple), [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream), [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).
-   Thread d’application : [**IMediaFilter ::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**IMediaFilter :: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**IMediaFilter :: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop), [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions), [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).
-   Soit : [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).

Le fait de disposer d’un thread de streaming distinct permet aux données de circuler dans le graphique alors que le thread d’application attend une entrée de l’utilisateur. Toutefois, le risque de plusieurs threads est qu’un filtre peut créer des ressources lorsqu’il s’interrompt (sur le thread d’application), les utiliser à l’intérieur d’une méthode de diffusion en continu et les détruire lorsqu’il s’arrête (également sur le thread d’application). Si vous n’êtes pas vigilant, le thread de streaming peut essayer d’utiliser les ressources une fois qu’elles ont été détruites. La solution consiste à protéger les ressources à l’aide de sections critiques et à synchroniser les méthodes de streaming avec les changements d’État.

Un filtre a besoin d’une section critique pour protéger l’état du filtre. La classe [**CBaseFilter**](cbasefilter.md) possède une variable membre pour cette section critique, [**CBaseFilter :: m \_ pLock**](cbasefilter-m-plock.md). Cette section critique est appelée verrou de filtre. En outre, chaque broche d’entrée a besoin d’une section critique pour protéger les ressources utilisées par le thread de streaming. Ces sections critiques sont appelées verrous de diffusion en continu. vous devez les déclarer dans votre classe pin dérivée. il est plus facile d’utiliser la classe [**CCritSec**](ccritsec.md) , qui encapsule un objet Windows **\_ SECTION critique** et peut être verrouillée à l’aide de la classe [**CAutoLock**](cautolock.md) . La classe **CCritSec** fournit également des fonctions de débogage utiles. Pour plus d’informations, consultez [tâches de débogage de la section critique](critical-section-debugging-functions.md).

Lorsqu’un filtre s’arrête ou vide, il doit synchroniser le thread d’application avec le thread de streaming. Pour éviter le blocage, il doit tout d’abord débloquer le thread de streaming, ce qui peut être bloqué pour plusieurs raisons :

-   Il attend d’obtenir un exemple à l’intérieur de la méthode [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) , car tous les exemples de l’allocateur sont en cours d’utilisation.
-   Il attend qu’un autre filtre retourne à partir d’une méthode de streaming, telle que **Receive**.
-   Elle est en attente dans l’une de ses propres méthodes de diffusion en continu, pour qu’une ressource soit disponible.
-   Il s’agit d’un filtre de convertisseur qui attend l’heure de présentation de l’exemple suivant
-   Il s’agit d’un filtre de convertisseur qui attend à l’intérieur de la méthode **Receive** tout en étant suspendu.

Par conséquent, lorsque le filtre s’arrête ou vide, il doit effectuer les opérations suivantes :

-   Publiez un échantillon qu’il détient pour une raison quelconque. Cela débloque la méthode **GetBuffer** .
-   Retournez à partir de n’importe quelle méthode de diffusion le plus rapidement possible. Si une méthode de streaming attend une ressource, elle doit cesser d’attendre immédiatement.
-   Commencez à rejeter les exemples dans **Receive**, afin que le thread de streaming n’accède plus à plus de ressources. (La classe [**CBaseInputPin**](cbaseinputpin.md) gère cela automatiquement.)
-   La méthode **Stop doit annuler** la validation de tous les allocateurs du filtre. (La classe **CBaseInputPin** gère cela automatiquement.)

Le vidage et l’arrêt des deux se produisent sur le thread d’application. Un filtre s’arrête en réponse à la méthode [**IMediaControl :: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) . le gestionnaire de Graph de filtre émet la commande stop dans l’ordre amont, en commençant par les convertisseurs et en remontant les filtres sources. La commande Stop se produit complètement à l’intérieur de la méthode **CBaseFilter :: Stop** du filtre. Lorsque la méthode retourne, le filtre doit être arrêté.

Le vidage se produit généralement en raison d’une commande Seek. Une commande flush démarre à partir du filtre source ou de l’analyseur et se déplace en aval. Le vidage se produit en deux étapes : la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) informe un filtre d’ignorer toutes les données en attente et entrantes ; la méthode [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) signale au filtre d’accepter à nouveau les données. Le vidage requiert deux étapes, car l’appel **BeginFlush** se trouve sur le thread d’application, pendant lequel le thread de streaming continue à remettre les données. Par conséquent, certains exemples peuvent arriver après l’appel **BeginFlush** . Le filtre doit les ignorer. Tous les exemples arrivant après l’appel **EndFlush** sont toujours nouveaux et doivent être remis.

Les sections qui suivent contiennent des exemples de code qui montrent comment implémenter les méthodes de filtre les plus importantes, telles que la **suspension**, la **réception**, etc., de manière à éviter les blocages et les conditions de concurrence critique. Toutefois, chaque filtre a des exigences différentes. vous devrez donc adapter ces exemples à votre filtre particulier.

> [!Note]  
> Les classes de base [**CTransformFilter**](ctransformfilter.md) et [**CTransInPlaceFilter**](ctransinplacefilter.md) gèrent un grand nombre des problèmes décrits dans cet article. Si vous écrivez un filtre de transformation et que votre filtre n’attend pas d’événements à l’intérieur d’une méthode de diffusion en continu ou si vous maintenez des exemples en dehors de **Receive**, ces classes de base doivent être suffisantes.

 

 

 



