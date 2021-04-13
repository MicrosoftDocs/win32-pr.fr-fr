---
title: Énumération des licences dans le magasin de licences local
description: Énumération des licences dans le magasin de licences local
ms.assetid: 1f380b9e-85e4-4190-a809-65dfd4658b7c
keywords:
- Windows Media Format SDK, énumération des licences
- Windows Media Format SDK, licences
- Windows Media Format SDK, magasin de licences local
- gestion des droits numériques (DRM), énumération des licences
- DRM (gestion des droits numériques), énumération des licences
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- gestion des droits numériques (DRM), magasin de licences local
- DRM (gestion des droits numériques), magasin de licences local
- API étendues du client DRM, énumération des licences
- API étendues du client, énumération des licences
- API étendues du client DRM, licences
- API étendues clientes, licences
- API étendues du client DRM, magasin de licences local
- API étendues du client, magasin de licences local
- licences, énumération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b1384e08a6789fedca9704f36ad8da1e31b4ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379760"
---
# <a name="enumerating-licenses-in-the-local-license-store"></a><span data-ttu-id="0ebe6-119">Énumération des licences dans le magasin de licences local</span><span class="sxs-lookup"><span data-stu-id="0ebe6-119">Enumerating Licenses in the Local License Store</span></span>

<span data-ttu-id="0ebe6-120">L’énumération est un processus qui consiste à obtenir des informations sur les licences dans le magasin de licences local, en les exécutant pas à pas une par une.</span><span class="sxs-lookup"><span data-stu-id="0ebe6-120">Enumeration is a process of getting information about the licenses in the local license store, by stepping through them one by one.</span></span> <span data-ttu-id="0ebe6-121">Vous pouvez créer une énumération de licences en appelant [**IWMDRMLicenseManagement :: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md).</span><span class="sxs-lookup"><span data-stu-id="0ebe6-121">You can create a license enumeration by calling the [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md).</span></span>

<span data-ttu-id="0ebe6-122">La raison la plus courante de l’énumération par le biais de licences dans le magasin est de trouver une licence particulière pour le déchiffrement de tout le contenu.</span><span class="sxs-lookup"><span data-stu-id="0ebe6-122">The most common reason for enumerating through licenses in the store is to find a particular license for decryption of some content.</span></span>

<span data-ttu-id="0ebe6-123">L’interface [**IWMDRMLicense**](iwmdrmlicense.md) sert à la fois de portail aux résultats individuels de la licence et de l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="0ebe6-123">The [**IWMDRMLicense**](iwmdrmlicense.md) interface serves as both a portal to the individual license results and as the enumerator.</span></span> <span data-ttu-id="0ebe6-124">Lorsque l’énumération de licences est créée, la première licence de la liste est chargée dans l’interface **IWMDRMLicense** .</span><span class="sxs-lookup"><span data-stu-id="0ebe6-124">When the license enumeration is created, the first license in the list is loaded into the **IWMDRMLicense** interface.</span></span> <span data-ttu-id="0ebe6-125">La plupart des méthodes de **IWMDRMLicense** vous permettent d’obtenir des informations sur la licence ou de créer des objets pour chiffrer ou déchiffrer le contenu en fonction de la licence.</span><span class="sxs-lookup"><span data-stu-id="0ebe6-125">Most of the methods of **IWMDRMLicense** enable you to get information about the license or to create objects to encrypt or decrypt content based on the license.</span></span> <span data-ttu-id="0ebe6-126">Toutefois, il existe deux méthodes qui contrôlent l’énumération : [**GetNext**](iwmdrmlicense-getnext.md) et [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md).</span><span class="sxs-lookup"><span data-stu-id="0ebe6-126">However, there are two methods that control the enumeration: [**GetNext**](iwmdrmlicense-getnext.md) and [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md).</span></span> <span data-ttu-id="0ebe6-127">**GetNext** charge la licence suivante dans la liste dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="0ebe6-127">**GetNext** loads the next license in the list into the interface.</span></span> <span data-ttu-id="0ebe6-128">**ResetEnumeration** retourne l’énumération à l’État dans lequel elle se trouvait lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="0ebe6-128">**ResetEnumeration** returns the enumeration to the state it was in when it was first created.</span></span> <span data-ttu-id="0ebe6-129">Lorsque l’énumération est réinitialisée, la première licence dans la liste est chargée à nouveau dans l’interface **IWMDRMLicense** .</span><span class="sxs-lookup"><span data-stu-id="0ebe6-129">When the enumeration is reset, the first license in the list is loaded back into the **IWMDRMLicense** interface.</span></span>

<span data-ttu-id="0ebe6-130">Lorsque vous avez atteint la dernière licence dans la liste, l’appel suivant à **GetNext** retourne l' \_ erreur \_ plus \_ aucun élément.</span><span class="sxs-lookup"><span data-stu-id="0ebe6-130">When you have reached the last license in the list, the next call to **GetNext** returns ERROR\_NO\_MORE\_ITEMS.</span></span>

<span data-ttu-id="0ebe6-131">Si votre application effectue une action avec le contenu couvert par DRM, vous devez vérifier les licences dans le magasin de licences local pour les droits et pour d’autres facteurs de limitation, tels que les niveaux de protection de sortie (OPLs).</span><span class="sxs-lookup"><span data-stu-id="0ebe6-131">If your application performs an action with the content that is covered by DRM, you should check the licenses in the local license store for the rights and for other limiting factors, such as output protection levels (OPLs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ebe6-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0ebe6-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ebe6-133">**Obtention d’informations à partir de licences dans le magasin de licences local**</span><span class="sxs-lookup"><span data-stu-id="0ebe6-133">**Getting Information from Licenses in the Local License Store**</span></span>](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




