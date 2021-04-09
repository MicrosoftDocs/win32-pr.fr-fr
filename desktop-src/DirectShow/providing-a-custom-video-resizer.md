---
description: Fournir un redimensionnement vidéo personnalisé
ms.assetid: 4009f93f-cd50-440f-b943-7e3700e0e2cb
title: Fournir un redimensionnement vidéo personnalisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5247727cf16ef3c94a699db2907ff240b1d8a289
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108906"
---
# <a name="providing-a-custom-video-resizer"></a>Fournir un redimensionnement vidéo personnalisé

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

> [!Note]  
> Cette fonctionnalité nécessite DirectX 9,0 ou une version ultérieure.

 

Lorsque les [services d’édition DirectShow](directshow-editing-services.md) redimensionnent un clip source vidéo, le comportement par défaut est un *StretchBlt*, qui est rapide, mais pas avec anticrénelage. Vous pouvez modifier le comportement de redimensionnement en implémentant un dimensionnement personnalisé en tant que filtre de transformation DirectShow. Le filtre doit exposer l’interface [**IResize**](iresize.md) , qui permet à des de spécifier la taille vidéo d’entrée et de sortie. Pour plus d’informations sur l’écriture d’un filtre de transformation, consultez [écriture de filtres de transformation](writing-transform-filters.md). La classe de base **CTransformFilter** est recommandée comme point de départ. Lorsque vous implémentez le filtre, notez les points suivants :

-   Prend en charge l’interface **IResize** sur le filtre (pas les broches).
-   Le filtre doit accepter uniquement les formats [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) (format \_ videoinfo). Refuser les autres types de format.
-   Le format vidéo à partir de peut être n’importe quel type RVB non compressé, y compris les RGB 32 bits avec alpha (MEDIASUBTYPE \_ ARGB32). Votre filtre peut rejeter en toute sécurité les formats avec la **bihauteur** < 0.
-   Avant que le moteur de rendu connecte la broche de sortie du filtre, il appelle [**IResize ::p ut \_ MediaType**](iresize-put-mediatype.md) pour définir le type de sortie. Elle peut également appeler [**IResize ::p ut \_**](iresize-put-size.md) pour ajuster la taille de sortie. Il peut appeler ces deux méthodes dans n’importe quel ordre, le nombre de fois, avant de connecter la broche de sortie.
-   Une fois que le moteur de rendu a connecté la broche de sortie, il peut appeler à nouveau **put \_ Size** . Le filtre de redimensionnement doit reconnecter sa broche de sortie avec la nouvelle taille.
-   À l’intérieur de la méthode [**CTransformFilter :: Transform**](ctransformfilter-transform.md) du filtre, étendez la vidéo d’entrée à la taille de sortie.
-   Votre filtre ne doit jamais définir l’indicateur de discontinuité sur l’exemple de sortie, ni attacher un type de média à l’exemple de sortie.
-   Pour enregistrer l’état du filtre dans un fichier GraphEdit (. GRF), implémentez l’interface **IPersistStream** . (Cette option est facultative, mais utile pour les tests.)

Pour utiliser le filtre de redimensionnement, le filtre doit être inscrit en tant qu’objet COM sur le système de l’utilisateur. Avant que l’application n’affiche le projet vidéo, interrogez le moteur de rendu de l’interface [**IRenderEngine2**](irenderengine2.md) et appelez [**IRenderEngine2 :: SETRESIZERGUID**](irenderengine2-setresizerguid.md) avec le CLSID du filtre de redimensionnement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu d’un projet](rendering-a-project.md)
</dt> </dl>

 

 



