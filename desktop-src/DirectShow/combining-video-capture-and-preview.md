---
description: Combinaison de la capture vidéo et de l’aperçu
ms.assetid: bffc1900-be05-4d7e-ab8d-3177365aeb7a
title: Combinaison de la capture vidéo et de l’aperçu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1894e9431cbfa9e7bbbd0ef0bcec48021055350030b54ffd2f3e2729db81c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084323"
---
# <a name="combining-video-capture-and-preview"></a>Combinaison de la capture vidéo et de l’aperçu

Les sections précédentes décrivent comment capturer des vidéos dans divers formats de fichiers. La section aperçu de la [vidéo](previewing-video.md) décrit comment créer un graphique d’aperçu instantané. Toutefois, de nombreuses applications doivent effectuer les deux à la fois. Pour créer un graphique combiné d’aperçu et d’écriture de fichiers, effectuez simplement deux appels à [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream):


```C++
// Render the preview stream to the video renderer.
hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap, 
    NULL, NULL);

// Render the capture stream to the mux.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap, 
    NULL, pMux);
```



dans ce code, le générateur de Graph de Capture masque certains détails :

-   Si le filtre de capture a une broche d’aperçu ou un code PIN de port vidéo, ainsi qu’un code confidentiel de capture, la méthode [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) affiche simplement les deux broches, comme indiqué dans l’illustration suivante.

    ![graphique de capture et d’aperçu](images/vidcap04.png)

-   si le filtre a uniquement un code confidentiel de capture, le générateur de Graph de capture utilise le filtre [Tee intelligent](smart-tee-filter.md) pour fractionner le flux de capture. L’illustration suivante montre le graphique avec un tee Smart.

    ![capturer et afficher un aperçu du graphique avec le filtre tee intelligent](images/vidcap05.png)

Le filtre tee intelligent a un code confidentiel de capture et un code PIN de prévisualisation. Il prend un flux vidéo unique du filtre de capture et le divise en deux flux, un pour la capture et un pour l’aperçu. Pour maintenir le débit sur le code confidentiel de capture, la broche de prévisualisation supprime les frames en fonction des besoins. elle supprime également les horodatages de chaque exemple avant de la diffuser, pour les raisons décrites dans la rubrique [DirectShow les filtres de Capture vidéo](directshow-video-capture-filters.md).

Bien que le tee intelligent fractionne le flux, il ne duplique pas physiquement les données vidéo. Au lieu de cela, il utilise des exemples d’objets de média personnalisés qui partagent les mémoires tampons. Les exemples sont marqués en lecture seule pour s’assurer que les filtres en aval n’écrivent pas sur les données.

si votre graphique de capture a une fenêtre d’aperçu, plusieurs choses peuvent amener le gestionnaire de Graph de filtre à arrêter l’ensemble du graphique, y compris le flux de capture :

-   Verrouillage de l’ordinateur.
-   En appuyant sur CTRL + ALT + SUPPR sur un ordinateur qui est membre d’un domaine.
-   Exécution d’une application Direct3D en plein écran, telle qu’un jeu ou un économiseur d’écran.
-   Basculement des moniteurs ou modification de la résolution d’affichage.
-   exécution d’un programme qui oblige Windows à afficher une boîte de dialogue de contrôle de compte d’utilisateur (UAC). (Windows Vista ou version ultérieure.)
-   Exécution d’une fenêtre DOS plein écran.

L’un de ces événements peut interrompre la session de capture, ce qui peut entraîner une perte de données. (Voici ce qui se produit en interne : le convertisseur vidéo perd les ressources Direct3D ou DirectDraw dont il a besoin. dans le processus de récupération de ces ressources, le convertisseur vidéo doit se reconnecter au filtre en amont, ce qui amène le gestionnaire de Graph de filtre à arrêter le graphique.)

Deux solutions possibles à ce problème sont les suivantes :

-   N’incluez pas de flux d’aperçu. Toutefois, sachez que la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) ajoute automatiquement une fenêtre d’aperçu lorsque l’appareil de capture a une broche de port vidéo. Consultez les [broches des ports vidéo dans la capture de fichiers](video-port-pins-in-file-capture.md).
-   Utilisez le moteur de mémoire tampon de flux pour envoyer le flux d’aperçu à un graphique dans un autre processus.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture vidéo dans un fichier](capturing-video-to-a-file.md)
</dt> </dl>

 

 



