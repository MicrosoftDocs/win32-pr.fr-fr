---
description: Pilote MSTape
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: Pilote MSTape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951084f8827f925bba43028c0792736883d5ff0f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909397"
---
# <a name="mstape-driver"></a><span data-ttu-id="4409d-103">Pilote MSTape</span><span class="sxs-lookup"><span data-stu-id="4409d-103">MSTape Driver</span></span>

<span data-ttu-id="4409d-104">Cette rubrique s’applique à Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4409d-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="4409d-105">Le pilote MSTape prend en charge les appareils caméscopes D-VHS et MPEG.</span><span class="sxs-lookup"><span data-stu-id="4409d-105">The MSTape driver supports D-VHS and MPEG camcorder devices.</span></span> <span data-ttu-id="4409d-106">Il est exposé aux applications en tant que filtre de [capture vidéo WDM](wdm-video-capture-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="4409d-106">It is exposed to applications as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="4409d-107">Sa fonctionnalité est semblable à celle de [MSDV](msdv-driver.md), le pilote de caméscope DV :</span><span class="sxs-lookup"><span data-stu-id="4409d-107">Its functionality is similar to that of [MSDV](msdv-driver.md), the DV camcorder driver:</span></span>

-   <span data-ttu-id="4409d-108">Il apparaît dans les catégories de filtres « sources de capture vidéo » (CLSID \_ VideoInputDeviceCategory) et « périphériques de rendu de streaming WDM » (am \_ KSCATEGORY \_ Render).</span><span class="sxs-lookup"><span data-stu-id="4409d-108">It appears in the "Video Capture Sources" (CLSID\_VideoInputDeviceCategory) and "WDM Streaming Rendering Devices" (AM\_KSCATEGORY\_RENDER) filter categories.</span></span>
-   <span data-ttu-id="4409d-109">Une application peut créer une instance du filtre à l’aide de l’interface [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) .</span><span class="sxs-lookup"><span data-stu-id="4409d-109">An application can create an instance of the filter using the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span>
-   <span data-ttu-id="4409d-110">Il possède une broche de sortie pour la capture et le transport à partir de l’appareil, et une broche d’entrée pour le transport vers l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4409d-110">It has an output pin for capture and transport from the device, and an input pin for transport to the device.</span></span> <span data-ttu-id="4409d-111">Un seul code confidentiel peut être connecté à la fois.</span><span class="sxs-lookup"><span data-stu-id="4409d-111">Only one pin can be connected at time.</span></span>

<span data-ttu-id="4409d-112">**Types de médias**</span><span class="sxs-lookup"><span data-stu-id="4409d-112">**Media Types**</span></span>

<span data-ttu-id="4409d-113">La broche d’entrée prend en charge un type de média.</span><span class="sxs-lookup"><span data-stu-id="4409d-113">The input pin supports one media type.</span></span>



| <span data-ttu-id="4409d-114">Étiquette</span><span class="sxs-lookup"><span data-stu-id="4409d-114">Label</span></span> | <span data-ttu-id="4409d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4409d-115">Value</span></span> |
|--------------|------------------------------------------------------------|
| <span data-ttu-id="4409d-116">Type principal</span><span class="sxs-lookup"><span data-stu-id="4409d-116">Major Type</span></span>   | <span data-ttu-id="4409d-117">Flux de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="4409d-117">MEDIATYPE\_Stream</span></span>                                          |
| <span data-ttu-id="4409d-118">Subtype</span><span class="sxs-lookup"><span data-stu-id="4409d-118">Subtype</span></span>      | <span data-ttu-id="4409d-119">\_Stride de \_ transport MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="4409d-119">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span>                     |
| <span data-ttu-id="4409d-120">Taille d’échantillon</span><span class="sxs-lookup"><span data-stu-id="4409d-120">Sample Size</span></span>  | <span data-ttu-id="4409d-121">192 x 256</span><span class="sxs-lookup"><span data-stu-id="4409d-121">192 x 256</span></span>                                                  |
| <span data-ttu-id="4409d-122">Bloc de format</span><span class="sxs-lookup"><span data-stu-id="4409d-122">Format Block</span></span> | [<span data-ttu-id="4409d-123">**\_Stride transport \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="4409d-123">**MPEG2\_TRANSPORT\_STRIDE**</span></span>](mpeg2-transport-stride.md) |



 

<span data-ttu-id="4409d-124">La broche de sortie prend en charge deux types de médias.</span><span class="sxs-lookup"><span data-stu-id="4409d-124">The output pin supports two media types.</span></span>



| <span data-ttu-id="4409d-125">Étiquette</span><span class="sxs-lookup"><span data-stu-id="4409d-125">Label</span></span> | <span data-ttu-id="4409d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4409d-126">Value</span></span> |
|--------------|----------------------------------------|
| <span data-ttu-id="4409d-127">Type principal</span><span class="sxs-lookup"><span data-stu-id="4409d-127">Major Type</span></span>   | <span data-ttu-id="4409d-128">Flux de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="4409d-128">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="4409d-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="4409d-129">Subtype</span></span>      | <span data-ttu-id="4409d-130">\_Stride de \_ transport MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="4409d-130">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="4409d-131">Taille d’échantillon</span><span class="sxs-lookup"><span data-stu-id="4409d-131">Sample Size</span></span>  | <span data-ttu-id="4409d-132">192 x 256</span><span class="sxs-lookup"><span data-stu-id="4409d-132">192 x 256</span></span>                              |
| <span data-ttu-id="4409d-133">Bloc de format</span><span class="sxs-lookup"><span data-stu-id="4409d-133">Format Block</span></span> | <span data-ttu-id="4409d-134">\_Stride transport \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="4409d-134">MPEG2\_TRANSPORT\_STRIDE</span></span>               |



 



| <span data-ttu-id="4409d-135">Étiquette</span><span class="sxs-lookup"><span data-stu-id="4409d-135">Label</span></span> | <span data-ttu-id="4409d-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="4409d-136">Value</span></span> |
|--------------|----------------------------------------|
| <span data-ttu-id="4409d-137">Type principal</span><span class="sxs-lookup"><span data-stu-id="4409d-137">Major Type</span></span>   | <span data-ttu-id="4409d-138">Flux de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="4409d-138">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="4409d-139">Subtype</span><span class="sxs-lookup"><span data-stu-id="4409d-139">Subtype</span></span>      | <span data-ttu-id="4409d-140">\_Stride de \_ transport MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="4409d-140">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="4409d-141">Taille d’échantillon</span><span class="sxs-lookup"><span data-stu-id="4409d-141">Sample Size</span></span>  | <span data-ttu-id="4409d-142">188 x 256</span><span class="sxs-lookup"><span data-stu-id="4409d-142">188 x 256</span></span>                              |
| <span data-ttu-id="4409d-143">Bloc de format</span><span class="sxs-lookup"><span data-stu-id="4409d-143">Format Block</span></span> | <span data-ttu-id="4409d-144">**NULL**</span><span class="sxs-lookup"><span data-stu-id="4409d-144">**NULL**</span></span>                               |



 

<span data-ttu-id="4409d-145">**Informations sur l’appareil**</span><span class="sxs-lookup"><span data-stu-id="4409d-145">**Device Information**</span></span>

<span data-ttu-id="4409d-146">Le pilote lit dynamiquement les informations à partir de la ROM de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4409d-146">The driver dynamically reads information from the device configuration ROM.</span></span> <span data-ttu-id="4409d-147">L’application peut récupérer ces informations en liant le moniker de l’appareil à un jeu de propriétés et en appelant la méthode **IPropertyBag :: Read** .</span><span class="sxs-lookup"><span data-stu-id="4409d-147">The application can retrieve this information by binding the device moniker to a property bag and calling the **IPropertyBag::Read** method.</span></span>



| <span data-ttu-id="4409d-148">Propriété</span><span class="sxs-lookup"><span data-stu-id="4409d-148">Property</span></span>            | <span data-ttu-id="4409d-149">Description</span><span class="sxs-lookup"><span data-stu-id="4409d-149">Description</span></span>                                                                                                                                                                         | <span data-ttu-id="4409d-150">Type de données</span><span class="sxs-lookup"><span data-stu-id="4409d-150">Data type</span></span>           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="4409d-151">UniqueId \_ faible</span><span class="sxs-lookup"><span data-stu-id="4409d-151">UniqueID\_Low</span></span>       | <span data-ttu-id="4409d-152">ID unique de l’appareil ( **DWORD** faible).</span><span class="sxs-lookup"><span data-stu-id="4409d-152">Unique ID of the device (low **DWORD**).</span></span>                                                                                                                                            | <span data-ttu-id="4409d-153">**long** (VT \_ I4)</span><span class="sxs-lookup"><span data-stu-id="4409d-153">**long** (VT\_I4)</span></span>   |
| <span data-ttu-id="4409d-154">UniqueId \_ élevé</span><span class="sxs-lookup"><span data-stu-id="4409d-154">UniqueID\_High</span></span>      | <span data-ttu-id="4409d-155">ID unique de l’appareil ( **DWORD** haute)</span><span class="sxs-lookup"><span data-stu-id="4409d-155">Unique ID of the device (high **DWORD**)</span></span>                                                                                                                                            | <span data-ttu-id="4409d-156">**long**</span><span class="sxs-lookup"><span data-stu-id="4409d-156">**long**</span></span>            |
| <span data-ttu-id="4409d-157">VendorID</span><span class="sxs-lookup"><span data-stu-id="4409d-157">VendorID</span></span>            | <span data-ttu-id="4409d-158">ID du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4409d-158">Vendor ID.</span></span>                                                                                                                                                                          | <span data-ttu-id="4409d-159">**long**</span><span class="sxs-lookup"><span data-stu-id="4409d-159">**long**</span></span>            |
| <span data-ttu-id="4409d-160">ModelID</span><span class="sxs-lookup"><span data-stu-id="4409d-160">ModelID</span></span>             | <span data-ttu-id="4409d-161">ID du modèle</span><span class="sxs-lookup"><span data-stu-id="4409d-161">Model ID.</span></span>                                                                                                                                                                           | <span data-ttu-id="4409d-162">**long**</span><span class="sxs-lookup"><span data-stu-id="4409d-162">**long**</span></span>            |
| <span data-ttu-id="4409d-163">VendorText</span><span class="sxs-lookup"><span data-stu-id="4409d-163">VendorText</span></span>          | <span data-ttu-id="4409d-164">Nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4409d-164">Vendor name.</span></span>                                                                                                                                                                        | <span data-ttu-id="4409d-165">**BSTR** (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="4409d-165">**BSTR** (VT\_BSTR)</span></span> |
| <span data-ttu-id="4409d-166">ModelText</span><span class="sxs-lookup"><span data-stu-id="4409d-166">ModelText</span></span>           | <span data-ttu-id="4409d-167">Nom du modèle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="4409d-167">Device model name.</span></span>                                                                                                                                                                  | <span data-ttu-id="4409d-168">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="4409d-168">**BSTR**</span></span>            |
| <span data-ttu-id="4409d-169">UnitModelText</span><span class="sxs-lookup"><span data-stu-id="4409d-169">UnitModelText</span></span>       | <span data-ttu-id="4409d-170">Nom du modèle d’unité ; peut être identique à ModelText.</span><span class="sxs-lookup"><span data-stu-id="4409d-170">Unit model name; may be the same as ModelText.</span></span>                                                                                                                                      | <span data-ttu-id="4409d-171">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="4409d-171">**BSTR**</span></span>            |
| <span data-ttu-id="4409d-172">DeviceOPcr0Payload</span><span class="sxs-lookup"><span data-stu-id="4409d-172">DeviceOPcr0Payload</span></span>  | <span data-ttu-id="4409d-173">charge utile oPCR (sortie de contrôle du plug-in).</span><span class="sxs-lookup"><span data-stu-id="4409d-173">oPCR (Output Plug Control) payload.</span></span> <span data-ttu-id="4409d-174">Exemple : 146 quadlets.</span><span class="sxs-lookup"><span data-stu-id="4409d-174">Example: 146 quadlets.</span></span>                                                                                                                          | <span data-ttu-id="4409d-175">**long**</span><span class="sxs-lookup"><span data-stu-id="4409d-175">**long**</span></span>            |
| <span data-ttu-id="4409d-176">DeviceOPcr0DataRate</span><span class="sxs-lookup"><span data-stu-id="4409d-176">DeviceOPcr0DataRate</span></span> | <span data-ttu-id="4409d-177">débit de données oPCR.</span><span class="sxs-lookup"><span data-stu-id="4409d-177">oPCR data rate.</span></span> <span data-ttu-id="4409d-178">Exemples : 0 (S100), 1 (S200) ou 2 (s400).</span><span class="sxs-lookup"><span data-stu-id="4409d-178">Examples: 0 (S100), 1 (S200), or 2 (S400).</span></span>                                                                                                                          | <span data-ttu-id="4409d-179">**long**</span><span class="sxs-lookup"><span data-stu-id="4409d-179">**long**</span></span>            |
| <span data-ttu-id="4409d-180">DeviceClassGUID</span><span class="sxs-lookup"><span data-stu-id="4409d-180">DeviceClassGUID</span></span>     | <span data-ttu-id="4409d-181">GUID qui identifie le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="4409d-181">GUID that identifies the device driver.</span></span> <span data-ttu-id="4409d-182">Pour MSTape, cette valeur est `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` .</span><span class="sxs-lookup"><span data-stu-id="4409d-182">For MSTape, this value is `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}`.</span></span> <span data-ttu-id="4409d-183">Ce GUID est défini en tant que MSTapeDeviceGUID dans le fichier d’en-tête Xprtdefs. h.</span><span class="sxs-lookup"><span data-stu-id="4409d-183">This GUID is defined as MSTapeDeviceGUID in the header file Xprtdefs.h.</span></span> | <span data-ttu-id="4409d-184">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="4409d-184">**BSTR**</span></span>            |
| <span data-ttu-id="4409d-185">Description</span><span class="sxs-lookup"><span data-stu-id="4409d-185">Description</span></span>         | <span data-ttu-id="4409d-186">Description de l’appareil, prise à partir du fichier INF.</span><span class="sxs-lookup"><span data-stu-id="4409d-186">A description of the device, taken from the INF file.</span></span> <span data-ttu-id="4409d-187">Cette chaîne contient généralement le nom de la personnalisation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4409d-187">This string usually contains the brand name of the device.</span></span>                                                                    | <span data-ttu-id="4409d-188">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="4409d-188">**BSTR**</span></span>            |



 

<span data-ttu-id="4409d-189">L’ID d’appareil est un entier 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4409d-189">The device ID is a 64-bit integer.</span></span> <span data-ttu-id="4409d-190">La **valeur DWORD** basse est stockée dans la propriété Low UniqueId \_ , et la **valeur DWORD** High est stockée dans la propriété High UniqueId \_ .</span><span class="sxs-lookup"><span data-stu-id="4409d-190">The low **DWORD** is stored in the UniqueID\_Low property, and the high **DWORD** is stored in the UniqueID\_High property.</span></span>

<span data-ttu-id="4409d-191">Pour plus d’informations sur les monikers de périphérique, consultez [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="4409d-191">For more information about device monikers, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4409d-192">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4409d-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4409d-193">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="4409d-193">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="4409d-194">Contrôle d’un caméscope DV</span><span class="sxs-lookup"><span data-stu-id="4409d-194">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



