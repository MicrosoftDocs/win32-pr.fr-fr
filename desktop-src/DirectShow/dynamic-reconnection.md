---
description: Reconnexion dynamique
ms.assetid: 5b777f64-6b62-48dd-8eae-6603582a452a
title: Reconnexion dynamique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b558a2e00ee2577cf1d31dda7aaebb15b5bd740c6dad5689e70b950c02d4d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966153"
---
# <a name="dynamic-reconnection"></a>Reconnexion dynamique

dans la plupart des DirectShow les filtres, les codes confidentiels ne peuvent pas être reconnectés lorsque le graphique diffuse activement des données. L’application doit arrêter le graphique avant de reconnecter les broches. Toutefois, certains filtres prennent en charge les reconnexions de code confidentiel pendant que le graphique est en cours d’exécution, un processus appelé reconnexion dynamique. Cela peut être effectué par l’application ou par un filtre dans le graphique.

À titre d’exemple, examinez le graphique dans l’illustration suivante.

![diagramme de création de graphique dynamique](images/dyngraph.png)

Un scénario de reconnexion dynamique peut consister à supprimer le filtre 2 du graphique, tandis que le graphique est en cours d’exécution et à le remplacer par un autre filtre. Pour que ce scénario fonctionne, les conditions suivantes doivent être remplies :

-   La broche d’entrée sur le filtre 3 (pin D) doit prendre en charge l’interface [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) . Cette interface permet de reconnecter le code confidentiel sans arrêter le filtre.
-   La broche de sortie sur le filtre 1 (pin A) doit pouvoir bloquer le workflow des données multimédias pendant la reconnexion. Aucune donnée ne peut voyager entre le code confidentiel A et le code pin D lors de la reconnexion. En général, cela signifie que la broche de sortie doit prendre en charge l’interface [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) . Toutefois, si Filter 1 est le filtre qui initie la reconnexion, il peut avoir un mécanisme interne pour bloquer son propre workflow de données.

La reconnexion dynamique implique les étapes suivantes :

1.  Bloque le flux de données du code confidentiel A.
2.  Reconnectez le code confidentiel A à la broche D, éventuellement par le biais d’un nouveau filtre intermédiaire.
3.  Débloquez le code confidentiel A afin que les données repassent à nouveau.

**Étape 1. Bloquer le flux de données**

Pour bloquer le flux de données, appelez [**IPinFlowControl :: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) sur le pin A. Cette méthode peut être appelée de façon asynchrone ou synchrone. Pour appeler la méthode de *façon asynchrone*, créez un objet d’événement Win32 et transmettez le descripteur d’événement à la méthode de **bloc** . La méthode est retournée immédiatement. Attendez que l’événement soit signalé, à l’aide d’une fonction telle que **WaitForSingleObject**. Le code confidentiel signale l’événement lorsqu’il a bloqué le Workflow. Par exemple :


```C++
// Create an event
HANDLE hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
if (hEvent != NULL)
{
    // Block the data flow.
    hr = pFlowControl->Block(AM_PIN_FLOW_CONTROL_BLOCK, hEvent); 
    if (SUCCEEDED(hr))
    {
        // Wait for the pin to finish.
        DWORD dwRes = WaitForSingleObject(hEvent, dwMilliseconds);
    }
}
```



Pour appeler la méthode de *façon synchrone*, il vous suffit de passer la valeur **null** au lieu du descripteur d’événement. À présent, la méthode est bloquée jusqu’à ce que l’opération se termine. Cela peut ne pas se produire tant que le code confidentiel n’est pas prêt à remettre un nouvel échantillon. Si le filtre est suspendu, cela peut prendre une durée arbitraire. Par conséquent, n’effectuez pas l’appel synchrone à partir de votre thread d’application principal. Utilisez un thread de travail ou appelez la méthode de manière asynchrone.

**Étape 2. Reconnecter les broches**

pour reconnecter les codes confidentiels, interrogez le gestionnaire de Graph de filtre de l’interface **IGraphConfig** et appelez [**IGraphConfig :: reconnect**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconnect) ou [**IGraphConfig :: reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-reconfigure). La méthode **reconnect** est plus simple à utiliser ; elle effectue les opérations suivantes :

-   Arrête les filtres intermédiaires (filtre 2 dans l’exemple) et les supprime du graphique.
-   Ajoute de nouveaux filtres intermédiaires, si nécessaire.
-   Connecte toutes les broches.
-   Met en pause ou exécute tout nouveau filtre pour qu’il corresponde à l’état du graphique.

La méthode **reconnect** comporte plusieurs paramètres facultatifs qui peuvent être utilisés pour spécifier le type de support de la connexion de code confidentiel et le filtre intermédiaire à utiliser. Par exemple :


```C++
pGraph->AddFilter(pNewFilter, L"New Filter for the Graph");
pConfig->Reconnect(
    pPinA,      // Reconnect this output pin...
    pPinD,      // ... to this input pin.
    pMediaType, // Use this media type.
    pNewFilter, // Connect them through this filter.
    NULL, 
    0);     
```



Pour plus d’informations, consultez la page de référence. Si la méthode **reconnect** n’est pas suffisamment flexible, vous pouvez utiliser la méthode **reconfigure** , qui appelle une méthode de rappel définie par l’application pour reconnecter les broches. Pour utiliser cette méthode, implémentez l’interface [**IGraphConfigCallback**](/windows/desktop/api/Strmif/nn-strmif-igraphconfigcallback) dans votre application.

Avant d’appeler **reconfigure**, bloquez le workflow à partir de la broche de sortie, comme décrit précédemment. Envoyez ensuite les données qui sont toujours en attente dans la section du graphique que vous reconnectez, comme suit :

1.  Appelez [**IPinConnection :: NotifyEndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-notifyendofstream) sur la broche d’entrée la plus en aval dans la chaîne de reconnexion (pin D dans l’exemple). Transmettez un handle à un événement Win32.
2.  Appelez [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sur la broche d’entrée qui est immédiatement en aval de la broche de sortie où vous avez bloqué le Workflow. (Dans cet exemple, le workflow a été bloqué au niveau du code confidentiel A. vous devez donc appeler **EndOfStream** sur pin B.)
3.  Attendez que l’événement soit signalé. La broche d’entrée (pin D) signale l’événement lorsqu’il reçoit la notification de fin de flux. Cela indique qu’aucune donnée n’est en déplacement entre les broches et que l’appelant peut reconnecter en toute sécurité les broches.

Notez que la méthode **IGraphConfig :: reconnect** gère automatiquement les étapes précédentes. Vous devez effectuer ces étapes uniquement si vous utilisez la méthode **reconfigure** .

Une fois que les données ont fait l’objet d’un push dans le graphique, appelez **reconfigure** et transmettez un pointeur à votre interface de rappel **IGraphConfigCallback** . le gestionnaire de Graph de filtre appellera la méthode [**IGraphConfigCallback :: reconfigure**](/windows/desktop/api/Strmif/nf-strmif-igraphconfigcallback-reconfigure) que vous avez fournie.

**Étape 3. Débloquer le Flow de données**

Une fois que vous avez reconnecté les codes confidentiels, débloquez le workflow en appelant **IPinFlowControl :: Block** avec une valeur de zéro pour le premier paramètre.

> [!Note]  
> Si une reconnexion dynamique est effectuée par un filtre, vous devez être conscient de certains problèmes de thread. si le gestionnaire de Graph de filtre tente d’arrêter le filtre, il peut se bloquer, car le graphique attend que le filtre s’arrête, alors que le filtre peut attendre que les données soient transmises par le biais du graphique. Pour éviter le blocage possible, certaines des méthodes décrites dans cette section prennent un handle vers un événement Win32. le filtre doit signaler l’événement si le gestionnaire de Graph de filtre tente d’arrêter le filtre. Pour plus d’informations, consultez [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) et [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[génération de Graph dynamique](dynamic-graph-building.md)
</dt> </dl>

 

 



