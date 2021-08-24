---
description: Broches de port vidéo
ms.assetid: a6be24e5-7937-48f1-abeb-3f29c3deeafd
title: Broches de port vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94202e05cc467eabb77719a145a77310a62482e6f82772261b57e5ff544d2b63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696782"
---
# <a name="video-port-pins"></a>Broches de port vidéo

Un périphérique de capture avec un port vidéo matériel peut utiliser les extensions de port vidéo (VPE) dans Microsoft® DirectX®. Si c’est le cas, le filtre de capture aura un code PIN de port vidéo (VP). Aucune donnée vidéo n’est acheminée du pin du VP via le graphique de filtre. Au lieu de cela, les images vidéo sont produites dans le matériel et envoyées directement à la mémoire vidéo. Le pin du VP permet d’envoyer des messages de contrôle au matériel.

Il est important de connecter le code confidentiel du VP, même si votre application n’effectue que la capture de fichiers sans aperçu. Si vous laissez le code confidentiel non connecté, le graphique ne s’exécutera pas correctement. Cela diffère des codes confidentiels d’aperçu, qui n’ont pas besoin d’être connectés.

les différents convertisseurs vidéo DirectShow offrent une prise en charge différente des broches de vice-président :

-   convertisseur vidéo : Connecter la broche du VP pour épingler 0 sur le filtre de [Mixer de recouvrement](overlay-mixer-filter.md) , puis connecter le filtre de Mixer de recouvrement au convertisseur vidéo.
-   VMR-7 : Connecter le code confidentiel du VP au filtre du [gestionnaire de port vidéo](video-port-manager.md) et connectez le gestionnaire de port vidéo au VMR-7.
-   VMR-9 : vous ne pouvez pas utiliser VMR-9 si l’appareil a un code confidentiel de directeur, car Direct3D 9 ne prend pas en charge les ports vidéo. Utilisez le convertisseur vidéo ou VMR-7.

pour les scénarios de port vidéo, le Mixer de recouvrement et le convertisseur vidéo sont recommandés sur le gestionnaire de port vidéo et VMR-7, car tous les pilotes ne prennent pas en charge le gestionnaire de port vidéo. en général, la superposition Mixer est l’option la plus fiable pour les ports vidéo.

la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) insère automatiquement la superposition Mixer s’il existe un code confidentiel VP. si vous générez le graphique sans utiliser cette méthode, vous devez vérifier la présence d’une broche de port vidéo sur le filtre de capture et, le cas échéant, la connecter à la superposition Mixer filtre, comme indiqué dans le diagramme suivant.

![connexion d’une broche de port vidéo au filtre de mixage de superposition.](images/vidcap11.png)

Vous pouvez utiliser la méthode [**ICaptureGraphBuilder2 :: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) pour rechercher un code confidentiel de VP sur le filtre de capture :


```C++
hr = pBuild->FindPin(
    pCap,                    // Pointer to the capture filter.
    PINDIR_OUTPUT,           // Look for an output pin.
    &PIN_CATEGORY_VIDEOPORT, // Look for a video port pin.
    NULL,                    // Any media type.
    FALSE,                   // Pin can be connected.
    0,                       // Retrieve the first matching pin.
    &pVPPin                  // Receives a pointer to the pin.
);
```



une fois que vous avez ajouté le Mixer de superposition au graphique, appelez à nouveau **FindPin** pour trouver la broche 0 dans le Mixer de recouvrement. La broche 0 est toujours la première broche d’entrée sur le filtre.


```C++
pBuild->FindPin(pOvMix, PINDIR_INPUT, NULL, NULL, TRUE, 0, &pOVPin);
```



Connecter les deux codes confidentiels en appelant [**IGraphBuilder :: Connecter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).


```C++
pGraph->Connect(pVPPin, pOvPin);
```



ensuite, connectez la broche de sortie de Mixer de recouvrement au filtre de convertisseur vidéo. vous pouvez masquer la vidéo en appelant les méthodes [**IVideoWindow ::p \_ ut**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) et [**IVideoWindow ::p ut \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) sur le gestionnaire de Graph de filtre.

Pour les tuners TV, le filtre de capture peut également avoir un code vidéo (PIN \_ catégorie \_ VIDEOPORT \_ VBI). Si c’est le cas, connectez ce code PIN au filtre d' [allocateur de surface VBI](vbi-surface-allocator.md) . Pour plus d’informations, consultez Affichage des sous- [titres](viewing-closed-captions.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rubriques avancées sur la capture](advanced-capture-topics.md)
</dt> <dt>

[utilisation de la superposition Mixer dans la Capture vidéo](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



