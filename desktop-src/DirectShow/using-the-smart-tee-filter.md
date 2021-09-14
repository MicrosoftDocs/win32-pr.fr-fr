---
description: Utilisation du filtre tee Smart
ms.assetid: d2828269-6841-41a8-8d45-f864c7e85857
title: Utilisation du filtre tee Smart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5260469634c613fe05c25eb9f55e24e108e8c434
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240617"
---
# <a name="using-the-smart-tee-filter"></a>Utilisation du filtre tee Smart

Si un filtre de capture a des codes confidentiels de capture et de prévisualisation distincts, vous pouvez effectuer une capture à partir d’un tout en visualisant l’un de l’autre. Toutefois, si le filtre n’a pas de pin d’aperçu, vous pouvez faire la même chose en incluant le filtre [tee intelligent](smart-tee-filter.md) dans le graphique. Ce filtre fractionne les données de l’épingle de capture en deux flux identiques, l’un pour la capture et l’autre pour l’aperçu. Le diagramme suivant illustre ce processus.

![capturer le graphique avec un filtre tee intelligent](images/vidcap05.png)

La méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) insère automatiquement le filtre tee intelligent si nécessaire. Toutefois, si vous utilisez des méthodes **IGraphBuilder** pour créer votre graphique, et non pas **RenderStream**, vous devrez peut-être insérer le filtre tee intelligent.

Avant de rendre des codes confidentiels sur le filtre de capture, vérifiez si le filtre a une broche d’aperçu ou un code PIN de port vidéo. Si ce n’est pas le cas, et que vous souhaitez afficher un aperçu, ajoutez le filtre tee intelligent au graphique et connectez-le à l’épingle de capture sur le filtre de capture.

> [!Note]  
> Vous pouvez traiter un code PIN de port vidéo (VP) comme un type de code PIN de préversion, de sorte qu’un filtre avec un code PIN de VP n’a pas besoin d’un filtre de tee intelligent. Toutefois, les pin de vice-président ont d’autres exigences spéciales. Pour plus d’informations, consultez [pin port Video](video-port-pins.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rubriques avancées sur la capture](advanced-capture-topics.md)
</dt> <dt>

[Combinaison de la capture vidéo et de l’aperçu](combining-video-capture-and-preview.md)
</dt> <dt>

[Utilisation des catégories de code confidentiel](working-with-pin-categories.md)
</dt> </dl>

 

 



