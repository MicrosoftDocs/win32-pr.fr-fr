---
description: Pilote MSTape
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: Pilote MSTape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f37e22c26866fca9519219d358e9733fb56151
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845754"
---
# <a name="mstape-driver"></a><span data-ttu-id="64bca-103">Pilote MSTape</span><span class="sxs-lookup"><span data-stu-id="64bca-103">MSTape Driver</span></span>

<span data-ttu-id="64bca-104">Cette rubrique s’applique à Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="64bca-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="64bca-105">Le pilote MSTape prend en charge les appareils caméscopes D-VHS et MPEG.</span><span class="sxs-lookup"><span data-stu-id="64bca-105">The MSTape driver supports D-VHS and MPEG camcorder devices.</span></span> <span data-ttu-id="64bca-106">Il est exposé aux applications en tant que filtre de [capture vidéo WDM](wdm-video-capture-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="64bca-106">It is exposed to applications as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="64bca-107">Sa fonctionnalité est semblable à celle de [MSDV](msdv-driver.md), le pilote de caméscope DV :</span><span class="sxs-lookup"><span data-stu-id="64bca-107">Its functionality is similar to that of [MSDV](msdv-driver.md), the DV camcorder driver:</span></span>

-   <span data-ttu-id="64bca-108">Il apparaît dans les catégories de filtres « sources de capture vidéo » (CLSID \_ VideoInputDeviceCategory) et « périphériques de rendu de streaming WDM » (am \_ KSCATEGORY \_ Render).</span><span class="sxs-lookup"><span data-stu-id="64bca-108">It appears in the "Video Capture Sources" (CLSID\_VideoInputDeviceCategory) and "WDM Streaming Rendering Devices" (AM\_KSCATEGORY\_RENDER) filter categories.</span></span>
-   <span data-ttu-id="64bca-109">Une application peut créer une instance du filtre à l’aide de l’interface [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) .</span><span class="sxs-lookup"><span data-stu-id="64bca-109">An application can create an instance of the filter using the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span>
-   <span data-ttu-id="64bca-110">Il possède une broche de sortie pour la capture et le transport à partir de l’appareil, et une broche d’entrée pour le transport vers l’appareil.</span><span class="sxs-lookup"><span data-stu-id="64bca-110">It has an output pin for capture and transport from the device, and an input pin for transport to the device.</span></span> <span data-ttu-id="64bca-111">Un seul code confidentiel peut être connecté à la fois.</span><span class="sxs-lookup"><span data-stu-id="64bca-111">Only one pin can be connected at time.</span></span>

<span data-ttu-id="64bca-112">**Types de médias**</span><span class="sxs-lookup"><span data-stu-id="64bca-112">**Media Types**</span></span>

<span data-ttu-id="64bca-113">La broche d’entrée prend en charge un type de média.</span><span class="sxs-lookup"><span data-stu-id="64bca-113">The input pin supports one media type.</span></span>



|              |                                                            |
|--------------|------------------------------------------------------------|
| <span data-ttu-id="64bca-114">Type principal</span><span class="sxs-lookup"><span data-stu-id="64bca-114">Major Type</span></span>   | <span data-ttu-id="64bca-115">Flux de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="64bca-115">MEDIATYPE\_Stream</span></span>                                          |
| <span data-ttu-id="64bca-116">Subtype</span><span class="sxs-lookup"><span data-stu-id="64bca-116">Subtype</span></span>      | <span data-ttu-id="64bca-117">\_Stride de \_ transport MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="64bca-117">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span>                     |
| <span data-ttu-id="64bca-118">Taille d’échantillon</span><span class="sxs-lookup"><span data-stu-id="64bca-118">Sample Size</span></span>  | <span data-ttu-id="64bca-119">192 x 256</span><span class="sxs-lookup"><span data-stu-id="64bca-119">192 x 256</span></span>                                                  |
| <span data-ttu-id="64bca-120">Bloc de format</span><span class="sxs-lookup"><span data-stu-id="64bca-120">Format Block</span></span> | [<span data-ttu-id="64bca-121">**\_Stride transport \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="64bca-121">**MPEG2\_TRANSPORT\_STRIDE**</span></span>](mpeg2-transport-stride.md) |



 

<span data-ttu-id="64bca-122">La broche de sortie prend en charge deux types de médias.</span><span class="sxs-lookup"><span data-stu-id="64bca-122">The output pin supports two media types.</span></span>



|              |                                        |
|--------------|----------------------------------------|
| <span data-ttu-id="64bca-123">Type principal</span><span class="sxs-lookup"><span data-stu-id="64bca-123">Major Type</span></span>   | <span data-ttu-id="64bca-124">Flux de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="64bca-124">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="64bca-125">Subtype</span><span class="sxs-lookup"><span data-stu-id="64bca-125">Subtype</span></span>      | <span data-ttu-id="64bca-126">\_Stride de \_ transport MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="64bca-126">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="64bca-127">Taille d’échantillon</span><span class="sxs-lookup"><span data-stu-id="64bca-127">Sample Size</span></span>  | <span data-ttu-id="64bca-128">192 x 256</span><span class="sxs-lookup"><span data-stu-id="64bca-128">192 x 256</span></span>                              |
| <span data-ttu-id="64bca-129">Bloc de format</span><span class="sxs-lookup"><span data-stu-id="64bca-129">Format Block</span></span> | <span data-ttu-id="64bca-130">\_Stride transport \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="64bca-130">MPEG2\_TRANSPORT\_STRIDE</span></span>               |



 



|              |                                        |
|--------------|----------------------------------------|
| <span data-ttu-id="64bca-131">Type principal</span><span class="sxs-lookup"><span data-stu-id="64bca-131">Major Type</span></span>   | <span data-ttu-id="64bca-132">Flux de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="64bca-132">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="64bca-133">Subtype</span><span class="sxs-lookup"><span data-stu-id="64bca-133">Subtype</span></span>      | <span data-ttu-id="64bca-134">\_Stride de \_ transport MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="64bca-134">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="64bca-135">Taille d’échantillon</span><span class="sxs-lookup"><span data-stu-id="64bca-135">Sample Size</span></span>  | <span data-ttu-id="64bca-136">188 x 256</span><span class="sxs-lookup"><span data-stu-id="64bca-136">188 x 256</span></span>                              |
| <span data-ttu-id="64bca-137">Bloc de format</span><span class="sxs-lookup"><span data-stu-id="64bca-137">Format Block</span></span> | <span data-ttu-id="64bca-138">**NULL**</span><span class="sxs-lookup"><span data-stu-id="64bca-138">**NULL**</span></span>                               |



 

<span data-ttu-id="64bca-139">**Informations sur l’appareil**</span><span class="sxs-lookup"><span data-stu-id="64bca-139">**Device Information**</span></span>

<span data-ttu-id="64bca-140">Le pilote lit dynamiquement les informations à partir de la ROM de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="64bca-140">The driver dynamically reads information from the device configuration ROM.</span></span> <span data-ttu-id="64bca-141">L’application peut récupérer ces informations en liant le moniker de l’appareil à un jeu de propriétés et en appelant la méthode **IPropertyBag :: Read** .</span><span class="sxs-lookup"><span data-stu-id="64bca-141">The application can retrieve this information by binding the device moniker to a property bag and calling the **IPropertyBag::Read** method.</span></span>



| <span data-ttu-id="64bca-142">Propriété</span><span class="sxs-lookup"><span data-stu-id="64bca-142">Property</span></span>            | <span data-ttu-id="64bca-143">Description</span><span class="sxs-lookup"><span data-stu-id="64bca-143">Description</span></span>                                                                                                                                                                         | <span data-ttu-id="64bca-144">Type de données</span><span class="sxs-lookup"><span data-stu-id="64bca-144">Data type</span></span>           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="64bca-145">UniqueId \_ faible</span><span class="sxs-lookup"><span data-stu-id="64bca-145">UniqueID\_Low</span></span>       | <span data-ttu-id="64bca-146">ID unique de l’appareil ( **DWORD** faible).</span><span class="sxs-lookup"><span data-stu-id="64bca-146">Unique ID of the device (low **DWORD**).</span></span>                                                                                                                                            | <span data-ttu-id="64bca-147">**long** (VT \_ I4)</span><span class="sxs-lookup"><span data-stu-id="64bca-147">**long** (VT\_I4)</span></span>   |
| <span data-ttu-id="64bca-148">UniqueId \_ élevé</span><span class="sxs-lookup"><span data-stu-id="64bca-148">UniqueID\_High</span></span>      | <span data-ttu-id="64bca-149">ID unique de l’appareil ( **DWORD** haute)</span><span class="sxs-lookup"><span data-stu-id="64bca-149">Unique ID of the device (high **DWORD**)</span></span>                                                                                                                                            | <span data-ttu-id="64bca-150">**long**</span><span class="sxs-lookup"><span data-stu-id="64bca-150">**long**</span></span>            |
| <span data-ttu-id="64bca-151">VendorID</span><span class="sxs-lookup"><span data-stu-id="64bca-151">VendorID</span></span>            | <span data-ttu-id="64bca-152">ID du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="64bca-152">Vendor ID.</span></span>                                                                                                                                                                          | <span data-ttu-id="64bca-153">**long**</span><span class="sxs-lookup"><span data-stu-id="64bca-153">**long**</span></span>            |
| <span data-ttu-id="64bca-154">ModelID</span><span class="sxs-lookup"><span data-stu-id="64bca-154">ModelID</span></span>             | <span data-ttu-id="64bca-155">ID du modèle</span><span class="sxs-lookup"><span data-stu-id="64bca-155">Model ID.</span></span>                                                                                                                                                                           | <span data-ttu-id="64bca-156">**long**</span><span class="sxs-lookup"><span data-stu-id="64bca-156">**long**</span></span>            |
| <span data-ttu-id="64bca-157">VendorText</span><span class="sxs-lookup"><span data-stu-id="64bca-157">VendorText</span></span>          | <span data-ttu-id="64bca-158">Nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="64bca-158">Vendor name.</span></span>                                                                                                                                                                        | <span data-ttu-id="64bca-159">**BSTR** (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="64bca-159">**BSTR** (VT\_BSTR)</span></span> |
| <span data-ttu-id="64bca-160">ModelText</span><span class="sxs-lookup"><span data-stu-id="64bca-160">ModelText</span></span>           | <span data-ttu-id="64bca-161">Nom du modèle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="64bca-161">Device model name.</span></span>                                                                                                                                                                  | <span data-ttu-id="64bca-162">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="64bca-162">**BSTR**</span></span>            |
| <span data-ttu-id="64bca-163">UnitModelText</span><span class="sxs-lookup"><span data-stu-id="64bca-163">UnitModelText</span></span>       | <span data-ttu-id="64bca-164">Nom du modèle d’unité ; peut être identique à ModelText.</span><span class="sxs-lookup"><span data-stu-id="64bca-164">Unit model name; may be the same as ModelText.</span></span>                                                                                                                                      | <span data-ttu-id="64bca-165">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="64bca-165">**BSTR**</span></span>            |
| <span data-ttu-id="64bca-166">DeviceOPcr0Payload</span><span class="sxs-lookup"><span data-stu-id="64bca-166">DeviceOPcr0Payload</span></span>  | <span data-ttu-id="64bca-167">charge utile oPCR (sortie de contrôle du plug-in).</span><span class="sxs-lookup"><span data-stu-id="64bca-167">oPCR (Output Plug Control) payload.</span></span> <span data-ttu-id="64bca-168">Exemple : 146 quadlets.</span><span class="sxs-lookup"><span data-stu-id="64bca-168">Example: 146 quadlets.</span></span>                                                                                                                          | <span data-ttu-id="64bca-169">**long**</span><span class="sxs-lookup"><span data-stu-id="64bca-169">**long**</span></span>            |
| <span data-ttu-id="64bca-170">DeviceOPcr0DataRate</span><span class="sxs-lookup"><span data-stu-id="64bca-170">DeviceOPcr0DataRate</span></span> | <span data-ttu-id="64bca-171">débit de données oPCR.</span><span class="sxs-lookup"><span data-stu-id="64bca-171">oPCR data rate.</span></span> <span data-ttu-id="64bca-172">Exemples : 0 (S100), 1 (S200) ou 2 (s400).</span><span class="sxs-lookup"><span data-stu-id="64bca-172">Examples: 0 (S100), 1 (S200), or 2 (S400).</span></span>                                                                                                                          | <span data-ttu-id="64bca-173">**long**</span><span class="sxs-lookup"><span data-stu-id="64bca-173">**long**</span></span>            |
| <span data-ttu-id="64bca-174">DeviceClassGUID</span><span class="sxs-lookup"><span data-stu-id="64bca-174">DeviceClassGUID</span></span>     | <span data-ttu-id="64bca-175">GUID qui identifie le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="64bca-175">GUID that identifies the device driver.</span></span> <span data-ttu-id="64bca-176">Pour MSTape, cette valeur est `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` .</span><span class="sxs-lookup"><span data-stu-id="64bca-176">For MSTape, this value is `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}`.</span></span> <span data-ttu-id="64bca-177">Ce GUID est défini en tant que MSTapeDeviceGUID dans le fichier d’en-tête Xprtdefs. h.</span><span class="sxs-lookup"><span data-stu-id="64bca-177">This GUID is defined as MSTapeDeviceGUID in the header file Xprtdefs.h.</span></span> | <span data-ttu-id="64bca-178">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="64bca-178">**BSTR**</span></span>            |
| <span data-ttu-id="64bca-179">Description</span><span class="sxs-lookup"><span data-stu-id="64bca-179">Description</span></span>         | <span data-ttu-id="64bca-180">Description de l’appareil, prise à partir du fichier INF.</span><span class="sxs-lookup"><span data-stu-id="64bca-180">A description of the device, taken from the INF file.</span></span> <span data-ttu-id="64bca-181">Cette chaîne contient généralement le nom de la personnalisation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="64bca-181">This string usually contains the brand name of the device.</span></span>                                                                    | <span data-ttu-id="64bca-182">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="64bca-182">**BSTR**</span></span>            |



 

<span data-ttu-id="64bca-183">L’ID d’appareil est un entier 64 bits.</span><span class="sxs-lookup"><span data-stu-id="64bca-183">The device ID is a 64-bit integer.</span></span> <span data-ttu-id="64bca-184">La **valeur DWORD** basse est stockée dans la propriété Low UniqueId \_ , et la **valeur DWORD** High est stockée dans la propriété High UniqueId \_ .</span><span class="sxs-lookup"><span data-stu-id="64bca-184">The low **DWORD** is stored in the UniqueID\_Low property, and the high **DWORD** is stored in the UniqueID\_High property.</span></span>

<span data-ttu-id="64bca-185">Pour plus d’informations sur les monikers de périphérique, consultez [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="64bca-185">For more information about device monikers, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="64bca-186">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="64bca-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64bca-187">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="64bca-187">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="64bca-188">Contrôle d’un caméscope DV</span><span class="sxs-lookup"><span data-stu-id="64bca-188">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



