---
description: La liste suivante fournit des descriptions des éléments de propriété pris en charge par Windows GDI+.
ms.assetid: fc95aa3f-8381-430d-8cbf-6d23816a738d
title: Descriptions des éléments de propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc2a627ec809bb4f7d7299c522fd0e9d3e1cc05
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/27/2021
ms.locfileid: "105636121"
---
# <a name="property-item-descriptions"></a><span data-ttu-id="f7aa7-103">Descriptions des éléments de propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-103">Property Item Descriptions</span></span>

<span data-ttu-id="f7aa7-104">La liste suivante fournit des descriptions des éléments de propriété pris en charge par Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-104">The following list gives descriptions of the property items supported by Windows GDI+.</span></span> <span data-ttu-id="f7aa7-105">Les descriptions sont courtes et générales afin qu’elles s’appliquent à un large éventail de formats de fichiers image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-105">The descriptions are brief and general so that they apply to a variety of image file formats.</span></span> <span data-ttu-id="f7aa7-106">Pour obtenir une description détaillée de la façon dont un élément de propriété est utilisé par un format de fichier particulier, consultez la spécification de ce format de fichier.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-106">For a detailed description of how a property item is used by a particular file format, see the specification for that file format.</span></span> <span data-ttu-id="f7aa7-107">Pour obtenir des liens vers plusieurs spécifications de fichier et d’autres documents qui décrivent les métadonnées en détail, consultez [spécifications de format de fichier image](-gdiplus-constant-image-file-format-specifications.md).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-107">For links to several file specifications and other documents that describe metadata in detail, see [Image File Format Specifications](-gdiplus-constant-image-file-format-specifications.md).</span></span>

<span data-ttu-id="f7aa7-108">Le format EXIF (Exchangeable Image File) est une norme JEIDA (Japon Electronic Development Association), révisée le 1998 juin en version 2,1.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-108">The Exchangeable Image File (EXIF) format is a Japan Electronic Industry Development Association (JEIDA) standard, revised June 1998 as version 2.1.</span></span> <span data-ttu-id="f7aa7-109">Des parties de la spécification EXIF sont utilisées avec l’autorisation JEIDA.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-109">Portions of the EXIF specification are used with permission of JEIDA.</span></span>

## <a name="propertytaggpsver"></a><span data-ttu-id="f7aa7-110">PropertyTagGpsVer</span><span class="sxs-lookup"><span data-stu-id="f7aa7-110">PropertyTagGpsVer</span></span>

<span data-ttu-id="f7aa7-111">Version de l’IFD du système de positionnement global (GPS), donnée sous la forme 2.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-111">Version of the Global Positioning Systems (GPS) IFD, given as 2.0.0.0.</span></span> <span data-ttu-id="f7aa7-112">Cette balise est obligatoire lorsque la balise PropertyTagGpsIFD est présente.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-112">This tag is mandatory when the PropertyTagGpsIFD tag is present.</span></span> <span data-ttu-id="f7aa7-113">Lorsque la version est 2.0.0.0, la valeur de la balise est 0x02000000.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-113">When the version is 2.0.0.0, the tag value is 0x02000000.</span></span>



| <span data-ttu-id="f7aa7-114">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-114">Property info</span></span> | <span data-ttu-id="f7aa7-115">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-115">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-116">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-116">Tag</span></span>   | <span data-ttu-id="f7aa7-117">0x0000</span><span class="sxs-lookup"><span data-stu-id="f7aa7-117">0x0000</span></span>              |
| <span data-ttu-id="f7aa7-118">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-118">Type</span></span>  | <span data-ttu-id="f7aa7-119">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="f7aa7-119">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="f7aa7-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-120">Count</span></span> | <span data-ttu-id="f7aa7-121">4</span><span class="sxs-lookup"><span data-stu-id="f7aa7-121">4</span></span>                   |



 

## <a name="propertytaggpslatituderef"></a><span data-ttu-id="f7aa7-122">PropertyTagGpsLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="f7aa7-122">PropertyTagGpsLatitudeRef</span></span>

<span data-ttu-id="f7aa7-123">Chaîne de caractères se terminant par un caractère null qui spécifie si la latitude est le Nord ou le sud.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-123">Null-terminated character string that specifies whether the latitude is north or south.</span></span> <span data-ttu-id="f7aa7-124">`N` spécifie la latitude nord et `S` spécifie la latitude sud.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-124">`N` specifies north latitude, and `S` specifies south latitude.</span></span>



| <span data-ttu-id="f7aa7-125">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-125">Property info</span></span> | <span data-ttu-id="f7aa7-126">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-126">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="f7aa7-127">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-127">Tag</span></span>   | <span data-ttu-id="f7aa7-128">0x0001</span><span class="sxs-lookup"><span data-stu-id="f7aa7-128">0x0001</span></span>                                     |
| <span data-ttu-id="f7aa7-129">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-129">Type</span></span>  | <span data-ttu-id="f7aa7-130">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-130">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="f7aa7-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-131">Count</span></span> | <span data-ttu-id="f7aa7-132">2 (un caractère plus la marque de fin NULL)</span><span class="sxs-lookup"><span data-stu-id="f7aa7-132">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpslatitude"></a><span data-ttu-id="f7aa7-133">PropertyTagGpsLatitude</span><span class="sxs-lookup"><span data-stu-id="f7aa7-133">PropertyTagGpsLatitude</span></span>

<span data-ttu-id="f7aa7-134">Latitude.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-134">Latitude.</span></span> <span data-ttu-id="f7aa7-135">La latitude est exprimée sous la forme de trois valeurs rationnelles donnant respectivement les degrés, les minutes et les secondes.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-135">Latitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="f7aa7-136">Lorsque les degrés, les minutes et les secondes sont exprimés, le format est JJ/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-136">When degrees, minutes, and seconds are expressed, the format is dd/1, mm/1, ss/1.</span></span> <span data-ttu-id="f7aa7-137">Lorsque les degrés et les minutes sont utilisés et, par exemple, les fractions de minutes sont indiquées jusqu’à deux décimales, le format est JJ/1, mmmm/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-137">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is dd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="f7aa7-138">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-138">Property info</span></span> | <span data-ttu-id="f7aa7-139">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-139">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-140">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-140">Tag</span></span>   | <span data-ttu-id="f7aa7-141">0x0002</span><span class="sxs-lookup"><span data-stu-id="f7aa7-141">0x0002</span></span>                  |
| <span data-ttu-id="f7aa7-142">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-142">Type</span></span>  | <span data-ttu-id="f7aa7-143">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-143">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-144">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-144">Count</span></span> | <span data-ttu-id="f7aa7-145">3</span><span class="sxs-lookup"><span data-stu-id="f7aa7-145">3</span></span>                       |



 

## <a name="propertytaggpslongituderef"></a><span data-ttu-id="f7aa7-146">PropertyTagGpsLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="f7aa7-146">PropertyTagGpsLongitudeRef</span></span>

<span data-ttu-id="f7aa7-147">Chaîne de caractères se terminant par un caractère null qui spécifie si la longitude est ou longitude ouest.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-147">Null-terminated character string that specifies whether the longitude is east or west longitude.</span></span> <span data-ttu-id="f7aa7-148">`E` spécifie la longitude est et `W` spécifie la longitude ouest.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-148">`E` specifies east longitude, and `W` specifies west longitude.</span></span>



| <span data-ttu-id="f7aa7-149">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-149">Property info</span></span> | <span data-ttu-id="f7aa7-150">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-150">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="f7aa7-151">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-151">Tag</span></span>   | <span data-ttu-id="f7aa7-152">0x0003</span><span class="sxs-lookup"><span data-stu-id="f7aa7-152">0x0003</span></span>                                     |
| <span data-ttu-id="f7aa7-153">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-153">Type</span></span>  | <span data-ttu-id="f7aa7-154">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-154">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="f7aa7-155">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-155">Count</span></span> | <span data-ttu-id="f7aa7-156">2 (un caractère plus la marque de fin NULL)</span><span class="sxs-lookup"><span data-stu-id="f7aa7-156">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpslongitude"></a><span data-ttu-id="f7aa7-157">PropertyTagGpsLongitude</span><span class="sxs-lookup"><span data-stu-id="f7aa7-157">PropertyTagGpsLongitude</span></span>

<span data-ttu-id="f7aa7-158">Longitude.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-158">Longitude.</span></span> <span data-ttu-id="f7aa7-159">La longitude est exprimée sous la forme de trois valeurs rationnelles accordant respectivement les degrés, les minutes et les secondes.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-159">Longitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="f7aa7-160">Lorsque les degrés, les minutes et les secondes sont exprimés, le format est DDD/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-160">When degrees, minutes and seconds are expressed, the format is ddd/1, mm/1, ss/1.</span></span> <span data-ttu-id="f7aa7-161">Lorsque les degrés et les minutes sont utilisés et, par exemple, les fractions de minutes sont indiquées jusqu’à deux décimales, le format est DDD/1, mmmm/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-161">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is ddd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="f7aa7-162">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-162">Property info</span></span> | <span data-ttu-id="f7aa7-163">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-163">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-164">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-164">Tag</span></span>   | <span data-ttu-id="f7aa7-165">0x0004</span><span class="sxs-lookup"><span data-stu-id="f7aa7-165">0x0004</span></span>                  |
| <span data-ttu-id="f7aa7-166">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-166">Type</span></span>  | <span data-ttu-id="f7aa7-167">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-167">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-168">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-168">Count</span></span> | <span data-ttu-id="f7aa7-169">3</span><span class="sxs-lookup"><span data-stu-id="f7aa7-169">3</span></span>                       |



 

## <a name="propertytaggpsaltituderef"></a><span data-ttu-id="f7aa7-170">PropertyTagGpsAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="f7aa7-170">PropertyTagGpsAltitudeRef</span></span>

<span data-ttu-id="f7aa7-171">Altitude de référence, en mètres.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-171">Reference altitude, in meters.</span></span>



| <span data-ttu-id="f7aa7-172">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-172">Property info</span></span> | <span data-ttu-id="f7aa7-173">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-173">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-174">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-174">Tag</span></span>   | <span data-ttu-id="f7aa7-175">0x0005</span><span class="sxs-lookup"><span data-stu-id="f7aa7-175">0x0005</span></span>              |
| <span data-ttu-id="f7aa7-176">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-176">Type</span></span>  | <span data-ttu-id="f7aa7-177">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="f7aa7-177">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="f7aa7-178">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-178">Count</span></span> | <span data-ttu-id="f7aa7-179">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-179">1</span></span>                   |



 

## <a name="propertytaggpsaltitude"></a><span data-ttu-id="f7aa7-180">PropertyTagGpsAltitude</span><span class="sxs-lookup"><span data-stu-id="f7aa7-180">PropertyTagGpsAltitude</span></span>

<span data-ttu-id="f7aa7-181">Altitude, en mètres, en fonction de l’altitude de référence spécifiée par PropertyTagGpsAltitudeRef.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-181">Altitude, in meters, based on the reference altitude specified by PropertyTagGpsAltitudeRef.</span></span>



| <span data-ttu-id="f7aa7-182">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-182">Property info</span></span> | <span data-ttu-id="f7aa7-183">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-183">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-184">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-184">Tag</span></span>   | <span data-ttu-id="f7aa7-185">0x0006</span><span class="sxs-lookup"><span data-stu-id="f7aa7-185">0x0006</span></span>                  |
| <span data-ttu-id="f7aa7-186">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-186">Type</span></span>  | <span data-ttu-id="f7aa7-187">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-187">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-188">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-188">Count</span></span> | <span data-ttu-id="f7aa7-189">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-189">1</span></span>                       |



 

## <a name="propertytaggpsgpstime"></a><span data-ttu-id="f7aa7-190">PropertyTagGpsGpsTime</span><span class="sxs-lookup"><span data-stu-id="f7aa7-190">PropertyTagGpsGpsTime</span></span>

<span data-ttu-id="f7aa7-191">Heure au format UTC (temps universel coordonné).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-191">Time as Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="f7aa7-192">La valeur est exprimée sous la forme de trois nombres rationnels qui donnent l’heure, la minute et la seconde.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-192">The value is expressed as three rational numbers that give the hour, minute, and second.</span></span>



| <span data-ttu-id="f7aa7-193">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-193">Property info</span></span> | <span data-ttu-id="f7aa7-194">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-194">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-195">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-195">Tag</span></span>   | <span data-ttu-id="f7aa7-196">0x0007</span><span class="sxs-lookup"><span data-stu-id="f7aa7-196">0x0007</span></span>                  |
| <span data-ttu-id="f7aa7-197">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-197">Type</span></span>  | <span data-ttu-id="f7aa7-198">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-198">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-199">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-199">Count</span></span> | <span data-ttu-id="f7aa7-200">3</span><span class="sxs-lookup"><span data-stu-id="f7aa7-200">3</span></span>                       |



 

## <a name="propertytaggpsgpssatellites"></a><span data-ttu-id="f7aa7-201">PropertyTagGpsGpsSatellites</span><span class="sxs-lookup"><span data-stu-id="f7aa7-201">PropertyTagGpsGpsSatellites</span></span>

<span data-ttu-id="f7aa7-202">Chaîne de caractères se terminant par un caractère null qui spécifie les satellites GPS utilisés pour les mesures.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-202">Null-terminated character string that specifies the GPS satellites used for measurements.</span></span> <span data-ttu-id="f7aa7-203">Cette balise peut être utilisée pour spécifier le numéro d’identification, l’angle d’élévation, l’azimut, le SNR et d’autres informations sur chaque satellite.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-203">This tag can be used to specify the ID number, angle of elevation, azimuth, SNR, and other information about each satellite.</span></span> <span data-ttu-id="f7aa7-204">Le format n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-204">The format is not specified.</span></span> <span data-ttu-id="f7aa7-205">Si le récepteur GPS n’est pas en mesure de prendre des mesures, la valeur de la balise doit être définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-205">If the GPS receiver is incapable of taking measurements, the value of the tag must be set to **NULL**.</span></span>



| <span data-ttu-id="f7aa7-206">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-206">Property info</span></span> | <span data-ttu-id="f7aa7-207">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-207">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-208">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-208">Tag</span></span>   | <span data-ttu-id="f7aa7-209">0x0008</span><span class="sxs-lookup"><span data-stu-id="f7aa7-209">0x0008</span></span>                                             |
| <span data-ttu-id="f7aa7-210">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-210">Type</span></span>  | <span data-ttu-id="f7aa7-211">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-211">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-212">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-212">Count</span></span> | <span data-ttu-id="f7aa7-213">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-213">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsgpsstatus"></a><span data-ttu-id="f7aa7-214">PropertyTagGpsGpsStatus</span><span class="sxs-lookup"><span data-stu-id="f7aa7-214">PropertyTagGpsGpsStatus</span></span>

<span data-ttu-id="f7aa7-215">Chaîne de caractères se terminant par un caractère null qui spécifie l’état du récepteur GPS lorsque l’image est enregistrée.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-215">Null-terminated character string that specifies the status of the GPS receiver when the image is recorded.</span></span> <span data-ttu-id="f7aa7-216">`A` signifie que la mesure est en cours et `V` signifie que la mesure est l’interopérabilité.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-216">`A` means measurement is in progress, and `V` means the measurement is Interoperability.</span></span>



| <span data-ttu-id="f7aa7-217">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-217">Property info</span></span> | <span data-ttu-id="f7aa7-218">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-218">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="f7aa7-219">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-219">Tag</span></span>   | <span data-ttu-id="f7aa7-220">0x0009</span><span class="sxs-lookup"><span data-stu-id="f7aa7-220">0x0009</span></span>                                     |
| <span data-ttu-id="f7aa7-221">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-221">Type</span></span>  | <span data-ttu-id="f7aa7-222">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-222">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="f7aa7-223">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-223">Count</span></span> | <span data-ttu-id="f7aa7-224">2 (un caractère plus la marque de fin NULL)</span><span class="sxs-lookup"><span data-stu-id="f7aa7-224">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsgpsmeasuremode"></a><span data-ttu-id="f7aa7-225">PropertyTagGpsGpsMeasureMode</span><span class="sxs-lookup"><span data-stu-id="f7aa7-225">PropertyTagGpsGpsMeasureMode</span></span>

<span data-ttu-id="f7aa7-226">Chaîne de caractères se terminant par un caractère null qui spécifie le mode de mesure GPS.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-226">Null-terminated character string that specifies the GPS measurement mode.</span></span> <span data-ttu-id="f7aa7-227">`2` spécifie la mesure 2D et `3` spécifie une mesure 3D.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-227">`2` specifies 2-D measurement, and `3` specifies 3-D measurement.</span></span>



| <span data-ttu-id="f7aa7-228">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-228">Property info</span></span> | <span data-ttu-id="f7aa7-229">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-229">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="f7aa7-230">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-230">Tag</span></span>   | <span data-ttu-id="f7aa7-231">0x000A</span><span class="sxs-lookup"><span data-stu-id="f7aa7-231">0x000A</span></span>                                     |
| <span data-ttu-id="f7aa7-232">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-232">Type</span></span>  | <span data-ttu-id="f7aa7-233">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-233">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="f7aa7-234">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-234">Count</span></span> | <span data-ttu-id="f7aa7-235">2 (un caractère plus la marque de fin NULL)</span><span class="sxs-lookup"><span data-stu-id="f7aa7-235">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsgpsdop"></a><span data-ttu-id="f7aa7-236">PropertyTagGpsGpsDop</span><span class="sxs-lookup"><span data-stu-id="f7aa7-236">PropertyTagGpsGpsDop</span></span>

<span data-ttu-id="f7aa7-237">GPS DOP (degré de précision des données).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-237">GPS DOP (data degree of precision).</span></span> <span data-ttu-id="f7aa7-238">Une valeur HDOP est écrite en cours de mesure 2D, et une valeur PDOP est écrite en cours de mesure 3D.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-238">An HDOP value is written during 2-D measurement, and a PDOP value is written during 3-D measurement.</span></span>



| <span data-ttu-id="f7aa7-239">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-239">Property info</span></span> | <span data-ttu-id="f7aa7-240">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-240">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-241">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-241">Tag</span></span>   | <span data-ttu-id="f7aa7-242">0x000B</span><span class="sxs-lookup"><span data-stu-id="f7aa7-242">0x000B</span></span>                  |
| <span data-ttu-id="f7aa7-243">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-243">Type</span></span>  | <span data-ttu-id="f7aa7-244">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-244">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-245">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-245">Count</span></span> | <span data-ttu-id="f7aa7-246">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-246">1</span></span>                       |



 

## <a name="propertytaggpsspeedref"></a><span data-ttu-id="f7aa7-247">PropertyTagGpsSpeedRef</span><span class="sxs-lookup"><span data-stu-id="f7aa7-247">PropertyTagGpsSpeedRef</span></span>

<span data-ttu-id="f7aa7-248">Chaîne de caractères se terminant par un caractère null qui spécifie l’unité utilisée pour exprimer la vitesse de déplacement du récepteur GPS.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-248">Null-terminated character string that specifies the unit used to express the GPS receiver speed of movement.</span></span> <span data-ttu-id="f7aa7-249">`K`, `M` et `N` représentent des kilomètres par heure, miles par heure et nœuds respectivement.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-249">`K`, `M`, and `N` represent kilometers per hour, miles per hour, and knots respectively.</span></span>



| <span data-ttu-id="f7aa7-250">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-250">Property info</span></span> | <span data-ttu-id="f7aa7-251">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-251">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="f7aa7-252">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-252">Tag</span></span>   | <span data-ttu-id="f7aa7-253">0x000C</span><span class="sxs-lookup"><span data-stu-id="f7aa7-253">0x000C</span></span>                                     |
| <span data-ttu-id="f7aa7-254">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-254">Type</span></span>  | <span data-ttu-id="f7aa7-255">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-255">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="f7aa7-256">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-256">Count</span></span> | <span data-ttu-id="f7aa7-257">2 (un caractère plus la marque de fin NULL)</span><span class="sxs-lookup"><span data-stu-id="f7aa7-257">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsspeed"></a><span data-ttu-id="f7aa7-258">PropertyTagGpsSpeed</span><span class="sxs-lookup"><span data-stu-id="f7aa7-258">PropertyTagGpsSpeed</span></span>

<span data-ttu-id="f7aa7-259">Vitesse du déplacement du récepteur GPS.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-259">Speed of the GPS receiver movement.</span></span>



| <span data-ttu-id="f7aa7-260">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-260">Property info</span></span> | <span data-ttu-id="f7aa7-261">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-261">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-262">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-262">Tag</span></span>   | <span data-ttu-id="f7aa7-263">0x000D</span><span class="sxs-lookup"><span data-stu-id="f7aa7-263">0x000D</span></span>                  |
| <span data-ttu-id="f7aa7-264">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-264">Type</span></span>  | <span data-ttu-id="f7aa7-265">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-265">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-266">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-266">Count</span></span> | <span data-ttu-id="f7aa7-267">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-267">1</span></span>                       |



 

## <a name="propertytaggpstrackref"></a><span data-ttu-id="f7aa7-268">PropertyTagGpsTrackRef</span><span class="sxs-lookup"><span data-stu-id="f7aa7-268">PropertyTagGpsTrackRef</span></span>

<span data-ttu-id="f7aa7-269">Chaîne de caractères se terminant par un caractère null qui spécifie la référence pour donner la direction du mouvement du récepteur GPS.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-269">Null-terminated character string that specifies the reference for giving the direction of GPS receiver movement.</span></span> <span data-ttu-id="f7aa7-270">`T` spécifie la direction réelle et `M` spécifie la direction magnétique.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-270">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="f7aa7-271">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-271">Property info</span></span> | <span data-ttu-id="f7aa7-272">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-272">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="f7aa7-273">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-273">Tag</span></span>   | <span data-ttu-id="f7aa7-274">0x000E</span><span class="sxs-lookup"><span data-stu-id="f7aa7-274">0x000E</span></span>                                     |
| <span data-ttu-id="f7aa7-275">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-275">Type</span></span>  | <span data-ttu-id="f7aa7-276">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-276">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="f7aa7-277">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-277">Count</span></span> | <span data-ttu-id="f7aa7-278">2 (un caractère plus la marque de fin NULL)</span><span class="sxs-lookup"><span data-stu-id="f7aa7-278">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpstrack"></a><span data-ttu-id="f7aa7-279">PropertyTagGpsTrack</span><span class="sxs-lookup"><span data-stu-id="f7aa7-279">PropertyTagGpsTrack</span></span>

<span data-ttu-id="f7aa7-280">Direction du mouvement du récepteur GPS.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-280">Direction of GPS receiver movement.</span></span> <span data-ttu-id="f7aa7-281">La plage de valeurs est comprise entre 0,00 et 359,99.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-281">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="f7aa7-282">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-282">Property info</span></span> | <span data-ttu-id="f7aa7-283">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-283">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-284">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-284">Tag</span></span>   | <span data-ttu-id="f7aa7-285">0x000F</span><span class="sxs-lookup"><span data-stu-id="f7aa7-285">0x000F</span></span>                  |
| <span data-ttu-id="f7aa7-286">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-286">Type</span></span>  | <span data-ttu-id="f7aa7-287">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-287">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-288">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-288">Count</span></span> | <span data-ttu-id="f7aa7-289">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-289">1</span></span>                       |



 

## <a name="propertytaggpsimgdirref"></a><span data-ttu-id="f7aa7-290">PropertyTagGpsImgDirRef</span><span class="sxs-lookup"><span data-stu-id="f7aa7-290">PropertyTagGpsImgDirRef</span></span>

<span data-ttu-id="f7aa7-291">Chaîne de caractères se terminant par un caractère null qui spécifie la référence pour la direction de l’image lorsqu’elle est capturée.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-291">Null-terminated character string that specifies the reference for the direction of the image when it is captured.</span></span> <span data-ttu-id="f7aa7-292">`T` spécifie la direction réelle et `M` spécifie la direction magnétique.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-292">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="f7aa7-293">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-293">Property info</span></span> | <span data-ttu-id="f7aa7-294">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-294">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="f7aa7-295">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-295">Tag</span></span>   | <span data-ttu-id="f7aa7-296">0x0010</span><span class="sxs-lookup"><span data-stu-id="f7aa7-296">0x0010</span></span>                                     |
| <span data-ttu-id="f7aa7-297">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-297">Type</span></span>  | <span data-ttu-id="f7aa7-298">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-298">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="f7aa7-299">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-299">Count</span></span> | <span data-ttu-id="f7aa7-300">2 (un caractère plus la marque de fin NULL)</span><span class="sxs-lookup"><span data-stu-id="f7aa7-300">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsimgdir"></a><span data-ttu-id="f7aa7-301">PropertyTagGpsImgDir</span><span class="sxs-lookup"><span data-stu-id="f7aa7-301">PropertyTagGpsImgDir</span></span>

<span data-ttu-id="f7aa7-302">Direction de l’image lors de sa capture.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-302">Direction of the image when it was captured.</span></span> <span data-ttu-id="f7aa7-303">La plage de valeurs est comprise entre 0,00 et 359,99.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-303">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="f7aa7-304">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-304">Property info</span></span> | <span data-ttu-id="f7aa7-305">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-305">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-306">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-306">Tag</span></span>   | <span data-ttu-id="f7aa7-307">0x0011</span><span class="sxs-lookup"><span data-stu-id="f7aa7-307">0x0011</span></span>                  |
| <span data-ttu-id="f7aa7-308">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-308">Type</span></span>  | <span data-ttu-id="f7aa7-309">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-309">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-310">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-310">Count</span></span> | <span data-ttu-id="f7aa7-311">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-311">1</span></span>                       |



 

## <a name="propertytaggpsmapdatum"></a><span data-ttu-id="f7aa7-312">PropertyTagGpsMapDatum</span><span class="sxs-lookup"><span data-stu-id="f7aa7-312">PropertyTagGpsMapDatum</span></span>

<span data-ttu-id="f7aa7-313">Chaîne de caractères se terminant par un caractère null qui spécifie les données d’enquête géodésique utilisées par le récepteur GPS.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-313">Null-terminated character string that specifies geodetic survey data used by the GPS receiver.</span></span> <span data-ttu-id="f7aa7-314">Si les données de l’enquête sont limitées au Japon, la valeur de cette balise est `TOKYO` ou `WGS-84` .</span><span class="sxs-lookup"><span data-stu-id="f7aa7-314">If the survey data is restricted to Japan, the value of this tag is `TOKYO` or `WGS-84`.</span></span>



| <span data-ttu-id="f7aa7-315">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-315">Property info</span></span> | <span data-ttu-id="f7aa7-316">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-316">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-317">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-317">Tag</span></span>   | <span data-ttu-id="f7aa7-318">0x0012</span><span class="sxs-lookup"><span data-stu-id="f7aa7-318">0x0012</span></span>                                             |
| <span data-ttu-id="f7aa7-319">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-319">Type</span></span>  | <span data-ttu-id="f7aa7-320">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-320">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-321">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-321">Count</span></span> | <span data-ttu-id="f7aa7-322">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-322">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsdestlatref"></a><span data-ttu-id="f7aa7-323">PropertyTagGpsDestLatRef</span><span class="sxs-lookup"><span data-stu-id="f7aa7-323">PropertyTagGpsDestLatRef</span></span>

<span data-ttu-id="f7aa7-324">Chaîne de caractères se terminant par un caractère null qui spécifie si la latitude du point de destination est la latitude nord ou sud.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-324">Null-terminated character string that specifies whether the latitude of the destination point is north or south latitude.</span></span> <span data-ttu-id="f7aa7-325">`N` spécifie la latitude nord et `S` spécifie la latitude sud.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-325">`N` specifies north latitude, and `S` specifies south latitude.</span></span>



| <span data-ttu-id="f7aa7-326">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-326">Property info</span></span> | <span data-ttu-id="f7aa7-327">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-327">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="f7aa7-328">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-328">Tag</span></span>   | <span data-ttu-id="f7aa7-329">0x0013</span><span class="sxs-lookup"><span data-stu-id="f7aa7-329">0x0013</span></span>                                     |
| <span data-ttu-id="f7aa7-330">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-330">Type</span></span>  | <span data-ttu-id="f7aa7-331">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-331">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="f7aa7-332">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-332">Count</span></span> | <span data-ttu-id="f7aa7-333">2 (un caractère plus la marque de fin NULL)</span><span class="sxs-lookup"><span data-stu-id="f7aa7-333">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestlat"></a><span data-ttu-id="f7aa7-334">PropertyTagGpsDestLat</span><span class="sxs-lookup"><span data-stu-id="f7aa7-334">PropertyTagGpsDestLat</span></span>

<span data-ttu-id="f7aa7-335">Latitude du point de destination.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-335">Latitude of the destination point.</span></span> <span data-ttu-id="f7aa7-336">La latitude est exprimée sous la forme de trois valeurs rationnelles donnant respectivement les degrés, les minutes et les secondes.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-336">The latitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="f7aa7-337">Lorsque les degrés, les minutes et les secondes sont exprimés, le format est JJ/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-337">When degrees, minutes, and seconds are expressed, the format is dd/1, mm/1, ss/1.</span></span> <span data-ttu-id="f7aa7-338">Lorsque les degrés et les minutes sont utilisés et, par exemple, les fractions de minutes sont indiquées jusqu’à deux décimales, le format est JJ/1, mmmm/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-338">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is dd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="f7aa7-339">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-339">Property info</span></span> | <span data-ttu-id="f7aa7-340">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-340">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-341">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-341">Tag</span></span>   | <span data-ttu-id="f7aa7-342">0x0014</span><span class="sxs-lookup"><span data-stu-id="f7aa7-342">0x0014</span></span>                  |
| <span data-ttu-id="f7aa7-343">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-343">Type</span></span>  | <span data-ttu-id="f7aa7-344">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-344">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-345">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-345">Count</span></span> | <span data-ttu-id="f7aa7-346">3</span><span class="sxs-lookup"><span data-stu-id="f7aa7-346">3</span></span>                       |



 

## <a name="propertytaggpsdestlongref"></a><span data-ttu-id="f7aa7-347">PropertyTagGpsDestLongRef</span><span class="sxs-lookup"><span data-stu-id="f7aa7-347">PropertyTagGpsDestLongRef</span></span>

<span data-ttu-id="f7aa7-348">Chaîne de caractères terminée par le caractère null qui spécifie si la longitude du point de destination est l’est ou la longitude ouest.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-348">Null-terminated character string that specifies whether the longitude of the destination point is east or west longitude.</span></span> <span data-ttu-id="f7aa7-349">`E` spécifie la longitude est et `W` spécifie la longitude ouest.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-349">`E` specifies east longitude, and `W` specifies west longitude.</span></span>



| <span data-ttu-id="f7aa7-350">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-350">Property info</span></span> | <span data-ttu-id="f7aa7-351">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-351">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="f7aa7-352">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-352">Tag</span></span>   | <span data-ttu-id="f7aa7-353">0x0015</span><span class="sxs-lookup"><span data-stu-id="f7aa7-353">0x0015</span></span>                                     |
| <span data-ttu-id="f7aa7-354">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-354">Type</span></span>  | <span data-ttu-id="f7aa7-355">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-355">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="f7aa7-356">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-356">Count</span></span> | <span data-ttu-id="f7aa7-357">2 (un caractère plus la marque de fin NULL)</span><span class="sxs-lookup"><span data-stu-id="f7aa7-357">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestlong"></a><span data-ttu-id="f7aa7-358">PropertyTagGpsDestLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-358">PropertyTagGpsDestLong</span></span>

<span data-ttu-id="f7aa7-359">Longitude du point de destination.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-359">Longitude of the destination point.</span></span> <span data-ttu-id="f7aa7-360">La longitude est exprimée sous la forme de trois valeurs rationnelles accordant respectivement les degrés, les minutes et les secondes.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-360">The longitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="f7aa7-361">Lorsque les degrés, les minutes et les secondes sont exprimés, le format est DDD/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-361">When degrees, minutes, and seconds are expressed, the format is ddd/1, mm/1, ss/1.</span></span> <span data-ttu-id="f7aa7-362">Lorsque les degrés et les minutes sont utilisés et, par exemple, les fractions de minutes sont indiquées jusqu’à deux décimales, le format est DDD/1, mmmm/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-362">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is ddd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="f7aa7-363">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-363">Property info</span></span> | <span data-ttu-id="f7aa7-364">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-364">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-365">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-365">Tag</span></span>   | <span data-ttu-id="f7aa7-366">0x0016</span><span class="sxs-lookup"><span data-stu-id="f7aa7-366">0x0016</span></span>                  |
| <span data-ttu-id="f7aa7-367">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-367">Type</span></span>  | <span data-ttu-id="f7aa7-368">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-368">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-369">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-369">Count</span></span> | <span data-ttu-id="f7aa7-370">3</span><span class="sxs-lookup"><span data-stu-id="f7aa7-370">3</span></span>                       |



 

## <a name="propertytaggpsdestbearref"></a><span data-ttu-id="f7aa7-371">PropertyTagGpsDestBearRef</span><span class="sxs-lookup"><span data-stu-id="f7aa7-371">PropertyTagGpsDestBearRef</span></span>

<span data-ttu-id="f7aa7-372">Chaîne de caractères se terminant par un caractère null qui spécifie la référence utilisée pour donner le palier au point de destination.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-372">Null-terminated character string that specifies the reference used for giving the bearing to the destination point.</span></span> <span data-ttu-id="f7aa7-373">`T` spécifie la direction réelle et `M` spécifie la direction magnétique.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-373">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="f7aa7-374">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-374">Property info</span></span> | <span data-ttu-id="f7aa7-375">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-375">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="f7aa7-376">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-376">Tag</span></span>   | <span data-ttu-id="f7aa7-377">0x0017</span><span class="sxs-lookup"><span data-stu-id="f7aa7-377">0x0017</span></span>                                     |
| <span data-ttu-id="f7aa7-378">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-378">Type</span></span>  | <span data-ttu-id="f7aa7-379">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-379">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="f7aa7-380">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-380">Count</span></span> | <span data-ttu-id="f7aa7-381">2 (un caractère plus la marque de fin NULL)</span><span class="sxs-lookup"><span data-stu-id="f7aa7-381">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestbear"></a><span data-ttu-id="f7aa7-382">PropertyTagGpsDestBear</span><span class="sxs-lookup"><span data-stu-id="f7aa7-382">PropertyTagGpsDestBear</span></span>

<span data-ttu-id="f7aa7-383">Palier au point de destination.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-383">Bearing to the destination point.</span></span> <span data-ttu-id="f7aa7-384">La plage de valeurs est comprise entre 0,00 et 359,99.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-384">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="f7aa7-385">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-385">Property info</span></span> | <span data-ttu-id="f7aa7-386">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-386">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-387">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-387">Tag</span></span>   | <span data-ttu-id="f7aa7-388">0x0018</span><span class="sxs-lookup"><span data-stu-id="f7aa7-388">0x0018</span></span>                  |
| <span data-ttu-id="f7aa7-389">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-389">Type</span></span>  | <span data-ttu-id="f7aa7-390">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-390">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-391">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-391">Count</span></span> | <span data-ttu-id="f7aa7-392">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-392">1</span></span>                       |



 

## <a name="propertytaggpsdestdistref"></a><span data-ttu-id="f7aa7-393">PropertyTagGpsDestDistRef</span><span class="sxs-lookup"><span data-stu-id="f7aa7-393">PropertyTagGpsDestDistRef</span></span>

<span data-ttu-id="f7aa7-394">Chaîne de caractères se terminant par un caractère null qui spécifie l’unité utilisée pour exprimer la distance au point de destination.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-394">Null-terminated character string that specifies the unit used to express the distance to the destination point.</span></span> <span data-ttu-id="f7aa7-395">K, M et N représentent les kilomètres, les miles et les nœuds, respectivement.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-395">K, M, and N represent kilometers, miles, and knots respectively.</span></span>



| <span data-ttu-id="f7aa7-396">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-396">Property info</span></span> | <span data-ttu-id="f7aa7-397">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-397">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="f7aa7-398">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-398">Tag</span></span>   | <span data-ttu-id="f7aa7-399">0x0019</span><span class="sxs-lookup"><span data-stu-id="f7aa7-399">0x0019</span></span>                                     |
| <span data-ttu-id="f7aa7-400">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-400">Type</span></span>  | <span data-ttu-id="f7aa7-401">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-401">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="f7aa7-402">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-402">Count</span></span> | <span data-ttu-id="f7aa7-403">2 (un caractère plus la marque de fin NULL)</span><span class="sxs-lookup"><span data-stu-id="f7aa7-403">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestdist"></a><span data-ttu-id="f7aa7-404">PropertyTagGpsDestDist</span><span class="sxs-lookup"><span data-stu-id="f7aa7-404">PropertyTagGpsDestDist</span></span>

<span data-ttu-id="f7aa7-405">Distance au point de destination.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-405">Distance to the destination point.</span></span>



| <span data-ttu-id="f7aa7-406">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-406">Property info</span></span> | <span data-ttu-id="f7aa7-407">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-407">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-408">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-408">Tag</span></span>   | <span data-ttu-id="f7aa7-409">0x001A</span><span class="sxs-lookup"><span data-stu-id="f7aa7-409">0x001A</span></span>                  |
| <span data-ttu-id="f7aa7-410">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-410">Type</span></span>  | <span data-ttu-id="f7aa7-411">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-411">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-412">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-412">Count</span></span> | <span data-ttu-id="f7aa7-413">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-413">1</span></span>                       |



 

## <a name="propertytagnewsubfiletype"></a><span data-ttu-id="f7aa7-414">PropertyTagNewSubfileType</span><span class="sxs-lookup"><span data-stu-id="f7aa7-414">PropertyTagNewSubfileType</span></span>

<span data-ttu-id="f7aa7-415">Type de données dans un sous-fichier.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-415">Type of data in a subfile.</span></span>



| <span data-ttu-id="f7aa7-416">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-416">Property info</span></span> | <span data-ttu-id="f7aa7-417">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-417">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-418">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-418">Tag</span></span>   | <span data-ttu-id="f7aa7-419">0x00FE</span><span class="sxs-lookup"><span data-stu-id="f7aa7-419">0x00FE</span></span>              |
| <span data-ttu-id="f7aa7-420">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-420">Type</span></span>  | <span data-ttu-id="f7aa7-421">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-421">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-422">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-422">Count</span></span> | <span data-ttu-id="f7aa7-423">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-423">1</span></span>                   |



 

## <a name="propertytagsubfiletype"></a><span data-ttu-id="f7aa7-424">PropertyTagSubfileType</span><span class="sxs-lookup"><span data-stu-id="f7aa7-424">PropertyTagSubfileType</span></span>

<span data-ttu-id="f7aa7-425">Type de données dans un sous-fichier.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-425">Type of data in a subfile.</span></span>



| <span data-ttu-id="f7aa7-426">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-426">Property info</span></span> | <span data-ttu-id="f7aa7-427">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-427">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-428">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-428">Tag</span></span>   | <span data-ttu-id="f7aa7-429">0x00FF</span><span class="sxs-lookup"><span data-stu-id="f7aa7-429">0x00FF</span></span>               |
| <span data-ttu-id="f7aa7-430">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-430">Type</span></span>  | <span data-ttu-id="f7aa7-431">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-431">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-432">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-432">Count</span></span> | <span data-ttu-id="f7aa7-433">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-433">1</span></span>                    |



 

## <a name="propertytagimagewidth"></a><span data-ttu-id="f7aa7-434">PropertyTagImageWidth</span><span class="sxs-lookup"><span data-stu-id="f7aa7-434">PropertyTagImageWidth</span></span>

<span data-ttu-id="f7aa7-435">Nombre de pixels par ligne.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-435">Number of pixels per row.</span></span>



| <span data-ttu-id="f7aa7-436">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-436">Property info</span></span> | <span data-ttu-id="f7aa7-437">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-437">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="f7aa7-438">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-438">Tag</span></span>   | <span data-ttu-id="f7aa7-439">0x0100</span><span class="sxs-lookup"><span data-stu-id="f7aa7-439">0x0100</span></span>                                      |
| <span data-ttu-id="f7aa7-440">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-440">Type</span></span>  | <span data-ttu-id="f7aa7-441">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-441">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-442">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-442">Count</span></span> | <span data-ttu-id="f7aa7-443">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-443">1</span></span>                                           |



 

## <a name="propertytagimageheight"></a><span data-ttu-id="f7aa7-444">PropertyTagImageHeight</span><span class="sxs-lookup"><span data-stu-id="f7aa7-444">PropertyTagImageHeight</span></span>

<span data-ttu-id="f7aa7-445">Nombre de lignes de pixels.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-445">Number of pixel rows.</span></span>



| <span data-ttu-id="f7aa7-446">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-446">Property info</span></span> | <span data-ttu-id="f7aa7-447">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-447">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="f7aa7-448">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-448">Tag</span></span>   | <span data-ttu-id="f7aa7-449">0x0101</span><span class="sxs-lookup"><span data-stu-id="f7aa7-449">0x0101</span></span>                                      |
| <span data-ttu-id="f7aa7-450">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-450">Type</span></span>  | <span data-ttu-id="f7aa7-451">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-451">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-452">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-452">Count</span></span> | <span data-ttu-id="f7aa7-453">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-453">1</span></span>                                           |



 

## <a name="propertytagbitspersample"></a><span data-ttu-id="f7aa7-454">PropertyTagBitsPerSample</span><span class="sxs-lookup"><span data-stu-id="f7aa7-454">PropertyTagBitsPerSample</span></span>

<span data-ttu-id="f7aa7-455">Nombre de bits par composant de couleur.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-455">Number of bits per color component.</span></span> <span data-ttu-id="f7aa7-456">Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-456">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="f7aa7-457">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-457">Property info</span></span> | <span data-ttu-id="f7aa7-458">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-458">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="f7aa7-459">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-459">Tag</span></span>   | <span data-ttu-id="f7aa7-460">0x0102</span><span class="sxs-lookup"><span data-stu-id="f7aa7-460">0x0102</span></span>                                   |
| <span data-ttu-id="f7aa7-461">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-461">Type</span></span>  | <span data-ttu-id="f7aa7-462">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-462">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="f7aa7-463">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-463">Count</span></span> | <span data-ttu-id="f7aa7-464">Nombre d’échantillons (composants) par pixel</span><span class="sxs-lookup"><span data-stu-id="f7aa7-464">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagcompression"></a><span data-ttu-id="f7aa7-465">PropertyTagCompression</span><span class="sxs-lookup"><span data-stu-id="f7aa7-465">PropertyTagCompression</span></span>

<span data-ttu-id="f7aa7-466">Schéma de compression utilisé pour les données de l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-466">Compression scheme used for the image data.</span></span>



| <span data-ttu-id="f7aa7-467">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-467">Property info</span></span> | <span data-ttu-id="f7aa7-468">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-468">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-469">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-469">Tag</span></span>   | <span data-ttu-id="f7aa7-470">0x0103</span><span class="sxs-lookup"><span data-stu-id="f7aa7-470">0x0103</span></span>               |
| <span data-ttu-id="f7aa7-471">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-471">Type</span></span>  | <span data-ttu-id="f7aa7-472">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-472">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-473">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-473">Count</span></span> | <span data-ttu-id="f7aa7-474">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-474">1</span></span>                    |



 

## <a name="propertytagphotometricinterp"></a><span data-ttu-id="f7aa7-475">PropertyTagPhotometricInterp</span><span class="sxs-lookup"><span data-stu-id="f7aa7-475">PropertyTagPhotometricInterp</span></span>

<span data-ttu-id="f7aa7-476">Comment les données de pixels seront interprétées.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-476">How pixel data will be interpreted.</span></span>



| <span data-ttu-id="f7aa7-477">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-477">Property info</span></span> | <span data-ttu-id="f7aa7-478">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-478">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-479">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-479">Tag</span></span>   | <span data-ttu-id="f7aa7-480">0x0106</span><span class="sxs-lookup"><span data-stu-id="f7aa7-480">0x0106</span></span>               |
| <span data-ttu-id="f7aa7-481">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-481">Type</span></span>  | <span data-ttu-id="f7aa7-482">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-482">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-483">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-483">Count</span></span> | <span data-ttu-id="f7aa7-484">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-484">1</span></span>                    |



 

## <a name="propertytagthreshholding"></a><span data-ttu-id="f7aa7-485">PropertyTagThreshHolding</span><span class="sxs-lookup"><span data-stu-id="f7aa7-485">PropertyTagThreshHolding</span></span>

<span data-ttu-id="f7aa7-486">Technique utilisée pour convertir des pixels gris en pixels noirs et blancs.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-486">Technique used to convert from gray pixels to black and white pixels.</span></span>



| <span data-ttu-id="f7aa7-487">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-487">Property info</span></span> | <span data-ttu-id="f7aa7-488">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-488">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-489">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-489">Tag</span></span>   | <span data-ttu-id="f7aa7-490">0x0107</span><span class="sxs-lookup"><span data-stu-id="f7aa7-490">0x0107</span></span>               |
| <span data-ttu-id="f7aa7-491">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-491">Type</span></span>  | <span data-ttu-id="f7aa7-492">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-492">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-493">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-493">Count</span></span> | <span data-ttu-id="f7aa7-494">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-494">1</span></span>                    |



 

## <a name="propertytagcellwidth"></a><span data-ttu-id="f7aa7-495">PropertyTagCellWidth</span><span class="sxs-lookup"><span data-stu-id="f7aa7-495">PropertyTagCellWidth</span></span>

<span data-ttu-id="f7aa7-496">Largeur de la matrice de trame ou de trame.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-496">Width of the dithering or halftoning matrix.</span></span>



| <span data-ttu-id="f7aa7-497">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-497">Property info</span></span> | <span data-ttu-id="f7aa7-498">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-498">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-499">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-499">Tag</span></span>   | <span data-ttu-id="f7aa7-500">0x0108</span><span class="sxs-lookup"><span data-stu-id="f7aa7-500">0x0108</span></span>               |
| <span data-ttu-id="f7aa7-501">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-501">Type</span></span>  | <span data-ttu-id="f7aa7-502">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-502">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-503">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-503">Count</span></span> | <span data-ttu-id="f7aa7-504">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-504">1</span></span>                    |



 

## <a name="propertytagcellheight"></a><span data-ttu-id="f7aa7-505">PropertyTagCellHeight</span><span class="sxs-lookup"><span data-stu-id="f7aa7-505">PropertyTagCellHeight</span></span>

<span data-ttu-id="f7aa7-506">Hauteur de la matrice de tramage ou de simili.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-506">Height of the dithering or halftoning matrix.</span></span>



| <span data-ttu-id="f7aa7-507">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-507">Property info</span></span> | <span data-ttu-id="f7aa7-508">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-508">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-509">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-509">Tag</span></span>   | <span data-ttu-id="f7aa7-510">0x0109</span><span class="sxs-lookup"><span data-stu-id="f7aa7-510">0x0109</span></span>               |
| <span data-ttu-id="f7aa7-511">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-511">Type</span></span>  | <span data-ttu-id="f7aa7-512">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-512">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-513">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-513">Count</span></span> | <span data-ttu-id="f7aa7-514">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-514">1</span></span>                    |



 

## <a name="propertytagfillorder"></a><span data-ttu-id="f7aa7-515">PropertyTagFillOrder</span><span class="sxs-lookup"><span data-stu-id="f7aa7-515">PropertyTagFillOrder</span></span>

<span data-ttu-id="f7aa7-516">Ordre logique des bits dans un octet.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-516">Logical order of bits in a byte.</span></span>



| <span data-ttu-id="f7aa7-517">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-517">Property info</span></span> | <span data-ttu-id="f7aa7-518">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-518">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-519">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-519">Tag</span></span>   | <span data-ttu-id="f7aa7-520">0x010A</span><span class="sxs-lookup"><span data-stu-id="f7aa7-520">0x010A</span></span>               |
| <span data-ttu-id="f7aa7-521">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-521">Type</span></span>  | <span data-ttu-id="f7aa7-522">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-522">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-523">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-523">Count</span></span> | <span data-ttu-id="f7aa7-524">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-524">1</span></span>                    |



 

## <a name="propertytagdocumentname"></a><span data-ttu-id="f7aa7-525">PropertyTagDocumentName</span><span class="sxs-lookup"><span data-stu-id="f7aa7-525">PropertyTagDocumentName</span></span>

<span data-ttu-id="f7aa7-526">Chaîne de caractères se terminant par un caractère null qui spécifie le nom du document à partir duquel l’image a été analysée.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-526">Null-terminated character string that specifies the name of the document from which the image was scanned.</span></span>



| <span data-ttu-id="f7aa7-527">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-527">Property info</span></span> | <span data-ttu-id="f7aa7-528">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-528">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-529">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-529">Tag</span></span>   | <span data-ttu-id="f7aa7-530">0x010D</span><span class="sxs-lookup"><span data-stu-id="f7aa7-530">0x010D</span></span>                                             |
| <span data-ttu-id="f7aa7-531">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-531">Type</span></span>  | <span data-ttu-id="f7aa7-532">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-532">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-533">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-533">Count</span></span> | <span data-ttu-id="f7aa7-534">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-534">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagimagedescription"></a><span data-ttu-id="f7aa7-535">PropertyTagImageDescription</span><span class="sxs-lookup"><span data-stu-id="f7aa7-535">PropertyTagImageDescription</span></span>

<span data-ttu-id="f7aa7-536">Chaîne de caractères se terminant par un caractère null qui spécifie le titre de l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-536">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="f7aa7-537">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-537">Property info</span></span> | <span data-ttu-id="f7aa7-538">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-538">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-539">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-539">Tag</span></span>   | <span data-ttu-id="f7aa7-540">0x010E</span><span class="sxs-lookup"><span data-stu-id="f7aa7-540">0x010E</span></span>                                             |
| <span data-ttu-id="f7aa7-541">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-541">Type</span></span>  | <span data-ttu-id="f7aa7-542">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-542">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-543">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-543">Count</span></span> | <span data-ttu-id="f7aa7-544">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-544">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagequipmake"></a><span data-ttu-id="f7aa7-545">PropertyTagEquipMake</span><span class="sxs-lookup"><span data-stu-id="f7aa7-545">PropertyTagEquipMake</span></span>

<span data-ttu-id="f7aa7-546">Chaîne de caractères se terminant par un caractère null qui spécifie le fabricant de l’équipement utilisé pour enregistrer l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-546">Null-terminated character string that specifies the manufacturer of the equipment used to record the image.</span></span>



| <span data-ttu-id="f7aa7-547">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-547">Property info</span></span> | <span data-ttu-id="f7aa7-548">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-548">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-549">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-549">Tag</span></span>   | <span data-ttu-id="f7aa7-550">0x010F</span><span class="sxs-lookup"><span data-stu-id="f7aa7-550">0x010F</span></span>                                             |
| <span data-ttu-id="f7aa7-551">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-551">Type</span></span>  | <span data-ttu-id="f7aa7-552">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-552">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-553">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-553">Count</span></span> | <span data-ttu-id="f7aa7-554">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-554">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagequipmodel"></a><span data-ttu-id="f7aa7-555">PropertyTagEquipModel</span><span class="sxs-lookup"><span data-stu-id="f7aa7-555">PropertyTagEquipModel</span></span>

<span data-ttu-id="f7aa7-556">Chaîne de caractères se terminant par un caractère null qui spécifie le nom du modèle ou le numéro de modèle de l’équipement utilisé pour enregistrer l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-556">Null-terminated character string that specifies the model name or model number of the equipment used to record the image.</span></span>



| <span data-ttu-id="f7aa7-557">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-557">Property info</span></span> | <span data-ttu-id="f7aa7-558">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-558">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-559">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-559">Tag</span></span>   | <span data-ttu-id="f7aa7-560">0x0110</span><span class="sxs-lookup"><span data-stu-id="f7aa7-560">0x0110</span></span>                                             |
| <span data-ttu-id="f7aa7-561">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-561">Type</span></span>  | <span data-ttu-id="f7aa7-562">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-562">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-563">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-563">Count</span></span> | <span data-ttu-id="f7aa7-564">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-564">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagstripoffsets"></a><span data-ttu-id="f7aa7-565">PropertyTagStripOffsets</span><span class="sxs-lookup"><span data-stu-id="f7aa7-565">PropertyTagStripOffsets</span></span>

<span data-ttu-id="f7aa7-566">Pour chaque bande, le décalage d’octet de cette bande.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-566">For each strip, the byte offset of that strip.</span></span> <span data-ttu-id="f7aa7-567">Voir aussi [PropertyTagRowsPerStrip](#propertytagrowsperstrip) et [PropertyTagStripBytesCount](#propertytagstripbytescount).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-567">See also [PropertyTagRowsPerStrip](#propertytagrowsperstrip) and [PropertyTagStripBytesCount](#propertytagstripbytescount).</span></span>



| <span data-ttu-id="f7aa7-568">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-568">Property info</span></span> | <span data-ttu-id="f7aa7-569">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-569">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="f7aa7-570">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-570">Tag</span></span>   | <span data-ttu-id="f7aa7-571">0x0111</span><span class="sxs-lookup"><span data-stu-id="f7aa7-571">0x0111</span></span>                                      |
| <span data-ttu-id="f7aa7-572">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-572">Type</span></span>  | <span data-ttu-id="f7aa7-573">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-573">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-574">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-574">Count</span></span> | <span data-ttu-id="f7aa7-575">Nombre de bandes</span><span class="sxs-lookup"><span data-stu-id="f7aa7-575">Number of strips</span></span>                            |



 

## <a name="propertytagorientation"></a><span data-ttu-id="f7aa7-576">PropertyTagOrientation</span><span class="sxs-lookup"><span data-stu-id="f7aa7-576">PropertyTagOrientation</span></span>

<span data-ttu-id="f7aa7-577">Orientation de l’image affichée en termes de lignes et de colonnes.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-577">Image orientation viewed in terms of rows and columns.</span></span>



<span data-ttu-id="f7aa7-578">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-578">Tag</span></span>

<span data-ttu-id="f7aa7-579">0x0112</span><span class="sxs-lookup"><span data-stu-id="f7aa7-579">0x0112</span></span>

<span data-ttu-id="f7aa7-580">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-580">Type</span></span>

<span data-ttu-id="f7aa7-581">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-581">PropertyTagTypeShort</span></span>

<span data-ttu-id="f7aa7-582">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-582">Count</span></span>

<span data-ttu-id="f7aa7-583">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-583">1</span></span>

<span data-ttu-id="f7aa7-584">1-la ligne 0 est en haut de l’image visuelle et la colonne 0 est le côté gauche du visuel.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-584">1 - The 0th row is at the top of the visual image, and the 0th column is the visual left side.</span></span> <span data-ttu-id="f7aa7-585">2-la ligne 0 est en haut de l’image et la colonne 0 est le côté droit visuel.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-585">2 - The 0th row is at the visual top of the image, and the 0th column is the visual right side.</span></span> <span data-ttu-id="f7aa7-586">3-la ligne 0 est au bas du visuel de l’image et la colonne 0 est le côté droit visuel.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-586">3 - The 0th row is at the visual bottom of the image, and the 0th column is the visual right side.</span></span> <span data-ttu-id="f7aa7-587">4-la ligne 0 est au bas du visuel de l’image et la colonne 0 est le côté gauche du visuel.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-587">4 - The 0th row is at the visual bottom of the image, and the 0th column is the visual left side.</span></span> <span data-ttu-id="f7aa7-588">5-la ligne 0 est le côté gauche de l’image et la colonne 0 est la partie supérieure du visuel.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-588">5 - The 0th row is the visual left side of the image, and the 0th column is the visual top.</span></span> <span data-ttu-id="f7aa7-589">6-la ligne 0 est le côté droit de l’image et la colonne 0 est la partie supérieure du visuel.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-589">6 - The 0th row is the visual right side of the image, and the 0th column is the visual top.</span></span> <span data-ttu-id="f7aa7-590">7-la ligne 0 est le côté droit de l’image et la colonne 0 est le bas du visuel.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-590">7 - The 0th row is the visual right side of the image, and the 0th column is the visual bottom.</span></span> <span data-ttu-id="f7aa7-591">8-la ligne 0 est le côté gauche de l’image et la colonne 0 est le bas du visuel.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-591">8 - The 0th row is the visual left side of the image, and the 0th column is the visual bottom.</span></span>



 

## <a name="propertytagsamplesperpixel"></a><span data-ttu-id="f7aa7-592">PropertyTagSamplesPerPixel</span><span class="sxs-lookup"><span data-stu-id="f7aa7-592">PropertyTagSamplesPerPixel</span></span>

<span data-ttu-id="f7aa7-593">Nombre de composants de couleur par pixel.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-593">Number of color components per pixel.</span></span>



| <span data-ttu-id="f7aa7-594">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-594">Property info</span></span> | <span data-ttu-id="f7aa7-595">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-595">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-596">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-596">Tag</span></span>   | <span data-ttu-id="f7aa7-597">0x0115</span><span class="sxs-lookup"><span data-stu-id="f7aa7-597">0x0115</span></span>               |
| <span data-ttu-id="f7aa7-598">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-598">Type</span></span>  | <span data-ttu-id="f7aa7-599">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-599">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-600">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-600">Count</span></span> | <span data-ttu-id="f7aa7-601">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-601">1</span></span>                    |



 

## <a name="propertytagrowsperstrip"></a><span data-ttu-id="f7aa7-602">PropertyTagRowsPerStrip</span><span class="sxs-lookup"><span data-stu-id="f7aa7-602">PropertyTagRowsPerStrip</span></span>

<span data-ttu-id="f7aa7-603">Nombre de lignes par bande.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-603">Number of rows per strip.</span></span> <span data-ttu-id="f7aa7-604">Voir aussi [PropertyTagStripBytesCount](#propertytagstripbytescount) et [PropertyTagStripOffsets](#propertytagstripoffsets).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-604">See also [PropertyTagStripBytesCount](#propertytagstripbytescount) and [PropertyTagStripOffsets](#propertytagstripoffsets).</span></span>



| <span data-ttu-id="f7aa7-605">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-605">Property info</span></span> | <span data-ttu-id="f7aa7-606">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-606">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="f7aa7-607">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-607">Tag</span></span>   | <span data-ttu-id="f7aa7-608">0x0116</span><span class="sxs-lookup"><span data-stu-id="f7aa7-608">0x0116</span></span>                                      |
| <span data-ttu-id="f7aa7-609">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-609">Type</span></span>  | <span data-ttu-id="f7aa7-610">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-610">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-611">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-611">Count</span></span> | <span data-ttu-id="f7aa7-612">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-612">1</span></span>                                           |



 

## <a name="propertytagstripbytescount"></a><span data-ttu-id="f7aa7-613">PropertyTagStripBytesCount</span><span class="sxs-lookup"><span data-stu-id="f7aa7-613">PropertyTagStripBytesCount</span></span>

<span data-ttu-id="f7aa7-614">Pour chaque bande, nombre total d’octets dans cette bande.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-614">For each strip, the total number of bytes in that strip.</span></span>



| <span data-ttu-id="f7aa7-615">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-615">Property info</span></span> | <span data-ttu-id="f7aa7-616">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-616">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="f7aa7-617">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-617">Tag</span></span>   | <span data-ttu-id="f7aa7-618">0x0117</span><span class="sxs-lookup"><span data-stu-id="f7aa7-618">0x0117</span></span>                                      |
| <span data-ttu-id="f7aa7-619">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-619">Type</span></span>  | <span data-ttu-id="f7aa7-620">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-620">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-621">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-621">Count</span></span> | <span data-ttu-id="f7aa7-622">Nombre de bandes</span><span class="sxs-lookup"><span data-stu-id="f7aa7-622">Number of strips</span></span>                            |



 

## <a name="propertytagminsamplevalue"></a><span data-ttu-id="f7aa7-623">PropertyTagMinSampleValue</span><span class="sxs-lookup"><span data-stu-id="f7aa7-623">PropertyTagMinSampleValue</span></span>

<span data-ttu-id="f7aa7-624">Pour chaque composant de couleur, valeur minimale assignée à ce composant.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-624">For each color component, the minimum value assigned to that component.</span></span> <span data-ttu-id="f7aa7-625">Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-625">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="f7aa7-626">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-626">Property info</span></span> | <span data-ttu-id="f7aa7-627">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-627">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="f7aa7-628">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-628">Tag</span></span>   | <span data-ttu-id="f7aa7-629">0x0118</span><span class="sxs-lookup"><span data-stu-id="f7aa7-629">0x0118</span></span>                                   |
| <span data-ttu-id="f7aa7-630">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-630">Type</span></span>  | <span data-ttu-id="f7aa7-631">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-631">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="f7aa7-632">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-632">Count</span></span> | <span data-ttu-id="f7aa7-633">Nombre d’échantillons (composants) par pixel</span><span class="sxs-lookup"><span data-stu-id="f7aa7-633">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagmaxsamplevalue"></a><span data-ttu-id="f7aa7-634">PropertyTagMaxSampleValue</span><span class="sxs-lookup"><span data-stu-id="f7aa7-634">PropertyTagMaxSampleValue</span></span>

<span data-ttu-id="f7aa7-635">Pour chaque composant de couleur, valeur maximale affectée à ce composant.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-635">For each color component, the maximum value assigned to that component.</span></span> <span data-ttu-id="f7aa7-636">Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-636">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="f7aa7-637">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-637">Property info</span></span> | <span data-ttu-id="f7aa7-638">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-638">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="f7aa7-639">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-639">Tag</span></span>   | <span data-ttu-id="f7aa7-640">0x0119</span><span class="sxs-lookup"><span data-stu-id="f7aa7-640">0x0119</span></span>                                   |
| <span data-ttu-id="f7aa7-641">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-641">Type</span></span>  | <span data-ttu-id="f7aa7-642">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-642">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="f7aa7-643">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-643">Count</span></span> | <span data-ttu-id="f7aa7-644">Nombre d’échantillons (composants) par pixel</span><span class="sxs-lookup"><span data-stu-id="f7aa7-644">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagxresolution"></a><span data-ttu-id="f7aa7-645">PropertyTagXResolution</span><span class="sxs-lookup"><span data-stu-id="f7aa7-645">PropertyTagXResolution</span></span>

<span data-ttu-id="f7aa7-646">Nombre de pixels par unité dans la direction de la largeur de l’image (x).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-646">Number of pixels per unit in the image width (x) direction.</span></span> <span data-ttu-id="f7aa7-647">L’unité est spécifiée par [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-647">The unit is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="f7aa7-648">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-648">Property info</span></span> | <span data-ttu-id="f7aa7-649">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-649">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-650">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-650">Tag</span></span>   | <span data-ttu-id="f7aa7-651">0x011A</span><span class="sxs-lookup"><span data-stu-id="f7aa7-651">0x011A</span></span>                  |
| <span data-ttu-id="f7aa7-652">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-652">Type</span></span>  | <span data-ttu-id="f7aa7-653">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-653">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-654">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-654">Count</span></span> | <span data-ttu-id="f7aa7-655">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-655">1</span></span>                       |



 

## <a name="propertytagyresolution"></a><span data-ttu-id="f7aa7-656">PropertyTagYResolution</span><span class="sxs-lookup"><span data-stu-id="f7aa7-656">PropertyTagYResolution</span></span>

<span data-ttu-id="f7aa7-657">Nombre de pixels par unité dans la direction de la hauteur d’image (y).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-657">Number of pixels per unit in the image height (y) direction.</span></span> <span data-ttu-id="f7aa7-658">L’unité est spécifiée par [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-658">The unit is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="f7aa7-659">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-659">Property info</span></span> | <span data-ttu-id="f7aa7-660">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-660">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-661">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-661">Tag</span></span>   | <span data-ttu-id="f7aa7-662">0x011B</span><span class="sxs-lookup"><span data-stu-id="f7aa7-662">0x011B</span></span>                  |
| <span data-ttu-id="f7aa7-663">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-663">Type</span></span>  | <span data-ttu-id="f7aa7-664">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-664">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-665">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-665">Count</span></span> | <span data-ttu-id="f7aa7-666">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-666">1</span></span>                       |



 

## <a name="propertytagplanarconfig"></a><span data-ttu-id="f7aa7-667">PropertyTagPlanarConfig</span><span class="sxs-lookup"><span data-stu-id="f7aa7-667">PropertyTagPlanarConfig</span></span>

<span data-ttu-id="f7aa7-668">Si les composants de pixel sont enregistrés au format de forme groupée ou planaire.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-668">Whether pixel components are recorded in chunky or planar format.</span></span>



| <span data-ttu-id="f7aa7-669">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-669">Property info</span></span> | <span data-ttu-id="f7aa7-670">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-670">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-671">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-671">Tag</span></span>   | <span data-ttu-id="f7aa7-672">0x011C</span><span class="sxs-lookup"><span data-stu-id="f7aa7-672">0x011C</span></span>               |
| <span data-ttu-id="f7aa7-673">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-673">Type</span></span>  | <span data-ttu-id="f7aa7-674">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-674">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-675">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-675">Count</span></span> | <span data-ttu-id="f7aa7-676">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-676">1</span></span>                    |



 

## <a name="propertytagpagename"></a><span data-ttu-id="f7aa7-677">PropertyTagPageName</span><span class="sxs-lookup"><span data-stu-id="f7aa7-677">PropertyTagPageName</span></span>

<span data-ttu-id="f7aa7-678">Chaîne de caractères se terminant par un caractère null qui spécifie le nom de la page à partir de laquelle l’image a été analysée.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-678">Null-terminated character string that specifies the name of the page from which the image was scanned.</span></span>



| <span data-ttu-id="f7aa7-679">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-679">Property info</span></span> | <span data-ttu-id="f7aa7-680">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-680">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-681">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-681">Tag</span></span>   | <span data-ttu-id="f7aa7-682">0x011D</span><span class="sxs-lookup"><span data-stu-id="f7aa7-682">0x011D</span></span>                                             |
| <span data-ttu-id="f7aa7-683">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-683">Type</span></span>  | <span data-ttu-id="f7aa7-684">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-684">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-685">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-685">Count</span></span> | <span data-ttu-id="f7aa7-686">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-686">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagxposition"></a><span data-ttu-id="f7aa7-687">PropertyTagXPosition</span><span class="sxs-lookup"><span data-stu-id="f7aa7-687">PropertyTagXPosition</span></span>

<span data-ttu-id="f7aa7-688">Décalage du côté gauche de la page vers le côté gauche de l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-688">Offset from the left side of the page to the left side of the image.</span></span> <span data-ttu-id="f7aa7-689">L’unité de mesure est spécifiée par [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-689">The unit of measure is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="f7aa7-690">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-690">Property info</span></span> | <span data-ttu-id="f7aa7-691">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-691">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-692">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-692">Tag</span></span>   | <span data-ttu-id="f7aa7-693">0x011E</span><span class="sxs-lookup"><span data-stu-id="f7aa7-693">0x011E</span></span>                  |
| <span data-ttu-id="f7aa7-694">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-694">Type</span></span>  | <span data-ttu-id="f7aa7-695">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-695">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-696">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-696">Count</span></span> | <span data-ttu-id="f7aa7-697">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-697">1</span></span>                       |



 

## <a name="propertytagyposition"></a><span data-ttu-id="f7aa7-698">PropertyTagYPosition</span><span class="sxs-lookup"><span data-stu-id="f7aa7-698">PropertyTagYPosition</span></span>

<span data-ttu-id="f7aa7-699">Décalage à partir du haut de la page vers le haut de l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-699">Offset from the top of the page to the top of the image.</span></span> <span data-ttu-id="f7aa7-700">L’unité de mesure est spécifiée par [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-700">The unit of measure is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="f7aa7-701">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-701">Property info</span></span> | <span data-ttu-id="f7aa7-702">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-702">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-703">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-703">Tag</span></span>   | <span data-ttu-id="f7aa7-704">0x011F</span><span class="sxs-lookup"><span data-stu-id="f7aa7-704">0x011F</span></span>                  |
| <span data-ttu-id="f7aa7-705">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-705">Type</span></span>  | <span data-ttu-id="f7aa7-706">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-706">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-707">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-707">Count</span></span> | <span data-ttu-id="f7aa7-708">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-708">1</span></span>                       |



 

## <a name="propertytagfreeoffset"></a><span data-ttu-id="f7aa7-709">PropertyTagFreeOffset</span><span class="sxs-lookup"><span data-stu-id="f7aa7-709">PropertyTagFreeOffset</span></span>

<span data-ttu-id="f7aa7-710">Pour chaque chaîne d’octets inutilisés contigus, il s’agit du décalage d’octet de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-710">For each string of contiguous unused bytes, the byte offset of that string.</span></span>



| <span data-ttu-id="f7aa7-711">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-711">Property info</span></span> | <span data-ttu-id="f7aa7-712">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-712">Value</span></span> |
|------|---------------------|
| <span data-ttu-id="f7aa7-713">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-713">Tag</span></span>  | <span data-ttu-id="f7aa7-714">0x0120</span><span class="sxs-lookup"><span data-stu-id="f7aa7-714">0x0120</span></span>              |
| <span data-ttu-id="f7aa7-715">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-715">Type</span></span> | <span data-ttu-id="f7aa7-716">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-716">PropertyTagTypeLong</span></span> |



 

## <a name="propertytagfreebytecounts"></a><span data-ttu-id="f7aa7-717">PropertyTagFreeByteCounts</span><span class="sxs-lookup"><span data-stu-id="f7aa7-717">PropertyTagFreeByteCounts</span></span>

<span data-ttu-id="f7aa7-718">Pour chaque chaîne d’octets inutilisés contigus, nombre d’octets dans cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-718">For each string of contiguous unused bytes, the number of bytes in that string.</span></span>



| <span data-ttu-id="f7aa7-719">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-719">Property info</span></span> | <span data-ttu-id="f7aa7-720">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-720">Value</span></span> |
|-------|-----------------------------------------------|
| <span data-ttu-id="f7aa7-721">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-721">Tag</span></span>   | <span data-ttu-id="f7aa7-722">0x0121</span><span class="sxs-lookup"><span data-stu-id="f7aa7-722">0x0121</span></span>                                        |
| <span data-ttu-id="f7aa7-723">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-723">Type</span></span>  | <span data-ttu-id="f7aa7-724">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-724">PropertyTagTypeLong</span></span>                           |
| <span data-ttu-id="f7aa7-725">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-725">Count</span></span> | <span data-ttu-id="f7aa7-726">Nombre de chaînes d’octets inutilisés contigus.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-726">Number of strings of contiguous unused bytes.</span></span> |



 

## <a name="propertytaggrayresponseunit"></a><span data-ttu-id="f7aa7-727">PropertyTagGrayResponseUnit</span><span class="sxs-lookup"><span data-stu-id="f7aa7-727">PropertyTagGrayResponseUnit</span></span>

<span data-ttu-id="f7aa7-728">Précision du nombre spécifié par PropertyTagGrayResponseCurve.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-728">Precision of the number specified by PropertyTagGrayResponseCurve.</span></span> <span data-ttu-id="f7aa7-729">1 spécifie dixièmes, 2 spécifie centièmes, 3 spécifie des millièmes, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-729">1 specifies tenths, 2 specifies hundredths, 3 specifies thousandths, and so on.</span></span>



| <span data-ttu-id="f7aa7-730">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-730">Property info</span></span> | <span data-ttu-id="f7aa7-731">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-731">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-732">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-732">Tag</span></span>   | <span data-ttu-id="f7aa7-733">0x0122</span><span class="sxs-lookup"><span data-stu-id="f7aa7-733">0x0122</span></span>               |
| <span data-ttu-id="f7aa7-734">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-734">Type</span></span>  | <span data-ttu-id="f7aa7-735">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-735">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-736">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-736">Count</span></span> | <span data-ttu-id="f7aa7-737">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-737">1</span></span>                    |



 

## <a name="propertytaggrayresponsecurve"></a><span data-ttu-id="f7aa7-738">PropertyTagGrayResponseCurve</span><span class="sxs-lookup"><span data-stu-id="f7aa7-738">PropertyTagGrayResponseCurve</span></span>

<span data-ttu-id="f7aa7-739">Pour chaque valeur de pixel possible dans une image en nuances de gris, la densité optique de cette valeur de pixel.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-739">For each possible pixel value in a grayscale image, the optical density of that pixel value.</span></span>



| <span data-ttu-id="f7aa7-740">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-740">Property info</span></span> | <span data-ttu-id="f7aa7-741">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-741">Value</span></span> |
|-------|---------------------------------|
| <span data-ttu-id="f7aa7-742">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-742">Tag</span></span>   | <span data-ttu-id="f7aa7-743">0x0123</span><span class="sxs-lookup"><span data-stu-id="f7aa7-743">0x0123</span></span>                          |
| <span data-ttu-id="f7aa7-744">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-744">Type</span></span>  | <span data-ttu-id="f7aa7-745">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-745">PropertyTagTypeShort</span></span>            |
| <span data-ttu-id="f7aa7-746">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-746">Count</span></span> | <span data-ttu-id="f7aa7-747">Nombre de valeurs de pixel possibles</span><span class="sxs-lookup"><span data-stu-id="f7aa7-747">Number of possible pixel values</span></span> |



 

## <a name="propertytagt4option"></a><span data-ttu-id="f7aa7-748">PropertyTagT4Option</span><span class="sxs-lookup"><span data-stu-id="f7aa7-748">PropertyTagT4Option</span></span>

<span data-ttu-id="f7aa7-749">Ensemble d’indicateurs liés à l’encodage T4.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-749">Set of flags that relate to T4 encoding.</span></span>



| <span data-ttu-id="f7aa7-750">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-750">Property info</span></span> | <span data-ttu-id="f7aa7-751">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-751">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-752">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-752">Tag</span></span>   | <span data-ttu-id="f7aa7-753">0x0124</span><span class="sxs-lookup"><span data-stu-id="f7aa7-753">0x0124</span></span>              |
| <span data-ttu-id="f7aa7-754">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-754">Type</span></span>  | <span data-ttu-id="f7aa7-755">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-755">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-756">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-756">Count</span></span> | <span data-ttu-id="f7aa7-757">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-757">1</span></span>                   |



 

## <a name="propertytagt6option"></a><span data-ttu-id="f7aa7-758">PropertyTagT6Option</span><span class="sxs-lookup"><span data-stu-id="f7aa7-758">PropertyTagT6Option</span></span>

<span data-ttu-id="f7aa7-759">Ensemble d’indicateurs associés à l’encodage T6.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-759">Set of flags that relate to T6 encoding.</span></span>



| <span data-ttu-id="f7aa7-760">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-760">Property info</span></span> | <span data-ttu-id="f7aa7-761">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-761">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-762">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-762">Tag</span></span>   | <span data-ttu-id="f7aa7-763">0x0125</span><span class="sxs-lookup"><span data-stu-id="f7aa7-763">0x0125</span></span>              |
| <span data-ttu-id="f7aa7-764">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-764">Type</span></span>  | <span data-ttu-id="f7aa7-765">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-765">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-766">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-766">Count</span></span> | <span data-ttu-id="f7aa7-767">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-767">1</span></span>                   |



 

## <a name="propertytagresolutionunit"></a><span data-ttu-id="f7aa7-768">PropertyTagResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="f7aa7-768">PropertyTagResolutionUnit</span></span>

<span data-ttu-id="f7aa7-769">Unité de mesure pour la résolution horizontale et la résolution verticale.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-769">Unit of measure for the horizontal resolution and the vertical resolution.</span></span>



<span data-ttu-id="f7aa7-770">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-770">Tag</span></span>

<span data-ttu-id="f7aa7-771">0x0128</span><span class="sxs-lookup"><span data-stu-id="f7aa7-771">0x0128</span></span>

<span data-ttu-id="f7aa7-772">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-772">Type</span></span>

<span data-ttu-id="f7aa7-773">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-773">PropertyTagTypeShort</span></span>

<span data-ttu-id="f7aa7-774">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-774">Count</span></span>

<span data-ttu-id="f7aa7-775">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-775">1</span></span>

<span data-ttu-id="f7aa7-776">2 pouces, 3-centimètres</span><span class="sxs-lookup"><span data-stu-id="f7aa7-776">2 - inch 3 - centimeter</span></span>



 

## <a name="propertytagpagenumber"></a><span data-ttu-id="f7aa7-777">PropertyTagPageNumber</span><span class="sxs-lookup"><span data-stu-id="f7aa7-777">PropertyTagPageNumber</span></span>

<span data-ttu-id="f7aa7-778">Numéro de page de la page à partir de laquelle l’image a été numérisée.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-778">Page number of the page from which the image was scanned.</span></span>



| <span data-ttu-id="f7aa7-779">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-779">Property info</span></span> | <span data-ttu-id="f7aa7-780">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-780">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-781">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-781">Tag</span></span>   | <span data-ttu-id="f7aa7-782">0x0129</span><span class="sxs-lookup"><span data-stu-id="f7aa7-782">0x0129</span></span>               |
| <span data-ttu-id="f7aa7-783">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-783">Type</span></span>  | <span data-ttu-id="f7aa7-784">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-784">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-785">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-785">Count</span></span> | <span data-ttu-id="f7aa7-786">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-786">1</span></span>                    |



 

## <a name="propertytagtransferfunction"></a><span data-ttu-id="f7aa7-787">PropertyTagTransferFunction</span><span class="sxs-lookup"><span data-stu-id="f7aa7-787">PropertyTagTransferFunction</span></span>

<span data-ttu-id="f7aa7-788">Tables qui spécifient des fonctions de transfert pour l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-788">Tables that specify transfer functions for the image.</span></span>



| <span data-ttu-id="f7aa7-789">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-789">Property info</span></span> | <span data-ttu-id="f7aa7-790">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-790">Value</span></span> |
|-------|------------------------------------------------------|
| <span data-ttu-id="f7aa7-791">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-791">Tag</span></span>   | <span data-ttu-id="f7aa7-792">0x012D</span><span class="sxs-lookup"><span data-stu-id="f7aa7-792">0x012D</span></span>                                               |
| <span data-ttu-id="f7aa7-793">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-793">Type</span></span>  | <span data-ttu-id="f7aa7-794">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-794">PropertyTagTypeShort</span></span>                                 |
| <span data-ttu-id="f7aa7-795">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-795">Count</span></span> | <span data-ttu-id="f7aa7-796">Nombre total de mots de 16 bits requis pour les tables</span><span class="sxs-lookup"><span data-stu-id="f7aa7-796">Total number of 16-bit words required for the tables</span></span> |



 

## <a name="propertytagsoftwareused"></a><span data-ttu-id="f7aa7-797">PropertyTagSoftwareUsed</span><span class="sxs-lookup"><span data-stu-id="f7aa7-797">PropertyTagSoftwareUsed</span></span>

<span data-ttu-id="f7aa7-798">Chaîne de caractères se terminant par un caractère null qui spécifie le nom et la version du logiciel ou du microprogramme de l’appareil utilisé pour générer l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-798">Null-terminated character string that specifies the name and version of the software or firmware of the device used to generate the image.</span></span>



| <span data-ttu-id="f7aa7-799">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-799">Property info</span></span> | <span data-ttu-id="f7aa7-800">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-800">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-801">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-801">Tag</span></span>   | <span data-ttu-id="f7aa7-802">0x0131</span><span class="sxs-lookup"><span data-stu-id="f7aa7-802">0x0131</span></span>                                             |
| <span data-ttu-id="f7aa7-803">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-803">Type</span></span>  | <span data-ttu-id="f7aa7-804">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-804">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-805">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-805">Count</span></span> | <span data-ttu-id="f7aa7-806">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-806">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagdatetime"></a><span data-ttu-id="f7aa7-807">PropertyTagDateTime</span><span class="sxs-lookup"><span data-stu-id="f7aa7-807">PropertyTagDateTime</span></span>

<span data-ttu-id="f7aa7-808">Date et heure de création de l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-808">Date and time the image was created.</span></span>



| <span data-ttu-id="f7aa7-809">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-809">Property info</span></span> | <span data-ttu-id="f7aa7-810">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-810">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-811">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-811">Tag</span></span>   | <span data-ttu-id="f7aa7-812">0x0132</span><span class="sxs-lookup"><span data-stu-id="f7aa7-812">0x0132</span></span>               |
| <span data-ttu-id="f7aa7-813">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-813">Type</span></span>  | <span data-ttu-id="f7aa7-814">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-814">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="f7aa7-815">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-815">Count</span></span> | <span data-ttu-id="f7aa7-816">20</span><span class="sxs-lookup"><span data-stu-id="f7aa7-816">20</span></span>                   |



 

## <a name="propertytagartist"></a><span data-ttu-id="f7aa7-817">PropertyTagArtist</span><span class="sxs-lookup"><span data-stu-id="f7aa7-817">PropertyTagArtist</span></span>

<span data-ttu-id="f7aa7-818">Chaîne de caractères se terminant par un caractère null qui spécifie le nom de la personne qui a créé l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-818">Null-terminated character string that specifies the name of the person who created the image.</span></span>



| <span data-ttu-id="f7aa7-819">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-819">Property info</span></span> | <span data-ttu-id="f7aa7-820">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-820">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-821">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-821">Tag</span></span>   | <span data-ttu-id="f7aa7-822">0x013B</span><span class="sxs-lookup"><span data-stu-id="f7aa7-822">0x013B</span></span>                                             |
| <span data-ttu-id="f7aa7-823">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-823">Type</span></span>  | <span data-ttu-id="f7aa7-824">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-824">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-825">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-825">Count</span></span> | <span data-ttu-id="f7aa7-826">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-826">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaghostcomputer"></a><span data-ttu-id="f7aa7-827">PropertyTagHostComputer</span><span class="sxs-lookup"><span data-stu-id="f7aa7-827">PropertyTagHostComputer</span></span>

<span data-ttu-id="f7aa7-828">Chaîne de caractères se terminant par un caractère null qui spécifie l’ordinateur et/ou le système d’exploitation utilisé pour créer l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-828">Null-terminated character string that specifies the computer and/or operating system used to create the image.</span></span>



| <span data-ttu-id="f7aa7-829">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-829">Property info</span></span> | <span data-ttu-id="f7aa7-830">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-830">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-831">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-831">Tag</span></span>   | <span data-ttu-id="f7aa7-832">0x013C</span><span class="sxs-lookup"><span data-stu-id="f7aa7-832">0x013C</span></span>                                             |
| <span data-ttu-id="f7aa7-833">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-833">Type</span></span>  | <span data-ttu-id="f7aa7-834">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-834">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-835">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-835">Count</span></span> | <span data-ttu-id="f7aa7-836">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-836">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagpredictor"></a><span data-ttu-id="f7aa7-837">PropertyTagPredictor</span><span class="sxs-lookup"><span data-stu-id="f7aa7-837">PropertyTagPredictor</span></span>

<span data-ttu-id="f7aa7-838">Type de schéma de prédiction appliqué aux données de l’image avant l’application du schéma d’encodage.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-838">Type of prediction scheme that was applied to the image data before the encoding scheme was applied.</span></span>



| <span data-ttu-id="f7aa7-839">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-839">Property info</span></span> | <span data-ttu-id="f7aa7-840">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-840">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-841">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-841">Tag</span></span>   | <span data-ttu-id="f7aa7-842">0x013D</span><span class="sxs-lookup"><span data-stu-id="f7aa7-842">0x013D</span></span>               |
| <span data-ttu-id="f7aa7-843">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-843">Type</span></span>  | <span data-ttu-id="f7aa7-844">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-844">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-845">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-845">Count</span></span> | <span data-ttu-id="f7aa7-846">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-846">1</span></span>                    |



 

## <a name="propertytagwhitepoint"></a><span data-ttu-id="f7aa7-847">PropertyTagWhitePoint</span><span class="sxs-lookup"><span data-stu-id="f7aa7-847">PropertyTagWhitePoint</span></span>

<span data-ttu-id="f7aa7-848">Chromatique du point blanc de l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-848">Chromaticity of the white point of the image.</span></span>



| <span data-ttu-id="f7aa7-849">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-849">Property info</span></span> | <span data-ttu-id="f7aa7-850">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-850">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-851">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-851">Tag</span></span>   | <span data-ttu-id="f7aa7-852">0x013E</span><span class="sxs-lookup"><span data-stu-id="f7aa7-852">0x013E</span></span>                  |
| <span data-ttu-id="f7aa7-853">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-853">Type</span></span>  | <span data-ttu-id="f7aa7-854">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-854">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-855">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-855">Count</span></span> | <span data-ttu-id="f7aa7-856">2</span><span class="sxs-lookup"><span data-stu-id="f7aa7-856">2</span></span>                       |



 

## <a name="propertytagprimarychromaticities"></a><span data-ttu-id="f7aa7-857">PropertyTagPrimaryChromaticities</span><span class="sxs-lookup"><span data-stu-id="f7aa7-857">PropertyTagPrimaryChromaticities</span></span>

<span data-ttu-id="f7aa7-858">Pour chacune des trois couleurs primaires dans l’image, la chromatique de cette couleur.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-858">For each of the three primary colors in the image, the chromaticity of that color.</span></span>



| <span data-ttu-id="f7aa7-859">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-859">Property info</span></span> | <span data-ttu-id="f7aa7-860">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-860">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-861">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-861">Tag</span></span>   | <span data-ttu-id="f7aa7-862">0x013F</span><span class="sxs-lookup"><span data-stu-id="f7aa7-862">0x013F</span></span>                  |
| <span data-ttu-id="f7aa7-863">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-863">Type</span></span>  | <span data-ttu-id="f7aa7-864">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-864">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-865">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-865">Count</span></span> | <span data-ttu-id="f7aa7-866">6</span><span class="sxs-lookup"><span data-stu-id="f7aa7-866">6</span></span>                       |



 

## <a name="propertytagcolormap"></a><span data-ttu-id="f7aa7-867">PropertyTagColorMap</span><span class="sxs-lookup"><span data-stu-id="f7aa7-867">PropertyTagColorMap</span></span>

<span data-ttu-id="f7aa7-868">Palette de couleurs (table de choix) pour une image indexée par palette.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-868">Color palette (lookup table) for a palette-indexed image.</span></span>



| <span data-ttu-id="f7aa7-869">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-869">Property info</span></span> | <span data-ttu-id="f7aa7-870">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-870">Value</span></span> |
|-------|-------------------------------------------------|
| <span data-ttu-id="f7aa7-871">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-871">Tag</span></span>   | <span data-ttu-id="f7aa7-872">0x0140</span><span class="sxs-lookup"><span data-stu-id="f7aa7-872">0x0140</span></span>                                          |
| <span data-ttu-id="f7aa7-873">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-873">Type</span></span>  | <span data-ttu-id="f7aa7-874">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-874">PropertyTagTypeShort</span></span>                            |
| <span data-ttu-id="f7aa7-875">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-875">Count</span></span> | <span data-ttu-id="f7aa7-876">Nombre de mots de 16 bits requis pour la palette</span><span class="sxs-lookup"><span data-stu-id="f7aa7-876">Number of 16-bit words required for the palette</span></span> |



 

## <a name="propertytaghalftonehints"></a><span data-ttu-id="f7aa7-877">PropertyTagHalftoneHints</span><span class="sxs-lookup"><span data-stu-id="f7aa7-877">PropertyTagHalftoneHints</span></span>

<span data-ttu-id="f7aa7-878">Informations utilisées par la fonction de demi-teinte</span><span class="sxs-lookup"><span data-stu-id="f7aa7-878">Information used by the halftone function</span></span>



| <span data-ttu-id="f7aa7-879">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-879">Property info</span></span> | <span data-ttu-id="f7aa7-880">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-880">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-881">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-881">Tag</span></span>   | <span data-ttu-id="f7aa7-882">0x0141</span><span class="sxs-lookup"><span data-stu-id="f7aa7-882">0x0141</span></span>               |
| <span data-ttu-id="f7aa7-883">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-883">Type</span></span>  | <span data-ttu-id="f7aa7-884">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-884">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-885">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-885">Count</span></span> | <span data-ttu-id="f7aa7-886">2</span><span class="sxs-lookup"><span data-stu-id="f7aa7-886">2</span></span>                    |



 

## <a name="propertytagtilewidth"></a><span data-ttu-id="f7aa7-887">PropertyTagTileWidth</span><span class="sxs-lookup"><span data-stu-id="f7aa7-887">PropertyTagTileWidth</span></span>

<span data-ttu-id="f7aa7-888">Nombre de colonnes de pixels dans chaque vignette.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-888">Number of pixel columns in each tile.</span></span>



| <span data-ttu-id="f7aa7-889">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-889">Property info</span></span> | <span data-ttu-id="f7aa7-890">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-890">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="f7aa7-891">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-891">Tag</span></span>   | <span data-ttu-id="f7aa7-892">0x0142</span><span class="sxs-lookup"><span data-stu-id="f7aa7-892">0x0142</span></span>                                      |
| <span data-ttu-id="f7aa7-893">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-893">Type</span></span>  | <span data-ttu-id="f7aa7-894">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-894">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-895">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-895">Count</span></span> | <span data-ttu-id="f7aa7-896">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-896">1</span></span>                                           |



 

## <a name="propertytagtilelength"></a><span data-ttu-id="f7aa7-897">PropertyTagTileLength</span><span class="sxs-lookup"><span data-stu-id="f7aa7-897">PropertyTagTileLength</span></span>

<span data-ttu-id="f7aa7-898">Nombre de lignes de pixels dans chaque vignette.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-898">Number of pixel rows in each tile.</span></span>



| <span data-ttu-id="f7aa7-899">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-899">Property info</span></span> | <span data-ttu-id="f7aa7-900">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-900">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="f7aa7-901">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-901">Tag</span></span>   | <span data-ttu-id="f7aa7-902">0x0143</span><span class="sxs-lookup"><span data-stu-id="f7aa7-902">0x0143</span></span>                                      |
| <span data-ttu-id="f7aa7-903">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-903">Type</span></span>  | <span data-ttu-id="f7aa7-904">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-904">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-905">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-905">Count</span></span> | <span data-ttu-id="f7aa7-906">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-906">1</span></span>                                           |



 

## <a name="propertytagtileoffset"></a><span data-ttu-id="f7aa7-907">PropertyTagTileOffset</span><span class="sxs-lookup"><span data-stu-id="f7aa7-907">PropertyTagTileOffset</span></span>

<span data-ttu-id="f7aa7-908">Pour chaque vignette, le décalage d’octet de cette vignette.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-908">For each tile, the byte offset of that tile.</span></span>



| <span data-ttu-id="f7aa7-909">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-909">Property info</span></span> | <span data-ttu-id="f7aa7-910">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-910">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-911">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-911">Tag</span></span>   | <span data-ttu-id="f7aa7-912">0x0144</span><span class="sxs-lookup"><span data-stu-id="f7aa7-912">0x0144</span></span>              |
| <span data-ttu-id="f7aa7-913">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-913">Type</span></span>  | <span data-ttu-id="f7aa7-914">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-914">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-915">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-915">Count</span></span> | <span data-ttu-id="f7aa7-916">Nombre de vignettes</span><span class="sxs-lookup"><span data-stu-id="f7aa7-916">Number of tiles</span></span>     |



 

## <a name="propertytagtilebytecounts"></a><span data-ttu-id="f7aa7-917">PropertyTagTileByteCounts</span><span class="sxs-lookup"><span data-stu-id="f7aa7-917">PropertyTagTileByteCounts</span></span>

<span data-ttu-id="f7aa7-918">Pour chaque vignette, nombre d’octets dans cette vignette.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-918">For each tile, the number of bytes in that tile.</span></span>



| <span data-ttu-id="f7aa7-919">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-919">Property info</span></span> | <span data-ttu-id="f7aa7-920">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-920">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="f7aa7-921">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-921">Tag</span></span>   | <span data-ttu-id="f7aa7-922">0x0145</span><span class="sxs-lookup"><span data-stu-id="f7aa7-922">0x0145</span></span>                                      |
| <span data-ttu-id="f7aa7-923">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-923">Type</span></span>  | <span data-ttu-id="f7aa7-924">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-924">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-925">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-925">Count</span></span> | <span data-ttu-id="f7aa7-926">Nombre de vignettes</span><span class="sxs-lookup"><span data-stu-id="f7aa7-926">Number of tiles</span></span>                             |



 

## <a name="propertytaginkset"></a><span data-ttu-id="f7aa7-927">PropertyTagInkSet</span><span class="sxs-lookup"><span data-stu-id="f7aa7-927">PropertyTagInkSet</span></span>

<span data-ttu-id="f7aa7-928">Jeu d’encres utilisé dans une image séparée.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-928">Set of inks used in a separated image.</span></span>



| <span data-ttu-id="f7aa7-929">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-929">Property info</span></span> | <span data-ttu-id="f7aa7-930">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-930">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-931">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-931">Tag</span></span>   | <span data-ttu-id="f7aa7-932">0x014C</span><span class="sxs-lookup"><span data-stu-id="f7aa7-932">0x014C</span></span>               |
| <span data-ttu-id="f7aa7-933">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-933">Type</span></span>  | <span data-ttu-id="f7aa7-934">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-934">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-935">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-935">Count</span></span> | <span data-ttu-id="f7aa7-936">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-936">1</span></span>                    |



 

## <a name="propertytaginknames"></a><span data-ttu-id="f7aa7-937">PropertyTagInkNames</span><span class="sxs-lookup"><span data-stu-id="f7aa7-937">PropertyTagInkNames</span></span>

<span data-ttu-id="f7aa7-938">Séquence de chaînes de caractères concaténées, se terminant par un caractère null, qui spécifient les noms des encres utilisées dans une image séparée.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-938">Sequence of concatenated, null-terminated, character strings that specify the names of the inks used in a separated image.</span></span>



| <span data-ttu-id="f7aa7-939">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-939">Property info</span></span> | <span data-ttu-id="f7aa7-940">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-940">Value</span></span> |
|-------|------------------------------------------------------------------------|
| <span data-ttu-id="f7aa7-941">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-941">Tag</span></span>   | <span data-ttu-id="f7aa7-942">0x014D</span><span class="sxs-lookup"><span data-stu-id="f7aa7-942">0x014D</span></span>                                                                 |
| <span data-ttu-id="f7aa7-943">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-943">Type</span></span>  | <span data-ttu-id="f7aa7-944">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-944">PropertyTagTypeASCII</span></span>                                                   |
| <span data-ttu-id="f7aa7-945">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-945">Count</span></span> | <span data-ttu-id="f7aa7-946">Longueur totale de la séquence de chaînes, y compris les marques de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-946">Total length of the sequence of strings including the NULL terminators</span></span> |



 

## <a name="propertytagnumberofinks"></a><span data-ttu-id="f7aa7-947">PropertyTagNumberOfInks</span><span class="sxs-lookup"><span data-stu-id="f7aa7-947">PropertyTagNumberOfInks</span></span>

<span data-ttu-id="f7aa7-948">Nombre d’encres.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-948">Number of inks.</span></span>



| <span data-ttu-id="f7aa7-949">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-949">Property info</span></span> | <span data-ttu-id="f7aa7-950">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-950">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-951">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-951">Tag</span></span>   | <span data-ttu-id="f7aa7-952">0x014E</span><span class="sxs-lookup"><span data-stu-id="f7aa7-952">0x014E</span></span>               |
| <span data-ttu-id="f7aa7-953">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-953">Type</span></span>  | <span data-ttu-id="f7aa7-954">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-954">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-955">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-955">Count</span></span> | <span data-ttu-id="f7aa7-956">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-956">1</span></span>                    |



 

## <a name="propertytagdotrange"></a><span data-ttu-id="f7aa7-957">PropertyTagDotRange</span><span class="sxs-lookup"><span data-stu-id="f7aa7-957">PropertyTagDotRange</span></span>

<span data-ttu-id="f7aa7-958">Valeurs de composant de couleur qui correspondent à un point de 0 pour cent et un point de 100 pour cent.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-958">Color component values that correspond to a 0 percent dot and a 100 percent dot.</span></span>



| <span data-ttu-id="f7aa7-959">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-959">Property info</span></span> | <span data-ttu-id="f7aa7-960">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-960">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="f7aa7-961">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-961">Tag</span></span>   | <span data-ttu-id="f7aa7-962">0x0150</span><span class="sxs-lookup"><span data-stu-id="f7aa7-962">0x0150</span></span>                                      |
| <span data-ttu-id="f7aa7-963">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-963">Type</span></span>  | <span data-ttu-id="f7aa7-964">PropertyTagTypeByte ou PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-964">PropertyTagTypeByte or PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-965">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-965">Count</span></span> | <span data-ttu-id="f7aa7-966">2 ou 2 × PropertyTagSamplesPerPixel</span><span class="sxs-lookup"><span data-stu-id="f7aa7-966">2 or 2×PropertyTagSamplesPerPixel</span></span>           |



 

## <a name="propertytagtargetprinter"></a><span data-ttu-id="f7aa7-967">PropertyTagTargetPrinter</span><span class="sxs-lookup"><span data-stu-id="f7aa7-967">PropertyTagTargetPrinter</span></span>

<span data-ttu-id="f7aa7-968">Chaîne de caractères se terminant par un caractère null qui décrit l’environnement d’impression prévu.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-968">Null-terminated character string that describes the intended printing environment.</span></span>



| <span data-ttu-id="f7aa7-969">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-969">Property info</span></span> | <span data-ttu-id="f7aa7-970">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-970">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-971">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-971">Tag</span></span>   | <span data-ttu-id="f7aa7-972">0x0151</span><span class="sxs-lookup"><span data-stu-id="f7aa7-972">0x0151</span></span>                                             |
| <span data-ttu-id="f7aa7-973">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-973">Type</span></span>  | <span data-ttu-id="f7aa7-974">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-974">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-975">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-975">Count</span></span> | <span data-ttu-id="f7aa7-976">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-976">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagextrasamples"></a><span data-ttu-id="f7aa7-977">PropertyTagExtraSamples</span><span class="sxs-lookup"><span data-stu-id="f7aa7-977">PropertyTagExtraSamples</span></span>

<span data-ttu-id="f7aa7-978">Nombre de composants de couleur supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-978">Number of extra color components.</span></span> <span data-ttu-id="f7aa7-979">Par exemple, un composant supplémentaire peut contenir une valeur alpha.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-979">For example, one extra component might hold an alpha value.</span></span>



| <span data-ttu-id="f7aa7-980">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-980">Property info</span></span> | <span data-ttu-id="f7aa7-981">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-981">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-982">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-982">Tag</span></span>   | <span data-ttu-id="f7aa7-983">0x0152</span><span class="sxs-lookup"><span data-stu-id="f7aa7-983">0x0152</span></span>               |
| <span data-ttu-id="f7aa7-984">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-984">Type</span></span>  | <span data-ttu-id="f7aa7-985">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-985">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-986">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-986">Count</span></span> | <span data-ttu-id="f7aa7-987">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-987">1</span></span>                    |



 

## <a name="propertytagsampleformat"></a><span data-ttu-id="f7aa7-988">PropertyTagSampleFormat</span><span class="sxs-lookup"><span data-stu-id="f7aa7-988">PropertyTagSampleFormat</span></span>

<span data-ttu-id="f7aa7-989">Pour chaque composant de couleur, le format numérique (non signé, signé, à virgule flottante) de ce composant.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-989">For each color component, the numerical format (unsigned, signed, floating point) of that component.</span></span> <span data-ttu-id="f7aa7-990">Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-990">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="f7aa7-991">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-991">Property info</span></span> | <span data-ttu-id="f7aa7-992">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-992">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="f7aa7-993">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-993">Tag</span></span>   | <span data-ttu-id="f7aa7-994">0x0153</span><span class="sxs-lookup"><span data-stu-id="f7aa7-994">0x0153</span></span>                                   |
| <span data-ttu-id="f7aa7-995">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-995">Type</span></span>  | <span data-ttu-id="f7aa7-996">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-996">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="f7aa7-997">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-997">Count</span></span> | <span data-ttu-id="f7aa7-998">Nombre d’échantillons (composants) par pixel</span><span class="sxs-lookup"><span data-stu-id="f7aa7-998">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagsminsamplevalue"></a><span data-ttu-id="f7aa7-999">PropertyTagSMinSampleValue</span><span class="sxs-lookup"><span data-stu-id="f7aa7-999">PropertyTagSMinSampleValue</span></span>

<span data-ttu-id="f7aa7-1000">Pour chaque composant de couleur, valeur minimale de ce composant.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1000">For each color component, the minimum value of that component.</span></span> <span data-ttu-id="f7aa7-1001">Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1001">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="f7aa7-1002">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1002">Property info</span></span> | <span data-ttu-id="f7aa7-1003">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1003">Value</span></span> |
|-------|-----------------------------------------------------|
| <span data-ttu-id="f7aa7-1004">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1004">Tag</span></span>   | <span data-ttu-id="f7aa7-1005">0x0154</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1005">0x0154</span></span>                                              |
| <span data-ttu-id="f7aa7-1006">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1006">Type</span></span>  | <span data-ttu-id="f7aa7-1007">Type qui correspond le mieux aux données du composant pixel</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1007">The type that best matches the pixel component data</span></span> |
| <span data-ttu-id="f7aa7-1008">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1008">Count</span></span> | <span data-ttu-id="f7aa7-1009">Nombre d’échantillons (composants) par pixel</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1009">Number of samples (components) per pixel</span></span>            |



 

## <a name="propertytagsmaxsamplevalue"></a><span data-ttu-id="f7aa7-1010">PropertyTagSMaxSampleValue</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1010">PropertyTagSMaxSampleValue</span></span>

<span data-ttu-id="f7aa7-1011">Pour chaque composant de couleur, valeur maximale de ce composant.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1011">For each color component, the maximum value of that component.</span></span> <span data-ttu-id="f7aa7-1012">Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1012">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="f7aa7-1013">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1013">Property info</span></span> | <span data-ttu-id="f7aa7-1014">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1014">Value</span></span> |
|-------|-----------------------------------------------------|
| <span data-ttu-id="f7aa7-1015">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1015">Tag</span></span>   | <span data-ttu-id="f7aa7-1016">0x0155</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1016">0x0155</span></span>                                              |
| <span data-ttu-id="f7aa7-1017">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1017">Type</span></span>  | <span data-ttu-id="f7aa7-1018">Type qui correspond le mieux aux données du composant pixel</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1018">The type that best matches the pixel component data</span></span> |
| <span data-ttu-id="f7aa7-1019">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1019">Count</span></span> | <span data-ttu-id="f7aa7-1020">Nombre d’échantillons (composants) par pixel</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1020">Number of samples (components) per pixel</span></span>            |



 

## <a name="propertytagtransferrange"></a><span data-ttu-id="f7aa7-1021">PropertyTagTransferRange</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1021">PropertyTagTransferRange</span></span>

<span data-ttu-id="f7aa7-1022">Table de valeurs qui étend la plage de la fonction de transfert.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1022">Table of values that extends the range of the transfer function.</span></span>



| <span data-ttu-id="f7aa7-1023">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1023">Property info</span></span> | <span data-ttu-id="f7aa7-1024">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1024">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1025">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1025">Tag</span></span>   | <span data-ttu-id="f7aa7-1026">0x0156</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1026">0x0156</span></span>               |
| <span data-ttu-id="f7aa7-1027">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1027">Type</span></span>  | <span data-ttu-id="f7aa7-1028">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1028">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1029">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1029">Count</span></span> | <span data-ttu-id="f7aa7-1030">6</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1030">6</span></span>                    |



 

## <a name="propertytagjpegproc"></a><span data-ttu-id="f7aa7-1031">PropertyTagJPEGProc</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1031">PropertyTagJPEGProc</span></span>

<span data-ttu-id="f7aa7-1032">Processus de compression JPEG.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1032">JPEG compression process.</span></span>



| <span data-ttu-id="f7aa7-1033">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1033">Property info</span></span> | <span data-ttu-id="f7aa7-1034">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1034">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1035">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1035">Tag</span></span>   | <span data-ttu-id="f7aa7-1036">0x0200</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1036">0x0200</span></span>               |
| <span data-ttu-id="f7aa7-1037">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1037">Type</span></span>  | <span data-ttu-id="f7aa7-1038">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1038">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1039">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1039">Count</span></span> | <span data-ttu-id="f7aa7-1040">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1040">1</span></span>                    |



 

## <a name="propertytagjpeginterformat"></a><span data-ttu-id="f7aa7-1041">PropertyTagJPEGInterFormat</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1041">PropertyTagJPEGInterFormat</span></span>

<span data-ttu-id="f7aa7-1042">Décalage au début d’un flux binaire JPEG.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1042">Offset to the start of a JPEG bitstream.</span></span>



| <span data-ttu-id="f7aa7-1043">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1043">Property info</span></span> | <span data-ttu-id="f7aa7-1044">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1044">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-1045">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1045">Tag</span></span>   | <span data-ttu-id="f7aa7-1046">0x0201</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1046">0x0201</span></span>              |
| <span data-ttu-id="f7aa7-1047">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1047">Type</span></span>  | <span data-ttu-id="f7aa7-1048">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1048">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-1049">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1049">Count</span></span> | <span data-ttu-id="f7aa7-1050">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1050">1</span></span>                   |



 

## <a name="propertytagjpeginterlength"></a><span data-ttu-id="f7aa7-1051">PropertyTagJPEGInterLength</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1051">PropertyTagJPEGInterLength</span></span>

<span data-ttu-id="f7aa7-1052">Longueur, en octets, du flux binaire JPEG.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1052">Length, in bytes, of the JPEG bitstream.</span></span>



| <span data-ttu-id="f7aa7-1053">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1053">Property info</span></span> | <span data-ttu-id="f7aa7-1054">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1054">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-1055">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1055">Tag</span></span>   | <span data-ttu-id="f7aa7-1056">0x0202</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1056">0x0202</span></span>              |
| <span data-ttu-id="f7aa7-1057">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1057">Type</span></span>  | <span data-ttu-id="f7aa7-1058">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1058">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-1059">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1059">Count</span></span> | <span data-ttu-id="f7aa7-1060">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1060">1</span></span>                   |



 

## <a name="propertytagjpegrestartinterval"></a><span data-ttu-id="f7aa7-1061">PropertyTagJPEGRestartInterval</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1061">PropertyTagJPEGRestartInterval</span></span>

<span data-ttu-id="f7aa7-1062">Longueur de l’intervalle de redémarrage.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1062">Length of the restart interval.</span></span>



| <span data-ttu-id="f7aa7-1063">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1063">Property info</span></span> | <span data-ttu-id="f7aa7-1064">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1064">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1065">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1065">Tag</span></span>   | <span data-ttu-id="f7aa7-1066">0x0203</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1066">0x0203</span></span>               |
| <span data-ttu-id="f7aa7-1067">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1067">Type</span></span>  | <span data-ttu-id="f7aa7-1068">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1068">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1069">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1069">Count</span></span> | <span data-ttu-id="f7aa7-1070">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1070">1</span></span>                    |



 

## <a name="propertytagjpeglosslesspredictors"></a><span data-ttu-id="f7aa7-1071">PropertyTagJPEGLosslessPredictors</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1071">PropertyTagJPEGLosslessPredictors</span></span>

<span data-ttu-id="f7aa7-1072">Pour chaque composant de couleur, il s’agit d’une valeur de sélection de prédiction sans perte pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1072">For each color component, a lossless predictor-selection value for that component.</span></span> <span data-ttu-id="f7aa7-1073">Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1073">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="f7aa7-1074">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1074">Property info</span></span> | <span data-ttu-id="f7aa7-1075">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1075">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="f7aa7-1076">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1076">Tag</span></span>   | <span data-ttu-id="f7aa7-1077">0x0205</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1077">0x0205</span></span>                                   |
| <span data-ttu-id="f7aa7-1078">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1078">Type</span></span>  | <span data-ttu-id="f7aa7-1079">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1079">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="f7aa7-1080">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1080">Count</span></span> | <span data-ttu-id="f7aa7-1081">Nombre d’échantillons (composants) par pixel</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1081">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegpointtransforms"></a><span data-ttu-id="f7aa7-1082">PropertyTagJPEGPointTransforms</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1082">PropertyTagJPEGPointTransforms</span></span>

<span data-ttu-id="f7aa7-1083">Pour chaque composant de couleur, valeur de transformation de point pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1083">For each color component, a point transformation value for that component.</span></span> <span data-ttu-id="f7aa7-1084">Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1084">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="f7aa7-1085">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1085">Property info</span></span> | <span data-ttu-id="f7aa7-1086">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1086">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="f7aa7-1087">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1087">Tag</span></span>   | <span data-ttu-id="f7aa7-1088">0x0206</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1088">0x0206</span></span>                                   |
| <span data-ttu-id="f7aa7-1089">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1089">Type</span></span>  | <span data-ttu-id="f7aa7-1090">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1090">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="f7aa7-1091">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1091">Count</span></span> | <span data-ttu-id="f7aa7-1092">Nombre d’échantillons (composants) par pixel</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1092">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegqtables"></a><span data-ttu-id="f7aa7-1093">PropertyTagJPEGQTables</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1093">PropertyTagJPEGQTables</span></span>

<span data-ttu-id="f7aa7-1094">Pour chaque composant de couleur, décalage vers la table de quantification pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1094">For each color component, the offset to the quantization table for that component.</span></span> <span data-ttu-id="f7aa7-1095">Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1095">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="f7aa7-1096">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1096">Property info</span></span> | <span data-ttu-id="f7aa7-1097">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1097">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="f7aa7-1098">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1098">Tag</span></span>   | <span data-ttu-id="f7aa7-1099">0x0207</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1099">0x0207</span></span>                                   |
| <span data-ttu-id="f7aa7-1100">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1100">Type</span></span>  | <span data-ttu-id="f7aa7-1101">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1101">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="f7aa7-1102">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1102">Count</span></span> | <span data-ttu-id="f7aa7-1103">Nombre d’échantillons (composants) par pixel</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1103">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegdctables"></a><span data-ttu-id="f7aa7-1104">PropertyTagJPEGDCTables</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1104">PropertyTagJPEGDCTables</span></span>

<span data-ttu-id="f7aa7-1105">Pour chaque composant de couleur, décalage vers la table de Huffman de contrôle de l’élément de contrôle (ou table de Huffman sans perte) pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1105">For each color component, the offset to the DC Huffman table (or lossless Huffman table) for that component.</span></span> <span data-ttu-id="f7aa7-1106">Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1106">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="f7aa7-1107">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1107">Property info</span></span> | <span data-ttu-id="f7aa7-1108">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1108">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="f7aa7-1109">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1109">Tag</span></span>   | <span data-ttu-id="f7aa7-1110">0x0208</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1110">0x0208</span></span>                                   |
| <span data-ttu-id="f7aa7-1111">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1111">Type</span></span>  | <span data-ttu-id="f7aa7-1112">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1112">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="f7aa7-1113">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1113">Count</span></span> | <span data-ttu-id="f7aa7-1114">Nombre d’échantillons (composants) par pixel</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1114">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegactables"></a><span data-ttu-id="f7aa7-1115">PropertyTagJPEGACTables</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1115">PropertyTagJPEGACTables</span></span>

<span data-ttu-id="f7aa7-1116">Pour chaque composant de couleur, décalage vers la table de Huffman AC pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1116">For each color component, the offset to the AC Huffman table for that component.</span></span> <span data-ttu-id="f7aa7-1117">Voir aussi [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1117">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="f7aa7-1118">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1118">Property info</span></span> | <span data-ttu-id="f7aa7-1119">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1119">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="f7aa7-1120">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1120">Tag</span></span>   | <span data-ttu-id="f7aa7-1121">0x0209</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1121">0x0209</span></span>                                   |
| <span data-ttu-id="f7aa7-1122">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1122">Type</span></span>  | <span data-ttu-id="f7aa7-1123">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1123">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="f7aa7-1124">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1124">Count</span></span> | <span data-ttu-id="f7aa7-1125">Nombre d’échantillons (composants) par pixel</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1125">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagycbcrcoefficients"></a><span data-ttu-id="f7aa7-1126">PropertyTagYCbCrCoefficients</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1126">PropertyTagYCbCrCoefficients</span></span>

<span data-ttu-id="f7aa7-1127">Coefficients pour la transformation des données d’image RVB en données d’image YCbCr.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1127">Coefficients for transformation from RGB to YCbCr image data.</span></span>



| <span data-ttu-id="f7aa7-1128">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1128">Property info</span></span> | <span data-ttu-id="f7aa7-1129">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1129">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-1130">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1130">Tag</span></span>   | <span data-ttu-id="f7aa7-1131">0x0211</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1131">0x0211</span></span>                  |
| <span data-ttu-id="f7aa7-1132">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1132">Type</span></span>  | <span data-ttu-id="f7aa7-1133">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1133">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-1134">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1134">Count</span></span> | <span data-ttu-id="f7aa7-1135">3</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1135">3</span></span>                       |



 

## <a name="propertytagycbcrsubsampling"></a><span data-ttu-id="f7aa7-1136">PropertyTagYCbCrSubsampling</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1136">PropertyTagYCbCrSubsampling</span></span>

<span data-ttu-id="f7aa7-1137">Taux d’échantillonnage des composants de chrominance par rapport au composant luminance.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1137">Sampling ratio of chrominance components in relation to the luminance component.</span></span>



| <span data-ttu-id="f7aa7-1138">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1138">Property info</span></span> | <span data-ttu-id="f7aa7-1139">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1139">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1140">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1140">Tag</span></span>   | <span data-ttu-id="f7aa7-1141">0x0212</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1141">0x0212</span></span>               |
| <span data-ttu-id="f7aa7-1142">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1142">Type</span></span>  | <span data-ttu-id="f7aa7-1143">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1143">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1144">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1144">Count</span></span> | <span data-ttu-id="f7aa7-1145">2</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1145">2</span></span>                    |



 

## <a name="propertytagycbcrpositioning"></a><span data-ttu-id="f7aa7-1146">PropertyTagYCbCrPositioning</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1146">PropertyTagYCbCrPositioning</span></span>

<span data-ttu-id="f7aa7-1147">Position des composants de chrominance par rapport au composant luminance.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1147">Position of chrominance components in relation to the luminance component.</span></span>



| <span data-ttu-id="f7aa7-1148">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1148">Property info</span></span> | <span data-ttu-id="f7aa7-1149">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1149">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1150">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1150">Tag</span></span>   | <span data-ttu-id="f7aa7-1151">0x0213</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1151">0x0213</span></span>               |
| <span data-ttu-id="f7aa7-1152">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1152">Type</span></span>  | <span data-ttu-id="f7aa7-1153">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1153">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1154">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1154">Count</span></span> | <span data-ttu-id="f7aa7-1155">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1155">1</span></span>                    |



 

## <a name="propertytagrefblackwhite"></a><span data-ttu-id="f7aa7-1156">PropertyTagREFBlackWhite</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1156">PropertyTagREFBlackWhite</span></span>

<span data-ttu-id="f7aa7-1157">Valeur du point noir de référence et valeur du point blanc de référence.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1157">Reference black point value and reference white point value.</span></span>



| <span data-ttu-id="f7aa7-1158">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1158">Property info</span></span> | <span data-ttu-id="f7aa7-1159">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1159">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-1160">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1160">Tag</span></span>   | <span data-ttu-id="f7aa7-1161">0x0214</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1161">0x0214</span></span>                  |
| <span data-ttu-id="f7aa7-1162">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1162">Type</span></span>  | <span data-ttu-id="f7aa7-1163">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1163">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-1164">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1164">Count</span></span> | <span data-ttu-id="f7aa7-1165">6</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1165">6</span></span>                       |



 

## <a name="propertytaggamma"></a><span data-ttu-id="f7aa7-1166">PropertyTagGamma</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1166">PropertyTagGamma</span></span>

<span data-ttu-id="f7aa7-1167">Valeur gamma attachée à l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1167">Gamma value attached to the image.</span></span> <span data-ttu-id="f7aa7-1168">La valeur gamma est stockée sous la forme d’un nombre rationnel (paire de **long**) avec un numérateur de 100000.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1168">The gamma value is stored as a rational number (pair of **long**) with a numerator of 100000.</span></span> <span data-ttu-id="f7aa7-1169">Par exemple, la valeur gamma 2,2 est stockée en tant que paire (100000, 45455).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1169">For example, a gamma value of 2.2 is stored as the pair (100000, 45455).</span></span>



| <span data-ttu-id="f7aa7-1170">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1170">Property info</span></span> | <span data-ttu-id="f7aa7-1171">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1171">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-1172">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1172">Tag</span></span>   | <span data-ttu-id="f7aa7-1173">0x0301</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1173">0x0301</span></span>                  |
| <span data-ttu-id="f7aa7-1174">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1174">Type</span></span>  | <span data-ttu-id="f7aa7-1175">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1175">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-1176">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1176">Count</span></span> | <span data-ttu-id="f7aa7-1177">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1177">1</span></span>                       |



 

## <a name="propertytagiccprofiledescriptor"></a><span data-ttu-id="f7aa7-1178">PropertyTagICCProfileDescriptor</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1178">PropertyTagICCProfileDescriptor</span></span>

<span data-ttu-id="f7aa7-1179">Chaîne de caractères se terminant par un caractère null qui identifie un profil ICC.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1179">Null-terminated character string that identifies an ICC profile.</span></span>



| <span data-ttu-id="f7aa7-1180">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1180">Property info</span></span> | <span data-ttu-id="f7aa7-1181">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1181">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-1182">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1182">Tag</span></span>   | <span data-ttu-id="f7aa7-1183">0x0302</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1183">0x0302</span></span>                                             |
| <span data-ttu-id="f7aa7-1184">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1184">Type</span></span>  | <span data-ttu-id="f7aa7-1185">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1185">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-1186">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1186">Count</span></span> | <span data-ttu-id="f7aa7-1187">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1187">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagsrgbrenderingintent"></a><span data-ttu-id="f7aa7-1188">PropertyTagSRGBRenderingIntent</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1188">PropertyTagSRGBRenderingIntent</span></span>

<span data-ttu-id="f7aa7-1189">Comment l’image doit être affichée comme défini par le consortium de couleur international (ICC).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1189">How the image should be displayed as defined by the International Color Consortium (ICC).</span></span> <span data-ttu-id="f7aa7-1190">Si un objet  [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) GDI+ est construit avec le paramètre *UseEmbeddedColorManagement* défini sur **true**, GDI+ effectue le rendu de l’image en fonction de l’intention de rendu spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1190">If a GDI+  [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object is constructed with the *useEmbeddedColorManagement* parameter set to **TRUE**, then GDI+ renders the image according to the specified rendering intent.</span></span> <span data-ttu-id="f7aa7-1191">L’intention peut être définie sur perception, Colorimétrie relative, saturation ou Colorimétrie absolue.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1191">The intent can be set to perceptual, relative colorimetric, saturation, or absolute colorimetric.</span></span>

-   <span data-ttu-id="f7aa7-1192">L’intention de perception, adaptée aux photographies, offre une bonne adaptation à la gamme d’appareils d’affichage au détriment de la précision colorimétrique.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1192">Perceptual intent, which is suitable for photographs, gives good adaptation to the display device gamut at the expense of colorimetric accuracy.</span></span>
-   <span data-ttu-id="f7aa7-1193">L’intention de Colorimétrie relative convient pour les images (par exemple, des logos) qui requièrent une correspondance d’apparence de couleur par rapport au point blanc de l’appareil d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1193">Relative colorimetric intent is suitable for images (for example, logos) that require color appearance matching that is relative to the display device white point.</span></span>
-   <span data-ttu-id="f7aa7-1194">L’objectif de saturation, qui convient aux graphiques et aux graphiques, conserve la saturation aux dépens de la teinte et de la luminosité.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1194">Saturation intent, which is suitable for charts and graphs, preserves saturation at the expense of hue and lightness.</span></span>
-   <span data-ttu-id="f7aa7-1195">L’intention de Colorimétrie absolue est adaptée aux épreuves (aperçus d’images destinées à un autre périphérique d’affichage) qui nécessitent la préservation de la colorimétrie absolue.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1195">Absolute colorimetric intent is suitable for proofs (previews of images destined for a different display device) that require preservation of absolute colorimetry.</span></span>



<span data-ttu-id="f7aa7-1196">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1196">Tag</span></span>

<span data-ttu-id="f7aa7-1197">0x0303</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1197">0x0303</span></span>

<span data-ttu-id="f7aa7-1198">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1198">Type</span></span>

<span data-ttu-id="f7aa7-1199">BYTE</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1199">BYTE</span></span>

<span data-ttu-id="f7aa7-1200">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1200">Count</span></span>

<span data-ttu-id="f7aa7-1201">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1201">1</span></span>

<span data-ttu-id="f7aa7-1202">0-perception 1-Colorimétrie relative 2-saturation 3-Colorimétrie absolue</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1202">0 - perceptual 1 - relative colorimetric 2 - saturation 3 - absolute colorimetric</span></span>



 

## <a name="propertytagimagetitle"></a><span data-ttu-id="f7aa7-1203">PropertyTagImageTitle</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1203">PropertyTagImageTitle</span></span>

<span data-ttu-id="f7aa7-1204">Chaîne de caractères se terminant par un caractère null qui spécifie le titre de l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1204">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="f7aa7-1205">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1205">Property info</span></span> | <span data-ttu-id="f7aa7-1206">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1206">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-1207">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1207">Tag</span></span>   | <span data-ttu-id="f7aa7-1208">0x0320</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1208">0x0320</span></span>                                             |
| <span data-ttu-id="f7aa7-1209">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1209">Type</span></span>  | <span data-ttu-id="f7aa7-1210">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1210">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-1211">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1211">Count</span></span> | <span data-ttu-id="f7aa7-1212">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1212">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagresolutionxunit"></a><span data-ttu-id="f7aa7-1213">PropertyTagResolutionXUnit</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1213">PropertyTagResolutionXUnit</span></span>

<span data-ttu-id="f7aa7-1214">Unités dans lesquelles afficher la résolution horizontale.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1214">Units in which to display horizontal resolution.</span></span>



<span data-ttu-id="f7aa7-1215">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1215">Tag</span></span>

<span data-ttu-id="f7aa7-1216">0x5001</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1216">0x5001</span></span>

<span data-ttu-id="f7aa7-1217">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1217">Type</span></span>

<span data-ttu-id="f7aa7-1218">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1218">PropertyTagTypeShort</span></span>

<span data-ttu-id="f7aa7-1219">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1219">Count</span></span>

<span data-ttu-id="f7aa7-1220">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1220">1</span></span>

<span data-ttu-id="f7aa7-1221">1-pixels par pouce 2-pixels par centimètre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1221">1 - pixels per inch 2 - pixels per centimeter</span></span>



 

## <a name="propertytagresolutionyunit"></a><span data-ttu-id="f7aa7-1222">PropertyTagResolutionYUnit</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1222">PropertyTagResolutionYUnit</span></span>

<span data-ttu-id="f7aa7-1223">Unités dans lesquelles afficher la résolution verticale.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1223">Units in which to display vertical resolution.</span></span>



<span data-ttu-id="f7aa7-1224">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1224">Tag</span></span>

<span data-ttu-id="f7aa7-1225">0x5002</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1225">0x5002</span></span>

<span data-ttu-id="f7aa7-1226">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1226">Type</span></span>

<span data-ttu-id="f7aa7-1227">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1227">PropertyTagTypeShort</span></span>

<span data-ttu-id="f7aa7-1228">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1228">Count</span></span>

<span data-ttu-id="f7aa7-1229">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1229">1</span></span>

<span data-ttu-id="f7aa7-1230">1-pixels par pouce 2-pixels par centimètre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1230">1 - pixels per inch 2 - pixels per centimeter</span></span>



 

## <a name="propertytagresolutionxlengthunit"></a><span data-ttu-id="f7aa7-1231">PropertyTagResolutionXLengthUnit</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1231">PropertyTagResolutionXLengthUnit</span></span>

<span data-ttu-id="f7aa7-1232">Unités dans lesquelles afficher la largeur de l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1232">Units in which to display the image width.</span></span>



<span data-ttu-id="f7aa7-1233">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1233">Tag</span></span>

<span data-ttu-id="f7aa7-1234">0x5003</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1234">0x5003</span></span>

<span data-ttu-id="f7aa7-1235">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1235">Type</span></span>

<span data-ttu-id="f7aa7-1236">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1236">PropertyTagTypeShort</span></span>

<span data-ttu-id="f7aa7-1237">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1237">Count</span></span>

<span data-ttu-id="f7aa7-1238">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1238">1</span></span>

<span data-ttu-id="f7aa7-1239">1-pouces 2-centimètres 3-points 4-picas 5-colonnes</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1239">1 - inches 2 - centimeters 3 - points 4 - picas 5 - columns</span></span>



 

## <a name="propertytagresolutionylengthunit"></a><span data-ttu-id="f7aa7-1240">PropertyTagResolutionYLengthUnit</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1240">PropertyTagResolutionYLengthUnit</span></span>

<span data-ttu-id="f7aa7-1241">Unités dans lesquelles afficher la hauteur de l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1241">Units in which to display the image height.</span></span>



<span data-ttu-id="f7aa7-1242">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1242">Tag</span></span>

<span data-ttu-id="f7aa7-1243">0x5004</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1243">0x5004</span></span>

<span data-ttu-id="f7aa7-1244">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1244">Type</span></span>

<span data-ttu-id="f7aa7-1245">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1245">PropertyTagTypeShort</span></span>

<span data-ttu-id="f7aa7-1246">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1246">Count</span></span>

<span data-ttu-id="f7aa7-1247">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1247">1</span></span>

<span data-ttu-id="f7aa7-1248">1-pouces 2-centimètres 3-points 4-picas 5-colonnes</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1248">1 - inches 2 - centimeters 3 - points 4 - picas 5 - columns</span></span>



 

## <a name="propertytagprintflags"></a><span data-ttu-id="f7aa7-1249">PropertyTagPrintFlags</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1249">PropertyTagPrintFlags</span></span>

<span data-ttu-id="f7aa7-1250">Séquence de valeurs booléennes sur un octet qui spécifient des options d’impression.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1250">Sequence of one-byte Boolean values that specify printing options.</span></span>



| <span data-ttu-id="f7aa7-1251">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1251">Property info</span></span> | <span data-ttu-id="f7aa7-1252">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1252">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1253">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1253">Tag</span></span>   | <span data-ttu-id="f7aa7-1254">0x5005</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1254">0x5005</span></span>               |
| <span data-ttu-id="f7aa7-1255">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1255">Type</span></span>  | <span data-ttu-id="f7aa7-1256">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1256">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="f7aa7-1257">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1257">Count</span></span> | <span data-ttu-id="f7aa7-1258">Nombre d’indicateurs</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1258">Number of flags</span></span>      |



 

## <a name="propertytagprintflagsversion"></a><span data-ttu-id="f7aa7-1259">PropertyTagPrintFlagsVersion</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1259">PropertyTagPrintFlagsVersion</span></span>

<span data-ttu-id="f7aa7-1260">Version des indicateurs d’impression.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1260">Print flags version.</span></span>



| <span data-ttu-id="f7aa7-1261">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1261">Property info</span></span> | <span data-ttu-id="f7aa7-1262">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1262">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1263">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1263">Tag</span></span>   | <span data-ttu-id="f7aa7-1264">0x5006</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1264">0x5006</span></span>               |
| <span data-ttu-id="f7aa7-1265">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1265">Type</span></span>  | <span data-ttu-id="f7aa7-1266">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1266">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1267">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1267">Count</span></span> | <span data-ttu-id="f7aa7-1268">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1268">1</span></span>                    |



 

## <a name="propertytagprintflagscrop"></a><span data-ttu-id="f7aa7-1269">PropertyTagPrintFlagsCrop</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1269">PropertyTagPrintFlagsCrop</span></span>

<span data-ttu-id="f7aa7-1270">Afficher le Centre des indicateurs de rognages.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1270">Print flags center crop marks.</span></span>



| <span data-ttu-id="f7aa7-1271">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1271">Property info</span></span> | <span data-ttu-id="f7aa7-1272">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1272">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-1273">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1273">Tag</span></span>   | <span data-ttu-id="f7aa7-1274">0x5007</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1274">0x5007</span></span>              |
| <span data-ttu-id="f7aa7-1275">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1275">Type</span></span>  | <span data-ttu-id="f7aa7-1276">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1276">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="f7aa7-1277">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1277">Count</span></span> | <span data-ttu-id="f7aa7-1278">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1278">1</span></span>                   |



 

## <a name="propertytagprintflagsbleedwidth"></a><span data-ttu-id="f7aa7-1279">PropertyTagPrintFlagsBleedWidth</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1279">PropertyTagPrintFlagsBleedWidth</span></span>

<span data-ttu-id="f7aa7-1280">Largeur du fonds perdus des indicateurs d’impression.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1280">Print flags bleed width.</span></span>



| <span data-ttu-id="f7aa7-1281">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1281">Property info</span></span> | <span data-ttu-id="f7aa7-1282">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1282">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-1283">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1283">Tag</span></span>   | <span data-ttu-id="f7aa7-1284">0x5008</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1284">0x5008</span></span>              |
| <span data-ttu-id="f7aa7-1285">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1285">Type</span></span>  | <span data-ttu-id="f7aa7-1286">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1286">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-1287">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1287">Count</span></span> | <span data-ttu-id="f7aa7-1288">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1288">1</span></span>                   |



 

## <a name="propertytagprintflagsbleedwidthscale"></a><span data-ttu-id="f7aa7-1289">PropertyTagPrintFlagsBleedWidthScale</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1289">PropertyTagPrintFlagsBleedWidthScale</span></span>

<span data-ttu-id="f7aa7-1290">Échelle de la largeur du fonds perdus des indicateurs d’impression.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1290">Print flags bleed width scale.</span></span>



| <span data-ttu-id="f7aa7-1291">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1291">Property info</span></span> | <span data-ttu-id="f7aa7-1292">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1292">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1293">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1293">Tag</span></span>   | <span data-ttu-id="f7aa7-1294">0x5009</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1294">0x5009</span></span>               |
| <span data-ttu-id="f7aa7-1295">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1295">Type</span></span>  | <span data-ttu-id="f7aa7-1296">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1296">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1297">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1297">Count</span></span> | <span data-ttu-id="f7aa7-1298">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1298">1</span></span>                    |



 

## <a name="propertytaghalftonelpi"></a><span data-ttu-id="f7aa7-1299">PropertyTagHalftoneLPI</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1299">PropertyTagHalftoneLPI</span></span>

<span data-ttu-id="f7aa7-1300">Fréquence d’écran de l’encre, en lignes par pouce.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1300">Ink's screen frequency, in lines per inch.</span></span>



| <span data-ttu-id="f7aa7-1301">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1301">Property info</span></span> | <span data-ttu-id="f7aa7-1302">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1302">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-1303">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1303">Tag</span></span>   | <span data-ttu-id="f7aa7-1304">0x500A</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1304">0x500A</span></span>                  |
| <span data-ttu-id="f7aa7-1305">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1305">Type</span></span>  | <span data-ttu-id="f7aa7-1306">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1306">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-1307">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1307">Count</span></span> | <span data-ttu-id="f7aa7-1308">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1308">1</span></span>                       |



 

## <a name="propertytaghalftonelpiunit"></a><span data-ttu-id="f7aa7-1309">PropertyTagHalftoneLPIUnit</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1309">PropertyTagHalftoneLPIUnit</span></span>

<span data-ttu-id="f7aa7-1310">Unités pour la fréquence d’écran.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1310">Units for the screen frequency.</span></span>



<span data-ttu-id="f7aa7-1311">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1311">Tag</span></span>

<span data-ttu-id="f7aa7-1312">0x500B</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1312">0x500B</span></span>

<span data-ttu-id="f7aa7-1313">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1313">Type</span></span>

<span data-ttu-id="f7aa7-1314">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1314">PropertyTagTypeShort</span></span>

<span data-ttu-id="f7aa7-1315">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1315">Count</span></span>

<span data-ttu-id="f7aa7-1316">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1316">1</span></span>

<span data-ttu-id="f7aa7-1317">1-lignes par pouce 2 lignes par centimètre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1317">1 - lines per inch 2 - lines per centimeter</span></span>



 

## <a name="propertytaghalftonedegree"></a><span data-ttu-id="f7aa7-1318">PropertyTagHalftoneDegree</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1318">PropertyTagHalftoneDegree</span></span>

<span data-ttu-id="f7aa7-1319">Angle pour l’écran.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1319">Angle for screen.</span></span>



| <span data-ttu-id="f7aa7-1320">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1320">Property info</span></span> | <span data-ttu-id="f7aa7-1321">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1321">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-1322">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1322">Tag</span></span>   | <span data-ttu-id="f7aa7-1323">0x500C</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1323">0x500C</span></span>                  |
| <span data-ttu-id="f7aa7-1324">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1324">Type</span></span>  | <span data-ttu-id="f7aa7-1325">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1325">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-1326">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1326">Count</span></span> | <span data-ttu-id="f7aa7-1327">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1327">1</span></span>                       |



 

## <a name="propertytaghalftoneshape"></a><span data-ttu-id="f7aa7-1328">PropertyTagHalftoneShape</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1328">PropertyTagHalftoneShape</span></span>

<span data-ttu-id="f7aa7-1329">Forme des points en demi-teinte.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1329">Shape of the halftone dots.</span></span>



<span data-ttu-id="f7aa7-1330">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1330">Tag</span></span>

<span data-ttu-id="f7aa7-1331">0x500D</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1331">0x500D</span></span>

<span data-ttu-id="f7aa7-1332">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1332">Type</span></span>

<span data-ttu-id="f7aa7-1333">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1333">PropertyTagTypeShort</span></span>

<span data-ttu-id="f7aa7-1334">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1334">Count</span></span>

<span data-ttu-id="f7aa7-1335">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1335">1</span></span>

<span data-ttu-id="f7aa7-1336">0-rond 1-ellipse 2-ligne 3-carré 4-Croix 6-losange</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1336">0 - round 1 - ellipse 2 - line 3 - square 4 - cross 6 - diamond</span></span>



 

## <a name="propertytaghalftonemisc"></a><span data-ttu-id="f7aa7-1337">PropertyTagHalftoneMisc</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1337">PropertyTagHalftoneMisc</span></span>

<span data-ttu-id="f7aa7-1338">Informations diverses sur les demi-teintes.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1338">Miscellaneous halftone information.</span></span>



| <span data-ttu-id="f7aa7-1339">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1339">Property info</span></span> | <span data-ttu-id="f7aa7-1340">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1340">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-1341">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1341">Tag</span></span>   | <span data-ttu-id="f7aa7-1342">0x500E</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1342">0x500E</span></span>              |
| <span data-ttu-id="f7aa7-1343">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1343">Type</span></span>  | <span data-ttu-id="f7aa7-1344">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1344">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-1345">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1345">Count</span></span> | <span data-ttu-id="f7aa7-1346">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1346">1</span></span>                   |



 

## <a name="propertytaghalftonescreen"></a><span data-ttu-id="f7aa7-1347">PropertyTagHalftoneScreen</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1347">PropertyTagHalftoneScreen</span></span>

<span data-ttu-id="f7aa7-1348">Valeur booléenne qui spécifie s’il faut utiliser les écrans par défaut de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1348">Boolean value that specifies whether to use the printer's default screens.</span></span>



<span data-ttu-id="f7aa7-1349">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1349">Tag</span></span>

<span data-ttu-id="f7aa7-1350">0x500F</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1350">0x500F</span></span>

<span data-ttu-id="f7aa7-1351">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1351">Type</span></span>

<span data-ttu-id="f7aa7-1352">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1352">PropertyTagTypeByte</span></span>

<span data-ttu-id="f7aa7-1353">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1353">Count</span></span>

<span data-ttu-id="f7aa7-1354">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1354">1</span></span>

<span data-ttu-id="f7aa7-1355">1-utiliser les écrans par défaut de l’imprimante 2-autres</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1355">1 - use printer's default screens 2 - other</span></span>



 

## <a name="propertytagjpegquality"></a><span data-ttu-id="f7aa7-1356">PropertyTagJPEGQuality</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1356">PropertyTagJPEGQuality</span></span>

<span data-ttu-id="f7aa7-1357">Balise privée utilisée par le format Adobe Photoshop.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1357">Private tag used by the Adobe Photoshop format.</span></span> <span data-ttu-id="f7aa7-1358">Pas d’usage public.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1358">Not for public use.</span></span>



| <span data-ttu-id="f7aa7-1359">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1359">Property info</span></span> | <span data-ttu-id="f7aa7-1360">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1360">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1361">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1361">Tag</span></span>   | <span data-ttu-id="f7aa7-1362">0x5010</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1362">0x5010</span></span>               |
| <span data-ttu-id="f7aa7-1363">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1363">Type</span></span>  | <span data-ttu-id="f7aa7-1364">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1364">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1365">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1365">Count</span></span> | <span data-ttu-id="f7aa7-1366">Quelconque</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1366">Any</span></span>                  |



 

## <a name="propertytaggridsize"></a><span data-ttu-id="f7aa7-1367">PropertyTagGridSize</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1367">PropertyTagGridSize</span></span>

<span data-ttu-id="f7aa7-1368">Bloc d’informations sur les grilles et les repères.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1368">Block of information about grids and guides.</span></span>



| <span data-ttu-id="f7aa7-1369">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1369">Property info</span></span> | <span data-ttu-id="f7aa7-1370">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1370">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="f7aa7-1371">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1371">Tag</span></span>   | <span data-ttu-id="f7aa7-1372">0x5011</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1372">0x5011</span></span>                   |
| <span data-ttu-id="f7aa7-1373">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1373">Type</span></span>  | <span data-ttu-id="f7aa7-1374">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1374">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="f7aa7-1375">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1375">Count</span></span> | <span data-ttu-id="f7aa7-1376">Quelconque</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1376">Any</span></span>                      |



 

## <a name="propertytagthumbnailformat"></a><span data-ttu-id="f7aa7-1377">PropertyTagThumbnailFormat</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1377">PropertyTagThumbnailFormat</span></span>

<span data-ttu-id="f7aa7-1378">Format de l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1378">Format of the thumbnail image.</span></span>



<span data-ttu-id="f7aa7-1379">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1379">Tag</span></span>

<span data-ttu-id="f7aa7-1380">0x5012</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1380">0x5012</span></span>

<span data-ttu-id="f7aa7-1381">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1381">Type</span></span>

<span data-ttu-id="f7aa7-1382">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1382">PropertyTagTypeLong</span></span>

<span data-ttu-id="f7aa7-1383">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1383">Count</span></span>

<span data-ttu-id="f7aa7-1384">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1384">1</span></span>

<span data-ttu-id="f7aa7-1385">0-RAW RGB 1-JPEG</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1385">0 - raw RGB 1 - JPEG</span></span>



 

## <a name="propertytagthumbnailwidth"></a><span data-ttu-id="f7aa7-1386">PropertyTagThumbnailWidth</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1386">PropertyTagThumbnailWidth</span></span>

<span data-ttu-id="f7aa7-1387">Largeur, en pixels, de l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1387">Width, in pixels, of the thumbnail image.</span></span>



| <span data-ttu-id="f7aa7-1388">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1388">Property info</span></span> | <span data-ttu-id="f7aa7-1389">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1389">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-1390">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1390">Tag</span></span>   | <span data-ttu-id="f7aa7-1391">0x5013</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1391">0x5013</span></span>              |
| <span data-ttu-id="f7aa7-1392">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1392">Type</span></span>  | <span data-ttu-id="f7aa7-1393">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1393">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-1394">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1394">Count</span></span> | <span data-ttu-id="f7aa7-1395">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1395">1</span></span>                   |



 

## <a name="propertytagthumbnailheight"></a><span data-ttu-id="f7aa7-1396">PropertyTagThumbnailHeight</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1396">PropertyTagThumbnailHeight</span></span>

<span data-ttu-id="f7aa7-1397">Hauteur, en pixels, de l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1397">Height, in pixels, of the thumbnail image.</span></span>



| <span data-ttu-id="f7aa7-1398">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1398">Property info</span></span> | <span data-ttu-id="f7aa7-1399">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1399">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-1400">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1400">Tag</span></span>   | <span data-ttu-id="f7aa7-1401">0x5014</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1401">0x5014</span></span>              |
| <span data-ttu-id="f7aa7-1402">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1402">Type</span></span>  | <span data-ttu-id="f7aa7-1403">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1403">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-1404">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1404">Count</span></span> | <span data-ttu-id="f7aa7-1405">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1405">1</span></span>                   |



 

## <a name="propertytagthumbnailcolordepth"></a><span data-ttu-id="f7aa7-1406">PropertyTagThumbnailColorDepth</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1406">PropertyTagThumbnailColorDepth</span></span>

<span data-ttu-id="f7aa7-1407">bits par pixel (BPP) pour l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1407">bits per pixel (BPP) for the thumbnail image.</span></span>



| <span data-ttu-id="f7aa7-1408">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1408">Property info</span></span> | <span data-ttu-id="f7aa7-1409">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1409">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1410">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1410">Tag</span></span>   | <span data-ttu-id="f7aa7-1411">0x5015</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1411">0x5015</span></span>               |
| <span data-ttu-id="f7aa7-1412">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1412">Type</span></span>  | <span data-ttu-id="f7aa7-1413">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1413">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1414">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1414">Count</span></span> | <span data-ttu-id="f7aa7-1415">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1415">1</span></span>                    |



 

## <a name="propertytagthumbnailplanes"></a><span data-ttu-id="f7aa7-1416">PropertyTagThumbnailPlanes</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1416">PropertyTagThumbnailPlanes</span></span>

<span data-ttu-id="f7aa7-1417">Nombre de plans de couleur pour l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1417">Number of color planes for the thumbnail image.</span></span>



| <span data-ttu-id="f7aa7-1418">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1418">Property info</span></span> | <span data-ttu-id="f7aa7-1419">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1419">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1420">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1420">Tag</span></span>   | <span data-ttu-id="f7aa7-1421">0x5016</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1421">0x5016</span></span>               |
| <span data-ttu-id="f7aa7-1422">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1422">Type</span></span>  | <span data-ttu-id="f7aa7-1423">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1423">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1424">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1424">Count</span></span> | <span data-ttu-id="f7aa7-1425">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1425">1</span></span>                    |



 

## <a name="propertytagthumbnailrawbytes"></a><span data-ttu-id="f7aa7-1426">PropertyTagThumbnailRawBytes</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1426">PropertyTagThumbnailRawBytes</span></span>

<span data-ttu-id="f7aa7-1427">Décalage d’octet entre les lignes de données de pixels.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1427">Byte offset between rows of pixel data.</span></span>



| <span data-ttu-id="f7aa7-1428">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1428">Property info</span></span> | <span data-ttu-id="f7aa7-1429">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1429">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-1430">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1430">Tag</span></span>   | <span data-ttu-id="f7aa7-1431">0x5017</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1431">0x5017</span></span>              |
| <span data-ttu-id="f7aa7-1432">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1432">Type</span></span>  | <span data-ttu-id="f7aa7-1433">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1433">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-1434">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1434">Count</span></span> | <span data-ttu-id="f7aa7-1435">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1435">1</span></span>                   |



 

## <a name="propertytagthumbnailsize"></a><span data-ttu-id="f7aa7-1436">PropertyTagThumbnailSize</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1436">PropertyTagThumbnailSize</span></span>

<span data-ttu-id="f7aa7-1437">Taille totale, en octets, de l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1437">Total size, in bytes, of the thumbnail image.</span></span>



| <span data-ttu-id="f7aa7-1438">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1438">Property info</span></span> | <span data-ttu-id="f7aa7-1439">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1439">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-1440">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1440">Tag</span></span>   | <span data-ttu-id="f7aa7-1441">0x5018</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1441">0x5018</span></span>              |
| <span data-ttu-id="f7aa7-1442">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1442">Type</span></span>  | <span data-ttu-id="f7aa7-1443">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1443">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-1444">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1444">Count</span></span> | <span data-ttu-id="f7aa7-1445">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1445">1</span></span>                   |



 

## <a name="propertytagthumbnailcompressedsize"></a><span data-ttu-id="f7aa7-1446">PropertyTagThumbnailCompressedSize</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1446">PropertyTagThumbnailCompressedSize</span></span>

<span data-ttu-id="f7aa7-1447">Taille compressée, en octets, de l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1447">Compressed size, in bytes, of the thumbnail image.</span></span>



| <span data-ttu-id="f7aa7-1448">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1448">Property info</span></span> | <span data-ttu-id="f7aa7-1449">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1449">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-1450">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1450">Tag</span></span>   | <span data-ttu-id="f7aa7-1451">0x5019</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1451">0x5019</span></span>              |
| <span data-ttu-id="f7aa7-1452">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1452">Type</span></span>  | <span data-ttu-id="f7aa7-1453">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1453">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-1454">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1454">Count</span></span> | <span data-ttu-id="f7aa7-1455">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1455">1</span></span>                   |



 

## <a name="propertytagcolortransferfunction"></a><span data-ttu-id="f7aa7-1456">PropertyTagColorTransferFunction</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1456">PropertyTagColorTransferFunction</span></span>

<span data-ttu-id="f7aa7-1457">Table de valeurs qui spécifient des fonctions de transfert de couleurs.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1457">Table of values that specify color transfer functions.</span></span>



| <span data-ttu-id="f7aa7-1458">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1458">Property info</span></span> | <span data-ttu-id="f7aa7-1459">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1459">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="f7aa7-1460">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1460">Tag</span></span>   | <span data-ttu-id="f7aa7-1461">0x501A</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1461">0x501A</span></span>                   |
| <span data-ttu-id="f7aa7-1462">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1462">Type</span></span>  | <span data-ttu-id="f7aa7-1463">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1463">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="f7aa7-1464">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1464">Count</span></span> | <span data-ttu-id="f7aa7-1465">Quelconque</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1465">Any</span></span>                      |



 

## <a name="propertytagthumbnaildata"></a><span data-ttu-id="f7aa7-1466">PropertyTagThumbnailData</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1466">PropertyTagThumbnailData</span></span>

<span data-ttu-id="f7aa7-1467">Bits de miniature brut au format JPEG ou RGB.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1467">Raw thumbnail bits in JPEG or RGB format.</span></span> <span data-ttu-id="f7aa7-1468">Dépend de PropertyTagThumbnailFormat.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1468">Depends on PropertyTagThumbnailFormat.</span></span>



| <span data-ttu-id="f7aa7-1469">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1469">Property info</span></span> | <span data-ttu-id="f7aa7-1470">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1470">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-1471">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1471">Tag</span></span>   | <span data-ttu-id="f7aa7-1472">0x501B</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1472">0x501B</span></span>              |
| <span data-ttu-id="f7aa7-1473">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1473">Type</span></span>  | <span data-ttu-id="f7aa7-1474">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1474">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="f7aa7-1475">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1475">Count</span></span> | <span data-ttu-id="f7aa7-1476">Variable</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1476">Variable</span></span>            |



 

## <a name="propertytagthumbnailimagewidth"></a><span data-ttu-id="f7aa7-1477">PropertyTagThumbnailImageWidth</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1477">PropertyTagThumbnailImageWidth</span></span>

<span data-ttu-id="f7aa7-1478">Nombre de pixels par ligne dans l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1478">Number of pixels per row in the thumbnail image.</span></span>



| <span data-ttu-id="f7aa7-1479">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1479">Property info</span></span> | <span data-ttu-id="f7aa7-1480">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1480">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="f7aa7-1481">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1481">Tag</span></span>   | <span data-ttu-id="f7aa7-1482">0x5020</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1482">0x5020</span></span>                                      |
| <span data-ttu-id="f7aa7-1483">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1483">Type</span></span>  | <span data-ttu-id="f7aa7-1484">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1484">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-1485">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1485">Count</span></span> | <span data-ttu-id="f7aa7-1486">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1486">1</span></span>                                           |



 

## <a name="propertytagthumbnailimageheight"></a><span data-ttu-id="f7aa7-1487">PropertyTagThumbnailImageHeight</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1487">PropertyTagThumbnailImageHeight</span></span>

<span data-ttu-id="f7aa7-1488">Nombre de lignes de pixels dans l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1488">Number of pixel rows in the thumbnail image.</span></span>



| <span data-ttu-id="f7aa7-1489">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1489">Property info</span></span> | <span data-ttu-id="f7aa7-1490">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1490">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="f7aa7-1491">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1491">Tag</span></span>   | <span data-ttu-id="f7aa7-1492">0x5021</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1492">0x5021</span></span>                                      |
| <span data-ttu-id="f7aa7-1493">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1493">Type</span></span>  | <span data-ttu-id="f7aa7-1494">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1494">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-1495">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1495">Count</span></span> | <span data-ttu-id="f7aa7-1496">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1496">1</span></span>                                           |



 

## <a name="propertytagthumbnailbitspersample"></a><span data-ttu-id="f7aa7-1497">PropertyTagThumbnailBitsPerSample</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1497">PropertyTagThumbnailBitsPerSample</span></span>

<span data-ttu-id="f7aa7-1498">Nombre de bits par composant de couleur dans l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1498">Number of bits per color component in the thumbnail image.</span></span> <span data-ttu-id="f7aa7-1499">Voir aussi [PropertyTagThumbnailSamplesPerPixel](#propertytagthumbnailsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1499">See also [PropertyTagThumbnailSamplesPerPixel](#propertytagthumbnailsamplesperpixel).</span></span>



| <span data-ttu-id="f7aa7-1500">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1500">Property info</span></span> | <span data-ttu-id="f7aa7-1501">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1501">Value</span></span> |
|-------|-----------------------------------------------------------------|
| <span data-ttu-id="f7aa7-1502">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1502">Tag</span></span>   | <span data-ttu-id="f7aa7-1503">0x5022</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1503">0x5022</span></span>                                                          |
| <span data-ttu-id="f7aa7-1504">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1504">Type</span></span>  | <span data-ttu-id="f7aa7-1505">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1505">PropertyTagTypeShort</span></span>                                            |
| <span data-ttu-id="f7aa7-1506">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1506">Count</span></span> | <span data-ttu-id="f7aa7-1507">Nombre d’échantillons (composants) par pixel dans l’image miniature</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1507">Number of samples (components) per pixel in the thumbnail image</span></span> |



 

## <a name="propertytagthumbnailcompression"></a><span data-ttu-id="f7aa7-1508">PropertyTagThumbnailCompression</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1508">PropertyTagThumbnailCompression</span></span>

<span data-ttu-id="f7aa7-1509">Schéma de compression utilisé pour les données de l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1509">Compression scheme used for thumbnail image data.</span></span>



| <span data-ttu-id="f7aa7-1510">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1510">Property info</span></span> | <span data-ttu-id="f7aa7-1511">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1511">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1512">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1512">Tag</span></span>   | <span data-ttu-id="f7aa7-1513">0x5023</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1513">0x5023</span></span>               |
| <span data-ttu-id="f7aa7-1514">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1514">Type</span></span>  | <span data-ttu-id="f7aa7-1515">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1515">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1516">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1516">Count</span></span> | <span data-ttu-id="f7aa7-1517">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1517">1</span></span>                    |



 

## <a name="propertytagthumbnailphotometricinterp"></a><span data-ttu-id="f7aa7-1518">PropertyTagThumbnailPhotometricInterp</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1518">PropertyTagThumbnailPhotometricInterp</span></span>

<span data-ttu-id="f7aa7-1519">Interprétation des données de pixels miniatures.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1519">How thumbnail pixel data will be interpreted.</span></span>



| <span data-ttu-id="f7aa7-1520">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1520">Property info</span></span> | <span data-ttu-id="f7aa7-1521">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1521">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1522">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1522">Tag</span></span>   | <span data-ttu-id="f7aa7-1523">0x5024</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1523">0x5024</span></span>               |
| <span data-ttu-id="f7aa7-1524">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1524">Type</span></span>  | <span data-ttu-id="f7aa7-1525">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1525">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1526">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1526">Count</span></span> | <span data-ttu-id="f7aa7-1527">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1527">1</span></span>                    |



 

## <a name="propertytagthumbnailimagedescription"></a><span data-ttu-id="f7aa7-1528">PropertyTagThumbnailImageDescription</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1528">PropertyTagThumbnailImageDescription</span></span>

<span data-ttu-id="f7aa7-1529">Chaîne de caractères se terminant par un caractère null qui spécifie le titre de l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1529">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="f7aa7-1530">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1530">Property info</span></span> | <span data-ttu-id="f7aa7-1531">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1531">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-1532">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1532">Tag</span></span>   | <span data-ttu-id="f7aa7-1533">0x5025</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1533">0x5025</span></span>                                             |
| <span data-ttu-id="f7aa7-1534">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1534">Type</span></span>  | <span data-ttu-id="f7aa7-1535">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1535">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-1536">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1536">Count</span></span> | <span data-ttu-id="f7aa7-1537">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1537">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailequipmake"></a><span data-ttu-id="f7aa7-1538">PropertyTagThumbnailEquipMake</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1538">PropertyTagThumbnailEquipMake</span></span>

<span data-ttu-id="f7aa7-1539">Chaîne de caractères se terminant par un caractère null qui spécifie le fabricant de l’équipement utilisé pour enregistrer l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1539">Null-terminated character string that specifies the manufacturer of the equipment used to record the thumbnail image.</span></span>



| <span data-ttu-id="f7aa7-1540">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1540">Property info</span></span> | <span data-ttu-id="f7aa7-1541">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1541">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-1542">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1542">Tag</span></span>   | <span data-ttu-id="f7aa7-1543">0x5026</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1543">0x5026</span></span>                                             |
| <span data-ttu-id="f7aa7-1544">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1544">Type</span></span>  | <span data-ttu-id="f7aa7-1545">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1545">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-1546">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1546">Count</span></span> | <span data-ttu-id="f7aa7-1547">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1547">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailequipmodel"></a><span data-ttu-id="f7aa7-1548">PropertyTagThumbnailEquipModel</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1548">PropertyTagThumbnailEquipModel</span></span>

<span data-ttu-id="f7aa7-1549">Chaîne de caractères se terminant par un caractère null qui spécifie le nom du modèle ou le numéro de modèle de l’équipement utilisé pour enregistrer l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1549">Null-terminated character string that specifies the model name or model number of the equipment used to record the thumbnail image.</span></span>



| <span data-ttu-id="f7aa7-1550">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1550">Property info</span></span> | <span data-ttu-id="f7aa7-1551">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1551">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-1552">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1552">Tag</span></span>   | <span data-ttu-id="f7aa7-1553">0x5027</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1553">0x5027</span></span>                                             |
| <span data-ttu-id="f7aa7-1554">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1554">Type</span></span>  | <span data-ttu-id="f7aa7-1555">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1555">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-1556">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1556">Count</span></span> | <span data-ttu-id="f7aa7-1557">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1557">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailstripoffsets"></a><span data-ttu-id="f7aa7-1558">PropertyTagThumbnailStripOffsets</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1558">PropertyTagThumbnailStripOffsets</span></span>

<span data-ttu-id="f7aa7-1559">Pour chaque bande dans l’image miniature, le décalage d’octet de cette bande.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1559">For each strip in the thumbnail image, the byte offset of that strip.</span></span> <span data-ttu-id="f7aa7-1560">Voir aussi [PropertyTagThumbnailRowsPerStrip](#propertytagthumbnailrowsperstrip) et [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1560">See also [PropertyTagThumbnailRowsPerStrip](#propertytagthumbnailrowsperstrip) and [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount).</span></span>



| <span data-ttu-id="f7aa7-1561">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1561">Property info</span></span> | <span data-ttu-id="f7aa7-1562">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1562">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="f7aa7-1563">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1563">Tag</span></span>   | <span data-ttu-id="f7aa7-1564">0x5028</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1564">0x5028</span></span>                                      |
| <span data-ttu-id="f7aa7-1565">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1565">Type</span></span>  | <span data-ttu-id="f7aa7-1566">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1566">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-1567">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1567">Count</span></span> | <span data-ttu-id="f7aa7-1568">Nombre de bandes</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1568">Number of strips</span></span>                            |



 

## <a name="propertytagthumbnailorientation"></a><span data-ttu-id="f7aa7-1569">PropertyTagThumbnailOrientation</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1569">PropertyTagThumbnailOrientation</span></span>

<span data-ttu-id="f7aa7-1570">Orientation de l’image miniature en termes de lignes et de colonnes.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1570">Thumbnail image orientation in terms of rows and columns.</span></span> <span data-ttu-id="f7aa7-1571">Voir aussi [PropertyTagOrientation](#propertytagorientation).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1571">See also [PropertyTagOrientation](#propertytagorientation).</span></span>



| <span data-ttu-id="f7aa7-1572">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1572">Property info</span></span> | <span data-ttu-id="f7aa7-1573">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1573">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1574">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1574">Tag</span></span>   | <span data-ttu-id="f7aa7-1575">0x5029</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1575">0x5029</span></span>               |
| <span data-ttu-id="f7aa7-1576">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1576">Type</span></span>  | <span data-ttu-id="f7aa7-1577">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1577">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1578">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1578">Count</span></span> | <span data-ttu-id="f7aa7-1579">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1579">1</span></span>                    |



 

## <a name="propertytagthumbnailsamplesperpixel"></a><span data-ttu-id="f7aa7-1580">PropertyTagThumbnailSamplesPerPixel</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1580">PropertyTagThumbnailSamplesPerPixel</span></span>

<span data-ttu-id="f7aa7-1581">Nombre de composants de couleur par pixel dans l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1581">Number of color components per pixel in the thumbnail image.</span></span>



| <span data-ttu-id="f7aa7-1582">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1582">Property info</span></span> | <span data-ttu-id="f7aa7-1583">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1583">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1584">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1584">Tag</span></span>   | <span data-ttu-id="f7aa7-1585">0x502A</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1585">0x502A</span></span>               |
| <span data-ttu-id="f7aa7-1586">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1586">Type</span></span>  | <span data-ttu-id="f7aa7-1587">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1587">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1588">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1588">Count</span></span> | <span data-ttu-id="f7aa7-1589">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1589">1</span></span>                    |



 

## <a name="propertytagthumbnailrowsperstrip"></a><span data-ttu-id="f7aa7-1590">PropertyTagThumbnailRowsPerStrip</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1590">PropertyTagThumbnailRowsPerStrip</span></span>

<span data-ttu-id="f7aa7-1591">Nombre de lignes par bande dans l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1591">Number of rows per strip in the thumbnail image.</span></span> <span data-ttu-id="f7aa7-1592">Voir aussi [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount) et [PropertyTagThumbnailStripOffsets](#propertytagthumbnailstripoffsets).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1592">See also [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount) and [PropertyTagThumbnailStripOffsets](#propertytagthumbnailstripoffsets).</span></span>



| <span data-ttu-id="f7aa7-1593">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1593">Property info</span></span> | <span data-ttu-id="f7aa7-1594">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1594">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="f7aa7-1595">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1595">Tag</span></span>   | <span data-ttu-id="f7aa7-1596">0x502B</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1596">0x502B</span></span>                                      |
| <span data-ttu-id="f7aa7-1597">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1597">Type</span></span>  | <span data-ttu-id="f7aa7-1598">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1598">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-1599">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1599">Count</span></span> | <span data-ttu-id="f7aa7-1600">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1600">1</span></span>                                           |



 

## <a name="propertytagthumbnailstripbytescount"></a><span data-ttu-id="f7aa7-1601">PropertyTagThumbnailStripBytesCount</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1601">PropertyTagThumbnailStripBytesCount</span></span>

<span data-ttu-id="f7aa7-1602">Pour chaque bande d’images miniatures, nombre total d’octets dans cette bande.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1602">For each thumbnail image strip, the total number of bytes in that strip.</span></span>



| <span data-ttu-id="f7aa7-1603">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1603">Property info</span></span> | <span data-ttu-id="f7aa7-1604">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1604">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="f7aa7-1605">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1605">Tag</span></span>   | <span data-ttu-id="f7aa7-1606">0x502C</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1606">0x502C</span></span>                                      |
| <span data-ttu-id="f7aa7-1607">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1607">Type</span></span>  | <span data-ttu-id="f7aa7-1608">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1608">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-1609">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1609">Count</span></span> | <span data-ttu-id="f7aa7-1610">Nombre de bandes dans l’image miniature</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1610">Number of strips in the thumbnail image</span></span>     |



 

## <a name="propertytagthumbnailresolutionx"></a><span data-ttu-id="f7aa7-1611">PropertyTagThumbnailResolutionX</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1611">PropertyTagThumbnailResolutionX</span></span>

<span data-ttu-id="f7aa7-1612">Résolution des miniatures dans le sens de la largeur.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1612">Thumbnail resolution in the width direction.</span></span> <span data-ttu-id="f7aa7-1613">L’unité de résolution est donnée dans [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1613">The resolution unit is given in [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span></span>



| <span data-ttu-id="f7aa7-1614">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1614">Property info</span></span> | <span data-ttu-id="f7aa7-1615">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1615">Value</span></span> |
|-----|--------|
| <span data-ttu-id="f7aa7-1616">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1616">Tag</span></span> | <span data-ttu-id="f7aa7-1617">0x502D</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1617">0x502D</span></span> |



 

## <a name="propertytagthumbnailresolutiony"></a><span data-ttu-id="f7aa7-1618">PropertyTagThumbnailResolutionY</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1618">PropertyTagThumbnailResolutionY</span></span>

<span data-ttu-id="f7aa7-1619">Résolution des miniatures dans le sens de la hauteur.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1619">Thumbnail resolution in the height direction.</span></span> <span data-ttu-id="f7aa7-1620">L’unité de résolution est donnée dans [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1620">The resolution unit is given in [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span></span>



| <span data-ttu-id="f7aa7-1621">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1621">Property info</span></span> | <span data-ttu-id="f7aa7-1622">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1622">Value</span></span> |
|-----|--------|
| <span data-ttu-id="f7aa7-1623">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1623">Tag</span></span> | <span data-ttu-id="f7aa7-1624">0x502E</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1624">0x502E</span></span> |



 

## <a name="propertytagthumbnailplanarconfig"></a><span data-ttu-id="f7aa7-1625">PropertyTagThumbnailPlanarConfig</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1625">PropertyTagThumbnailPlanarConfig</span></span>

<span data-ttu-id="f7aa7-1626">Si les composants de pixels de l’image miniature sont enregistrés au format de forme groupée ou planaire.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1626">Whether pixel components in the thumbnail image are recorded in chunky or planar format.</span></span> <span data-ttu-id="f7aa7-1627">Voir aussi [PropertyTagPlanarConfig](#propertytagplanarconfig).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1627">See also [PropertyTagPlanarConfig](#propertytagplanarconfig).</span></span>



| <span data-ttu-id="f7aa7-1628">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1628">Property info</span></span> | <span data-ttu-id="f7aa7-1629">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1629">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1630">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1630">Tag</span></span>   | <span data-ttu-id="f7aa7-1631">0x502F</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1631">0x502F</span></span>               |
| <span data-ttu-id="f7aa7-1632">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1632">Type</span></span>  | <span data-ttu-id="f7aa7-1633">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1633">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1634">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1634">Count</span></span> | <span data-ttu-id="f7aa7-1635">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1635">1</span></span>                    |



 

## <a name="propertytagthumbnailresolutionunit"></a><span data-ttu-id="f7aa7-1636">PropertyTagThumbnailResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1636">PropertyTagThumbnailResolutionUnit</span></span>

<span data-ttu-id="f7aa7-1637">Unité de mesure pour la résolution horizontale et la résolution verticale de l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1637">Unit of measure for the horizontal resolution and the vertical resolution of the thumbnail image.</span></span> <span data-ttu-id="f7aa7-1638">Voir aussi [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1638">See also [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="f7aa7-1639">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1639">Property info</span></span> | <span data-ttu-id="f7aa7-1640">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1640">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1641">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1641">Tag</span></span>   | <span data-ttu-id="f7aa7-1642">0x5030</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1642">0x5030</span></span>               |
| <span data-ttu-id="f7aa7-1643">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1643">Type</span></span>  | <span data-ttu-id="f7aa7-1644">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1644">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1645">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1645">Count</span></span> | <span data-ttu-id="f7aa7-1646">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1646">1</span></span>                    |



 

## <a name="propertytagthumbnailtransferfunction"></a><span data-ttu-id="f7aa7-1647">PropertyTagThumbnailTransferFunction</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1647">PropertyTagThumbnailTransferFunction</span></span>

<span data-ttu-id="f7aa7-1648">Tables qui spécifient des fonctions de transfert pour l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1648">Tables that specify transfer functions for the thumbnail image.</span></span> <span data-ttu-id="f7aa7-1649">Voir aussi [PropertyTagTransferFunction](#propertytagtransferfunction).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1649">See also [PropertyTagTransferFunction](#propertytagtransferfunction).</span></span>



| <span data-ttu-id="f7aa7-1650">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1650">Property info</span></span> | <span data-ttu-id="f7aa7-1651">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1651">Value</span></span> |
|-------|------------------------------------------------------|
| <span data-ttu-id="f7aa7-1652">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1652">Tag</span></span>   | <span data-ttu-id="f7aa7-1653">0x5031</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1653">0x5031</span></span>                                               |
| <span data-ttu-id="f7aa7-1654">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1654">Type</span></span>  | <span data-ttu-id="f7aa7-1655">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1655">PropertyTagTypeShort</span></span>                                 |
| <span data-ttu-id="f7aa7-1656">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1656">Count</span></span> | <span data-ttu-id="f7aa7-1657">Nombre total de mots de 16 bits requis pour les tables</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1657">Total number of 16-bit words required for the tables</span></span> |



 

## <a name="propertytagthumbnailsoftwareused"></a><span data-ttu-id="f7aa7-1658">PropertyTagThumbnailSoftwareUsed</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1658">PropertyTagThumbnailSoftwareUsed</span></span>

<span data-ttu-id="f7aa7-1659">Chaîne de caractères se terminant par un caractère null qui spécifie le nom et la version du logiciel ou du microprogramme de l’appareil utilisé pour générer l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1659">Null-terminated character string that specifies the name and version of the software or firmware of the device used to generate the thumbnail image.</span></span>



| <span data-ttu-id="f7aa7-1660">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1660">Property info</span></span> | <span data-ttu-id="f7aa7-1661">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1661">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-1662">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1662">Tag</span></span>   | <span data-ttu-id="f7aa7-1663">0x5032</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1663">0x5032</span></span>                                             |
| <span data-ttu-id="f7aa7-1664">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1664">Type</span></span>  | <span data-ttu-id="f7aa7-1665">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1665">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-1666">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1666">Count</span></span> | <span data-ttu-id="f7aa7-1667">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1667">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnaildatetime"></a><span data-ttu-id="f7aa7-1668">PropertyTagThumbnailDateTime</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1668">PropertyTagThumbnailDateTime</span></span>

<span data-ttu-id="f7aa7-1669">Date et heure de création de l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1669">Date and time the thumbnail image was created.</span></span> <span data-ttu-id="f7aa7-1670">Voir aussi [PropertyTagDateTime](#propertytagdatetime).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1670">See also [PropertyTagDateTime](#propertytagdatetime).</span></span>



| <span data-ttu-id="f7aa7-1671">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1671">Property info</span></span> | <span data-ttu-id="f7aa7-1672">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1672">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1673">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1673">Tag</span></span>   | <span data-ttu-id="f7aa7-1674">0x5033</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1674">0x5033</span></span>               |
| <span data-ttu-id="f7aa7-1675">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1675">Type</span></span>  | <span data-ttu-id="f7aa7-1676">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1676">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="f7aa7-1677">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1677">Count</span></span> | <span data-ttu-id="f7aa7-1678">20</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1678">20</span></span>                   |



 

## <a name="propertytagthumbnailartist"></a><span data-ttu-id="f7aa7-1679">PropertyTagThumbnailArtist</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1679">PropertyTagThumbnailArtist</span></span>

<span data-ttu-id="f7aa7-1680">Chaîne de caractères se terminant par un caractère null qui spécifie le nom de la personne qui a créé l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1680">Null-terminated character string that specifies the name of the person who created the thumbnail image.</span></span>



| <span data-ttu-id="f7aa7-1681">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1681">Property info</span></span> | <span data-ttu-id="f7aa7-1682">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1682">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-1683">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1683">Tag</span></span>   | <span data-ttu-id="f7aa7-1684">0x5034</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1684">0x5034</span></span>                                             |
| <span data-ttu-id="f7aa7-1685">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1685">Type</span></span>  | <span data-ttu-id="f7aa7-1686">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1686">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-1687">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1687">Count</span></span> | <span data-ttu-id="f7aa7-1688">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1688">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailwhitepoint"></a><span data-ttu-id="f7aa7-1689">PropertyTagThumbnailWhitePoint</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1689">PropertyTagThumbnailWhitePoint</span></span>

<span data-ttu-id="f7aa7-1690">Chromatique du point blanc de l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1690">Chromaticity of the white point of the thumbnail image.</span></span> <span data-ttu-id="f7aa7-1691">Voir aussi [PropertyTagWhitePoint](#propertytagwhitepoint).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1691">See also [PropertyTagWhitePoint](#propertytagwhitepoint).</span></span>



| <span data-ttu-id="f7aa7-1692">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1692">Property info</span></span> | <span data-ttu-id="f7aa7-1693">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1693">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-1694">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1694">Tag</span></span>   | <span data-ttu-id="f7aa7-1695">0x5035</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1695">0x5035</span></span>                  |
| <span data-ttu-id="f7aa7-1696">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1696">Type</span></span>  | <span data-ttu-id="f7aa7-1697">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1697">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-1698">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1698">Count</span></span> | <span data-ttu-id="f7aa7-1699">2</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1699">2</span></span>                       |



 

## <a name="propertytagthumbnailprimarychromaticities"></a><span data-ttu-id="f7aa7-1700">PropertyTagThumbnailPrimaryChromaticities</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1700">PropertyTagThumbnailPrimaryChromaticities</span></span>

<span data-ttu-id="f7aa7-1701">Pour chacune des trois couleurs primaires dans l’image miniature, la chromatique de cette couleur.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1701">For each of the three primary colors in the thumbnail image, the chromaticity of that color.</span></span> <span data-ttu-id="f7aa7-1702">Voir aussi [PropertyTagPrimaryChromaticities](#propertytagprimarychromaticities).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1702">See also [PropertyTagPrimaryChromaticities](#propertytagprimarychromaticities).</span></span>



| <span data-ttu-id="f7aa7-1703">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1703">Property info</span></span> | <span data-ttu-id="f7aa7-1704">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1704">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-1705">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1705">Tag</span></span>   | <span data-ttu-id="f7aa7-1706">0x5036</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1706">0x5036</span></span>                  |
| <span data-ttu-id="f7aa7-1707">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1707">Type</span></span>  | <span data-ttu-id="f7aa7-1708">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1708">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-1709">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1709">Count</span></span> | <span data-ttu-id="f7aa7-1710">6</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1710">6</span></span>                       |



 

## <a name="propertytagthumbnailycbcrcoefficients"></a><span data-ttu-id="f7aa7-1711">PropertyTagThumbnailYCbCrCoefficients</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1711">PropertyTagThumbnailYCbCrCoefficients</span></span>

<span data-ttu-id="f7aa7-1712">Coefficients pour la transformation des données RVB en données YCbCr pour l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1712">Coefficients for transformation from RGB to YCbCr data for the thumbnail image.</span></span> <span data-ttu-id="f7aa7-1713">Voir aussi [PropertyTagYCbCrCoefficients](#propertytagycbcrcoefficients).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1713">See also [PropertyTagYCbCrCoefficients](#propertytagycbcrcoefficients).</span></span>



| <span data-ttu-id="f7aa7-1714">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1714">Property info</span></span> | <span data-ttu-id="f7aa7-1715">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1715">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-1716">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1716">Tag</span></span>   | <span data-ttu-id="f7aa7-1717">0x5037</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1717">0x5037</span></span>                  |
| <span data-ttu-id="f7aa7-1718">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1718">Type</span></span>  | <span data-ttu-id="f7aa7-1719">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1719">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-1720">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1720">Count</span></span> | <span data-ttu-id="f7aa7-1721">3</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1721">3</span></span>                       |



 

## <a name="propertytagthumbnailycbcrsubsampling"></a><span data-ttu-id="f7aa7-1722">PropertyTagThumbnailYCbCrSubsampling</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1722">PropertyTagThumbnailYCbCrSubsampling</span></span>

<span data-ttu-id="f7aa7-1723">Taux d’échantillonnage des composants de chrominance par rapport au composant luminance pour l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1723">Sampling ratio of chrominance components in relation to the luminance component for the thumbnail image.</span></span> <span data-ttu-id="f7aa7-1724">Voir aussi [PropertyTagYCbCrSubsampling](#propertytagycbcrsubsampling).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1724">See also [PropertyTagYCbCrSubsampling](#propertytagycbcrsubsampling).</span></span>



| <span data-ttu-id="f7aa7-1725">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1725">Property info</span></span> | <span data-ttu-id="f7aa7-1726">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1726">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1727">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1727">Tag</span></span>   | <span data-ttu-id="f7aa7-1728">0x5038</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1728">0x5038</span></span>               |
| <span data-ttu-id="f7aa7-1729">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1729">Type</span></span>  | <span data-ttu-id="f7aa7-1730">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1730">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1731">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1731">Count</span></span> | <span data-ttu-id="f7aa7-1732">2</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1732">2</span></span>                    |



 

## <a name="propertytagthumbnailycbcrpositioning"></a><span data-ttu-id="f7aa7-1733">PropertyTagThumbnailYCbCrPositioning</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1733">PropertyTagThumbnailYCbCrPositioning</span></span>

<span data-ttu-id="f7aa7-1734">Position des composants de chrominance par rapport au composant luminance pour l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1734">Position of chrominance components in relation to the luminance component for the thumbnail image.</span></span> <span data-ttu-id="f7aa7-1735">Voir aussi [PropertyTagYCbCrPositioning](#propertytagycbcrpositioning).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1735">See also [PropertyTagYCbCrPositioning](#propertytagycbcrpositioning).</span></span>



| <span data-ttu-id="f7aa7-1736">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1736">Property info</span></span> | <span data-ttu-id="f7aa7-1737">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1737">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1738">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1738">Tag</span></span>   | <span data-ttu-id="f7aa7-1739">0x5039</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1739">0x5039</span></span>               |
| <span data-ttu-id="f7aa7-1740">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1740">Type</span></span>  | <span data-ttu-id="f7aa7-1741">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1741">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1742">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1742">Count</span></span> | <span data-ttu-id="f7aa7-1743">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1743">1</span></span>                    |



 

## <a name="propertytagthumbnailrefblackwhite"></a><span data-ttu-id="f7aa7-1744">PropertyTagThumbnailRefBlackWhite</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1744">PropertyTagThumbnailRefBlackWhite</span></span>

<span data-ttu-id="f7aa7-1745">Valeur du point noir de référence et valeur du point blanc de référence pour l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1745">Reference black point value and reference white point value for the thumbnail image.</span></span> <span data-ttu-id="f7aa7-1746">Voir aussi [PropertyTagREFBlackWhite](#propertytagrefblackwhite).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1746">See also [PropertyTagREFBlackWhite](#propertytagrefblackwhite).</span></span>



| <span data-ttu-id="f7aa7-1747">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1747">Property info</span></span> | <span data-ttu-id="f7aa7-1748">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1748">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-1749">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1749">Tag</span></span>   | <span data-ttu-id="f7aa7-1750">0x503A</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1750">0x503A</span></span>                  |
| <span data-ttu-id="f7aa7-1751">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1751">Type</span></span>  | <span data-ttu-id="f7aa7-1752">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1752">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-1753">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1753">Count</span></span> | <span data-ttu-id="f7aa7-1754">6</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1754">6</span></span>                       |



 

## <a name="propertytagthumbnailcopyright"></a><span data-ttu-id="f7aa7-1755">PropertyTagThumbnailCopyRight</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1755">PropertyTagThumbnailCopyRight</span></span>

<span data-ttu-id="f7aa7-1756">Chaîne de caractères se terminant par un caractère null qui contient les informations de copyright pour l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1756">Null-terminated character string that contains copyright information for the thumbnail image.</span></span>



| <span data-ttu-id="f7aa7-1757">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1757">Property info</span></span> | <span data-ttu-id="f7aa7-1758">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1758">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-1759">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1759">Tag</span></span>   | <span data-ttu-id="f7aa7-1760">0x503B</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1760">0x503B</span></span>                                             |
| <span data-ttu-id="f7aa7-1761">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1761">Type</span></span>  | <span data-ttu-id="f7aa7-1762">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1762">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-1763">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1763">Count</span></span> | <span data-ttu-id="f7aa7-1764">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1764">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagluminancetable"></a><span data-ttu-id="f7aa7-1765">PropertyTagLuminanceTable</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1765">PropertyTagLuminanceTable</span></span>

<span data-ttu-id="f7aa7-1766">Table de luminance.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1766">Luminance table.</span></span> <span data-ttu-id="f7aa7-1767">La table de luminance et la table de chrominance sont utilisées pour contrôler la qualité JPEG.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1767">The luminance table and the chrominance table are used to control JPEG quality.</span></span> <span data-ttu-id="f7aa7-1768">Une table de luminance ou de chrominance valide a 64 entrées de type PropertyTagTypeShort.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1768">A valid luminance or chrominance table has 64 entries of type PropertyTagTypeShort.</span></span> <span data-ttu-id="f7aa7-1769">Si une image a une table de luminance ou une table de chrominance, elle doit avoir les deux tables.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1769">If an image has either a luminance table or a chrominance table, then it must have both tables.</span></span>



| <span data-ttu-id="f7aa7-1770">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1770">Property info</span></span> | <span data-ttu-id="f7aa7-1771">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1771">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1772">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1772">Tag</span></span>   | <span data-ttu-id="f7aa7-1773">0x5090</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1773">0x5090</span></span>               |
| <span data-ttu-id="f7aa7-1774">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1774">Type</span></span>  | <span data-ttu-id="f7aa7-1775">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1775">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1776">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1776">Count</span></span> | <span data-ttu-id="f7aa7-1777">64</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1777">64</span></span>                   |



 

## <a name="propertytagchrominancetable"></a><span data-ttu-id="f7aa7-1778">PropertyTagChrominanceTable</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1778">PropertyTagChrominanceTable</span></span>

<span data-ttu-id="f7aa7-1779">Table de chrominance.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1779">Chrominance table.</span></span> <span data-ttu-id="f7aa7-1780">La table de luminance et la table de chrominance sont utilisées pour contrôler la qualité JPEG.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1780">The luminance table and the chrominance table are used to control JPEG quality.</span></span> <span data-ttu-id="f7aa7-1781">Une table de luminance ou de chrominance valide a 64 entrées de type PropertyTagTypeShort.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1781">A valid luminance or chrominance table has 64 entries of type PropertyTagTypeShort.</span></span> <span data-ttu-id="f7aa7-1782">Si une image a une table de luminance ou une table de chrominance, elle doit avoir les deux tables.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1782">If an image has either a luminance table or a chrominance table, then it must have both tables.</span></span>



| <span data-ttu-id="f7aa7-1783">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1783">Property info</span></span> | <span data-ttu-id="f7aa7-1784">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1784">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1785">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1785">Tag</span></span>   | <span data-ttu-id="f7aa7-1786">0x5091</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1786">0x5091</span></span>               |
| <span data-ttu-id="f7aa7-1787">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1787">Type</span></span>  | <span data-ttu-id="f7aa7-1788">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1788">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1789">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1789">Count</span></span> | <span data-ttu-id="f7aa7-1790">64</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1790">64</span></span>                   |



 

## <a name="propertytagframedelay"></a><span data-ttu-id="f7aa7-1791">PropertyTagFrameDelay</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1791">PropertyTagFrameDelay</span></span>

<span data-ttu-id="f7aa7-1792">Délai, en centièmes de seconde, entre deux frames dans une image GIF animée.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1792">Time delay, in hundredths of a second, between two frames in an animated GIF image.</span></span>



| <span data-ttu-id="f7aa7-1793">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1793">Property info</span></span> | <span data-ttu-id="f7aa7-1794">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1794">Value</span></span> |
|-------|-------------------------------|
| <span data-ttu-id="f7aa7-1795">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1795">Tag</span></span>   | <span data-ttu-id="f7aa7-1796">0x5100</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1796">0x5100</span></span>                        |
| <span data-ttu-id="f7aa7-1797">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1797">Type</span></span>  | <span data-ttu-id="f7aa7-1798">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1798">PropertyTagTypeLong</span></span>           |
| <span data-ttu-id="f7aa7-1799">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1799">Count</span></span> | <span data-ttu-id="f7aa7-1800">Nombre de frames dans l’image</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1800">Number of frames in the image</span></span> |



 

## <a name="propertytagloopcount"></a><span data-ttu-id="f7aa7-1801">PropertyTagLoopCount</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1801">PropertyTagLoopCount</span></span>

<span data-ttu-id="f7aa7-1802">Pour une image GIF animée, le nombre d’affichages de l’animation.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1802">For an animated GIF image, the number of times to display the animation.</span></span> <span data-ttu-id="f7aa7-1803">La valeur 0 spécifie que l’animation doit être affichée de façon infinie.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1803">A value of 0 specifies that the animation should be displayed infinitely.</span></span>



| <span data-ttu-id="f7aa7-1804">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1804">Property info</span></span> | <span data-ttu-id="f7aa7-1805">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1805">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1806">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1806">Tag</span></span>   | <span data-ttu-id="f7aa7-1807">0x5101</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1807">0x5101</span></span>               |
| <span data-ttu-id="f7aa7-1808">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1808">Type</span></span>  | <span data-ttu-id="f7aa7-1809">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1809">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1810">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1810">Count</span></span> | <span data-ttu-id="f7aa7-1811">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1811">1</span></span>                    |



 

## <a name="propertytagglobalpalette"></a><span data-ttu-id="f7aa7-1812">PropertyTagGlobalPalette</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1812">PropertyTagGlobalPalette</span></span>

<span data-ttu-id="f7aa7-1813">Palette de couleurs pour une bitmap indexée dans une image GIF.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1813">Color palette for an indexed bitmap in a GIF image.</span></span>



| <span data-ttu-id="f7aa7-1814">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1814">Property info</span></span> | <span data-ttu-id="f7aa7-1815">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1815">Value</span></span> |
|-------|-------------------------------|
| <span data-ttu-id="f7aa7-1816">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1816">Tag</span></span>   | <span data-ttu-id="f7aa7-1817">0x5102</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1817">0x5102</span></span>                        |
| <span data-ttu-id="f7aa7-1818">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1818">Type</span></span>  | <span data-ttu-id="f7aa7-1819">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1819">PropertyTagTypeByte</span></span>           |
| <span data-ttu-id="f7aa7-1820">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1820">Count</span></span> | <span data-ttu-id="f7aa7-1821">3 x nombre d’entrées de palette</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1821">3 x number of palette entries</span></span> |



 

## <a name="propertytagindexbackground"></a><span data-ttu-id="f7aa7-1822">PropertyTagIndexBackground</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1822">PropertyTagIndexBackground</span></span>

<span data-ttu-id="f7aa7-1823">Index de la couleur d’arrière-plan dans la palette d’une image GIF.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1823">Index of the background color in the palette of a GIF image.</span></span>



| <span data-ttu-id="f7aa7-1824">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1824">Property info</span></span> | <span data-ttu-id="f7aa7-1825">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1825">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-1826">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1826">Tag</span></span>   | <span data-ttu-id="f7aa7-1827">0x5103</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1827">0x5103</span></span>              |
| <span data-ttu-id="f7aa7-1828">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1828">Type</span></span>  | <span data-ttu-id="f7aa7-1829">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1829">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="f7aa7-1830">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1830">Count</span></span> | <span data-ttu-id="f7aa7-1831">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1831">1</span></span>                   |



 

## <a name="propertytagindextransparent"></a><span data-ttu-id="f7aa7-1832">PropertyTagIndexTransparent</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1832">PropertyTagIndexTransparent</span></span>

<span data-ttu-id="f7aa7-1833">Index de la couleur transparente dans la palette d’une image GIF.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1833">Index of the transparent color in the palette of a GIF image.</span></span>



| <span data-ttu-id="f7aa7-1834">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1834">Property info</span></span> | <span data-ttu-id="f7aa7-1835">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1835">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-1836">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1836">Tag</span></span>   | <span data-ttu-id="f7aa7-1837">0x5104</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1837">0x5104</span></span>              |
| <span data-ttu-id="f7aa7-1838">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1838">Type</span></span>  | <span data-ttu-id="f7aa7-1839">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1839">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="f7aa7-1840">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1840">Count</span></span> | <span data-ttu-id="f7aa7-1841">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1841">1</span></span>                   |



 

## <a name="propertytagpixelunit"></a><span data-ttu-id="f7aa7-1842">PropertyTagPixelUnit</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1842">PropertyTagPixelUnit</span></span>

<span data-ttu-id="f7aa7-1843">Unité pour PropertyTagPixelPerUnitX et PropertyTagPixelPerUnitY.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1843">Unit for PropertyTagPixelPerUnitX and PropertyTagPixelPerUnitY.</span></span>



<span data-ttu-id="f7aa7-1844">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1844">Tag</span></span>

<span data-ttu-id="f7aa7-1845">0x5110</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1845">0x5110</span></span>

<span data-ttu-id="f7aa7-1846">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1846">Type</span></span>

<span data-ttu-id="f7aa7-1847">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1847">PropertyTagTypeByte</span></span>

<span data-ttu-id="f7aa7-1848">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1848">Count</span></span>

<span data-ttu-id="f7aa7-1849">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1849">1</span></span>

<span data-ttu-id="f7aa7-1850">0-Inconnu</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1850">0 - unknown</span></span>



 

## <a name="propertytagpixelperunitx"></a><span data-ttu-id="f7aa7-1851">PropertyTagPixelPerUnitX</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1851">PropertyTagPixelPerUnitX</span></span>

<span data-ttu-id="f7aa7-1852">Pixels par unité sur l’axe x.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1852">Pixels per unit in the x direction.</span></span>



| <span data-ttu-id="f7aa7-1853">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1853">Property info</span></span> | <span data-ttu-id="f7aa7-1854">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1854">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-1855">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1855">Tag</span></span>   | <span data-ttu-id="f7aa7-1856">0x5111</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1856">0x5111</span></span>              |
| <span data-ttu-id="f7aa7-1857">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1857">Type</span></span>  | <span data-ttu-id="f7aa7-1858">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1858">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-1859">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1859">Count</span></span> | <span data-ttu-id="f7aa7-1860">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1860">1</span></span>                   |



 

## <a name="propertytagpixelperunity"></a><span data-ttu-id="f7aa7-1861">PropertyTagPixelPerUnitY</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1861">PropertyTagPixelPerUnitY</span></span>

<span data-ttu-id="f7aa7-1862">Pixels par unité dans l’axe y.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1862">Pixels per unit in the y direction.</span></span>



| <span data-ttu-id="f7aa7-1863">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1863">Property info</span></span> | <span data-ttu-id="f7aa7-1864">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1864">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-1865">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1865">Tag</span></span>   | <span data-ttu-id="f7aa7-1866">0x5112</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1866">0x5112</span></span>              |
| <span data-ttu-id="f7aa7-1867">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1867">Type</span></span>  | <span data-ttu-id="f7aa7-1868">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1868">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-1869">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1869">Count</span></span> | <span data-ttu-id="f7aa7-1870">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1870">1</span></span>                   |



 

## <a name="propertytagpalettehistogram"></a><span data-ttu-id="f7aa7-1871">PropertyTagPaletteHistogram</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1871">PropertyTagPaletteHistogram</span></span>

<span data-ttu-id="f7aa7-1872">Histogramme de la palette.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1872">Palette histogram.</span></span>



| <span data-ttu-id="f7aa7-1873">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1873">Property info</span></span> | <span data-ttu-id="f7aa7-1874">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1874">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-1875">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1875">Tag</span></span>   | <span data-ttu-id="f7aa7-1876">0x5113</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1876">0x5113</span></span>                  |
| <span data-ttu-id="f7aa7-1877">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1877">Type</span></span>  | <span data-ttu-id="f7aa7-1878">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1878">PropertyTagTypeByte</span></span>     |
| <span data-ttu-id="f7aa7-1879">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1879">Count</span></span> | <span data-ttu-id="f7aa7-1880">Longueur de l’histogramme</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1880">Length of the histogram</span></span> |



 

## <a name="propertytagcopyright"></a><span data-ttu-id="f7aa7-1881">PropertyTagCopyright</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1881">PropertyTagCopyright</span></span>

<span data-ttu-id="f7aa7-1882">Chaîne de caractères se terminant par un caractère null qui contient des informations de copyright.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1882">Null-terminated character string that contains copyright information.</span></span>



| <span data-ttu-id="f7aa7-1883">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1883">Property info</span></span> | <span data-ttu-id="f7aa7-1884">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1884">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-1885">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1885">Tag</span></span>   | <span data-ttu-id="f7aa7-1886">0x8298</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1886">0x8298</span></span>                                             |
| <span data-ttu-id="f7aa7-1887">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1887">Type</span></span>  | <span data-ttu-id="f7aa7-1888">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1888">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-1889">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1889">Count</span></span> | <span data-ttu-id="f7aa7-1890">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1890">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifexposuretime"></a><span data-ttu-id="f7aa7-1891">PropertyTagExifExposureTime</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1891">PropertyTagExifExposureTime</span></span>

<span data-ttu-id="f7aa7-1892">Temps d’exposition, mesuré en secondes.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1892">Exposure time, measured in seconds.</span></span>



| <span data-ttu-id="f7aa7-1893">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1893">Property info</span></span> | <span data-ttu-id="f7aa7-1894">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1894">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-1895">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1895">Tag</span></span>   | <span data-ttu-id="f7aa7-1896">0x829A</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1896">0x829A</span></span>                  |
| <span data-ttu-id="f7aa7-1897">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1897">Type</span></span>  | <span data-ttu-id="f7aa7-1898">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1898">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-1899">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1899">Count</span></span> | <span data-ttu-id="f7aa7-1900">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1900">1</span></span>                       |



 

## <a name="propertytagexiffnumber"></a><span data-ttu-id="f7aa7-1901">PropertyTagExifFNumber</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1901">PropertyTagExifFNumber</span></span>

<span data-ttu-id="f7aa7-1902">Numéro F.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1902">F number.</span></span>



| <span data-ttu-id="f7aa7-1903">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1903">Property info</span></span> | <span data-ttu-id="f7aa7-1904">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1904">Value</span></span> |
|-------|----------|
| <span data-ttu-id="f7aa7-1905">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1905">Tag</span></span>   | <span data-ttu-id="f7aa7-1906">0x829D</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1906">0x829D</span></span>   |
| <span data-ttu-id="f7aa7-1907">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1907">Type</span></span>  | <span data-ttu-id="f7aa7-1908">RATIONNELLE</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1908">RATIONAL</span></span> |
| <span data-ttu-id="f7aa7-1909">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1909">Count</span></span> | <span data-ttu-id="f7aa7-1910">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1910">1</span></span>        |



 

## <a name="propertytagexififd"></a><span data-ttu-id="f7aa7-1911">PropertyTagExifIFD</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1911">PropertyTagExifIFD</span></span>

<span data-ttu-id="f7aa7-1912">Balise privée utilisée par GDI+.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1912">Private tag used by GDI+.</span></span> <span data-ttu-id="f7aa7-1913">Pas d’usage public.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1913">Not for public use.</span></span> <span data-ttu-id="f7aa7-1914">GDI+ utilise cette balise pour localiser des informations spécifiques à EXIF.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1914">GDI+ uses this tag to locate Exif-specific information.</span></span>



| <span data-ttu-id="f7aa7-1915">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1915">Property info</span></span> | <span data-ttu-id="f7aa7-1916">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1916">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-1917">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1917">Tag</span></span>   | <span data-ttu-id="f7aa7-1918">0x8769</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1918">0x8769</span></span>              |
| <span data-ttu-id="f7aa7-1919">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1919">Type</span></span>  | <span data-ttu-id="f7aa7-1920">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1920">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-1921">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1921">Count</span></span> | <span data-ttu-id="f7aa7-1922">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1922">1</span></span>                   |



 

## <a name="propertytagiccprofile"></a><span data-ttu-id="f7aa7-1923">PropertyTagICCProfile</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1923">PropertyTagICCProfile</span></span>

<span data-ttu-id="f7aa7-1924">Profil ICC incorporé dans l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1924">ICC profile embedded in the image.</span></span>



| <span data-ttu-id="f7aa7-1925">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1925">Property info</span></span> | <span data-ttu-id="f7aa7-1926">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1926">Value</span></span> |
|-------|-----------------------|
| <span data-ttu-id="f7aa7-1927">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1927">Tag</span></span>   | <span data-ttu-id="f7aa7-1928">0x8773</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1928">0x8773</span></span>                |
| <span data-ttu-id="f7aa7-1929">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1929">Type</span></span>  | <span data-ttu-id="f7aa7-1930">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1930">PropertyTagTypeByte</span></span>   |
| <span data-ttu-id="f7aa7-1931">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1931">Count</span></span> | <span data-ttu-id="f7aa7-1932">Longueur du profil</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1932">Length of the profile</span></span> |



 

## <a name="propertytagexifexposureprog"></a><span data-ttu-id="f7aa7-1933">PropertyTagExifExposureProg</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1933">PropertyTagExifExposureProg</span></span>

<span data-ttu-id="f7aa7-1934">Classe du programme utilisée par l’appareil photo pour définir l’exposition lorsque l’image est prise.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1934">Class of the program used by the camera to set exposure when the picture is taken.</span></span>



<span data-ttu-id="f7aa7-1935">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1935">Tag</span></span>

<span data-ttu-id="f7aa7-1936">0x8822</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1936">0x8822</span></span>

<span data-ttu-id="f7aa7-1937">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1937">Type</span></span>

<span data-ttu-id="f7aa7-1938">SHORT</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1938">SHORT</span></span>

<span data-ttu-id="f7aa7-1939">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1939">Count</span></span>

<span data-ttu-id="f7aa7-1940">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1940">1</span></span>

<span data-ttu-id="f7aa7-1941">Default</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1941">Default</span></span>

<span data-ttu-id="f7aa7-1942">0</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1942">0</span></span>

<span data-ttu-id="f7aa7-1943">0-non défini 1-Manuel 2-programme normal 3-priorité 4-priorité 5-programme créatif (en faveur de la profondeur du champ) 6-Programme d’action (biaisé vers rapide) Vitesse d’obturation) 7-mode Portrait (pour les photos de plus haut en arrière-plan) 8-mode paysage (pour les photos en mode paysage avec l’arrière-plan) 9 à 255-réservé</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1943">0 - not defined 1 - manual 2 - normal program 3 - aperture priority 4 - shutter priority 5 - creative program (biased toward depth of field) 6 - action program (biased toward fast shutter speed) 7 - portrait mode (for close-up photos with the background out of focus) 8 - landscape mode (for landscape photos with the background in focus) 9 to 255 - reserved</span></span>



 

## <a name="propertytagexifspectralsense"></a><span data-ttu-id="f7aa7-1944">PropertyTagExifSpectralSense</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1944">PropertyTagExifSpectralSense</span></span>

<span data-ttu-id="f7aa7-1945">Chaîne de caractères se terminant par un caractère null qui spécifie la sensibilité spectrale de chaque canal de l’appareil photo utilisé.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1945">Null-terminated character string that specifies the spectral sensitivity of each channel of the camera used.</span></span> <span data-ttu-id="f7aa7-1946">La chaîne est compatible avec la norme développée par le Comité technique ASTM.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1946">The string is compatible with the standard developed by the ASTM Technical Committee.</span></span>



| <span data-ttu-id="f7aa7-1947">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1947">Property info</span></span> | <span data-ttu-id="f7aa7-1948">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1948">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-1949">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1949">Tag</span></span>   | <span data-ttu-id="f7aa7-1950">0x8824</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1950">0x8824</span></span>                                             |
| <span data-ttu-id="f7aa7-1951">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1951">Type</span></span>  | <span data-ttu-id="f7aa7-1952">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1952">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-1953">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1953">Count</span></span> | <span data-ttu-id="f7aa7-1954">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1954">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsifd"></a><span data-ttu-id="f7aa7-1955">PropertyTagGpsIFD</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1955">PropertyTagGpsIFD</span></span>

<span data-ttu-id="f7aa7-1956">Décalage d’un bloc d’éléments de propriété GPS.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1956">Offset to a block of GPS property items.</span></span> <span data-ttu-id="f7aa7-1957">Les éléments de propriété dont les balises ont le préfixe PropertyTagGps sont stockés dans le bloc GPS.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1957">Property items whose tags have the prefix PropertyTagGps are stored in the GPS block.</span></span> <span data-ttu-id="f7aa7-1958">Les éléments de propriété GPS sont définis dans la spécification EXIF.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1958">The GPS property items are defined in the EXIF specification.</span></span> <span data-ttu-id="f7aa7-1959">GDI+ utilise cette balise pour localiser les informations GPS, mais GDI+ n’expose pas cette balise pour une utilisation publique.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1959">GDI+ uses this tag to locate GPS information, but GDI+ does not expose this tag for public use.</span></span>



| <span data-ttu-id="f7aa7-1960">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1960">Property info</span></span> | <span data-ttu-id="f7aa7-1961">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1961">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-1962">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1962">Tag</span></span>   | <span data-ttu-id="f7aa7-1963">0x8825</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1963">0x8825</span></span>              |
| <span data-ttu-id="f7aa7-1964">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1964">Type</span></span>  | <span data-ttu-id="f7aa7-1965">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1965">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-1966">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1966">Count</span></span> | <span data-ttu-id="f7aa7-1967">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1967">1</span></span>                   |



 

## <a name="propertytagexifisospeed"></a><span data-ttu-id="f7aa7-1968">PropertyTagExifISOSpeed</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1968">PropertyTagExifISOSpeed</span></span>

<span data-ttu-id="f7aa7-1969">Vitesse ISO et ISO latitude de l’appareil photo ou de l’appareil d’entrée comme spécifié dans la norme ISO 12232.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1969">ISO speed and ISO latitude of the camera or input device as specified in ISO 12232.</span></span>



| <span data-ttu-id="f7aa7-1970">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1970">Property info</span></span> | <span data-ttu-id="f7aa7-1971">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1971">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-1972">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1972">Tag</span></span>   | <span data-ttu-id="f7aa7-1973">0x8827</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1973">0x8827</span></span>               |
| <span data-ttu-id="f7aa7-1974">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1974">Type</span></span>  | <span data-ttu-id="f7aa7-1975">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1975">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-1976">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1976">Count</span></span> | <span data-ttu-id="f7aa7-1977">Quelconque</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1977">Any</span></span>                  |



 

## <a name="propertytagexifoecf"></a><span data-ttu-id="f7aa7-1978">PropertyTagExifOECF</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1978">PropertyTagExifOECF</span></span>

<span data-ttu-id="f7aa7-1979">Fonction de conversion optoélectronique (OECF) spécifiée dans ISO 14524.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1979">Optoelectronic conversion function (OECF) specified in ISO 14524.</span></span> <span data-ttu-id="f7aa7-1980">Le OECF est la relation entre l’entrée optique de l’appareil photo et les valeurs de l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1980">The OECF is the relationship between the camera optical input and the image values.</span></span>



| <span data-ttu-id="f7aa7-1981">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1981">Property info</span></span> | <span data-ttu-id="f7aa7-1982">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1982">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="f7aa7-1983">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1983">Tag</span></span>   | <span data-ttu-id="f7aa7-1984">0x8828</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1984">0x8828</span></span>                   |
| <span data-ttu-id="f7aa7-1985">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1985">Type</span></span>  | <span data-ttu-id="f7aa7-1986">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1986">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="f7aa7-1987">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1987">Count</span></span> | <span data-ttu-id="f7aa7-1988">Quelconque</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1988">Any</span></span>                      |



 

## <a name="propertytagexifver"></a><span data-ttu-id="f7aa7-1989">PropertyTagExifVer</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1989">PropertyTagExifVer</span></span>

<span data-ttu-id="f7aa7-1990">Version de la norme EXIF prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1990">Version of the EXIF standard supported.</span></span> <span data-ttu-id="f7aa7-1991">L’absence de ce champ est utilisée pour signifier la non-conformité à la norme.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1991">Nonexistence of this field is taken to mean nonconformance to the standard.</span></span> <span data-ttu-id="f7aa7-1992">La conformité à la norme est indiquée par l’enregistrement de 0210 sous la forme d’une chaîne ASCII sur 4 octets.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1992">Conformance to the standard is indicated by recording 0210 as a 4-byte ASCII string.</span></span> <span data-ttu-id="f7aa7-1993">Étant donné que le type est PropertyTagTypeUndefined, il n’y a aucune marque de fin NULL.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1993">Because the type is PropertyTagTypeUndefined, there is no NULL terminator.</span></span>



| <span data-ttu-id="f7aa7-1994">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1994">Property info</span></span> | <span data-ttu-id="f7aa7-1995">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1995">Value</span></span> |
|---------|--------------------------|
| <span data-ttu-id="f7aa7-1996">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1996">Tag</span></span>     | <span data-ttu-id="f7aa7-1997">0x9000</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1997">0x9000</span></span>                   |
| <span data-ttu-id="f7aa7-1998">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1998">Type</span></span>    | <span data-ttu-id="f7aa7-1999">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="f7aa7-1999">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="f7aa7-2000">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2000">Count</span></span>   | <span data-ttu-id="f7aa7-2001">4</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2001">4</span></span>                        |
| <span data-ttu-id="f7aa7-2002">Default</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2002">Default</span></span> | <span data-ttu-id="f7aa7-2003">0210</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2003">0210</span></span>                     |



 

## <a name="propertytagexifdtorig"></a><span data-ttu-id="f7aa7-2004">PropertyTagExifDTOrig</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2004">PropertyTagExifDTOrig</span></span>

<span data-ttu-id="f7aa7-2005">Date et heure de génération des données de l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2005">Date and time when the original image data was generated.</span></span> <span data-ttu-id="f7aa7-2006">Pour un DSC, date et heure auxquelles l’image a été prise.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2006">For a DSC, the date and time when the picture was taken.</span></span> <span data-ttu-id="f7aa7-2007">Le format est YYYY : MM : JJ HH : MM : SS avec l’heure affichée au format 24 heures et la date et l’heure séparées par un caractère vide (0x2000).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2007">The format is YYYY:MM:DD HH:MM:SS with time shown in 24-hour format and the date and time separated by one blank character (0x2000).</span></span> <span data-ttu-id="f7aa7-2008">La longueur de la chaîne de caractères est de 20 octets, y compris le terminateur NULL.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2008">The character string length is 20 bytes including the NULL terminator.</span></span> <span data-ttu-id="f7aa7-2009">Lorsque le champ est vide, il est considéré comme inconnu.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2009">When the field is empty, it is treated as unknown.</span></span>



| <span data-ttu-id="f7aa7-2010">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2010">Property info</span></span> | <span data-ttu-id="f7aa7-2011">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2011">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-2012">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2012">Tag</span></span>   | <span data-ttu-id="f7aa7-2013">0x9003</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2013">0x9003</span></span>               |
| <span data-ttu-id="f7aa7-2014">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2014">Type</span></span>  | <span data-ttu-id="f7aa7-2015">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2015">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="f7aa7-2016">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2016">Count</span></span> | <span data-ttu-id="f7aa7-2017">20</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2017">20</span></span>                   |



 

## <a name="propertytagexifdtdigitized"></a><span data-ttu-id="f7aa7-2018">PropertyTagExifDTDigitized</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2018">PropertyTagExifDTDigitized</span></span>

<span data-ttu-id="f7aa7-2019">Date et heure auxquelles l’image a été stockée en tant que données numériques.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2019">Date and time when the image was stored as digital data.</span></span> <span data-ttu-id="f7aa7-2020">Si, par exemple, une image a été capturée par DSC et qu’au même moment, le fichier a été enregistré, DateTimeOriginal et DateTimeDigitized auront le même contenu.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2020">If, for example, an image was captured by DSC and at the same time the file was recorded, then DateTimeOriginal and DateTimeDigitized will have the same contents.</span></span>

<span data-ttu-id="f7aa7-2021">Le format est YYYY : MM : JJ HH : MM : SS avec l’heure affichée au format 24 heures et la date et l’heure séparées par un caractère vide (0x2000).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2021">The format is YYYY:MM:DD HH:MM:SS with time shown in 24-hour format and the date and time separated by one blank character (0x2000).</span></span> <span data-ttu-id="f7aa7-2022">La longueur de la chaîne de caractères est de 20 octets, y compris le terminateur NULL.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2022">The character string length is 20 bytes including the NULL terminator.</span></span> <span data-ttu-id="f7aa7-2023">Lorsque le champ est vide, il est considéré comme inconnu.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2023">When the field is empty, it is treated as unknown.</span></span>



| <span data-ttu-id="f7aa7-2024">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2024">Property info</span></span> | <span data-ttu-id="f7aa7-2025">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2025">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-2026">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2026">Tag</span></span>   | <span data-ttu-id="f7aa7-2027">0x9004</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2027">0x9004</span></span>               |
| <span data-ttu-id="f7aa7-2028">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2028">Type</span></span>  | <span data-ttu-id="f7aa7-2029">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2029">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="f7aa7-2030">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2030">Count</span></span> | <span data-ttu-id="f7aa7-2031">20</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2031">20</span></span>                   |



 

## <a name="propertytagexifcompconfig"></a><span data-ttu-id="f7aa7-2032">PropertyTagExifCompConfig</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2032">PropertyTagExifCompConfig</span></span>

<span data-ttu-id="f7aa7-2033">Informations spécifiques aux données compressées.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2033">Information specific to compressed data.</span></span> <span data-ttu-id="f7aa7-2034">Les canaux de chaque composant sont organisés dans l’ordre du premier composant au quatrième.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2034">The channels of each component are arranged in order from the first component to the fourth.</span></span> <span data-ttu-id="f7aa7-2035">Pour les données non compressées, la disposition des données est indiquée dans la balise PropertyTagPhotometricInterp.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2035">For uncompressed data, the data arrangement is given in the PropertyTagPhotometricInterp tag.</span></span>

<span data-ttu-id="f7aa7-2036">Toutefois, étant donné que PropertyTagPhotometricInterp peut uniquement exprimer l’ordre de Y, CB et CR, cette balise est fournie pour les cas où les données compressées utilisent des composants autres que Y, CB et CR et pour prendre en charge d’autres séquences.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2036">However, because PropertyTagPhotometricInterp can only express the order of Y, Cb, and Cr, this tag is provided for cases when compressed data uses components other than Y, Cb, and Cr and to support other sequences.</span></span>



<span data-ttu-id="f7aa7-2037">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2037">Tag</span></span>

<span data-ttu-id="f7aa7-2038">0x9101</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2038">0x9101</span></span>

<span data-ttu-id="f7aa7-2039">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2039">Type</span></span>

<span data-ttu-id="f7aa7-2040">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2040">PropertyTagTypeUndefined</span></span>

<span data-ttu-id="f7aa7-2041">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2041">Count</span></span>

<span data-ttu-id="f7aa7-2042">4</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2042">4</span></span>

<span data-ttu-id="f7aa7-2043">Default</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2043">Default</span></span>

<span data-ttu-id="f7aa7-2044">4 5 6 0 (si RVB non compressé) 1 2 3 0 (autres cas)</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2044">4 5 6 0 (if RGB uncompressed) 1 2 3 0 (other cases)</span></span>

<span data-ttu-id="f7aa7-2045">0-n’existe pas 1-Y 2-CB 3-CR 4-R 5-G 6-B autre-réservé</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2045">0 - does not exist 1 - Y 2 - Cb 3 - Cr 4 - R 5 - G 6 - B Other - reserved</span></span>



 

## <a name="propertytagexifcompbpp"></a><span data-ttu-id="f7aa7-2046">PropertyTagExifCompBPP</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2046">PropertyTagExifCompBPP</span></span>

<span data-ttu-id="f7aa7-2047">Informations spécifiques aux données compressées.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2047">Information specific to compressed data.</span></span> <span data-ttu-id="f7aa7-2048">Le mode de compression utilisé pour une image compressée est indiqué dans unités BPP.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2048">The compression mode used for a compressed image is indicated in unit BPP.</span></span>



| <span data-ttu-id="f7aa7-2049">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2049">Property info</span></span> | <span data-ttu-id="f7aa7-2050">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2050">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-2051">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2051">Tag</span></span>   | <span data-ttu-id="f7aa7-2052">0x9102</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2052">0x9102</span></span>                  |
| <span data-ttu-id="f7aa7-2053">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2053">Type</span></span>  | <span data-ttu-id="f7aa7-2054">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2054">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-2055">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2055">Count</span></span> | <span data-ttu-id="f7aa7-2056">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2056">1</span></span>                       |



 

## <a name="propertytagexifshutterspeed"></a><span data-ttu-id="f7aa7-2057">PropertyTagExifShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2057">PropertyTagExifShutterSpeed</span></span>

<span data-ttu-id="f7aa7-2058">Vitesse d’obturation.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2058">Shutter speed.</span></span> <span data-ttu-id="f7aa7-2059">L’unité est la valeur système additive de l’exposition photographique (APEX).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2059">The unit is the Additive System of Photographic Exposure (APEX) value.</span></span>



| <span data-ttu-id="f7aa7-2060">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2060">Property info</span></span> | <span data-ttu-id="f7aa7-2061">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2061">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="f7aa7-2062">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2062">Tag</span></span>   | <span data-ttu-id="f7aa7-2063">0x9201</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2063">0x9201</span></span>                   |
| <span data-ttu-id="f7aa7-2064">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2064">Type</span></span>  | <span data-ttu-id="f7aa7-2065">PropertyTagTypeSRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2065">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="f7aa7-2066">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2066">Count</span></span> | <span data-ttu-id="f7aa7-2067">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2067">1</span></span>                        |



 

## <a name="propertytagexifaperture"></a><span data-ttu-id="f7aa7-2068">PropertyTagExifAperture</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2068">PropertyTagExifAperture</span></span>

<span data-ttu-id="f7aa7-2069">Ouverture de l’objectif.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2069">Lens aperture.</span></span> <span data-ttu-id="f7aa7-2070">L’unité est la valeur APEX.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2070">The unit is the APEX value.</span></span>



| <span data-ttu-id="f7aa7-2071">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2071">Property info</span></span> | <span data-ttu-id="f7aa7-2072">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2072">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-2073">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2073">Tag</span></span>   | <span data-ttu-id="f7aa7-2074">0x9202</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2074">0x9202</span></span>                  |
| <span data-ttu-id="f7aa7-2075">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2075">Type</span></span>  | <span data-ttu-id="f7aa7-2076">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2076">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-2077">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2077">Count</span></span> | <span data-ttu-id="f7aa7-2078">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2078">1</span></span>                       |



 

## <a name="propertytagexifbrightness"></a><span data-ttu-id="f7aa7-2079">PropertyTagExifBrightness</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2079">PropertyTagExifBrightness</span></span>

<span data-ttu-id="f7aa7-2080">Valeur de luminosité.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2080">Brightness value.</span></span> <span data-ttu-id="f7aa7-2081">L’unité est la valeur APEX.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2081">The unit is the APEX value.</span></span> <span data-ttu-id="f7aa7-2082">En règle générale, elle est indiquée dans la plage de-99,99 à 99,99.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2082">Ordinarily it is given in the range of -99.99 to 99.99.</span></span>



| <span data-ttu-id="f7aa7-2083">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2083">Property info</span></span> | <span data-ttu-id="f7aa7-2084">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2084">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="f7aa7-2085">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2085">Tag</span></span>   | <span data-ttu-id="f7aa7-2086">0x9203</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2086">0x9203</span></span>                   |
| <span data-ttu-id="f7aa7-2087">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2087">Type</span></span>  | <span data-ttu-id="f7aa7-2088">PropertyTagTypeSRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2088">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="f7aa7-2089">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2089">Count</span></span> | <span data-ttu-id="f7aa7-2090">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2090">1</span></span>                        |



 

## <a name="propertytagexifexposurebias"></a><span data-ttu-id="f7aa7-2091">PropertyTagExifExposureBias</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2091">PropertyTagExifExposureBias</span></span>

<span data-ttu-id="f7aa7-2092">Décalage de l’exposition.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2092">Exposure bias.</span></span> <span data-ttu-id="f7aa7-2093">L’unité est la valeur APEX.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2093">The unit is the APEX value.</span></span> <span data-ttu-id="f7aa7-2094">En règle générale, elle est comprise entre-99,99 et 99,99.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2094">Ordinarily it is given in the range -99.99 to 99.99.</span></span>



| <span data-ttu-id="f7aa7-2095">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2095">Property info</span></span> | <span data-ttu-id="f7aa7-2096">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2096">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="f7aa7-2097">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2097">Tag</span></span>   | <span data-ttu-id="f7aa7-2098">0x9204</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2098">0x9204</span></span>                   |
| <span data-ttu-id="f7aa7-2099">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2099">Type</span></span>  | <span data-ttu-id="f7aa7-2100">PropertyTagTypeSRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2100">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="f7aa7-2101">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2101">Count</span></span> | <span data-ttu-id="f7aa7-2102">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2102">1</span></span>                        |



 

## <a name="propertytagexifmaxaperture"></a><span data-ttu-id="f7aa7-2103">PropertyTagExifMaxAperture</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2103">PropertyTagExifMaxAperture</span></span>

<span data-ttu-id="f7aa7-2104">Plus petit numéro F de la lentille.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2104">Smallest F number of the lens.</span></span> <span data-ttu-id="f7aa7-2105">L’unité est la valeur APEX.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2105">The unit is the APEX value.</span></span> <span data-ttu-id="f7aa7-2106">En règle générale, elle est comprise dans la plage de 00,00 à 99,99, mais elle n’est pas limitée à cette plage.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2106">Ordinarily it is given in the range of 00.00 to 99.99, but it is not limited to this range.</span></span>



| <span data-ttu-id="f7aa7-2107">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2107">Property info</span></span> | <span data-ttu-id="f7aa7-2108">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2108">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-2109">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2109">Tag</span></span>   | <span data-ttu-id="f7aa7-2110">0x9205</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2110">0x9205</span></span>                  |
| <span data-ttu-id="f7aa7-2111">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2111">Type</span></span>  | <span data-ttu-id="f7aa7-2112">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2112">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-2113">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2113">Count</span></span> | <span data-ttu-id="f7aa7-2114">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2114">1</span></span>                       |



 

## <a name="propertytagexifsubjectdist"></a><span data-ttu-id="f7aa7-2115">PropertyTagExifSubjectDist</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2115">PropertyTagExifSubjectDist</span></span>

<span data-ttu-id="f7aa7-2116">Distance à l’objet, mesurée en mètres.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2116">Distance to the subject, measured in meters.</span></span>



| <span data-ttu-id="f7aa7-2117">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2117">Property info</span></span> | <span data-ttu-id="f7aa7-2118">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2118">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-2119">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2119">Tag</span></span>   | <span data-ttu-id="f7aa7-2120">0x9206</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2120">0x9206</span></span>                  |
| <span data-ttu-id="f7aa7-2121">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2121">Type</span></span>  | <span data-ttu-id="f7aa7-2122">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2122">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-2123">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2123">Count</span></span> | <span data-ttu-id="f7aa7-2124">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2124">1</span></span>                       |



 

## <a name="propertytagexifmeteringmode"></a><span data-ttu-id="f7aa7-2125">PropertyTagExifMeteringMode</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2125">PropertyTagExifMeteringMode</span></span>

<span data-ttu-id="f7aa7-2126">Mode de contrôle.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2126">Metering mode.</span></span>



<span data-ttu-id="f7aa7-2127">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2127">Tag</span></span>

<span data-ttu-id="f7aa7-2128">0x9207</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2128">0x9207</span></span>

<span data-ttu-id="f7aa7-2129">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2129">Type</span></span>

<span data-ttu-id="f7aa7-2130">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2130">PropertyTagTypeShort</span></span>

<span data-ttu-id="f7aa7-2131">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2131">Count</span></span>

<span data-ttu-id="f7aa7-2132">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2132">1</span></span>

<span data-ttu-id="f7aa7-2133">Default</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2133">Default</span></span>

<span data-ttu-id="f7aa7-2134">0</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2134">0</span></span>

<span data-ttu-id="f7aa7-2135">0-Unknown 1-Average 2-CenterWeightedAverage 3-Spot 4-multipoint 5-pattern 6-partial 7 à 254-reserved 255-Other</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2135">0 - unknown 1 - Average 2 - CenterWeightedAverage 3 - Spot 4 - MultiSpot 5 - Pattern 6 - Partial 7 to 254 - reserved 255 - other</span></span>



 

## <a name="propertytagexiflightsource"></a><span data-ttu-id="f7aa7-2136">PropertyTagExifLightSource</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2136">PropertyTagExifLightSource</span></span>

<span data-ttu-id="f7aa7-2137">Type de source de lumière.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2137">Type of light source.</span></span>



<span data-ttu-id="f7aa7-2138">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2138">Tag</span></span>

<span data-ttu-id="f7aa7-2139">0x9208</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2139">0x9208</span></span>

<span data-ttu-id="f7aa7-2140">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2140">Type</span></span>

<span data-ttu-id="f7aa7-2141">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2141">PropertyTagTypeShort</span></span>

<span data-ttu-id="f7aa7-2142">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2142">Count</span></span>

<span data-ttu-id="f7aa7-2143">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2143">1</span></span>

<span data-ttu-id="f7aa7-2144">Default</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2144">Default</span></span>

<span data-ttu-id="f7aa7-2145">0</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2145">0</span></span>

<span data-ttu-id="f7aa7-2146">0-Inconnu 1-heure d’été 2-fluorescents 3-tungstène 17-standard lumière 18-standard clair B 19-standard Light C 20-D55 21-D65 22-D75 23 254-réservé 255-Other</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2146">0 - unknown 1 - Daylight 2 - Flourescent 3 - Tungsten 17 - Standard Light A 18 - Standard Light B 19 - Standard Light C 20 - D55 21 - D65 22 - D75 23 to 254 - reserved 255 - other</span></span>



 

## <a name="propertytagexifflash"></a><span data-ttu-id="f7aa7-2147">PropertyTagExifFlash</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2147">PropertyTagExifFlash</span></span>

<span data-ttu-id="f7aa7-2148">État Flash.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2148">Flash status.</span></span> <span data-ttu-id="f7aa7-2149">Cette balise est enregistrée lorsqu’une image est prise à l’aide d’une lumière stroboscopique (Flash).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2149">This tag is recorded when an image is taken using a strobe light (flash).</span></span> <span data-ttu-id="f7aa7-2150">Le bit 0 indique l’état de déclenchement Flash et les bits 1 et 2 indiquent l’état de retour du flash.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2150">Bit 0 indicates the flash firing status, and bits 1 and 2 indicate the flash return status.</span></span>



<span data-ttu-id="f7aa7-2151">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2151">Tag</span></span>

<span data-ttu-id="f7aa7-2152">0x9209</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2152">0x9209</span></span>

<span data-ttu-id="f7aa7-2153">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2153">Type</span></span>

<span data-ttu-id="f7aa7-2154">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2154">PropertyTagTypeShort</span></span>

<span data-ttu-id="f7aa7-2155">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2155">Count</span></span>

<span data-ttu-id="f7aa7-2156">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2156">1</span></span>

<span data-ttu-id="f7aa7-2157">Valeurs de bit 0 qui indiquent si le flash s’est déclenché : 0b-Flash n’a pas déclenché 1b-Flash déclenché</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2157">Values for bit 0 that indicate whether the flash fired: 0b - flash did not fire 1b - flash fired</span></span>

<span data-ttu-id="f7aa7-2158">Valeurs pour bits 1 et 2 qui indiquent l’état de la lumière renvoyée : 00B-aucune fonction de détection de retour de lumière 01b-réservée 10 b-lumière de retour stroboscopique non détectée 11B-lumière de retour stroboscopique détectée</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2158">Values for bits 1 and 2 that indicate the status of returned light: 00b - no strobe return detection function 01b - reserved 10b - strobe return light not detected 11b - strobe return light detected</span></span>

<span data-ttu-id="f7aa7-2159">Valeurs de balise Flash résultantes : 0x0000-Flash n’a pas déclenché 0x0001-Flash déclenché 0x0005-lumière de retour stroboscopique non détectée</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2159">Resulting flash tag values: 0x0000 - flash did not fire 0x0001 - flash fired 0x0005 - strobe return light not detected</span></span>



 

## <a name="propertytagexiffocallength"></a><span data-ttu-id="f7aa7-2160">PropertyTagExifFocalLength</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2160">PropertyTagExifFocalLength</span></span>

<span data-ttu-id="f7aa7-2161">Longueur focale réelle, en millimètres, de la lentille.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2161">Actual focal length, in millimeters, of the lens.</span></span> <span data-ttu-id="f7aa7-2162">La conversion n’est pas effectuée à la longueur focale d’une caméra de film 35 millimètres.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2162">Conversion is not made to the focal length of a 35 millimeter film camera.</span></span>



| <span data-ttu-id="f7aa7-2163">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2163">Property info</span></span> | <span data-ttu-id="f7aa7-2164">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2164">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-2165">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2165">Tag</span></span>   | <span data-ttu-id="f7aa7-2166">0x920A</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2166">0x920A</span></span>                  |
| <span data-ttu-id="f7aa7-2167">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2167">Type</span></span>  | <span data-ttu-id="f7aa7-2168">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2168">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-2169">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2169">Count</span></span> | <span data-ttu-id="f7aa7-2170">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2170">1</span></span>                       |



 

## <a name="propertytagexifmakernote"></a><span data-ttu-id="f7aa7-2171">PropertyTagExifMakerNote</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2171">PropertyTagExifMakerNote</span></span>

<span data-ttu-id="f7aa7-2172">Étiquette de note.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2172">Note tag.</span></span> <span data-ttu-id="f7aa7-2173">Balise utilisée par les fabricants de rédacteurs EXIF pour enregistrer des informations.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2173">A tag used by manufacturers of EXIF writers to record information.</span></span> <span data-ttu-id="f7aa7-2174">Le contenu est destiné au fabricant.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2174">The contents are up to the manufacturer.</span></span>



| <span data-ttu-id="f7aa7-2175">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2175">Property info</span></span> | <span data-ttu-id="f7aa7-2176">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2176">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="f7aa7-2177">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2177">Tag</span></span>   | <span data-ttu-id="f7aa7-2178">0x927C</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2178">0x927C</span></span>                   |
| <span data-ttu-id="f7aa7-2179">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2179">Type</span></span>  | <span data-ttu-id="f7aa7-2180">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2180">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="f7aa7-2181">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2181">Count</span></span> | <span data-ttu-id="f7aa7-2182">Quelconque</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2182">Any</span></span>                      |



 

## <a name="propertytagexifusercomment"></a><span data-ttu-id="f7aa7-2183">PropertyTagExifUserComment</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2183">PropertyTagExifUserComment</span></span>

<span data-ttu-id="f7aa7-2184">Balise de commentaire.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2184">Comment tag.</span></span> <span data-ttu-id="f7aa7-2185">Balise utilisée par les utilisateurs EXIF pour écrire des mots clés ou des commentaires sur l’image en plus de ceux de PropertyTagImageDescription et sans les limitations de code de caractères de la balise PropertyTagImageDescription.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2185">A tag used by EXIF users to write keywords or comments about the image besides those in PropertyTagImageDescription and without the character-code limitations of the PropertyTagImageDescription tag.</span></span>



| <span data-ttu-id="f7aa7-2186">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2186">Property info</span></span> | <span data-ttu-id="f7aa7-2187">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2187">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="f7aa7-2188">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2188">Tag</span></span>   | <span data-ttu-id="f7aa7-2189">0x9286</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2189">0x9286</span></span>                   |
| <span data-ttu-id="f7aa7-2190">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2190">Type</span></span>  | <span data-ttu-id="f7aa7-2191">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2191">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="f7aa7-2192">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2192">Count</span></span> | <span data-ttu-id="f7aa7-2193">Quelconque</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2193">Any</span></span>                      |



 

<span data-ttu-id="f7aa7-2194">Le code de caractère utilisé dans la balise PropertyTagExifUserComment est identifié en fonction d’un code d’ID dans une zone fixe de 8 octets au début de la zone de données de la balise.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2194">The character code used in the PropertyTagExifUserComment tag is identified based on an ID code in a fixed 8-byte area at the start of the tag data area.</span></span> <span data-ttu-id="f7aa7-2195">La partie inutilisée de la zone est remplie avec des caractères null (0).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2195">The unused portion of the area is padded with null characters (0).</span></span> <span data-ttu-id="f7aa7-2196">Les codes d’ID sont affectés par le biais de l’inscription.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2196">ID codes are assigned by means of registration.</span></span> <span data-ttu-id="f7aa7-2197">Étant donné que le type n’est pas ASCII, il n’est pas nécessaire d’utiliser une marque de fin NULL.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2197">Because the type is not ASCII, it is not necessary to use a NULL terminator.</span></span>

## <a name="propertytagexifdtsubsec"></a><span data-ttu-id="f7aa7-2198">PropertyTagExifDTSubsec</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2198">PropertyTagExifDTSubsec</span></span>

<span data-ttu-id="f7aa7-2199">Chaîne de caractères se terminant par un caractère null qui spécifie une fraction de seconde pour la balise PropertyTagDateTime.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2199">Null-terminated character string that specifies a fraction of a second for the PropertyTagDateTime tag.</span></span>



| <span data-ttu-id="f7aa7-2200">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2200">Property info</span></span> | <span data-ttu-id="f7aa7-2201">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2201">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-2202">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2202">Tag</span></span>   | <span data-ttu-id="f7aa7-2203">0x9290</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2203">0x9290</span></span>                                             |
| <span data-ttu-id="f7aa7-2204">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2204">Type</span></span>  | <span data-ttu-id="f7aa7-2205">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2205">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-2206">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2206">Count</span></span> | <span data-ttu-id="f7aa7-2207">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2207">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifdtorigss"></a><span data-ttu-id="f7aa7-2208">PropertyTagExifDTOrigSS</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2208">PropertyTagExifDTOrigSS</span></span>

<span data-ttu-id="f7aa7-2209">Chaîne de caractères se terminant par un caractère null qui spécifie une fraction de seconde pour la balise PropertyTagExifDTOrig.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2209">Null-terminated character string that specifies a fraction of a second for the PropertyTagExifDTOrig tag.</span></span>



| <span data-ttu-id="f7aa7-2210">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2210">Property info</span></span> | <span data-ttu-id="f7aa7-2211">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2211">Value</span></span> |
|------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-2212">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2212">Tag</span></span>  | <span data-ttu-id="f7aa7-2213">0x9291</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2213">0x9291</span></span>                                             |
| <span data-ttu-id="f7aa7-2214">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2214">Type</span></span> | <span data-ttu-id="f7aa7-2215">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2215">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="f7aa7-2216">N</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2216">N</span></span>    | <span data-ttu-id="f7aa7-2217">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2217">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifdtdigss"></a><span data-ttu-id="f7aa7-2218">PropertyTagExifDTDigSS</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2218">PropertyTagExifDTDigSS</span></span>

<span data-ttu-id="f7aa7-2219">Chaîne de caractères se terminant par un caractère null qui spécifie une fraction de seconde pour la balise PropertyTagExifDTDigitized.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2219">Null-terminated character string that specifies a fraction of a second for the PropertyTagExifDTDigitized tag.</span></span>



| <span data-ttu-id="f7aa7-2220">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2220">Property info</span></span> | <span data-ttu-id="f7aa7-2221">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2221">Value</span></span> |
|------|----------------------------------------------------|
| <span data-ttu-id="f7aa7-2222">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2222">Tag</span></span>  | <span data-ttu-id="f7aa7-2223">0x9292</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2223">0x9292</span></span>                                             |
| <span data-ttu-id="f7aa7-2224">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2224">Type</span></span> | <span data-ttu-id="f7aa7-2225">ASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2225">ASCII</span></span>                                              |
| <span data-ttu-id="f7aa7-2226">N</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2226">N</span></span>    | <span data-ttu-id="f7aa7-2227">Longueur de la chaîne, y compris la marque de fin NULL</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2227">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexiffpxver"></a><span data-ttu-id="f7aa7-2228">PropertyTagExifFPXVer</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2228">PropertyTagExifFPXVer</span></span>

<span data-ttu-id="f7aa7-2229">Version du format FlashPix prise en charge par un fichier FPXR.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2229">FlashPix format version supported by an FPXR file.</span></span> <span data-ttu-id="f7aa7-2230">Si la fonction FPXR prend en charge le format FlashPix version 1,0, cela est indiqué de la même façon que PropertyTagExifVer en enregistrant 0100 comme chaîne ASCII de 4 octets.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2230">If the FPXR function supports FlashPix format version 1.0, this is indicated similarly to PropertyTagExifVer by recording 0100 as a 4-byte ASCII string.</span></span> <span data-ttu-id="f7aa7-2231">Étant donné que le type est PropertyTagTypeUndefined, il n’y a aucune marque de fin NULL.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2231">Because the type is PropertyTagTypeUndefined, there is no NULL terminator.</span></span>



<span data-ttu-id="f7aa7-2232">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2232">Tag</span></span>

<span data-ttu-id="f7aa7-2233">0xA000</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2233">0xA000</span></span>

<span data-ttu-id="f7aa7-2234">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2234">Type</span></span>

<span data-ttu-id="f7aa7-2235">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2235">PropertyTagTypeUndefined</span></span>

<span data-ttu-id="f7aa7-2236">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2236">Count</span></span>

<span data-ttu-id="f7aa7-2237">4</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2237">4</span></span>

<span data-ttu-id="f7aa7-2238">Default</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2238">Default</span></span>

<span data-ttu-id="f7aa7-2239">0100</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2239">0100</span></span>

<span data-ttu-id="f7aa7-2240">0100-version du format FlashPix 1,0 autre-réservé</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2240">0100 - FlashPix format version 1.0 Other - reserved</span></span>



 

## <a name="propertytagexifcolorspace"></a><span data-ttu-id="f7aa7-2241">PropertyTagExifColorSpace</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2241">PropertyTagExifColorSpace</span></span>

<span data-ttu-id="f7aa7-2242">Spécificateur d’espace colorimétrique.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2242">Color space specifier.</span></span> <span data-ttu-id="f7aa7-2243">Normalement, sRVB (= 1) est utilisé pour définir l’espace colorimétrique en fonction des conditions et de l’environnement du moniteur PC.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2243">Normally sRGB (=1) is used to define the color space based on the PC monitor conditions and environment.</span></span> <span data-ttu-id="f7aa7-2244">Si un espace de couleurs autre que sRVB est utilisé, non étalonné (= 0xFFFF) est défini.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2244">If a color space other than sRGB is used, Uncalibrated (=0xFFFF) is set.</span></span> <span data-ttu-id="f7aa7-2245">Les données d’image enregistrées comme non calibrées peuvent être traitées comme sRVB lorsqu’elles sont converties en FlashPix.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2245">Image data recorded as Uncalibrated can be treated as sRGB when it is converted to FlashPix.</span></span>



<span data-ttu-id="f7aa7-2246">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2246">Tag</span></span>

<span data-ttu-id="f7aa7-2247">0xA001</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2247">0xA001</span></span>

<span data-ttu-id="f7aa7-2248">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2248">Type</span></span>

<span data-ttu-id="f7aa7-2249">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2249">PropertyTagTypeShort</span></span>

<span data-ttu-id="f7aa7-2250">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2250">Count</span></span>

<span data-ttu-id="f7aa7-2251">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2251">1</span></span>

<span data-ttu-id="f7aa7-2252">0x1-sRVB 0xFFFF-non étalonné autre-réservé</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2252">0x1 - sRGB 0xFFFF - uncalibrated Other - reserved</span></span>



 

## <a name="propertytagexifpixxdim"></a><span data-ttu-id="f7aa7-2253">PropertyTagExifPixXDim</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2253">PropertyTagExifPixXDim</span></span>

<span data-ttu-id="f7aa7-2254">Informations spécifiques aux données compressées.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2254">Information specific to compressed data.</span></span> <span data-ttu-id="f7aa7-2255">Lorsqu’un fichier compressé est enregistré, la largeur valide de l’image explicite doit être enregistrée dans cette balise, qu’il y ait ou non des données de remplissage ou un marqueur de redémarrage.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2255">When a compressed file is recorded, the valid width of the meaningful image must be recorded in this tag, whether or not there is padding data or a restart marker.</span></span> <span data-ttu-id="f7aa7-2256">Cette balise ne doit pas exister dans un fichier non compressé.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2256">This tag should not exist in an uncompressed file.</span></span>



| <span data-ttu-id="f7aa7-2257">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2257">Property info</span></span> | <span data-ttu-id="f7aa7-2258">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2258">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="f7aa7-2259">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2259">Tag</span></span>   | <span data-ttu-id="f7aa7-2260">0xA002</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2260">0xA002</span></span>                                      |
| <span data-ttu-id="f7aa7-2261">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2261">Type</span></span>  | <span data-ttu-id="f7aa7-2262">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2262">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-2263">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2263">Count</span></span> | <span data-ttu-id="f7aa7-2264">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2264">1</span></span>                                           |



 

## <a name="propertytagexifpixydim"></a><span data-ttu-id="f7aa7-2265">PropertyTagExifPixYDim</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2265">PropertyTagExifPixYDim</span></span>

<span data-ttu-id="f7aa7-2266">Informations spécifiques aux données compressées.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2266">Information specific to compressed data.</span></span> <span data-ttu-id="f7aa7-2267">Lorsqu’un fichier compressé est enregistré, la hauteur valide de l’image explicite doit être enregistrée dans cette balise, qu’il y ait ou non des données de remplissage ou un marqueur de redémarrage.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2267">When a compressed file is recorded, the valid height of the meaningful image must be recorded in this tag whether or not there is padding data or a restart marker.</span></span> <span data-ttu-id="f7aa7-2268">Cette balise ne doit pas exister dans un fichier non compressé.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2268">This tag should not exist in an uncompressed file.</span></span> <span data-ttu-id="f7aa7-2269">Étant donné que le remplissage des données n’est pas nécessaire dans le sens vertical, le nombre de lignes enregistrées dans cette balise de hauteur d’image valide sera le même que celui enregistré dans le SOF.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2269">Because data padding is unnecessary in the vertical direction, the number of lines recorded in this valid image height tag will be the same as that recorded in the SOF.</span></span>



| <span data-ttu-id="f7aa7-2270">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2270">Property info</span></span> | <span data-ttu-id="f7aa7-2271">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2271">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="f7aa7-2272">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2272">Tag</span></span>   | <span data-ttu-id="f7aa7-2273">0xA003</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2273">0xA003</span></span>                                      |
| <span data-ttu-id="f7aa7-2274">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2274">Type</span></span>  | <span data-ttu-id="f7aa7-2275">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2275">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-2276">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2276">Count</span></span> | <span data-ttu-id="f7aa7-2277">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2277">1</span></span>                                           |



 

## <a name="propertytagexifrelatedwav"></a><span data-ttu-id="f7aa7-2278">PropertyTagExifRelatedWav</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2278">PropertyTagExifRelatedWav</span></span>

<span data-ttu-id="f7aa7-2279">Nom d’un fichier audio associé aux données de l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2279">The name of an audio file related to the image data.</span></span> <span data-ttu-id="f7aa7-2280">Les seules informations relationnelles enregistrées sont le nom et l’extension du fichier audio EXIF (une chaîne ASCII composée de 8 caractères plus un point (.), plus 3 caractères).</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2280">The only relational information recorded is the EXIF audio file name and extension (an ASCII string that consists of 8 characters plus a period (.), plus 3 characters).</span></span> <span data-ttu-id="f7aa7-2281">Le chemin d’accès n’est pas enregistré.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2281">The path is not recorded.</span></span> <span data-ttu-id="f7aa7-2282">Lorsque vous utilisez cette balise, les fichiers audio doivent être enregistrés conformément au format audio EXIF.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2282">When you use this tag, audio files must be recorded in conformance with the EXIF audio format.</span></span> <span data-ttu-id="f7aa7-2283">Les enregistreurs peuvent également stocker des données audio dans APP2 sous forme de données de flux d’extension FlashPix.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2283">Writers can also store audio data within APP2 as FlashPix extension stream data.</span></span>



| <span data-ttu-id="f7aa7-2284">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2284">Property info</span></span> | <span data-ttu-id="f7aa7-2285">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2285">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-2286">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2286">Tag</span></span>   | <span data-ttu-id="f7aa7-2287">0xA004</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2287">0xA004</span></span>               |
| <span data-ttu-id="f7aa7-2288">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2288">Type</span></span>  | <span data-ttu-id="f7aa7-2289">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2289">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="f7aa7-2290">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2290">Count</span></span> | <span data-ttu-id="f7aa7-2291">13</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2291">13</span></span>                   |



 

## <a name="propertytagexifinterop"></a><span data-ttu-id="f7aa7-2292">PropertyTagExifInterop</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2292">PropertyTagExifInterop</span></span>

<span data-ttu-id="f7aa7-2293">Décalage d’un bloc d’éléments de propriété qui contiennent des informations d’interopérabilité.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2293">Offset to a block of property items that contain interoperability information.</span></span>



| <span data-ttu-id="f7aa7-2294">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2294">Property info</span></span> | <span data-ttu-id="f7aa7-2295">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2295">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="f7aa7-2296">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2296">Tag</span></span>   | <span data-ttu-id="f7aa7-2297">0xA005</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2297">0xA005</span></span>              |
| <span data-ttu-id="f7aa7-2298">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2298">Type</span></span>  | <span data-ttu-id="f7aa7-2299">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2299">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="f7aa7-2300">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2300">Count</span></span> | <span data-ttu-id="f7aa7-2301">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2301">1</span></span>                   |



 

## <a name="propertytagexifflashenergy"></a><span data-ttu-id="f7aa7-2302">PropertyTagExifFlashEnergy</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2302">PropertyTagExifFlashEnergy</span></span>

<span data-ttu-id="f7aa7-2303">Énergie stroboscopique, en secondes de puissance de la bougie (BCPS), au moment où l’image a été capturée.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2303">Strobe energy, in Beam Candle Power Seconds (BCPS), at the time the image was captured.</span></span>



| <span data-ttu-id="f7aa7-2304">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2304">Property info</span></span> | <span data-ttu-id="f7aa7-2305">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2305">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-2306">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2306">Tag</span></span>   | <span data-ttu-id="f7aa7-2307">0xA20B</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2307">0xA20B</span></span>                  |
| <span data-ttu-id="f7aa7-2308">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2308">Type</span></span>  | <span data-ttu-id="f7aa7-2309">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2309">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-2310">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2310">Count</span></span> | <span data-ttu-id="f7aa7-2311">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2311">1</span></span>                       |



 

## <a name="propertytagexifspatialfr"></a><span data-ttu-id="f7aa7-2312">PropertyTagExifSpatialFR</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2312">PropertyTagExifSpatialFR</span></span>

<span data-ttu-id="f7aa7-2313">Table de fréquence spatiale des appareils d’entrée et de caméra et valeurs SFR dans la largeur de l’image, la hauteur de l’image et la direction diagonale, comme spécifié dans la norme ISO 12233.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2313">Camera or input device spatial frequency table and SFR values in the image width, image height, and diagonal direction, as specified in ISO 12233.</span></span>



| <span data-ttu-id="f7aa7-2314">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2314">Property info</span></span> | <span data-ttu-id="f7aa7-2315">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2315">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="f7aa7-2316">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2316">Tag</span></span>   | <span data-ttu-id="f7aa7-2317">0xA20C</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2317">0xA20C</span></span>                   |
| <span data-ttu-id="f7aa7-2318">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2318">Type</span></span>  | <span data-ttu-id="f7aa7-2319">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2319">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="f7aa7-2320">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2320">Count</span></span> | <span data-ttu-id="f7aa7-2321">Quelconque</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2321">Any</span></span>                      |



 

## <a name="propertytagexiffocalxres"></a><span data-ttu-id="f7aa7-2322">PropertyTagExifFocalXRes</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2322">PropertyTagExifFocalXRes</span></span>

<span data-ttu-id="f7aa7-2323">Nombre de pixels dans la direction de l’image (x) par unité sur le plan focal de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2323">Number of pixels in the image width (x) direction per unit on the camera focal plane.</span></span> <span data-ttu-id="f7aa7-2324">L’unité est spécifiée dans PropertyTagExifFocalResUnit.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2324">The unit is specified in PropertyTagExifFocalResUnit.</span></span>



| <span data-ttu-id="f7aa7-2325">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2325">Property info</span></span> | <span data-ttu-id="f7aa7-2326">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2326">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-2327">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2327">Tag</span></span>   | <span data-ttu-id="f7aa7-2328">0xA20E</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2328">0xA20E</span></span>                  |
| <span data-ttu-id="f7aa7-2329">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2329">Type</span></span>  | <span data-ttu-id="f7aa7-2330">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2330">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-2331">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2331">Count</span></span> | <span data-ttu-id="f7aa7-2332">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2332">1</span></span>                       |



 

## <a name="propertytagexiffocalyres"></a><span data-ttu-id="f7aa7-2333">PropertyTagExifFocalYRes</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2333">PropertyTagExifFocalYRes</span></span>

<span data-ttu-id="f7aa7-2334">Nombre de pixels dans la direction de la hauteur d’image (y) par unité sur le plan focal de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2334">Number of pixels in the image height (y) direction per unit on the camera focal plane.</span></span> <span data-ttu-id="f7aa7-2335">L’unité est spécifiée dans PropertyTagExifFocalResUnit.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2335">The unit is specified in PropertyTagExifFocalResUnit.</span></span>



| <span data-ttu-id="f7aa7-2336">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2336">Property info</span></span> | <span data-ttu-id="f7aa7-2337">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2337">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-2338">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2338">Tag</span></span>   | <span data-ttu-id="f7aa7-2339">0xA20F</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2339">0xA20F</span></span>                  |
| <span data-ttu-id="f7aa7-2340">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2340">Type</span></span>  | <span data-ttu-id="f7aa7-2341">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2341">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-2342">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2342">Count</span></span> | <span data-ttu-id="f7aa7-2343">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2343">1</span></span>                       |



 

## <a name="propertytagexiffocalresunit"></a><span data-ttu-id="f7aa7-2344">PropertyTagExifFocalResUnit</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2344">PropertyTagExifFocalResUnit</span></span>

<span data-ttu-id="f7aa7-2345">Unité de mesure pour PropertyTagExifFocalXRes et PropertyTagExifFocalYRes.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2345">Unit of measure for PropertyTagExifFocalXRes and PropertyTagExifFocalYRes.</span></span>



<span data-ttu-id="f7aa7-2346">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2346">Tag</span></span>

<span data-ttu-id="f7aa7-2347">0xA210</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2347">0xA210</span></span>

<span data-ttu-id="f7aa7-2348">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2348">Type</span></span>

<span data-ttu-id="f7aa7-2349">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2349">PropertyTagTypeShort</span></span>

<span data-ttu-id="f7aa7-2350">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2350">Count</span></span>

<span data-ttu-id="f7aa7-2351">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2351">1</span></span>

<span data-ttu-id="f7aa7-2352">2 pouces, 3-centimètres</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2352">2 - inch 3 - centimeter</span></span>



 

## <a name="propertytagexifsubjectloc"></a><span data-ttu-id="f7aa7-2353">PropertyTagExifSubjectLoc</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2353">PropertyTagExifSubjectLoc</span></span>

<span data-ttu-id="f7aa7-2354">Emplacement du sujet principal de la scène.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2354">Location of the main subject in the scene.</span></span> <span data-ttu-id="f7aa7-2355">La valeur de cette balise représente le pixel au centre du sujet principal par rapport au bord gauche.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2355">The value of this tag represents the pixel at the center of the main subject relative to the left edge.</span></span> <span data-ttu-id="f7aa7-2356">La première valeur indique le numéro de colonne, tandis que la deuxième valeur indique le numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2356">The first value indicates the column number, and the second value indicates the row number.</span></span>



| <span data-ttu-id="f7aa7-2357">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2357">Property info</span></span> | <span data-ttu-id="f7aa7-2358">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2358">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="f7aa7-2359">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2359">Tag</span></span>   | <span data-ttu-id="f7aa7-2360">0xA214</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2360">0xA214</span></span>               |
| <span data-ttu-id="f7aa7-2361">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2361">Type</span></span>  | <span data-ttu-id="f7aa7-2362">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2362">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="f7aa7-2363">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2363">Count</span></span> | <span data-ttu-id="f7aa7-2364">2</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2364">2</span></span>                    |



 

## <a name="propertytagexifexposureindex"></a><span data-ttu-id="f7aa7-2365">PropertyTagExifExposureIndex</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2365">PropertyTagExifExposureIndex</span></span>

<span data-ttu-id="f7aa7-2366">Index d’exposition sélectionné sur l’appareil photo ou l’appareil d’entrée au moment où l’image a été capturée.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2366">Exposure index selected on the camera or input device at the time the image was captured.</span></span>



| <span data-ttu-id="f7aa7-2367">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2367">Property info</span></span> | <span data-ttu-id="f7aa7-2368">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2368">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="f7aa7-2369">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2369">Tag</span></span>   | <span data-ttu-id="f7aa7-2370">0xA215</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2370">0xA215</span></span>                  |
| <span data-ttu-id="f7aa7-2371">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2371">Type</span></span>  | <span data-ttu-id="f7aa7-2372">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2372">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="f7aa7-2373">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2373">Count</span></span> | <span data-ttu-id="f7aa7-2374">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2374">1</span></span>                       |



 

## <a name="propertytagexifsensingmethod"></a><span data-ttu-id="f7aa7-2375">PropertyTagExifSensingMethod</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2375">PropertyTagExifSensingMethod</span></span>

<span data-ttu-id="f7aa7-2376">Type de capteur d’image sur l’appareil photo ou le périphérique d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2376">Image sensor type on the camera or input device.</span></span>



<span data-ttu-id="f7aa7-2377">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2377">Tag</span></span>

<span data-ttu-id="f7aa7-2378">0xA217</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2378">0xA217</span></span>

<span data-ttu-id="f7aa7-2379">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2379">Type</span></span>

<span data-ttu-id="f7aa7-2380">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2380">PropertyTagTypeShort</span></span>

<span data-ttu-id="f7aa7-2381">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2381">Count</span></span>

<span data-ttu-id="f7aa7-2382">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2382">1</span></span>

<span data-ttu-id="f7aa7-2383">capteur de zone de couleur à deux puces non défini (2-un), capteur de zone de couleur à deux processeurs 4-capteur de zone de couleur à trois puces-capteur de zone de couleur séquentielle 7-capteur trilinéaire 8-capteur linéaire séquentiel en couleur</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2383">1 - not defined 2 - one-chip color area sensor 3 - two-chip color area sensor 4 - three-chip color area sensor 5 - color sequential area sensor 7 - trilinear sensor 8 - color sequential linear sensor Other - reserved</span></span>



 

## <a name="propertytagexiffilesource"></a><span data-ttu-id="f7aa7-2384">PropertyTagExifFileSource</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2384">PropertyTagExifFileSource</span></span>

<span data-ttu-id="f7aa7-2385">Source de l’image.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2385">The image source.</span></span> <span data-ttu-id="f7aa7-2386">Si un DSC a enregistré l’image, la valeur de cette balise est 3.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2386">If a DSC recorded the image, the value of this tag is 3.</span></span>



| <span data-ttu-id="f7aa7-2387">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2387">Property info</span></span> | <span data-ttu-id="f7aa7-2388">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2388">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="f7aa7-2389">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2389">Tag</span></span>   | <span data-ttu-id="f7aa7-2390">0xA300</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2390">0xA300</span></span>                   |
| <span data-ttu-id="f7aa7-2391">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2391">Type</span></span>  | <span data-ttu-id="f7aa7-2392">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2392">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="f7aa7-2393">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2393">Count</span></span> | <span data-ttu-id="f7aa7-2394">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2394">1</span></span>                        |



 

## <a name="propertytagexifscenetype"></a><span data-ttu-id="f7aa7-2395">PropertyTagExifSceneType</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2395">PropertyTagExifSceneType</span></span>

<span data-ttu-id="f7aa7-2396">Type de scène.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2396">The type of scene.</span></span> <span data-ttu-id="f7aa7-2397">Si un DSC a enregistré l’image, la valeur de cette balise doit être définie sur 1, ce qui indique que l’image a été directement photographiée.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2397">If a DSC recorded the image, the value of this tag must be set to 1, indicating that the image was directly photographed.</span></span>



| <span data-ttu-id="f7aa7-2398">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2398">Property info</span></span> | <span data-ttu-id="f7aa7-2399">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2399">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="f7aa7-2400">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2400">Tag</span></span>   | <span data-ttu-id="f7aa7-2401">0xA301</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2401">0xA301</span></span>                   |
| <span data-ttu-id="f7aa7-2402">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2402">Type</span></span>  | <span data-ttu-id="f7aa7-2403">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2403">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="f7aa7-2404">Count</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2404">Count</span></span> | <span data-ttu-id="f7aa7-2405">1</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2405">1</span></span>                        |



 

## <a name="propertytagexifcfapattern"></a><span data-ttu-id="f7aa7-2406">PropertyTagExifCfaPattern</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2406">PropertyTagExifCfaPattern</span></span>

<span data-ttu-id="f7aa7-2407">Motif géométrique CFA (Color Filter Array) du capteur d’images lorsqu’un capteur de zone de couleurs à une seule puce est utilisé.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2407">The color filter array (CFA) geometric pattern of the image sensor when a one-chip color area sensor is used.</span></span> <span data-ttu-id="f7aa7-2408">Elle ne s’applique pas à toutes les méthodes de détection.</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2408">It does not apply to all sensing methods.</span></span>



| <span data-ttu-id="f7aa7-2409">Informations sur la propriété</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2409">Property info</span></span> | <span data-ttu-id="f7aa7-2410">Value</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2410">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="f7aa7-2411">Tag</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2411">Tag</span></span>   | <span data-ttu-id="f7aa7-2412">0xA302</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2412">0xA302</span></span>                   |
| <span data-ttu-id="f7aa7-2413">Type</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2413">Type</span></span>  | <span data-ttu-id="f7aa7-2414">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2414">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="f7aa7-2415">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2415">Count</span></span> | <span data-ttu-id="f7aa7-2416">Quelconque</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2416">Any</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="f7aa7-2417">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2417">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7aa7-2418">Spécifications des formats de fichiers image</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2418">Image File Format Specifications</span></span>](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[<span data-ttu-id="f7aa7-2419">Constantes de balise de propriété d’image</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2419">Image Property Tag Constants</span></span>](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[<span data-ttu-id="f7aa7-2420">**Constantes de type de balise de propriété d’image**</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2420">**Image Property Tag Type Constants**</span></span>](-gdiplus-constant-image-property-tag-type-constants.md)
</dt> <dt>

[<span data-ttu-id="f7aa7-2421">Balises de propriété par ordre alphabétique</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2421">Property Tags in Alphabetical Order</span></span>](-gdiplus-constant-property-tags-in-alphabetical-order.md)
</dt> <dt>

[<span data-ttu-id="f7aa7-2422">Balises de propriété dans l’ordre numérique</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2422">Property Tags in Numerical Order</span></span>](-gdiplus-constant-property-tags-in-numerical-order.md)
</dt> <dt>

[<span data-ttu-id="f7aa7-2423">Lecture et écriture de métadonnées</span><span class="sxs-lookup"><span data-stu-id="f7aa7-2423">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 



