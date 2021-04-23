---
description: Contrôle d’un graphique de capture
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Contrôle d’un graphique de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0089fa11adbc0ac861fb9e8e30e2cd0f56b23680
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909047"
---
# <a name="controlling-a-capture-graph"></a>Contrôle d’un graphique de capture

L’interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) du gestionnaire de graphique de filtre a des méthodes pour l’exécution, l’arrêt et la suspension de l’ensemble du graphique. Toutefois, si le graphique de filtre a des flux de capture et d’aperçu, vous souhaiterez probablement contrôler les deux flux indépendamment. Par exemple, vous souhaiterez peut-être afficher un aperçu de la vidéo sans la capturer. Pour ce faire, vous pouvez utiliser la méthode [**ICaptureGraphBuilder2 :: ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) .

> [!Note]  
> Cette méthode ne fonctionne pas lors de la capture dans un fichier ASF (Advanced Systems Format).

 

Contrôle du flux de capture

Le code suivant définit le flux de capture vidéo à exécuter pendant quatre secondes, à partir d’une seconde après l’exécution du graphique :


```C++
// Control the video capture stream. 
REFERENCE_TIME rtStart = 10000000, rtStop = 50000000;
const WORD wStartCookie = 1, wStopCookie = 2;  // Arbitrary values.
hr = pBuild->ControlStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                 // Capture filter.
    &rtStart, &rtStop,     // Start and stop times.
    wStartCookie, wStopCookie  // Values for the start and stop events.
);
pControl->Run();
```



Le premier paramètre spécifie le flux à contrôler, en tant que GUID de catégorie de code confidentiel. Le deuxième paramètre donne le type de média. Le troisième paramètre est un pointeur vers le filtre de capture. Pour contrôler tous les flux de capture dans le graphique, définissez les deuxième et troisième paramètres sur **null**.

Les deux paramètres suivants définissent les heures de démarrage et d’arrêt du flux, par rapport à l’heure de début de l’exécution du graphique. Appelez [**IMediaControl :: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) pour exécuter le graphique. Tant que vous n’avez pas exécuté le graphique, la méthode **ControlStream** n’a aucun effet. Si le graphique est déjà en cours d’exécution, les paramètres prennent effet immédiatement.

Les deux derniers paramètres sont utilisés pour obtenir des notifications d’événements lorsque le flux démarre et s’arrête. Pour chaque flux que vous contrôlez à l’aide de cette méthode, le graphique de filtre envoie une paire d’événements : le contrôle de flux de la [**ce \_ \_ \_ a démarré**](ec-stream-control-started.md) au démarrage du flux et le [**contrôle de \_ flux ce \_ \_ est arrêté**](ec-stream-control-stopped.md) lorsque le flux s’arrête. Les valeurs de **wStartCookie** et **wStopCookie** sont utilisées comme deuxième paramètre d’événement. Ainsi, *lParam2* dans l’événement de début est égal à **wStartCookie** et *lParam2* dans l’événement d’arrêt est égal à **wStopCookie**. Le code suivant illustre l’obtention de ces événements :


```C++
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch (evCode)
    {
    case EC_STREAM_CONTROL_STARTED: 
    // param2 == wStartCookie
    break;

    case EC_STREAM_CONTROL_STOPPED: 
    // param2 == wStopCookie
    break;
    
    } 
    pEvent->FreeEventParams(evCode, param1, param2);
}
```



La méthode **ControlStream** définit des valeurs spéciales pour les heures de début et de fin.



| Étiquette | Valeur |
|-------------|----------------------------------------|------------------------------------|
|             | Démarrer                                  | Stop                               |
| MAXLONGLONG | Ne jamais démarrer ce flux.               | Ne s’arrête pas tant que le graphique n’est pas arrêté. |
| **NULL**    | Démarrer immédiatement lorsque le graphique s’exécute. | Arrêter immédiatement.                  |



 

Par exemple, le code suivant arrête immédiatement le flux de capture :


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



Bien que vous puissiez arrêter le flux de capture et le redémarrer ultérieurement, cela crée un intervalle dans les horodatages. Lors de la lecture, la vidéo semble bloquée pendant l’intervalle (selon le format de fichier).

Contrôle du flux de la version préliminaire

Pour contrôler la broche d’aperçu, appelez **ControlStream** , mais définissez le premier paramètre sur épingler la \_ catégorie \_ aperçu. Cela fonctionne comme pour la capture de catégorie de code confidentiel \_ \_ , sauf que vous ne pouvez pas utiliser les temps de référence pour spécifier le démarrage et l’arrêt, car les images d’aperçu n’ont pas de datage. Par conséquent, vous devez utiliser la **valeur null** ou MAXLONGLONG. Utilisez la **valeur null** pour démarrer le flux de préversion :


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    NULL,    // Start now.
    0,       // (Don't care.)
    wStartCookie, wStopCookie); 
```



Utilisez MAXLONGLONG pour arrêter le flux de la version préliminaire :


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    0,               // (Don't care.)
    MAXLONGLONG,     // Stop now.
    wStartCookie, wStopCookie); 
```



Peu importe si le flux de préversion provient d’une épingle d’aperçu sur le filtre de capture ou du filtre des tees intelligents. La méthode **ControlStream** fonctionne dans les deux sens.

Toutefois, pour les broches de port vidéo, la méthode échoue. Dans ce cas, une autre approche consiste à masquer la fenêtre vidéo. Interrogez le graphique pour **IVideoWindow** et utilisez la méthode [**IVideoWindow ::p ut \_ visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) pour afficher ou masquer la fenêtre.


```C++
// Hide the video window.
IVideoWindow *pVidWin = 0;
hr = pGraph->QueryInterface(IID_IVideoWindow, (void**)&pVidWin);
if (SUCCEEDED(hr))
{
    pVidWin->put_Visible(OAFALSE);
    pVidWin->Release();
}
```



En outre, si vous appelez [**IVideoWindow ::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) avec la valeur OAFALSE avant d’exécuter le graphique, le filtre de convertisseur vidéo masque la fenêtre jusqu’à ce que vous spécifiiez autrement. Par défaut, le convertisseur vidéo affiche la fenêtre lorsque vous exécutez le graphique.

Remarques sur le contrôle Stream

Le comportement par défaut d’un code confidentiel est de fournir des exemples lorsque le graphique s’exécute. Supposons, par exemple, que vous appelez **ControlStream** avec la \_ capture de catégorie pin \_ mais pas avec l' \_ aperçu de catégorie pin \_ . Lorsque vous exécutez le graphique, le flux de préversion s’exécute immédiatement, tandis que le flux de capture est exécuté à l’heure que vous avez spécifiée dans **ControlStream**.

Si vous capturez plusieurs flux et les envoyez à un filtre Mux (par exemple, si vous capturez des données audio et vidéo dans un fichier AVI), vous devez contrôler les deux flux en tandem. Dans le cas contraire, le filtre MUX peut bloquer l’attente d’un flux, car il tente d’entrelacer les deux flux. Définissez les mêmes heures de démarrage et d’arrêt sur tous les flux de capture avant d’exécuter le graphique :


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



En interne, la méthode **ControlStream** utilise l’interface [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) , qui est exposée sur les broches du filtre de capture, le filtre tee intelligent (le cas échéant) et éventuellement le filtre Mux. Vous pouvez utiliser cette interface directement, au lieu d’appeler **ControlStream**, bien qu’il n’y ait aucun avantage particulier à le faire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture vidéo](video-capture.md)
</dt> </dl>

 

 



