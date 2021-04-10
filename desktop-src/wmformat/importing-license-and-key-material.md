---
title: Importation de la licence et du matériel de clé
description: Importation de la licence et du matériel de clé
ms.assetid: 72ce5901-3e5b-4339-b695-592895ac6bfe
keywords:
- Windows Media Format SDK, importation DRM
- Windows Media Format SDK, importer
- Windows Media Format SDK, licences
- gestion des droits numériques (DRM), importation
- DRM (gestion des droits numériques), importation
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- gestion des droits numériques (DRM), matériel de clé
- DRM (gestion des droits numériques), matériel de clé
- API étendues du client DRM, importation
- API étendues du client, importation
- API étendues du client DRM, licences
- API étendues clientes, licences
- API étendues du client DRM, matériel de clé
- API étendues du client, matériel de clé
- licences, importation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a142d0087916a45b6dd8661b67f7e42eaed245c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197319"
---
# <a name="importing-license-and-key-material"></a><span data-ttu-id="f13eb-119">Importation de la licence et du matériel de clé</span><span class="sxs-lookup"><span data-stu-id="f13eb-119">Importing License and Key Material</span></span>

<span data-ttu-id="f13eb-120">Si vous avez un contenu multimédia qui a été chiffré à l’aide d’un système de protection de contenu tiers et que vous souhaitez importer la licence et le matériel de clé dans Windows Media DRM, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="f13eb-120">If you have media content that was encrypted using a third-party content protection system and you want to import the license and key material into Windows Media DRM, follow these steps:</span></span>

1.  <span data-ttu-id="f13eb-121">Récupérez la collection de certificats de l’ordinateur Windows Media DRM en appelant la méthode [**IWMDRMSecurity :: GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="f13eb-121">Retrieve the Windows Media DRM machine certificate collection by calling the [**IWMDRMSecurity::GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md) method.</span></span>
2.  <span data-ttu-id="f13eb-122">Analysez la collection de certificats, en vous assurant qu’elle est correctement signée et qu’elle est validée avec une clé publique racine Microsoft connue.</span><span class="sxs-lookup"><span data-stu-id="f13eb-122">Parse the certificate collection, ensuring that it is signed correctly and is validated to a known Microsoft root public key.</span></span> <span data-ttu-id="f13eb-123">La collection de certificats est conforme au schéma XMR.</span><span class="sxs-lookup"><span data-stu-id="f13eb-123">The certificate collection conforms to the XMR schema.</span></span> <span data-ttu-id="f13eb-124">Pour plus d’informations, consultez [génération d’une licence XMR](building-an-xmr-license.md).</span><span class="sxs-lookup"><span data-stu-id="f13eb-124">For more information, see [Building an XMR License](building-an-xmr-license.md).</span></span>
3.  <span data-ttu-id="f13eb-125">Facultatif : extrayez la liste de révocation en appelant la méthode [**IWMDRMSecurity :: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .</span><span class="sxs-lookup"><span data-stu-id="f13eb-125">Optional: Extract the revocation list by calling the [**IWMDRMSecurity::GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) method.</span></span>
4.  <span data-ttu-id="f13eb-126">Facultatif : Assurez-vous qu’aucun certificat de la collection n’est révoqué.</span><span class="sxs-lookup"><span data-stu-id="f13eb-126">Optional: Insure that no certificate in the collection is revoked.</span></span> <span data-ttu-id="f13eb-127">Pour plus d’informations, consultez vérification de la [révocation des certificats](checking-certificate-revocation.md).</span><span class="sxs-lookup"><span data-stu-id="f13eb-127">For more information, see [Checking Certificate Revocation](checking-certificate-revocation.md).</span></span>
5.  <span data-ttu-id="f13eb-128">Générez une licence au format XMR qui représente les spécifications de la stratégie pour le contenu d’importation et qui contient le matériel de clé DRM Windows Media approprié.</span><span class="sxs-lookup"><span data-stu-id="f13eb-128">Generate a license in the XMR format that represents the policy requirements for the import content and contains the appropriate Windows Media DRM key material.</span></span> <span data-ttu-id="f13eb-129">Pour plus d’informations, consultez la rubrique [création d’une licence XMR](building-an-xmr-license.md).</span><span class="sxs-lookup"><span data-stu-id="f13eb-129">For more information, see the topic [Building an XMR License](building-an-xmr-license.md).</span></span>
6.  <span data-ttu-id="f13eb-130">Transmettez la licence XMR au système Windows Media DRM en vue de son traitement, à l’aide de la méthode [**IWMDRMLicenseManagement :: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="f13eb-130">Pass the XMR license to the Windows Media DRM system for processing, by using the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="f13eb-131">Des informations sur le schéma XMR vous seront fournies lors de la licence de Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="f13eb-131">Details about the XMR schema will be provided to you when you license Windows Media DRM.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f13eb-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f13eb-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f13eb-133">**Vérification de la révocation des certificats**</span><span class="sxs-lookup"><span data-stu-id="f13eb-133">**Checking Certificate Revocation**</span></span>](checking-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="f13eb-134">**Génération d’une licence XMR**</span><span class="sxs-lookup"><span data-stu-id="f13eb-134">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> <dt>

[<span data-ttu-id="f13eb-135">**Importation DRM**</span><span class="sxs-lookup"><span data-stu-id="f13eb-135">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




