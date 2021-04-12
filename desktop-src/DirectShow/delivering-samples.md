---
description: Exemples de livrables
ms.assetid: 31aabb6d-dec6-41fa-b24d-35a77b67bc4a
title: Exemples de livrables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083bc8c88649c04bdf9f93f86ebcc277ee48e75e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392896"
---
# <a name="delivering-samples"></a>Exemples de livrables

Cet article décrit comment un filtre fournit un exemple. Il décrit à la fois le modèle push, l’utilisation des méthodes [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) et le modèle pull, à l’aide de [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).

**Modèle push : distribution d’un exemple**

La broche de sortie fournit un exemple en appelant la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) ou la méthode [**IMemInputPin :: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) , qui est équivalente, mais fournit un tableau d’exemples. La broche d’entrée peut bloquer l’intérieur de **Receive** (ou **ReceiveMultiple**). Si le code pin peut se bloquer, sa méthode [**IMemInputPin :: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) doit retourner S \_ OK. Si le code confidentiel ne peut jamais se bloquer, **ReceiveCanBlock** doit retourner S \_ false. La \_ valeur de retour OK ne signifie pas que **Receive** Always se bloque.

Bien que la **réception** peut bloquer l’attente de la disponibilité d’une ressource, elle ne doit pas bloquer l’attente d’un plus grand nombre de données à partir du filtre en amont. Cela peut provoquer un blocage où le filtre en amont attend que le filtre en aval libère l’exemple, ce qui ne se produit jamais car le filtre en aval attend sur le filtre amont. Toutefois, si un filtre a plusieurs broches d’entrée, l’un d’eux peut attendre la réception de données par un autre code PIN. Par exemple, le filtre [multiplex MUX](avi-mux-filter.md) effectue cette opération afin qu’il puisse entrelacer les données audio et vidéo.

Un code confidentiel peut rejeter un échantillon pour plusieurs raisons :

-   Le code PIN est vidé (voir [vidage](flushing.md)).
-   Le pin n’est pas connecté.
-   Le filtre est arrêté.
-   Une autre erreur s’est produite.

La méthode **Receive** doit retourner S \_ false dans le premier cas, et un code d’échec dans les autres cas. Le filtre amont doit cesser d’envoyer des exemples quand le code de retour est différent de S \_ OK.

Vous pouvez considérer les trois premiers cas comme des défaillances « attendues », dans le sens où le filtre était dans un état incorrect pour recevoir des exemples. Une défaillance inattendue serait une erreur qui amène le code confidentiel à rejeter un échantillon, même si le code PIN est dans un état de réception. Si une erreur de ce type se produit, le code PIN doit envoyer une notification de fin de flux en aval et envoyer un événement [**EC \_ ERRORABORT**](ec-errorabort.md) au gestionnaire de graphique de filtre.

Dans les classes de base DirectShow, la méthode [**CBaseInputPin :: CheckStreaming**](cbaseinputpin-checkstreaming.md) vérifie les cas d’échec généraux (vidage, arrêt, etc.). La classe dérivée doit vérifier les erreurs qui sont spécifiques au filtre. En cas d’erreur, la méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) envoie la notification de fin de flux et l' \_ événement EC ERRORABORT.

**Modèle d’extraction : demande d’un exemple**

Dans l’interface **IAsyncReader** , la broche d’entrée demande des exemples à partir de la broche de sortie en appelant l’une des méthodes suivantes :

-   [**IAsyncReader :: Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [**IAsyncReader::SyncRead**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   [**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)

La méthode de **demande** est asynchrone ; la broche d’entrée appelle [**IAsyncReader :: WaitForNext**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-waitfornext) pour attendre la fin de la demande. Les deux autres méthodes sont synchrones.

**Quand fournir des données**

Un filtre remet toujours des exemples alors qu’il est à l’État en cours d’exécution. Dans la plupart des cas, un filtre fournit également des exemples lorsqu’il est suspendu. Cela permet au graphique d’indiquer les données afin que la lecture démarre immédiatement lorsque l' **exécution** est appelée (voir les [États de filtre](filter-states.md)). Si votre filtre ne remet pas de données pendant qu’il est suspendu, la méthode **IMediaFilter :: GetState** du filtre doit retourner VFW s ne peut pas se mettre \_ \_ \_ en pause. Ce code de retour indique au graphique de filtre de ne pas attendre les données de votre filtre avant de terminer la transition de pause. Dans le cas contraire, la méthode **Pause** se bloque indéfiniment. Pour obtenir un exemple de code, consultez [**CBaseFilter :: GetState**](cbasefilter-getstate.md).

Voici quelques exemples de cas où un filtre peut avoir besoin de retourner VFW S ne peut pas \_ \_ \_ signaler :

-   Les sources en direct, telles que les filtres de capture, ne doivent pas envoyer de données pendant la suspension. Consultez [production de données dans un filtre de capture](producing-data-in-a-capture-filter.md).
-   Un filtre de fractionnement peut ou non envoyer des données pendant la suspension, en fonction de l’implémentation. Si le filtre utilise des threads distincts pour mettre en file d’attente des données sur chaque broche de sortie, il peut envoyer des données en pause. Toutefois, si le filtre utilise un seul thread pour chaque broche de sortie, le premier code pin peut bloquer le thread lorsqu’il appelle **Receive**, ce qui empêche les autres broches d’envoyer des données. Dans ce cas, vous devez retourner VFW \_ S \_ \_ .
-   Un filtre peut fournir des données de façon sporadique. Par exemple, il peut analyser un flux de données personnalisé et filtrer certains paquets tout en distribuant d’autres utilisateurs. Dans ce cas, il n’est peut-être pas garanti que le filtre remette les données pendant la suspension.

Un filtre source (à l’aide du modèle push) ou un filtre d’analyseur (à l’aide du modèle push/pull) crée un ou plusieurs threads de streaming, qui fournissent des échantillons aussi rapidement que possible. Les filtres en aval, tels que les décodeurs et les transformations, envoient généralement des données uniquement lorsque la **réception** est appelée sur leurs broches d’entrée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Réception et envoi d’exemples](receiving-and-delivering-samples.md)
</dt> </dl>

 

 



