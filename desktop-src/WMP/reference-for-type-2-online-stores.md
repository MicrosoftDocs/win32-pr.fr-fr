---
title: Référence pour les magasins en ligne de type 2
description: Référence pour les magasins en ligne de type 2
ms.assetid: b3f580cc-b02d-4312-a7a1-a35778a222bc
keywords:
- Windows Media Player Online stores, référence
- magasins en ligne, référence
- type 2 magasins en ligne, référence
- référence pour les magasins en ligne de type 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c164ad74481030a52cd31605b29833d3bfbd3f1d
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "103724190"
---
# <a name="reference-for-type-2-online-stores"></a><span data-ttu-id="bf7ba-107">Référence pour les magasins en ligne de type 2</span><span class="sxs-lookup"><span data-stu-id="bf7ba-107">Reference for Type 2 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="bf7ba-108">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="bf7ba-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="bf7ba-109">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="bf7ba-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="bf7ba-110">Le lecteur Windows Media 10 ou version ultérieure fournit des objets, des interfaces, des propriétés et des méthodes qui prennent en charge les magasins de type 2 en ligne.</span><span class="sxs-lookup"><span data-stu-id="bf7ba-110">Windows Media Player 10 or later provides objects, interfaces, properties, and methods that support type 2 online stores.</span></span> <span data-ttu-id="bf7ba-111">Les sections suivantes documentent ces informations en détail.</span><span class="sxs-lookup"><span data-stu-id="bf7ba-111">The following sections document these in detail.</span></span>



| <span data-ttu-id="bf7ba-112">Section</span><span class="sxs-lookup"><span data-stu-id="bf7ba-112">Section</span></span>                                                                                                        | <span data-ttu-id="bf7ba-113">Description</span><span class="sxs-lookup"><span data-stu-id="bf7ba-113">Description</span></span>                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf7ba-114">Interface IWMPSubscriptionService</span><span class="sxs-lookup"><span data-stu-id="bf7ba-114">IWMPSubscriptionService Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)                                               | <span data-ttu-id="bf7ba-115">Fournit des méthodes pour augmenter la gestion des droits numériques (DRM) et initier des processus en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="bf7ba-115">Provides methods to augment digital rights management (DRM) and initiate background processes.</span></span>                                                                              |
| [<span data-ttu-id="bf7ba-116">Interface IWMPSubscriptionService2</span><span class="sxs-lookup"><span data-stu-id="bf7ba-116">IWMPSubscriptionService2 Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)                                             | <span data-ttu-id="bf7ba-117">Fournit des méthodes pour initier des processus en arrière-plan, fournir des informations sur l’activité du magasin en ligne et fournir un pointeur vers l’interface principale du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bf7ba-117">Provides methods to initiate background processes, to provide information about online store activity, and to provide a pointer to the Windows Media Player core interface.</span></span> |
| [<span data-ttu-id="bf7ba-118">Interface IWMPSubscriptionServiceCallback</span><span class="sxs-lookup"><span data-stu-id="bf7ba-118">IWMPSubscriptionServiceCallback Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)                               | <span data-ttu-id="bf7ba-119">Définit une méthode utilisée par les magasins en ligne pour notifier le lecteur Windows Media quand un processus en arrière-plan est terminé.</span><span class="sxs-lookup"><span data-stu-id="bf7ba-119">Defines a method that online stores use to notify Windows Media Player when a background process is completed.</span></span>                                                              |
| [<span data-ttu-id="bf7ba-120">WMPNotifySubscriptionPluginAddRemove</span><span class="sxs-lookup"><span data-stu-id="bf7ba-120">WMPNotifySubscriptionPluginAddRemove</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-wmpnotifysubscriptionpluginaddremove)                               | <span data-ttu-id="bf7ba-121">Fonction utilisée pour informer le lecteur Windows Media qu’un plug-in a été installé ou désinstallé.</span><span class="sxs-lookup"><span data-stu-id="bf7ba-121">A function used to notify Windows Media Player that a plug-in has been installed or uninstalled.</span></span>                                                                            |
| [<span data-ttu-id="bf7ba-122">Objet DownloadCollection</span><span class="sxs-lookup"><span data-stu-id="bf7ba-122">DownloadCollection Object</span></span>](downloadcollection-object.md)                                                     | <span data-ttu-id="bf7ba-123">Fournit des méthodes et des propriétés pour gérer des collections d’éléments de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="bf7ba-123">Provides methods and properties to manage collections of download items.</span></span>                                                                                                    |
| [<span data-ttu-id="bf7ba-124">Objet DownloadItem</span><span class="sxs-lookup"><span data-stu-id="bf7ba-124">DownloadItem Object</span></span>](downloaditem-object.md)                                                                 | <span data-ttu-id="bf7ba-125">Fournit des méthodes et des propriétés relatives aux demandes de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="bf7ba-125">Provides methods and properties relating to download requests.</span></span>                                                                                                              |
| [<span data-ttu-id="bf7ba-126">Objet DownloadManager</span><span class="sxs-lookup"><span data-stu-id="bf7ba-126">DownloadManager Object</span></span>](downloadmanager-object.md)                                                           | <span data-ttu-id="bf7ba-127">Fournit des méthodes pour gérer les collections de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="bf7ba-127">Provides methods to manage download collections.</span></span>                                                                                                                            |
| [<span data-ttu-id="bf7ba-128">Objet externe pour les magasins de type 2 en ligne</span><span class="sxs-lookup"><span data-stu-id="bf7ba-128">External Object for Type 2 Online Stores</span></span>](external-object-for-type-2-online-stores.md)                       | <span data-ttu-id="bf7ba-129">Fournit des propriétés, des méthodes et un événement accessibles à partir des pages Web du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="bf7ba-129">Provides properties, methods, and an event accessible from online store webpages.</span></span>                                                                                           |
| [<span data-ttu-id="bf7ba-130">Énumérations pour les magasins de type 2 en ligne</span><span class="sxs-lookup"><span data-stu-id="bf7ba-130">Enumerations for Type 2 Online Stores</span></span>](enumerations-for-type-2-online-stores.md)                             | <span data-ttu-id="bf7ba-131">Décrit les énumérations utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="bf7ba-131">Describes enumerations used by online stores.</span></span>                                                                                                                               |
| [<span data-ttu-id="bf7ba-132">Convention de travail de BITS du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="bf7ba-132">Windows Media Player BITS Job Convention</span></span>](windows-media-player-bits-job-convention.md)                       | <span data-ttu-id="bf7ba-133">Décrit une convention pour l’utilisation du Service de transfert intelligent en arrière-plan (BITS).</span><span class="sxs-lookup"><span data-stu-id="bf7ba-133">Describes a convention for using the Background Intelligent Transfer Service (BITS).</span></span>                                                                                        |
| [<span data-ttu-id="bf7ba-134">Clés et entrées de Registre pour un magasin de type 2 en ligne</span><span class="sxs-lookup"><span data-stu-id="bf7ba-134">Registry Keys and Entries for a Type 2 Online Store</span></span>](registry-keys-and-entries-for-a-type-2-online-store.md) | <span data-ttu-id="bf7ba-135">Décrit les entrées de registre qu’un magasin en ligne doit créer dans le registre sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bf7ba-135">Describes registry entries that an online store must create in the registry on the user's computer.</span></span>                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="bf7ba-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bf7ba-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf7ba-137">**Tapez 2 magasins en ligne**</span><span class="sxs-lookup"><span data-stu-id="bf7ba-137">**Type 2 Online Stores**</span></span>](type-2-online-stores.md)
</dt> </dl>

 

 




