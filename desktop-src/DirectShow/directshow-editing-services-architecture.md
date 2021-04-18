---
description: Architecture des services de modification DirectShow
ms.assetid: ba6cc3f1-9130-4197-8501-c2d0a088e847
title: Architecture des services de modification DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c6059eebe9228e61d3de9677972eedfcb51c62
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106527175"
---
# <a name="directshow-editing-services-architecture"></a>Architecture des services de modification DirectShow

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

L’illustration suivante montre l’architecture des [services de modification DirectShow](directshow-editing-services.md) (des).

![architecture des services de modification DirectShow](images/architecture.png)

-   Timeline : représente une production vidéo sous la forme d’une collection d’éléments sources, de transitions et d’effets, organisée en un ensemble de pistes imbriquées. Pour plus d’informations, consultez [le modèle Timeline](the-timeline-model.md).
-   Analyseur XML : analyse la chronologie et génère un fichier de sortie, ou lit un fichier d’entrée et génère une chronologie. DES prend en charge un format de persistance XML.
-   Moteur de rendu : traduit la chronologie en un format qui peut être rendu en tant que média de diffusion en continu. Par défaut, le moteur de rendu produit un graphique de filtre DirectShow (voir la section suivante).
-   Localisateur de média : conserve un cache d’emplacements d’éléments multimédias. En cas d’échec d’une tentative d’ouverture d’un élément multimédia, les utilisent le cache pour localiser l’élément, en fonction de l’historique des ouvertures réussies.

La chronologie est une description abstraite d’un projet de montage vidéo. Il spécifie les éléments sources utilisés dans le projet, les heures de démarrage et d’arrêt, les effets et les transitions, etc. Toutefois, la chronologie ne rend pas les flux vidéo et audio. Au lieu de cela, le moteur de rendu traduit la chronologie en un graphique de filtre, pour la sortie de l’aperçu ou du fichier. Une application manipule la chronologie plutôt que de manipuler directement le graphique de filtre, ce qui serait fastidieux et sujet aux erreurs.

Le tableau suivant répertorie les principales tâches qu’une application de modification vidéo classique effectue, ainsi que les interfaces qui prennent en charge chaque tâche. Les sections suivantes décrivent ces tâches et les interfaces plus en détail.



| Tâche                                     | Interface (s)                                                                             |
|------------------------------------------|------------------------------------------------------------------------------------------|
| Construisez ou modifiez une chronologie.          | [**IAMTimeline**](iamtimeline.md) et les autres interfaces **IAMTimelineXXXX**          |
| Enregistrez et chargez les fichiers projet.             | [**IXml2Dex**](ixml2dex.md)                                                             |
| Affichez l’aperçu d’un projet ou écrivez-le dans un fichier. | [**IRenderEngine**](irenderengine.md), [ **ISmartRenderEngine**](ismartrenderengine.md) |



 

En outre, une application peut effectuer une partie ou l’ensemble des tâches secondaires suivantes.



| Tâche                                                                                           | Interface (s)                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| Obtenir des informations sur les fichiers multimédias. (Nombre de flux, format et durée de chaque flux.) | [**IMediaDet**](imediadet.md)                                               |
| Définissez les propriétés des transitions et des effets.                                                     | [**IPropertySetter**](ipropertysetter.md)                                   |
| Recevoir une notification lorsque des erreurs se produisent pendant le rendu.                                       | [**IAMSetErrorLog**](iamseterrorlog.md), [ **IAMErrorLog**](iamerrorlog.md) |
| Récupérez les images de poster.                                                                        | [**IMediaDet**](imediadet.md), [ **ISampleGrabber**](isamplegrabber.md)     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec les services d’édition DirectShow](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



