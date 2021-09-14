---
description: Utilisation du détecteur de média
ms.assetid: 462150d5-7315-4c2b-81b0-964a788ec47d
title: Utilisation du détecteur de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebdb05eb47c7efabcc3234fb6ac2411a46e40d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857373"
---
# <a name="using-the-media-detector"></a>Utilisation du détecteur de média

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Le détecteur de média est un objet d’assistance qui peut récupérer des informations sur un fichier, telles que le nombre de flux, leur type et leur durée. Elle contient également des méthodes permettant de récupérer des images de affiches à partir d’un flux vidéo. Il expose l’interface [**IMediaDet**](imediadet.md) .

Le détecteur de média fonctionne dans l’un des deux modes. Lorsque vous créez une instance du détecteur de média, celle-ci n’est pas attachée à un fichier source particulier. Dans ce mode, vous pouvez récupérer des informations de flux à partir de plusieurs fichiers sources. Toutefois, une fois que vous avez utilisé le détecteur de média pour obtenir un cadre d’affiche, celui-ci bascule en *mode de manipulation bitmap*. En mode de manipulation bitmap, le détecteur de média est attaché à un flux vidéo spécifique, et les méthodes d’informations de flux ne fonctionnent plus. En outre, il n’existe aucun moyen de basculer le détecteur de média vers son mode de démarrage. Par conséquent, obtenez les informations de flux dont vous avez besoin avant de récupérer les images de poster, ou créez de nouvelles instances du détecteur de média pour chaque flux.

Pour obtenir des informations sur le flux, procédez comme suit :

1.  Appelez [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) avec le nom du fichier source.
2.  Appelez [**IMediaDet :: obtenir \_ OutputStreams**](imediadet-get-outputstreams.md) pour obtenir le nombre de flux dans la source.
3.  Spécifiez un numéro de flux avec [**IMediaDet ::p ut \_ CurrentStream**](imediadet-put-currentstream.md). Appelez ensuite une ou plusieurs des méthodes suivantes :
    -   [**IMediaDet :: obtient \_ StreamType**](imediadet-get-streamtype.md): récupère le type de média du flux.
    -   [**IMediaDet :: obtient \_ StreamLength**](imediadet-get-streamlength.md): récupère la durée du flux.
    -   [**IMediaDet :: obtient \_ Cadence**](imediadet-get-framerate.md): récupère la fréquence d’images d’un flux vidéo.

Pour obtenir un cadre d’affiche, spécifiez le numéro du flux, comme dans l’étape précédente. Ensuite, appelez [**IMediaDet :: GetBitmapBits**](imediadet-getbitmapbits.md), qui copie une image postérisée dans une mémoire tampon ou [**IMediaDet :: WriteBitmapBits**](imediadet-writebitmapbits.md), qui enregistre une image postérisée dans un fichier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des sources](working-with-sources.md)
</dt> </dl>

 

 



