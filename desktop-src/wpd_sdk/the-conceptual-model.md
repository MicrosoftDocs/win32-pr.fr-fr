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
# <a name="the-conceptual-model"></a><span data-ttu-id="66892-103">Modèle conceptuel</span><span class="sxs-lookup"><span data-stu-id="66892-103">The Conceptual Model</span></span>

<span data-ttu-id="66892-104">Cette section décrit les objets, les propriétés et les ressources qui constituent le modèle conceptuel WPD.</span><span class="sxs-lookup"><span data-stu-id="66892-104">This section describes the objects, properties, and resources that constitute the WPD conceptual model.</span></span>

### <a name="objects"></a><span data-ttu-id="66892-105">Objets</span><span class="sxs-lookup"><span data-stu-id="66892-105">Objects</span></span>

<span data-ttu-id="66892-106">Dans WPD, les entités logiques sur les appareils sont appelées objets.</span><span class="sxs-lookup"><span data-stu-id="66892-106">In WPD, logical entities on devices are referred to as objects.</span></span> <span data-ttu-id="66892-107">En général, mais pas toujours, ceux-ci représentent des données sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="66892-107">Typically, but not always, these represent data on the device.</span></span> <span data-ttu-id="66892-108">Les objets ont des propriétés et sont référencés par des identificateurs d’objet.</span><span class="sxs-lookup"><span data-stu-id="66892-108">Objects have properties, and are referenced by object identifiers.</span></span> <span data-ttu-id="66892-109">Des images et des dossiers sur un appareil photo, des chansons et des sélections sur un lecteur multimédia, des contacts sur un téléphone mobile, etc. sont des exemples d’objets.</span><span class="sxs-lookup"><span data-stu-id="66892-109">Examples of objects include pictures and folders on a camera, songs and playlists on a media player, contacts on a mobile phone, and so on.</span></span>

<span data-ttu-id="66892-110">Les objets peuvent également représenter des parties fonctionnelles ou informatifs de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="66892-110">Objects can also represent functional or informational parts of the device.</span></span> <span data-ttu-id="66892-111">Par exemple, les contrôles de lecteur (lecture/enregistrement/pause), les paramètres de l’appareil photo, les fonctionnalités SMS d’un téléphone mobile, etc.</span><span class="sxs-lookup"><span data-stu-id="66892-111">Examples of these include player controls (play/record/pause), camera settings, a mobile phone's SMS capabilities, and so on.</span></span>

<span data-ttu-id="66892-112">Les deux rubriques suivantes donnent des exemples et des illustrations de deux types d’objets : l’objet image et l’objet Mediacast.</span><span class="sxs-lookup"><span data-stu-id="66892-112">The two following topics give examples and illustrations of two types of objects: the Image object and the Mediacast object.</span></span>

### <a name="image-object"></a><span data-ttu-id="66892-113">Image (objet)</span><span class="sxs-lookup"><span data-stu-id="66892-113">Image Object</span></span>

<span data-ttu-id="66892-114">Un objet image représente une image continue.</span><span class="sxs-lookup"><span data-stu-id="66892-114">An image object represents a still image.</span></span> <span data-ttu-id="66892-115">Le diagramme suivant montre les relations entre un objet image, ses propriétés et ses ressources.</span><span class="sxs-lookup"><span data-stu-id="66892-115">The following diagram shows the relationships between an Image object, its properties, and its resources.</span></span>

![Diagramme montrant un objet wpd et sa relation avec ses propriétés et ressources](images/wpd-overview-figure2.gif)

<span data-ttu-id="66892-117">Pour plus d’informations sur l’objet image et ses propriétés, consultez la rubrique [**\_ image de \_ type \_ de contenu wpd**](wpd-content-type-image.md) .</span><span class="sxs-lookup"><span data-stu-id="66892-117">For more information about the Image object and its properties, see the [**WPD\_CONTENT\_TYPE\_IMAGE**](wpd-content-type-image.md) topic.</span></span>

### <a name="mediacast-object"></a><span data-ttu-id="66892-118">Objet Mediacast</span><span class="sxs-lookup"><span data-stu-id="66892-118">Mediacast Object</span></span>

<span data-ttu-id="66892-119">Un objet Mediacast peut être considéré comme un objet conteneur qui regroupe du contenu associé, de la même façon qu’une sélection de musique.</span><span class="sxs-lookup"><span data-stu-id="66892-119">A Mediacast object can be thought of as a container object that groups related content, just as a playlist groups music.</span></span> <span data-ttu-id="66892-120">Souvent, un objet Mediacast est utilisé pour regrouper le contenu multimédia qui a été publié en ligne.</span><span class="sxs-lookup"><span data-stu-id="66892-120">Often, a Mediacast object is used to group media content that was published online.</span></span> <span data-ttu-id="66892-121">Par exemple, un canal RSS peut être représenté sous la forme d’un objet Mediacast dont les références d’objet pointent vers les objets de contenu qui représentent chaque élément dans le canal.</span><span class="sxs-lookup"><span data-stu-id="66892-121">For example, an RSS channel can be represented as a Mediacast object whose object references point to content objects that represent each item in the channel.</span></span> <span data-ttu-id="66892-122">Le diagramme suivant montre la relation entre un objet Mediacast et les trois objets audio qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="66892-122">The following diagram shows the relationship between a Mediacast object and the three audio objects it contains.</span></span>

![Diagramme montrant la structure hiérarchique d’un objet le plus médicamenteux et trois objets qu’il contient](images/mediacast1.gif)

<span data-ttu-id="66892-124">Les références à l’objet audio sont spécifiées dans la propriété [ \_ \_ références de l’objet wpd](object-properties.md) pour l’objet Mediacast.</span><span class="sxs-lookup"><span data-stu-id="66892-124">The references to the audio object are specified in the [WPD\_OBJECT\_REFERENCES](object-properties.md) property for the Mediacast object.</span></span> <span data-ttu-id="66892-125">Pour plus d’informations sur les propriétés prises en charge par un objet Mediacast, consultez la rubrique [**\_ \_ \_ \_ diffusion multimédia type de contenu wpd**](wpd-content-type-media-cast.md) .</span><span class="sxs-lookup"><span data-stu-id="66892-125">For more information about the properties supported by a Mediacast object, see the [**WPD\_CONTENT\_TYPE\_MEDIA\_CAST**](wpd-content-type-media-cast.md) topic.</span></span>

### <a name="properties"></a><span data-ttu-id="66892-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="66892-126">Properties</span></span>

<span data-ttu-id="66892-127">Les propriétés d’objet fournissent un mécanisme permettant d’échanger des métadonnées de description d’objet.</span><span class="sxs-lookup"><span data-stu-id="66892-127">Object properties provide a mechanism for exchanging object-describing metadata.</span></span> <span data-ttu-id="66892-128">Par exemple, un objet image peut inclure des propriétés qui décrivent son nom de fichier, sa taille, son format, sa largeur en pixels, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="66892-128">For example, an image object may include properties that describe its filename, size, format, width in pixels, and so on.</span></span>

<span data-ttu-id="66892-129">Les propriétés ont une valeur actuelle, ainsi que des attributs.</span><span class="sxs-lookup"><span data-stu-id="66892-129">Properties have a current value, as well as attributes.</span></span> <span data-ttu-id="66892-130">WPD définit un ensemble de propriétés standard qui composent les définitions API et DDI.</span><span class="sxs-lookup"><span data-stu-id="66892-130">WPD defines a set of standard properties that make up the API and DDI definitions.</span></span> <span data-ttu-id="66892-131">Les fournisseurs ne sont pas limités aux propriétés WPD prédéfinies et sont libres d’ajouter leur propre propriété.</span><span class="sxs-lookup"><span data-stu-id="66892-131">Vendors are not limited to the predefined WPD properties and are free to add their own.</span></span>

### <a name="property-attributes"></a><span data-ttu-id="66892-132">Attributs de propriété</span><span class="sxs-lookup"><span data-stu-id="66892-132">Property Attributes</span></span>

<span data-ttu-id="66892-133">Les attributs de propriété décrivent les droits d’accès, les valeurs valides et d’autres informations relatives à une propriété.</span><span class="sxs-lookup"><span data-stu-id="66892-133">Property attributes describe the access rights, valid values, and other information related to a property.</span></span> <span data-ttu-id="66892-134">Par exemple, la propriété représentant la vitesse de transmission peut être comprise entre 8 kilobits par seconde (Kbits/s) et 20 kbps, avec une valeur de pas de 1 kbps.</span><span class="sxs-lookup"><span data-stu-id="66892-134">For example, the property representing bit rate could be a range from 8 kilobits per second (Kbps) to 20 Kbps with a step value of 1 Kbps.</span></span>

<span data-ttu-id="66892-135">Les droits d’accès indiquent si les appelants peuvent lire, écrire et/ou supprimer la propriété.</span><span class="sxs-lookup"><span data-stu-id="66892-135">Access rights indicate whether callers can read, write and/or delete the property.</span></span> <span data-ttu-id="66892-136">Les valeurs valides indiquent des restrictions pour les valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="66892-136">Valid values indicate restrictions for property values.</span></span> <span data-ttu-id="66892-137">Les valeurs valides sont dites sous la forme d’un formulaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="66892-137">Valid values are said to be of a specific form.</span></span> <span data-ttu-id="66892-138">Les formulaires de valeurs valides incluent Range (autrement dit, la propriété peut prendre une valeur comprise entre min et Max avec l’étape spécifiée), l’énumération (c’est-à-dire, la valeur de propriété est l’une de celles de la liste spécifiée) et None (il n’y a pas de valeurs valides spécifiques).</span><span class="sxs-lookup"><span data-stu-id="66892-138">Valid value forms include Range (that is, property can take a value from Min to Max with specified Step), Enumeration (that is, property value is one of those in the specified List), and None (that is, there are no specific valid values).</span></span>

### <a name="resources"></a><span data-ttu-id="66892-139">Ressources</span><span class="sxs-lookup"><span data-stu-id="66892-139">Resources</span></span>

<span data-ttu-id="66892-140">Les ressources sont des espaces réservés pour les données binaires.</span><span class="sxs-lookup"><span data-stu-id="66892-140">Resources are placeholders for binary data.</span></span> <span data-ttu-id="66892-141">Un objet peut avoir plusieurs ressources.</span><span class="sxs-lookup"><span data-stu-id="66892-141">An object can have more than one resource.</span></span> <span data-ttu-id="66892-142">Par exemple, si l’objet représente un fichier image avec une annotation audio, les ressources pour cet objet peuvent se présenter comme suit :</span><span class="sxs-lookup"><span data-stu-id="66892-142">For example, if the object represented an image file with an audio annotation, then the resources for this object might be as follows:</span></span>

-   <span data-ttu-id="66892-143">Ressource par défaut.</span><span class="sxs-lookup"><span data-stu-id="66892-143">A default resource.</span></span> <span data-ttu-id="66892-144">Cette ressource représente l’intégralité du fichier image.</span><span class="sxs-lookup"><span data-stu-id="66892-144">This resource represents the entire image file.</span></span> <span data-ttu-id="66892-145">(Cela comprend les données incorporées, telles que les annotations audio, les miniatures, etc.)</span><span class="sxs-lookup"><span data-stu-id="66892-145">(This includes any embedded data such as audio annotations, thumbnails, and so on)</span></span>
-   <span data-ttu-id="66892-146">Ressource miniature.</span><span class="sxs-lookup"><span data-stu-id="66892-146">A thumbnail resource.</span></span> <span data-ttu-id="66892-147">Cette ressource représente les données de la miniature de l’image.</span><span class="sxs-lookup"><span data-stu-id="66892-147">This resource represents the thumbnail data for the image.</span></span>
-   <span data-ttu-id="66892-148">Ressource d’annotation audio.</span><span class="sxs-lookup"><span data-stu-id="66892-148">An audio annotation resource.</span></span> <span data-ttu-id="66892-149">Cette ressource représente les données audio associées à l’image.</span><span class="sxs-lookup"><span data-stu-id="66892-149">This resource represents the audio data associated with the image.</span></span>

### <a name="resource-attributes"></a><span data-ttu-id="66892-150">Attributs de ressource</span><span class="sxs-lookup"><span data-stu-id="66892-150">Resource Attributes</span></span>

<span data-ttu-id="66892-151">À l’instar des attributs de propriété, les attributs de ressource décrivent les droits d’accès, la taille, le format et d’autres informations relatives à une ressource.</span><span class="sxs-lookup"><span data-stu-id="66892-151">Similar to property attributes, resource attributes describe the access rights, size, format, and other information related to a resource.</span></span> <span data-ttu-id="66892-152">Par exemple, les attributs d’une ressource d’annotation audio sur un objet image peuvent spécifier la vitesse de transmission, le nombre de canaux et le format de données de l’audio.</span><span class="sxs-lookup"><span data-stu-id="66892-152">For example, the attributes for an audio annotation resource on an image object may specify the bit rate, channel count, and data format of the audio.</span></span>

### <a name="rendering-profiles-and-resource-attributes"></a><span data-ttu-id="66892-153">Rendu des profils et des attributs de ressource</span><span class="sxs-lookup"><span data-stu-id="66892-153">Rendering Profiles and Resource Attributes</span></span>

<span data-ttu-id="66892-154">Le profil de rendu est une méthode utilisée par les applications pour découvrir les attributs valides pour une ressource donnée.</span><span class="sxs-lookup"><span data-stu-id="66892-154">The rendering profile is one method that applications use to discover the valid attributes for a given resource.</span></span> <span data-ttu-id="66892-155">Par exemple, un téléphone mobile peut prendre en charge les bitmaps avec des restrictions spécifiques sur les valeurs de largeur et de hauteur minimales et maximales.</span><span class="sxs-lookup"><span data-stu-id="66892-155">For example, a mobile phone may support bitmaps with specific restrictions on the minimum and maximum width and height values.</span></span> <span data-ttu-id="66892-156">En interrogeant les profils de rendu pour l’objet Bitmap, une application peut récupérer ces valeurs exactes.</span><span class="sxs-lookup"><span data-stu-id="66892-156">By querying the rendering profiles for the bitmap object, an application can retrieve those exact values.</span></span>

<span data-ttu-id="66892-157">L’exemple de sortie suivant identifie les informations de profil de rendu que l’appareil retournerait s’il prenait en charge des bitmaps d’une hauteur minimale de 10 pixels, une largeur minimale de 20 pixels, une hauteur maximale de 1000 pixels et une largeur maximale de 2000 pixels.</span><span class="sxs-lookup"><span data-stu-id="66892-157">The following sample output identifies the rendering profile information that the device would return if it supported bitmaps with a minimum height of 10 pixels, a minimum width of 20 pixels, a maximum height of 1000 pixels and a maximum width of 2000 pixels.</span></span>


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



<span data-ttu-id="66892-158">Consultez la rubrique [récupération des fonctionnalités de rendu prises en charge par un appareil](retrieving-the-rendering-capabilities-supported-by-a-device.md) dans le Guide de programmation pour obtenir une description de la manière dont votre application peut récupérer un profil de rendu (et les attributs de ressource associés).</span><span class="sxs-lookup"><span data-stu-id="66892-158">See the [Retrieving the Rendering Capabilities Supported by a Device](retrieving-the-rendering-capabilities-supported-by-a-device.md) topic in the programming guide for a description of how your application can retrieve a rendering profile (and the associated resource attributes).</span></span>

## <a name="related-topics"></a><span data-ttu-id="66892-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="66892-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66892-160">**Vue d’ensemble de l’application**</span><span class="sxs-lookup"><span data-stu-id="66892-160">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



