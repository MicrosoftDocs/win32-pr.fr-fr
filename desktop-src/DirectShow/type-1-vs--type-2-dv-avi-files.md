---
description: Type-1 et
ms.assetid: 3f1cf981-f678-46a6-9784-ffb389438b6d
title: Types-1 et fichiers AVI DV type-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0000b81e94e25749b5590287145a88a28280e16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952187"
---
# <a name="type-1-vs-type-2-dv-avi-files"></a>Types-1 et fichiers AVI DV type-2

Les caméras DV produisent une vidéo audio entrelacée ; chaque image de la vidéo contient également les informations audio. Si vous enregistrez des données DV dans un fichier AVI, vous avez le choix entre les options suivantes :

-   Stockez les données entrelacées sous la forme d’un flux dans le fichier AVI. C’est ce qu’on appelle un fichier de type 1.
-   Fractionner les données entrelacées en flux audio et vidéo distincts. C’est ce qu’on appelle un fichier de type 2.

Pour la capture vidéo, où le débit maximal est essentiel, il est préférable d’utiliser un fichier de type 1, car les fichiers de type 2 transmettent des données audio redondantes. (Le flux vidéo contient toujours les données audio. L’audio est simplement masqué en étiquetant le flux en tant que vidéo.) En outre, l’écriture d’un fichier de type 2 nécessite du temps processeur supplémentaire pour fractionner le flux entrelacé.

En revanche, les fichiers de type 1 sont moins efficaces pour la modification en temps réel. L’application doit extraire le contenu audio du flux entrelacé, effectuer les modifications et entrelacer à nouveau les données. En outre, le format type-1 n’est pas compatible avec Microsoft® Video pour Windows® (VFW). DirectShow peut gérer les deux types de fichiers.

Un fichier de type 2 peut être converti en type-1 à l’aide du filtre [DV du multiplexeur](dv-muxer-filter.md) . Un fichier de type 1 peut être converti en type-2 à l’aide du filtre de [séparateur DV](dv-splitter-filter.md) . Le diagramme suivant illustre la différence entre les deux formats.

![conversion entre type-1 et DV de type 2](images/dv-filters3.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vidéo numérique dans DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Données DV au format de fichier AVI](dv-data-in-the-avi-file-format.md)
</dt> </dl>

 

 



