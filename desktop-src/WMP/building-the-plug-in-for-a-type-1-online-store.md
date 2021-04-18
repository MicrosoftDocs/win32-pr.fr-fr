---
title: Création du plug-in pour un magasin de type 1 en ligne
description: Création du plug-in pour un magasin de type 1 en ligne
ms.assetid: 5d38a41f-9859-452b-953f-3449c2b0ce06
keywords:
- Windows Media Player Online stores, plug-ins
- magasins en ligne, plug-ins
- types 1 magasins en ligne, plug-ins
- Windows Media Player Online stores, création de plug-ins
- magasins en ligne, création de plug-ins
- types 1 magasins en ligne, création de plug-ins
- Windows Media Player Online stores, interface IWMPContentPartner
- magasins en ligne, interface IWMPContentPartner
- types 1 magasins en ligne, interface IWMPContentPartner
- plug-ins, Windows Media Player Online stores
- plug-ins, magasins en ligne
- plug-ins, type 1 magasins en ligne
- plug-ins, interface IWMPContentPartner
- plug-ins, génération
- Plug-ins du lecteur Windows Media, type 1 magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne Windows Media Player
- Plug-ins du lecteur Windows Media, interface IWMPContentPartner
- Plug-ins du lecteur Windows Media, génération
- IWMPContentPartner
- génération de plug-ins, tapez 1 magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36272e3497eebc7b5362d793a0ee265d2c3166fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106512084"
---
# <a name="building-the-plug-in-for-a-type-1-online-store"></a><span data-ttu-id="92f86-124">Création du plug-in pour un magasin de type 1 en ligne</span><span class="sxs-lookup"><span data-stu-id="92f86-124">Building the Plug-in for a Type 1 Online Store</span></span>

<span data-ttu-id="92f86-125">Un magasin en ligne de type 1 doit fournir un plug-in qui implémente l’interface [**IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) .</span><span class="sxs-lookup"><span data-stu-id="92f86-125">A type 1 online store must provide a plug-in that implements the [**IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="92f86-126">Le plug-in s’exécute dans un processus distinct à partir du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="92f86-126">The plug-in runs in a separate process from Windows Media Player.</span></span>

<span data-ttu-id="92f86-127">Les étapes de création d’un plug-in qui s’exécute hors processus sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="92f86-127">The steps for creating a plug-in that runs out-of-process are as follows:</span></span>

1.  <span data-ttu-id="92f86-128">Écrivez votre plug-in comme s’il s’agissait d’un serveur COM in-process.</span><span class="sxs-lookup"><span data-stu-id="92f86-128">Write your plug-in as if it were an in-process COM server.</span></span>
2.  <span data-ttu-id="92f86-129">Créez une entrée de Registre **DllSurrogate** sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="92f86-129">Create a **DllSurrogate** registry entry on the user's computer.</span></span> <span data-ttu-id="92f86-130">L’entrée **DllSurrogate** informe le runtime com que votre plug-in doit être créé dans une instance du substitut de la dll par défaut, dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="92f86-130">The **DllSurrogate** entry informs the COM runtime that your plug-in should be created in an instance of the default DLL surrogate, dllhost.exe.</span></span>

<span data-ttu-id="92f86-131">Pour plus d’informations sur l’enregistrement de votre plug-in, consultez [clés et entrées de Registre pour un magasin de type 1 en ligne](registry-keys-and-entries-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="92f86-131">For detailed information about registering your plug-in, see [Registry Keys and Entries for a Type 1 Online Store](registry-keys-and-entries-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="92f86-132">Vous n’avez pas besoin de créer de code proxy ou stub pour votre plug-in.</span><span class="sxs-lookup"><span data-stu-id="92f86-132">You do not need to create any proxy or stub code for your plug-in.</span></span> <span data-ttu-id="92f86-133">L’ensemble de la prise en charge du marshaling est fourni par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="92f86-133">All of the marshaling support is provided by Windows Media Player.</span></span>

<span data-ttu-id="92f86-134">Vous pouvez utiliser l’Assistant de plug-in de magasin en ligne pour créer rapidement un plug-in qui sert de point de départ.</span><span class="sxs-lookup"><span data-stu-id="92f86-134">You can use the online store plug-in wizard to quickly create a plug-in that serves as a starting point.</span></span> <span data-ttu-id="92f86-135">Pour plus d’informations, consultez [installation de l’Assistant de plug-in de boutique en ligne](installing-the-online-store-plug-in-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="92f86-135">For more information, see [Installing the Online Store Plug-in Wizard](installing-the-online-store-plug-in-wizard.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="92f86-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="92f86-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92f86-137">**Guide de programmation pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="92f86-137">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




