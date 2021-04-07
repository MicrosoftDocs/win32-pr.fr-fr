---
description: Autres objets sources
ms.assetid: 67482227-9df6-4e89-b16f-160a0bae6609
title: Autres objets sources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c76c8f6cb104e87630f178a82d613675b96723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747052"
---
# <a name="other-source-objects"></a>Autres objets sources

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

En plus des sources audio et vidéo, les [services de modification DirectShow](directshow-editing-services.md) (des) prennent en charge les objets sources suivants.

**Images fixes**

DES prend en charge les formats de fichier suivants pour les images fixes :

-   Bitmap (.bmp)
-   GIF (format d’échange Graphics)
-   JPEG (Joint Photographic Experts Group)
-   Carte graphique Targa ou Truevision (. TGA) : mode 2 (RGB non compressé) en format 16 bits, 24,-bit ou 32 bits.

Ces fichiers peuvent être utilisés comme images fixes ou pour créer des animations. Pour les fichiers bitmap, JPEG et Targa, si vous utilisez le fichier comme image continue, appelez la méthode [**IAMTimelineSrc :: SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) pour définir la fréquence d’images sur zéro.

**Séquences DIB**

Étant donné une série de fichiers bitmap, JPEG ou Targa, le moteur de rendu peut construire une séquence DIB. Pour créer une séquence DIB, donnez des noms séquentiels aux fichiers, par exemple Image001.bmp, Image002.bmp, Image003.bmp, etc. Utilisez le premier fichier de la séquence comme source. Définissez la fréquence d’images de la séquence en appelant [**IAMTimelineSrc :: SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md). Le moteur de rendu parcourt les images de la séquence à la fréquence d’images spécifiée.

Si la séquence est trop petite pour remplir la durée, en fonction de la fréquence d’images, le reste de la durée est un noir fixe. Aucune erreur ne se produit pendant le rendu.

**Sources GIF**

DES prend en charge les sources GIF, y compris les gif animés et transparents, à l’aide de la spécification GIF89a. Avec une image GIF animée, contrairement aux autres types de fichiers, vous n’avez pas besoin de définir la fréquence d’images. Le fichier GIF spécifie le délai entre chaque image de l’animation.

Pour prendre en charge les images GIF transparentes, DES convertit des zones transparentes dans l’image en RVB triple RGB (0, 0, 0). Vous pouvez ensuite utiliser la [transition de clé](key-transition.md) vers la touche sur RVB (0, 0, 0).

DES convertit également les régions noires qui se trouvent dans la plage RVB (de 0 à 7, de 0 à 7, de 0 à 7) à la valeur RVB (8, 8, 8), à l’exception de l’index de transparence, si cette plage est comprise dans cette plage. Cette conversion n’est pas détectable à l’oeil.

**Source de couleur vidéo**

L’objet [source de couleur vidéo](video-color-source.md) crée une image vidéo continue d’une couleur unie. Une utilisation pour cet objet consiste à en faire une couche dans une transition. Par exemple, utilisez-le dans une vidéo en fondu ou en fondu.

**Filtres de source personnalisés**

DES peut utiliser un filtre source DirectShow comme source de chronologie, si le filtre remplit les conditions suivantes :

-   Il prend en charge la recherche
-   Il produit un format pris en charge par. Le format peut être compressé tant que le système de l’utilisateur dispose d’un filtre DirectShow capable de le décoder.

Pour utiliser une source personnalisée, spécifiez le CLSID du filtre en tant que GUID de sous-objet de l’objet source. Pour plus d’informations, consultez sous- [objets](subobjects.md). Pour prendre en charge les propriétés personnalisées, implémentez-les en tant que propriétés « put » **IDispatch** . Seules les propriétés statiques sont prises en charge sur les objets sources ; les propriétés dynamiques ne sont pas prises en charge.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des sources](working-with-sources.md)
</dt> </dl>

 

 



