---
description: Modèle conceptuel
ms.assetid: f906466e-acdc-4d0f-bf27-c5a25dc56c01
title: Modèle conceptuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a17538e7fdb454fa8eb61ab951a3316b0f0c327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209753"
---
# <a name="the-conceptual-model"></a>Modèle conceptuel

Cette section décrit les objets, les propriétés et les ressources qui constituent le modèle conceptuel WPD.

### <a name="objects"></a>Objets

Dans WPD, les entités logiques sur les appareils sont appelées objets. En général, mais pas toujours, ceux-ci représentent des données sur l’appareil. Les objets ont des propriétés et sont référencés par des identificateurs d’objet. Des images et des dossiers sur un appareil photo, des chansons et des sélections sur un lecteur multimédia, des contacts sur un téléphone mobile, etc. sont des exemples d’objets.

Les objets peuvent également représenter des parties fonctionnelles ou informatifs de l’appareil. Par exemple, les contrôles de lecteur (lecture/enregistrement/pause), les paramètres de l’appareil photo, les fonctionnalités SMS d’un téléphone mobile, etc.

Les deux rubriques suivantes donnent des exemples et des illustrations de deux types d’objets : l’objet image et l’objet Mediacast.

### <a name="image-object"></a>Image (objet)

Un objet image représente une image continue. Le diagramme suivant montre les relations entre un objet image, ses propriétés et ses ressources.

![Diagramme montrant un objet wpd et sa relation avec ses propriétés et ressources](images/wpd-overview-figure2.gif)

Pour plus d’informations sur l’objet image et ses propriétés, consultez la rubrique [**\_ image de \_ type \_ de contenu wpd**](wpd-content-type-image.md) .

### <a name="mediacast-object"></a>Objet Mediacast

Un objet Mediacast peut être considéré comme un objet conteneur qui regroupe du contenu associé, de la même façon qu’une sélection de musique. Souvent, un objet Mediacast est utilisé pour regrouper le contenu multimédia qui a été publié en ligne. Par exemple, un canal RSS peut être représenté sous la forme d’un objet Mediacast dont les références d’objet pointent vers les objets de contenu qui représentent chaque élément dans le canal. Le diagramme suivant montre la relation entre un objet Mediacast et les trois objets audio qu’il contient.

![Diagramme montrant la structure hiérarchique d’un objet le plus médicamenteux et trois objets qu’il contient](images/mediacast1.gif)

Les références à l’objet audio sont spécifiées dans la propriété [ \_ \_ références de l’objet wpd](object-properties.md) pour l’objet Mediacast. Pour plus d’informations sur les propriétés prises en charge par un objet Mediacast, consultez la rubrique [**\_ \_ \_ \_ diffusion multimédia type de contenu wpd**](wpd-content-type-media-cast.md) .

### <a name="properties"></a>Propriétés

Les propriétés d’objet fournissent un mécanisme permettant d’échanger des métadonnées de description d’objet. Par exemple, un objet image peut inclure des propriétés qui décrivent son nom de fichier, sa taille, son format, sa largeur en pixels, et ainsi de suite.

Les propriétés ont une valeur actuelle, ainsi que des attributs. WPD définit un ensemble de propriétés standard qui composent les définitions API et DDI. Les fournisseurs ne sont pas limités aux propriétés WPD prédéfinies et sont libres d’ajouter leur propre propriété.

### <a name="property-attributes"></a>Attributs de propriété

Les attributs de propriété décrivent les droits d’accès, les valeurs valides et d’autres informations relatives à une propriété. Par exemple, la propriété représentant la vitesse de transmission peut être comprise entre 8 kilobits par seconde (Kbits/s) et 20 kbps, avec une valeur de pas de 1 kbps.

Les droits d’accès indiquent si les appelants peuvent lire, écrire et/ou supprimer la propriété. Les valeurs valides indiquent des restrictions pour les valeurs de propriété. Les valeurs valides sont dites sous la forme d’un formulaire spécifique. Les formulaires de valeurs valides incluent Range (autrement dit, la propriété peut prendre une valeur comprise entre min et Max avec l’étape spécifiée), l’énumération (c’est-à-dire, la valeur de propriété est l’une de celles de la liste spécifiée) et None (il n’y a pas de valeurs valides spécifiques).

### <a name="resources"></a>Ressources

Les ressources sont des espaces réservés pour les données binaires. Un objet peut avoir plusieurs ressources. Par exemple, si l’objet représente un fichier image avec une annotation audio, les ressources pour cet objet peuvent se présenter comme suit :

-   Ressource par défaut. Cette ressource représente l’intégralité du fichier image. (Cela comprend les données incorporées, telles que les annotations audio, les miniatures, etc.)
-   Ressource miniature. Cette ressource représente les données de la miniature de l’image.
-   Ressource d’annotation audio. Cette ressource représente les données audio associées à l’image.

### <a name="resource-attributes"></a>Attributs de ressource

À l’instar des attributs de propriété, les attributs de ressource décrivent les droits d’accès, la taille, le format et d’autres informations relatives à une ressource. Par exemple, les attributs d’une ressource d’annotation audio sur un objet image peuvent spécifier la vitesse de transmission, le nombre de canaux et le format de données de l’audio.

### <a name="rendering-profiles-and-resource-attributes"></a>Rendu des profils et des attributs de ressource

Le profil de rendu est une méthode utilisée par les applications pour découvrir les attributs valides pour une ressource donnée. Par exemple, un téléphone mobile peut prendre en charge les bitmaps avec des restrictions spécifiques sur les valeurs de largeur et de hauteur minimales et maximales. En interrogeant les profils de rendu pour l’objet Bitmap, une application peut récupérer ces valeurs exactes.

L’exemple de sortie suivant identifie les informations de profil de rendu que l’appareil retournerait s’il prenait en charge des bitmaps d’une hauteur minimale de 10 pixels, une largeur minimale de 20 pixels, une hauteur maximale de 1000 pixels et une largeur maximale de 2000 pixels.


```C++
WPD_OBJECT_FORMAT = WPD_OBJECT_FORMAT_BMP
WPD_MEDIA_HEIGHT:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  10
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  10 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_MEDIA_WIDTH:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX =  2000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE = 0
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  2000 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
```



Consultez la rubrique [récupération des fonctionnalités de rendu prises en charge par un appareil](retrieving-the-rendering-capabilities-supported-by-a-device.md) dans le Guide de programmation pour obtenir une description de la manière dont votre application peut récupérer un profil de rendu (et les attributs de ressource associés).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble de l’application**](application-overview.md)
</dt> </dl>

 

 



