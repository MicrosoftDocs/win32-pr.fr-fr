---
title: Révocation et renouvellement de composants automatisés
description: Révocation et renouvellement de composants automatisés
ms.assetid: be4899d7-1d87-4450-8c0e-75cf112ca66a
keywords:
- Windows Media Format SDK, révocation et renouvellement automatisés
- Windows Media Format SDK, révocation
- Windows Media Format SDK, renouvellement
- gestion des droits numériques (DRM), révocation et renouvellement automatisés
- DRM (gestion des droits numériques), révocation et renouvellement automatisés
- gestion des droits numériques (DRM), révocation
- DRM (gestion des droits numériques), révocation
- gestion des droits numériques (DRM), renouvellement
- DRM (gestion des droits numériques), renouvellement
- API étendues du client DRM, révocation et renouvellement automatisés
- API étendues clientes, révocation et renouvellement automatisés
- API étendues du client DRM, révocation
- API étendues clientes, révocation
- API étendues du client DRM, renouvellement
- API étendues clientes, renouvellement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9046d04d8ca7a138a06cba4d26cd82bc5a12b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316001"
---
# <a name="automated-component-revocation-and-renewal"></a><span data-ttu-id="c4476-118">Révocation et renouvellement de composants automatisés</span><span class="sxs-lookup"><span data-stu-id="c4476-118">Automated Component Revocation and Renewal</span></span>

<span data-ttu-id="c4476-119">Les applications logicielles ou les composants considérés comme compromis peuvent être révoqués par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c4476-119">Software applications or components that are considered compromised can be revoked by Microsoft.</span></span> <span data-ttu-id="c4476-120">L’API étendue du client Windows Media Format fournit un mécanisme pour la révocation et le renouvellement automatisés des composants.</span><span class="sxs-lookup"><span data-stu-id="c4476-120">The Windows Media Format Client Extended API provides a mechanism for the automated revocation and renewal of components.</span></span>

<span data-ttu-id="c4476-121">Les composants révoqués sont répertoriés dans une liste de révocation de certificats publiée par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c4476-121">Revoked components are listed in a certificate revocation list, which is published by Microsoft.</span></span> <span data-ttu-id="c4476-122">Lorsqu’un composant est révoqué, son certificat est ajouté à la liste de révocation de certificats, et l’objet BLOB des informations de révocation \_ est mis à jour sur les serveurs Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c4476-122">When a component is revoked, its certificate is added to the certificate revocation list, and the revocation information BLOB (REV\_INFO) is updated on the Microsoft servers.</span></span>

<span data-ttu-id="c4476-123">Pour effectuer une révocation et un renouvellement automatisés lorsqu’un utilisateur tente de traiter le contenu protégé par DRM Windows Media, votre application doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c4476-123">To perform automated revocation and renewal when a user attempts to process Windows Media DRM protected content, your application must do the following:</span></span>

1.  <span data-ttu-id="c4476-124">Extrayez la \_ version infos Rev de la licence.</span><span class="sxs-lookup"><span data-stu-id="c4476-124">Extract the REV\_INFO version from the license.</span></span> <span data-ttu-id="c4476-125">Le \_ numéro de version des informations Rev se trouve à l’emplacement suivant dans une licence XMR :</span><span class="sxs-lookup"><span data-stu-id="c4476-125">The REV\_INFO version number is located in the following location in an XMR license:</span></span>
    ```C++
    <LICENSE version="2.0.0.0">
        <LICENSORINFO/>
        <DATA>
            <LID>...</LID>
            <KID>...</KID>
            <RevInfoVersion>42</RevInfoVersion>
            ...
         </DATA>
    ....
    </LICENSE>
    ```

    

2.  <span data-ttu-id="c4476-126">Comparez le \_ numéro de version des informations Rev de la licence avec le \_ numéro de version d’informations Rev dans le magasin local en appelant la méthode [**IWMDRMSecurity :: GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md) .</span><span class="sxs-lookup"><span data-stu-id="c4476-126">Compare the REV\_INFO version number of the license with the REV\_INFO version number in the local store by calling the [**IWMDRMSecurity::GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md) method.</span></span>
3.  <span data-ttu-id="c4476-127">Si la \_ version infos Rev n’est pas à jour, appelez la méthode [**IWMDRMSecurity ::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) , en passant l' \_ \_ \_ \_ indicateur d’actualisation de la sécurité WMDRM dans le paramètre *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="c4476-127">If the REV\_INFO version is not up to date, call the [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) method, passing the WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH flag in the *dwFlags* parameter.</span></span>
4.  <span data-ttu-id="c4476-128">Récupérez la liste de révocation de certificats à partir du magasin local en appelant la méthode [**IWMDRMSecurity :: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .</span><span class="sxs-lookup"><span data-stu-id="c4476-128">Retrieve the certificate revocation list from the local store by calling the [**IWMDRMSecurity::GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) method.</span></span>
5.  <span data-ttu-id="c4476-129">Analyser la liste de révocation et vérifier les révocations DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c4476-129">Parse the revocation list, and check for Windows Media DRM revocations.</span></span> <span data-ttu-id="c4476-130">Pour plus d’informations, consultez vérification de la [révocation des certificats](checking-certificate-revocation.md).</span><span class="sxs-lookup"><span data-stu-id="c4476-130">For more information, see [Checking Certificate Revocation](checking-certificate-revocation.md).</span></span>
6.  <span data-ttu-id="c4476-131">S’il existe des révocations DRM Windows Media :</span><span class="sxs-lookup"><span data-stu-id="c4476-131">If there are any Windows Media DRM revocations:</span></span>
    1.  <span data-ttu-id="c4476-132">Créez un activateur de contenu pour renouveler les composants révoqués en appelant la méthode [**IWMDRMSecurity :: GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) .</span><span class="sxs-lookup"><span data-stu-id="c4476-132">Create a content enabler to renew the revoked components by calling the [**IWMDRMSecurity::GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) method.</span></span>
    2.  <span data-ttu-id="c4476-133">Appelez **IMFContentEnabler :: AutomaticEnable** qui dirige l’utilisateur vers une URL qui contient des informations de renouvellement de composant.</span><span class="sxs-lookup"><span data-stu-id="c4476-133">Call **IMFContentEnabler::AutomaticEnable** which directs the user to a URL that contains component renewal information.</span></span> <span data-ttu-id="c4476-134">Cette méthode est documentée dans le [Kit de développement logiciel (SDK) Media Foundation](../medfound/microsoft-media-foundation-sdk.md) ( https://msdn.microsoft.com/library/ms694197(VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="c4476-134">This method is documented in the [Media Foundation SDK](../medfound/microsoft-media-foundation-sdk.md) (https://msdn.microsoft.com/library/ms694197(VS.85).aspx).</span></span>
        > [!Note]  
        > <span data-ttu-id="c4476-135">Vous devez clarifier ce processus à l’utilisateur à l’aide d’une déclaration de confidentialité, car le processus de mise à jour envoie des informations à partir de l’ordinateur client vers un site Web Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c4476-135">You must clarify this process to the user through the use of a privacy statement because the update process sends information from the client computer to a Microsoft Web site.</span></span>

         

    3.  <span data-ttu-id="c4476-136">Si possible, l’utilisateur renouvelle le composant à partir de l’URL, soit automatiquement, soit en suivant les instructions spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c4476-136">If possible, the user will renew the component from the URL, either automatically or by following specific instructions.</span></span> <span data-ttu-id="c4476-137">Dans certaines situations, le composant ne peut pas être renouvelé.</span><span class="sxs-lookup"><span data-stu-id="c4476-137">There will be some situations in which the component cannot be renewed.</span></span>
    4.  <span data-ttu-id="c4476-138">Essayez d’accéder à nouveau au contenu jusqu’à ce qu’il n’y ait plus de révocations, sinon le processus est interrompu pour une raison quelconque.</span><span class="sxs-lookup"><span data-stu-id="c4476-138">Try to access the content again until there are no more revocations, or the process is halted for some reason.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4476-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c4476-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4476-140">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="c4476-140">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 