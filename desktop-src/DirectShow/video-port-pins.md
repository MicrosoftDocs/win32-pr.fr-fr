---
description: Broches de port vidéo
ms.assetid: a6be24e5-7937-48f1-abeb-3f29c3deeafd
title: Broches de port vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d13ab4ad63995dd38460bf29064035c9c1802dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866434"
---
# <a name="video-port-pins"></a>Broches de port vidéo

Un périphérique de capture avec un port vidéo matériel peut utiliser les extensions de port vidéo (VPE) dans Microsoft® DirectX®. Si c’est le cas, le filtre de capture aura un code PIN de port vidéo (VP). Aucune donnée vidéo n’est acheminée du pin du VP via le graphique de filtre. Au lieu de cela, les images vidéo sont produites dans le matériel et envoyées directement à la mémoire vidéo. Le pin du VP permet d’envoyer des messages de contrôle au matériel.

Il est important de connecter le code confidentiel du VP, même si votre application n’effectue que la capture de fichiers sans aperçu. Si vous laissez le code confidentiel non connecté, le graphique ne s’exécutera pas correctement. Cela diffère des codes confidentiels d’aperçu, qui n’ont pas besoin d’être connectés.

Les différents convertisseurs vidéo DirectShow offrent une prise en charge différente des broches de vice-président :

-   Convertisseur vidéo : Connectez le code confidentiel du VP à la broche 0 sur le filtre de [mixage de superposition](overlay-mixer-filter.md) et connectez le filtre de mixage de recouvrement au convertisseur vidéo.
-   VMR-7 : Connectez le code confidentiel du VP au filtre du [Gestionnaire de port vidéo](video-port-manager.md) et connectez le gestionnaire de port vidéo au VMR-7.
-   VMR-9 : vous ne pouvez pas utiliser VMR-9 si l’appareil a un code confidentiel de directeur, car Direct3D 9 ne prend pas en charge les ports vidéo. Utilisez le convertisseur vidéo ou VMR-7.

Pour les scénarios de port vidéo, le mélangeur de superposition et le convertisseur vidéo sont recommandés sur le gestionnaire de port vidéo et VMR-7, car tous les pilotes ne prennent pas en charge le gestionnaire de port vidéo. En général, le mélangeur de superposition est l’option la plus fiable pour les ports vidéo.

La méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) insère automatiquement le mélangeur de superposition s’il y a un code confidentiel de VP. Si vous générez le graphique sans utiliser cette méthode, vous devez vérifier la présence d’une broche de port vidéo sur le filtre de capture et, le cas échéant, la connecter au filtre de mixage de superposition, comme indiqué dans le diagramme suivant.

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



Une fois que vous avez ajouté le mélangeur de superposition au graphique, appelez à nouveau **FindPin** pour trouver la broche 0 sur le mélangeur de superposition. La broche 0 est toujours la première broche d’entrée sur le filtre.


```C++
pBuild->FindPin(pOvMix, PINDIR_INPUT, NULL, NULL, TRUE, 0, &pOVPin);
```



Connectez les deux codes confidentiels en appelant [**IGraphBuilder :: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).


```C++
pGraph->Connect(pVPPin, pOvPin);
```



Ensuite, connectez la broche de sortie du mixer de superposition au filtre de convertisseur vidéo. Vous pouvez masquer la vidéo en appelant les méthodes [**IVideoWindow ::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) et [**IVideoWindow ::p ut \_ visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) sur le gestionnaire de graphique de filtre.

Pour les tuners TV, le filtre de capture peut également avoir un code vidéo (PIN \_ catégorie \_ VIDEOPORT \_ VBI). Si c’est le cas, connectez ce code PIN au filtre d' [allocateur de surface VBI](vbi-surface-allocator.md) . Pour plus d’informations, consultez Affichage des sous- [titres](viewing-closed-captions.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rubriques avancées sur la capture](advanced-capture-topics.md)
</dt> <dt>

[Utilisation du mélangeur de superposition dans la capture vidéo](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



