---
title: Génération d’une licence XMR
description: Génération d’une licence XMR
ms.assetid: c43e4913-82a6-4dd0-9d1f-1fb237ecbb30
keywords:
- Windows Media Format SDK, importation DRM
- Windows Media Format SDK, importer
- Windows Media Format SDK, licences XMR
- Windows Media Format SDK, licences
- Windows Media Format SDK, extensible Media Rights (XMR)
- gestion des droits numériques (DRM), importation
- DRM (gestion des droits numériques), importation
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- gestion des droits numériques (DRM), licences XMR
- DRM (gestion des droits numériques), licences XMR
- gestion des droits numériques (DRM), XMR (extensible Media Rights)
- DRM (gestion des droits numériques), XMR (extensible Media Rights)
- API étendues du client DRM, importation
- API étendues du client, importation
- API étendues du client DRM, licences XMR
- API étendues clientes, licences XMR
- API étendues du client DRM, licences
- API étendues clientes, licences
- API étendues du client DRM, XMR (extensible Media Rights)
- API étendues clientes, droits multimédias extensibles (XMR)
- licences, XMR
- Droits multimédias extensibles (XMR)
- XMR (droits multimédias extensibles)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc275419116362c08cabe4dc70aa227687705fdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379612"
---
# <a name="building-an-xmr-license"></a><span data-ttu-id="9f046-127">Génération d’une licence XMR</span><span class="sxs-lookup"><span data-stu-id="9f046-127">Building an XMR License</span></span>

<span data-ttu-id="9f046-128">Pour générer une licence pour le traitement DRM Windows Media, vous devez utiliser le schéma binaire XMR (extensible Media Rights).</span><span class="sxs-lookup"><span data-stu-id="9f046-128">To generate a license for Windows Media DRM to process, you must use the Extensible Media Rights (XMR) binary schema.</span></span> <span data-ttu-id="9f046-129">XMR est un schéma permettant de transmettre des restrictions et des droits d’utilisation de média et doit être concédé sous licence séparément.</span><span class="sxs-lookup"><span data-stu-id="9f046-129">XMR is a schema for conveying media usage rights and restrictions and needs to be licensed separately.</span></span>

<span data-ttu-id="9f046-130">Le matériel important d’une licence est chiffré à l’aide de la clé publique dans la collection de certificats DRM Windows Media. il est donc visible uniquement pour le sous-système de l’API étendue du client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="9f046-130">The important material in a license is encrypted using the public key in the Windows Media DRM certificate collection, so it is visible only to the Windows Media DRM Client Extended API subsystem.</span></span> <span data-ttu-id="9f046-131">.</span><span class="sxs-lookup"><span data-stu-id="9f046-131">.</span></span>

<span data-ttu-id="9f046-132">Il vous incombe de vous assurer que la structure de licence et les paramètres de stratégie sont valides et cohérents avec l’intention de l’émetteur de licence et qu’ils sont conformes aux règles de conformité.</span><span class="sxs-lookup"><span data-stu-id="9f046-132">It is your responsibility to ensure that the license structure and policy settings are valid and consistent with the license issuer's intent, and that they conform to the compliance rules.</span></span>

<span data-ttu-id="9f046-133">Vous devez lire les règles de conformité de l’importation Windows Media DRM pour connaître l’ensemble complet d’objets XMR qui doivent être présents dans la licence.</span><span class="sxs-lookup"><span data-stu-id="9f046-133">You should read the Windows Media DRM import compliance rules to learn the complete set of XMR objects that must be present in the license.</span></span>

<span data-ttu-id="9f046-134">Pour transmettre la licence XMR au sous-système DRM, appelez la méthode [**IWMDRMLicenseManagement :: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="9f046-134">To pass the XMR license to the DRM subsystem, call the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span> <span data-ttu-id="9f046-135">Utilisez le format suivant pour transmettre la licence dans le paramètre *bstrLicenseResponse* :</span><span class="sxs-lookup"><span data-stu-id="9f046-135">Use the following format to pass the license in the *bstrLicenseResponse* parameter:</span></span>


```C++
<LICENSERESPONSE>
    <LICENSE version="3.0.0.0">insert base64-encoded XMR license here</LICENSE>
</LICENSERESPONSE>
```



<span data-ttu-id="9f046-136">Cette chaîne doit être au format Unicode (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="9f046-136">This string must be in Unicode format (UTF-16).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f046-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9f046-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f046-138">**Importation DRM**</span><span class="sxs-lookup"><span data-stu-id="9f046-138">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




