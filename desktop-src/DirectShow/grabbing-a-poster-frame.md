---
description: Saisie d’un cadre d’affiche
ms.assetid: 0727a1ed-1bc7-49fc-a288-00283e637a71
title: Saisie d’un cadre d’affiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6668526d83f17c4ceab260f3a31ed43d19ec1d142bd8f8fdae080161350ded8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536569"
---
# <a name="grabbing-a-poster-frame"></a>Saisie d’un cadre d’affiche

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

cet article explique comment afficher un cadre d’affiche à partir d’un fichier multimédia numérique à l’aide de l’objet [MediaDet (media detecter)](media-detector--mediadet.md) fourni avec les [Services d’édition de DirectShow](directshow-editing-services.md).

Le détecteur de média est un objet d’assistance qui peut obtenir des informations de format à partir d’un fichier source de média. Il peut également récupérer une image bitmap à partir d’un flux vidéo dans le fichier source. En supposant que le fichier peut être recherché, vous pouvez obtenir l’image à partir de n’importe quel point du fichier. L’image retournée est toujours au format RGB 24 bits.

le détecteur de média n’est pas un filtre et l’application n’a pas besoin d’utiliser le gestionnaire de Graph de filtre ou de créer un graphique de filtre. En interne, le détecteur de média crée un graphique de filtre qui contient l' [**exemple de filtre d’accrochage**](sample-grabber-filter.md). Pour obtenir une image bitmap, le détecteur de média recherche et interrompt le graphique de filtre, puis récupère le bitmap à partir de l’exemple de filtre d’accrochage. L’application communique avec le détecteur de média par le biais de l’interface [**IMediaDet**](imediadet.md) . Le détecteur de média est un bon exemple d’encapsulation d’un graphique de filtre à l’intérieur d’un objet d’assistance, afin de protéger les applications des détails liés au graphique.

Le détecteur de média fonctionne en deux modes. La première fois que vous la créez, le détecteur de média est en mode « collecte d’informations ». Vous pouvez spécifier le nom d’un fichier multimédia et obtenir des informations sur chacun des flux du fichier, tels que le type de format, la fréquence d’images ou la durée. Si le fichier contient un flux vidéo, vous pouvez basculer le détecteur de média en mode « manipulation bitmap » et récupérer les bitmaps à partir de la source. Toutefois, une fois que vous avez fait cela, vous ne pouvez pas rétablir le mode d’origine du détecteur de média. elle est attachée de manière permanente à ce flux vidéo. Pour utiliser un autre flux ou un autre fichier, vous devez créer une nouvelle instance du détecteur de média.

> [!Note]  
> Les exemples de code de ce didacticiel utilisent la classe ATL **CComPtr** qui gère automatiquement les décomptes de références. Si vous préférez utiliser des pointeurs d’interface bruts, n’oubliez pas de libérer chaque interface lorsque vous n’en avez plus besoin. Par ailleurs, par souci de concision, les exemples de code omettent une grande partie de la vérification des erreurs qu’une application doit effectuer. Dans le code de travail, vérifiez toujours les valeurs **HRESULT** .

 

Ce didacticiel comprend les étapes suivantes :

-   [étape 1 : créer le Framework Windows](step-1--create-the-windows-framework.md)
-   [Étape 2 : ajouter une commande de menu pour récupérer un cadre d’affiche](step-2--add-a-menu-command-to-grab-a-poster-frame.md)
-   [Étape 3 : implémenter la fonction Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md)
-   [Étape 4 : dessiner l’image bitmap sur la zone cliente](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[utilisation des Services de modification DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



