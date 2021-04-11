---
title: Type 1 plug-in de magasin en ligne
description: Type 1 plug-in de magasin en ligne
ms.assetid: 3aa74282-522b-4240-8d72-73bd3015abeb
keywords:
- Windows Media Player Online stores, plug-ins
- magasins en ligne, plug-ins
- types 1 magasins en ligne, plug-ins
- Windows Media Player Online stores, interface IWMPContentPartner
- magasins en ligne, interface IWMPContentPartner
- types 1 magasins en ligne, interface IWMPContentPartner
- plug-ins, Windows Media Player Online stores
- plug-ins, magasins en ligne
- plug-ins, type 1 magasins en ligne
- plug-ins, interface IWMPContentPartner
- Plug-ins du lecteur Windows Media, type 1 magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne Windows Media Player
- Plug-ins du lecteur Windows Media, interface IWMPContentPartner
- IWMPContentPartner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe42095d08262520734603a5418ac6831ce6685
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104030940"
---
# <a name="type-1-online-store-plug-in"></a><span data-ttu-id="b4659-118">Type 1 plug-in de magasin en ligne</span><span class="sxs-lookup"><span data-stu-id="b4659-118">Type 1 Online Store Plug-in</span></span>

<span data-ttu-id="b4659-119">Pour tirer parti des fonctionnalités d’intégration de la bibliothèque, tapez 1 les fournisseurs de magasin en ligne doivent créer un plug-in qui implémente l’interface [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) .</span><span class="sxs-lookup"><span data-stu-id="b4659-119">To take advantage of library integration features, type 1 online store providers must create a plug-in that implements the [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="b4659-120">Cette interface fournit les méthodes appelées par le lecteur Windows Media pour informer le magasin en ligne sur les activités qui ont lieu dans le lecteur et pour récupérer des informations spécifiques sur le contenu du magasin en ligne, le catalogue ou le magasin lui-même.</span><span class="sxs-lookup"><span data-stu-id="b4659-120">This interface provides the methods that Windows Media Player calls to notify the online store about activities taking place in the Player and to retrieve specific information about online store content, the catalog, or the store itself.</span></span>

<span data-ttu-id="b4659-121">Une fois que le lecteur Windows Media a instancié le plug-in, le lecteur appelle [IWMPContentPartner :: SetCallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback)et fournit un pointeur vers l’interface **IWMPContentPartnerCallback** .</span><span class="sxs-lookup"><span data-stu-id="b4659-121">After Windows Media Player instantiates the plug-in, the Player calls [IWMPContentPartner::SetCallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback), and provides a pointer to the **IWMPContentPartnerCallback** interface.</span></span> <span data-ttu-id="b4659-122">Cette interface permet à la Banque en ligne d’effectuer des appels au lecteur Windows Media pour fournir des informations d’État ou pour lancer des processus spécifiques, tels que le téléchargement d’une piste de musique.</span><span class="sxs-lookup"><span data-stu-id="b4659-122">This interface gives the online store a way to make calls into Windows Media Player to provide status information or to initiate specific processes, such as downloading a music track.</span></span>

<span data-ttu-id="b4659-123">Le lecteur Windows Media et le plug-in s’exécutent dans des processus distincts.</span><span class="sxs-lookup"><span data-stu-id="b4659-123">Windows Media Player and the plug-in run in separate processes.</span></span> <span data-ttu-id="b4659-124">Le plug-in est un serveur in-process qui s’exécute dans le substitut de DLL par défaut, dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="b4659-124">The plug-in is an in-process server that runs in the default DLL surrogate, dllhost.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4659-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b4659-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4659-126">**À propos des magasins en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="b4659-126">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="b4659-127">**Interface IWMPContentPartner**</span><span class="sxs-lookup"><span data-stu-id="b4659-127">**IWMPContentPartner Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> <dt>

[<span data-ttu-id="b4659-128">**Interface IWMPContentPartnerCallback**</span><span class="sxs-lookup"><span data-stu-id="b4659-128">**IWMPContentPartnerCallback Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)
</dt> </dl>

 

 




