---
description: Métadonnées de média
ms.assetid: dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9
title: Métadonnées de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb17f286673663976e17b4178239507765c2101
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106525801"
---
# <a name="media-metadata"></a><span data-ttu-id="d6264-103">Métadonnées de média</span><span class="sxs-lookup"><span data-stu-id="d6264-103">Media Metadata</span></span>

<span data-ttu-id="d6264-104">Les fichiers multimédias contiennent des propriétés qui décrivent le contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="d6264-104">Media files contain properties that describe the contents of the file.</span></span> <span data-ttu-id="d6264-105">Dans Microsoft Media Foundation, ces propriétés peuvent être classées comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6264-105">In Microsoft Media Foundation, these properties can be categorized as follows:</span></span>

-   <span data-ttu-id="d6264-106">Les **attributs de type de média** spécifient les paramètres d’encodage, tels que l’algorithme d’encodage (sous-type de média), la taille d’image vidéo, la fréquence d’images vidéo, la vitesse de transmission audio et le taux d’échantillonnage audio.</span><span class="sxs-lookup"><span data-stu-id="d6264-106">**Media-type attributes** specify the encoding parameters, such as the encoding algorithm (media subtype), video frame size, video frame rate, audio bit rate, and audio sample rate.</span></span> <span data-ttu-id="d6264-107">Pour plus d’informations sur les attributs de type de média, consultez [types de médias](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="d6264-107">For more information about media-type attributes, see [Media Types](media-types.md).</span></span>
-   <span data-ttu-id="d6264-108">Les **métadonnées** contiennent des informations descriptives sur le contenu multimédia, telles que le titre, l’artiste, le compositeur et le genre.</span><span class="sxs-lookup"><span data-stu-id="d6264-108">**Metadata** contains descriptive information for the media content, such as title, artist, composer, and genre.</span></span> <span data-ttu-id="d6264-109">Les métadonnées peuvent également décrire les paramètres d’encodage.</span><span class="sxs-lookup"><span data-stu-id="d6264-109">Metadata can also describe encoding parameters.</span></span> <span data-ttu-id="d6264-110">Il peut être plus rapide d’accéder à ces informations par le biais de métadonnées que par le biais d’attributs de type média.</span><span class="sxs-lookup"><span data-stu-id="d6264-110">It can be faster to access this information through metadata than through media-type attributes.</span></span>
-   <span data-ttu-id="d6264-111">Les **Propriétés DRM** contiennent des informations sur les restrictions d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="d6264-111">**DRM properties** contain information on usage restrictions.</span></span> <span data-ttu-id="d6264-112">Actuellement Media Foundation ne prend pas en charge les propriétés DRM par le biais de métadonnées, à l’exception de la propriété **\_ hyperdrm \_ IsProtected** .</span><span class="sxs-lookup"><span data-stu-id="d6264-112">Currently Media Foundation does not support DRM properties through metadata, with the exception of the **PKEY\_DRM\_IsProtected** property.</span></span>

<span data-ttu-id="d6264-113">Il existe deux façons de lire les métadonnées dans Media Foundation :</span><span class="sxs-lookup"><span data-stu-id="d6264-113">There are two ways to read metadata in Media Foundation:</span></span>

-   <span data-ttu-id="d6264-114">Interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) (métadonnées de la version 1 Media Foundation).</span><span class="sxs-lookup"><span data-stu-id="d6264-114">The [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface (Media Foundation version 1 metadata).</span></span>
-   <span data-ttu-id="d6264-115">Interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) de l’interpréteur de commandes Windows (métadonnées de l’interpréteur de commandes).</span><span class="sxs-lookup"><span data-stu-id="d6264-115">The Windows Shell [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface (Shell metadata).</span></span>

<span data-ttu-id="d6264-116">Les métadonnées de l’interpréteur de commandes se rapportent non seulement aux fichiers multimédias, mais à un plus grand nombre de fichiers sur le système.</span><span class="sxs-lookup"><span data-stu-id="d6264-116">Shell metadata pertains not only to media files but to a much wider range of files on the system.</span></span>

<span data-ttu-id="d6264-117">Le tableau suivant compare les fonctionnalités et les limitations de chaque API de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="d6264-117">The following table compares the features and limitations of each metadata API.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6264-118">Media Foundation les métadonnées v1</span><span class="sxs-lookup"><span data-stu-id="d6264-118">Media Foundation v1 Metadata</span></span></th>
<th><span data-ttu-id="d6264-119">Métadonnées de Shell</span><span class="sxs-lookup"><span data-stu-id="d6264-119">Shell Metadata</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d6264-120">Nécessite Windows Vista ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d6264-120">Requires Windows Vista or later.</span></span></td>
<td><span data-ttu-id="d6264-121">Requiert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d6264-121">Requires Windows 7.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="d6264-122">En général, les métadonnées de l’interpréteur de commandes ne nécessitent pas Windows 7, mais Media Foundation ne prenait pas en charge les métadonnées d’environnement antérieures à Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d6264-122">Shell metadata in general does not require Windows 7, but Media Foundation did not support Shell metadata prior to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6264-123">Les propriétés ne sont pas compatibles avec le système de propriétés de Shell.</span><span class="sxs-lookup"><span data-stu-id="d6264-123">Properties are not compatible with Shell property system.</span></span></td>
<td><span data-ttu-id="d6264-124">Les propriétés sont compatibles avec le système de propriétés de Shell.</span><span class="sxs-lookup"><span data-stu-id="d6264-124">Properties are compatible with the Shell property system.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6264-125">Les propriétés peuvent s’appliquer à la totalité du fichier ou au niveau du flux.</span><span class="sxs-lookup"><span data-stu-id="d6264-125">Properties can apply to the entire file, or at the stream level.</span></span></td>
<td><span data-ttu-id="d6264-126">Seules les propriétés au niveau du fichier sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d6264-126">Only file-level properties are supported.</span></span> <span data-ttu-id="d6264-127">Les propriétés au niveau du flux ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d6264-127">Stream-level properties are not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6264-128">Les propriétés peuvent avoir des valeurs dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="d6264-128">Properties can have values in multiple languages.</span></span></td>
<td><span data-ttu-id="d6264-129">Les valeurs dans plusieurs langues ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d6264-129">Values in multiple languages are not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6264-130">Les clés de propriété sont des chaînes à caractères larges.</span><span class="sxs-lookup"><span data-stu-id="d6264-130">Property keys are wide-character strings.</span></span></td>
<td><span data-ttu-id="d6264-131">Les clés de propriété sont des valeurs <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d6264-131">Property keys are <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6264-132">Les valeurs de propriété sont des valeurs <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d6264-132">Property values are <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> values.</span></span></td>
<td><span data-ttu-id="d6264-133">Les valeurs de propriété sont des valeurs <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d6264-133">Property values are <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> values.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="in-this-section"></a><span data-ttu-id="d6264-134">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="d6264-134">In this section</span></span>



| <span data-ttu-id="d6264-135">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d6264-135">Topic</span></span>                                                                                     | <span data-ttu-id="d6264-136">Description</span><span class="sxs-lookup"><span data-stu-id="d6264-136">Description</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6264-137">Fournisseurs de métadonnées de Shell</span><span class="sxs-lookup"><span data-stu-id="d6264-137">Shell Metadata Providers</span></span>](shell-metadata-providers.md)<br/>                       | <span data-ttu-id="d6264-138">À compter de Windows 7, Media Foundation expose des métadonnées par le biais de l’interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="d6264-138">Starting in Windows 7, Media Foundation exposes metadata through the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span><br/> |
| [<span data-ttu-id="d6264-139">Propriétés de métadonnées pour les fichiers multimédias</span><span class="sxs-lookup"><span data-stu-id="d6264-139">Metadata Properties for Media Files</span></span>](metadata-properties-for-media-files.md)<br/> | <span data-ttu-id="d6264-140">Cette rubrique répertorie les propriétés de métadonnées les plus courantes pour les fichiers multimédias.</span><span class="sxs-lookup"><span data-stu-id="d6264-140">This topic lists the most common metadata properties for media files.</span></span><br/>                                                           |
| [<span data-ttu-id="d6264-141">Fournisseurs de métadonnées dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6264-141">Metadata Providers in Windows Vista</span></span>](metadata-providers-in-windows-vista.md)<br/> | <span data-ttu-id="d6264-142">Dans Windows Vista, Media Foundation expose les métadonnées par le biais de l’interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="d6264-142">In Windows Vista, Media Foundation exposes metadata through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span><br/>                   |



 

<span data-ttu-id="d6264-143">Si vous implémentez une source de média personnalisée et souhaitez exposer les métadonnées de l’interpréteur de commandes, consultez [fournisseurs de métadonnées personnalisés pour les fichiers multimédias](custom-metadata-providers-for-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="d6264-143">If you are implementing a custom media source and want to expose Shell metadata, see [Custom Metadata Providers for Media Files](custom-metadata-providers-for-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6264-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d6264-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6264-145">Guide de programmation Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d6264-145">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 
