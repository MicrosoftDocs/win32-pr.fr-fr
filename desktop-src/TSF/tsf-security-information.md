---
title: Security Considerations Text Services Framework
description: Security Considerations Text Services Framework
ms.assetid: c1250ca0-3887-4519-888f-2ed436a39917
keywords:
- Text Services Framework (TSF), sécurité
- TSF (Text Services Framework), sécurité
- services de texte, sécurité
- Applications compatibles TSF, sécurité
- sécurité pour TSF
- Text Services Framework (TSF), meilleures pratiques
- TSF (Text Services Framework), meilleures pratiques
- Applications compatibles TSF, meilleures pratiques
- services de texte, meilleures pratiques
- meilleures pratiques pour TSF
- Text Services Framework (TSF), vérification des erreurs
- TSF (Text Services Framework), vérification des erreurs
- Applications compatibles TSF, vérification des erreurs
- services de texte, vérification des erreurs
- vérification des erreurs
- Text Services Framework (TSF), signatures numériques
- TSF (Text Services Framework), signatures numériques
- services de texte, signatures numériques
- Applications compatibles TSF, signatures numériques
- signatures numériques
- Text Services Framework (TSF), LoadLibrary appelle
- TSF (Text Services Framework), LoadLibrary appelle
- services de texte, LoadLibrary appelle
- Applications compatibles TSF, LoadLibrary appelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d71966106cde0f59d39442f7e2bf9b2a216cd94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513721"
---
# <a name="security-considerations-text-services-framework"></a><span data-ttu-id="3e4d2-127">Considérations relatives à la sécurité : Text Services Framework</span><span class="sxs-lookup"><span data-stu-id="3e4d2-127">Security Considerations: Text Services Framework</span></span>

## <a name="best-practices-for-developing-with-tsf"></a><span data-ttu-id="3e4d2-128">Meilleures pratiques pour le développement avec TSF</span><span class="sxs-lookup"><span data-stu-id="3e4d2-128">Best Practices for Developing with TSF</span></span>

-   <span data-ttu-id="3e4d2-129">**Signatures numériques :** Les fournisseurs de services de texte doivent fournir des signatures numériques avec leurs exécutables binaires.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-129">**Digital Signatures:** Text service providers should provide digital signatures with their binary executables.</span></span> <span data-ttu-id="3e4d2-130">Un service de texte inscrit a accès aux threads système et peut exposer des informations qui seraient autrement inaccessibles.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-130">A registered text service has access to system threads and could expose information that would otherwise not be accessible.</span></span> <span data-ttu-id="3e4d2-131">Pour garantir un fonctionnement stable et sécurisé, l’utilisateur doit vérifier la signature numérique d’un service de texte avant que le service de texte ne soit autorisé à charger.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-131">To help ensure stable and secure operation, the user should verify the digital signature of a text service before the text service is allowed to load.</span></span> <span data-ttu-id="3e4d2-132">Consultez [Introduction à la signature du code](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) pour connaître la procédure appropriée pour créer une signature numérique.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-132">See [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) for the proper procedure to create a digital signature.</span></span>
-   <span data-ttu-id="3e4d2-133">**Vérification des erreurs :** La réussite de chaque appel de méthode ou de fonction doit être vérifiée.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-133">**Error Checking:** Each method or function call should be checked for success.</span></span> <span data-ttu-id="3e4d2-134">En cas d’échec, les appels de méthode ou de fonction restants doivent être ignorés.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-134">In the event of failure, the remaining method or function calls should be skipped.</span></span> <span data-ttu-id="3e4d2-135">La plupart des exemples de code de cette documentation ont une vérification limitée des erreurs, ou aucun d’entre eux, pour éviter d’obscurcir le point à illustrer.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-135">Most of the code examples in this documentation have limited error checking, or none at all, to avoid obscuring the point to be illustrated.</span></span> <span data-ttu-id="3e4d2-136">Vous ne devez pas coller des exemples de la documentation directement dans le code de production ; au lieu de cela, vous devez améliorer les exemples en ajoutant votre propre vérification des erreurs.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-136">You should not paste examples from the documentation directly into production code; rather, you should enhance the examples by adding your own error checking.</span></span>

-   <span data-ttu-id="3e4d2-137">**LoadLibrary appelle :** Pour obtenir un pointeur vers l’une des [fonctions TSF](text-services-framework-functions.md), vous devrez utiliser [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="3e4d2-137">**LoadLibrary Calls:** To obtain a pointer to any of the [TSF functions](text-services-framework-functions.md), you will need to use [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="3e4d2-138">Toutefois, il est important de suivre les procédures de mise en forme du nom du chemin d’accès à la DLL, comme indiqué dans la documentation de **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="3e4d2-138">However, it is important to follow procedures for formatting the DLL path name, as given in **LoadLibrary** documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e4d2-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e4d2-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e4d2-140">Meilleures pratiques de sécurité</span><span class="sxs-lookup"><span data-stu-id="3e4d2-140">Security Best Practices</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

<span data-ttu-id="3e4d2-141">[Présentation de la signature de code](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3e4d2-141">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3e4d2-142">TSF, fonctions</span><span class="sxs-lookup"><span data-stu-id="3e4d2-142">TSF functions</span></span>](text-services-framework-functions.md)
</dt> <dt>

[<span data-ttu-id="3e4d2-143">LoadLibrary</span><span class="sxs-lookup"><span data-stu-id="3e4d2-143">LoadLibrary</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="3e4d2-144">GetProcAddress</span><span class="sxs-lookup"><span data-stu-id="3e4d2-144">GetProcAddress</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 