---
title: Liste des attributs DRM
description: Liste des attributs DRM
ms.assetid: 222ef91c-b776-4de8-b1ad-88c2beca05aa
keywords:
- Windows Media Format SDK, attributs
- ASF (Advanced Systems Format), attributs
- ASF (format des systèmes avancés), attributs
- attributs, gestion des droits numériques (DRM)
- gestion des droits numériques (DRM), attributs
- DRM (gestion des droits numériques), attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3beccc33a48f57015040f06c140a55f5f9691daa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511454"
---
# <a name="drm-attribute-list"></a><span data-ttu-id="b6af5-109">Liste des attributs DRM</span><span class="sxs-lookup"><span data-stu-id="b6af5-109">DRM Attribute List</span></span>

<span data-ttu-id="b6af5-110">Pour plus de commodité, le tableau suivant répertorie tous les attributs de fichier DRM.</span><span class="sxs-lookup"><span data-stu-id="b6af5-110">For convenience, the following table lists all the DRM-related file attributes.</span></span> <span data-ttu-id="b6af5-111">(Ces attributs sont également répertoriés dans le tableau de tous les attributs sous [liste](attribute-list.md)d’attributs.)</span><span class="sxs-lookup"><span data-stu-id="b6af5-111">(These attributes are also listed in the table of all attributes under [Attribute List](attribute-list.md).)</span></span>

<span data-ttu-id="b6af5-112">Les applications peuvent définir ces valeurs lors de l’écriture de fichiers DRM et peuvent les récupérer lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="b6af5-112">Applications can set these values when writing DRM files and can retrieve them when reading.</span></span>



| <span data-ttu-id="b6af5-113">Attribut de fichier DRM</span><span class="sxs-lookup"><span data-stu-id="b6af5-113">DRM file attribute</span></span>                                                                   | <span data-ttu-id="b6af5-114">Identificateur global</span><span class="sxs-lookup"><span data-stu-id="b6af5-114">Global identifier</span></span>                             | <span data-ttu-id="b6af5-115">Type de données</span><span class="sxs-lookup"><span data-stu-id="b6af5-115">Data type</span></span>             |
|--------------------------------------------------------------------------------------|-----------------------------------------------|-----------------------|
| [<span data-ttu-id="b6af5-116">**\_CONTENTID DRM**</span><span class="sxs-lookup"><span data-stu-id="b6af5-116">**DRM\_ContentID**</span></span>](drm-contentid.md)                                              | <span data-ttu-id="b6af5-117">g \_ wszWMDRM \_ contentid</span><span class="sxs-lookup"><span data-stu-id="b6af5-117">g\_wszWMDRM\_ContentID</span></span>                        | <span data-ttu-id="b6af5-118">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b6af5-118">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="b6af5-119">**\_DRMHEADER DRM \_ ContentDistributor**</span><span class="sxs-lookup"><span data-stu-id="b6af5-119">**DRM\_DRMHeader\_ContentDistributor**</span></span>](drm-drmheader-contentdistributor.md)       | <span data-ttu-id="b6af5-120">g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor</span><span class="sxs-lookup"><span data-stu-id="b6af5-120">g\_wszWMDRM\_DRMHeader\_ContentDistributor</span></span>    | <span data-ttu-id="b6af5-121">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b6af5-121">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="b6af5-122">**\_DRMHEADER DRM \_ contentid**</span><span class="sxs-lookup"><span data-stu-id="b6af5-122">**DRM\_DRMHeader\_ContentID**</span></span>](drm-drmheader-contentid.md)                         | <span data-ttu-id="b6af5-123">g \_ wszWMDRM \_ DRMHeader \_ contentid</span><span class="sxs-lookup"><span data-stu-id="b6af5-123">g\_wszWMDRM\_DRMHeader\_ContentID</span></span>             | <span data-ttu-id="b6af5-124">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b6af5-124">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="b6af5-125">**\_DRMHEADER DRM \_ IndividualizedVersion**</span><span class="sxs-lookup"><span data-stu-id="b6af5-125">**DRM\_DRMHeader\_IndividualizedVersion**</span></span>](drm-drmheader-individualizedversion.md) | <span data-ttu-id="b6af5-126">g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="b6af5-126">g\_wszWMDRM\_DRMHeader\_IndividualizedVersion</span></span> | <span data-ttu-id="b6af5-127">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b6af5-127">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="b6af5-128">**\_DRMHEADER DRM \_ KeyId**</span><span class="sxs-lookup"><span data-stu-id="b6af5-128">**DRM\_DRMHeader\_KeyID**</span></span>](drm-drmheader-keyid.md)                                 | <span data-ttu-id="b6af5-129">g \_ wszWMDRM \_ DRMHeader \_ KeyId</span><span class="sxs-lookup"><span data-stu-id="b6af5-129">g\_wszWMDRM\_DRMHeader\_KeyID</span></span>                 | <span data-ttu-id="b6af5-130">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b6af5-130">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="b6af5-131">**\_DRMHEADER DRM \_ LicenseAcqURL**</span><span class="sxs-lookup"><span data-stu-id="b6af5-131">**DRM\_DRMHeader\_LicenseAcqURL**</span></span>](drm-drmheader-licenseacqurl.md)                 | <span data-ttu-id="b6af5-132">g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="b6af5-132">g\_wszWMDRM\_DRMHeader\_LicenseAcqURL</span></span>         | <span data-ttu-id="b6af5-133">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b6af5-133">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="b6af5-134">**\_DRMHEADER DRM \_ SubscriptionContentID**</span><span class="sxs-lookup"><span data-stu-id="b6af5-134">**DRM\_DRMHeader\_SubscriptionContentID**</span></span>](drm-drmheader-subscriptioncontentid.md) | <span data-ttu-id="b6af5-135">g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID</span><span class="sxs-lookup"><span data-stu-id="b6af5-135">g\_wszWMDRM\_DRMHeader\_SubscriptionContentID</span></span> | <span data-ttu-id="b6af5-136">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b6af5-136">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="b6af5-137">**\_DRMHEADER DRM**</span><span class="sxs-lookup"><span data-stu-id="b6af5-137">**DRM\_DRMHeader**</span></span>](drm-drmheader.md)                                              | <span data-ttu-id="b6af5-138">g \_ wszWMDRM \_ DRMHeader</span><span class="sxs-lookup"><span data-stu-id="b6af5-138">g\_wszWMDRM\_DRMHeader</span></span>                        | <span data-ttu-id="b6af5-139">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b6af5-139">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="b6af5-140">**\_INDIVIDUALIZEDVERSION DRM**</span><span class="sxs-lookup"><span data-stu-id="b6af5-140">**DRM\_IndividualizedVersion**</span></span>](drm-individualizedversion.md)                      | <span data-ttu-id="b6af5-141">g \_ wszWMDRM \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="b6af5-141">g\_wszWMDRM\_IndividualizedVersion</span></span>            | <span data-ttu-id="b6af5-142">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b6af5-142">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="b6af5-143">**\_KEYID DRM**</span><span class="sxs-lookup"><span data-stu-id="b6af5-143">**DRM\_KeyID**</span></span>](drm-keyid.md)                                                      | <span data-ttu-id="b6af5-144">g \_ wszWMDRM \_ KeyId</span><span class="sxs-lookup"><span data-stu-id="b6af5-144">g\_wszWMDRM\_KeyID</span></span>                            | <span data-ttu-id="b6af5-145">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b6af5-145">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="b6af5-146">**\_LASIGNATURECERT DRM**</span><span class="sxs-lookup"><span data-stu-id="b6af5-146">**DRM\_LASignatureCert**</span></span>](drm-lasignaturecert.md)                                  | <span data-ttu-id="b6af5-147">g \_ wszWMDRM \_ LASignatureCert</span><span class="sxs-lookup"><span data-stu-id="b6af5-147">g\_wszWMDRM\_LASignatureCert</span></span>                  | <span data-ttu-id="b6af5-148">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b6af5-148">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="b6af5-149">**\_LASIGNATURELICSRVCERT DRM**</span><span class="sxs-lookup"><span data-stu-id="b6af5-149">**DRM\_LASignatureLicSrvCert**</span></span>](drm-lasignaturelicsrvcert.md)                      | <span data-ttu-id="b6af5-150">g \_ wszWMDRM \_ LASignatureLicSrvCert</span><span class="sxs-lookup"><span data-stu-id="b6af5-150">g\_wszWMDRM\_LASignatureLicSrvCert</span></span>            | <span data-ttu-id="b6af5-151">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b6af5-151">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="b6af5-152">**\_LASIGNATUREPRIVKEY DRM**</span><span class="sxs-lookup"><span data-stu-id="b6af5-152">**DRM\_LASignaturePrivKey**</span></span>](drm-lasignatureprivkey.md)                            | <span data-ttu-id="b6af5-153">g \_ wszWMDRM \_ LASignaturePrivKey</span><span class="sxs-lookup"><span data-stu-id="b6af5-153">g\_wszWMDRM\_LASignaturePrivKey</span></span>               | <span data-ttu-id="b6af5-154">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b6af5-154">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="b6af5-155">**\_LASIGNATUREROOTCERT DRM**</span><span class="sxs-lookup"><span data-stu-id="b6af5-155">**DRM\_LASignatureRootCert**</span></span>](drm-lasignaturerootcert.md)                          | <span data-ttu-id="b6af5-156">g \_ wszWMDRM \_ LASignatureRootCert</span><span class="sxs-lookup"><span data-stu-id="b6af5-156">g\_wszWMDRM\_LASignatureRootCert</span></span>              | <span data-ttu-id="b6af5-157">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b6af5-157">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="b6af5-158">**\_LICENSEACQURL DRM**</span><span class="sxs-lookup"><span data-stu-id="b6af5-158">**DRM\_LicenseAcqURL**</span></span>](drm-licenseacqurl.md)                                      | <span data-ttu-id="b6af5-159">g \_ wszWMDRM \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="b6af5-159">g\_wszWMDRM\_LicenseAcqURL</span></span>                    | <span data-ttu-id="b6af5-160">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b6af5-160">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="b6af5-161">**\_V1LICENSEACQURL DRM**</span><span class="sxs-lookup"><span data-stu-id="b6af5-161">**DRM\_V1LicenseAcqURL**</span></span>](drm-v1licenseacqurl.md)                                  | <span data-ttu-id="b6af5-162">g \_ wszWMDRM \_ V1LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="b6af5-162">g\_wszWMDRM\_V1LicenseAcqURL</span></span>                  | <span data-ttu-id="b6af5-163">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b6af5-163">**WMT\_TYPE\_STRING**</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b6af5-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b6af5-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6af5-165">**Attributs par type**</span><span class="sxs-lookup"><span data-stu-id="b6af5-165">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="b6af5-166">**Propriétés DRM**</span><span class="sxs-lookup"><span data-stu-id="b6af5-166">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




