---
title: Installation en mode hors connexion
description: Installation en mode hors connexion
ms.assetid: 29d80b6b-161d-44a7-b91e-70766b849c55
keywords:
- Windows Media Player Online, installation en mode hors connexion
- magasins en ligne, installation en mode hors connexion
- tapez 1 magasins en ligne, installation en mode hors connexion
- tapez 2 magasins en ligne, installation en mode hors connexion
- Windows Media Player Online stores, installations hors connexion
- magasins en ligne, installations hors connexion
- types 1 magasins en ligne, installations hors connexion
- type 2 magasins en ligne, installations hors connexion
- installation de magasins en ligne en mode hors connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cad7048926f218ea7be74a2522eb32c58241a017
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840249"
---
# <a name="installing-while-offline"></a><span data-ttu-id="f05ea-112">Installation en mode hors connexion</span><span class="sxs-lookup"><span data-stu-id="f05ea-112">Installing While Offline</span></span>

<span data-ttu-id="f05ea-113">Les utilisateurs peuvent installer le lecteur Windows Media alors qu’ils ne sont pas connectés à Internet.</span><span class="sxs-lookup"><span data-stu-id="f05ea-113">Users can install Windows Media Player while not connected to the Internet.</span></span> <span data-ttu-id="f05ea-114">Dans ce cas, le programme d’installation de Windows Media Player localise le document ServiceInfo.xml spécifié par le paramètre de ligne de commande *serviceInfo* .</span><span class="sxs-lookup"><span data-stu-id="f05ea-114">When this happens, Windows Media Player setup locates the ServiceInfo.xml document specified by the *ServiceInfo* command line parameter.</span></span> <span data-ttu-id="f05ea-115">Si l’attribut de **clé** correspond au paramètre de ligne de commande *DefaultService* , le programme d’installation applique les informations des éléments suivants au lecteur Windows Media :</span><span class="sxs-lookup"><span data-stu-id="f05ea-115">If the **Key** attribute matches the *DefaultService* command line parameter, setup applies information from the following elements to Windows Media Player:</span></span>

-   <span data-ttu-id="f05ea-116">Convivial.</span><span class="sxs-lookup"><span data-stu-id="f05ea-116">FriendlyName.</span></span> <span data-ttu-id="f05ea-117">Le nom convivial du magasin en ligne est affiché dans l’interface utilisateur du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f05ea-117">The friendly name of the online store is shown in the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="f05ea-118">Couleur.</span><span class="sxs-lookup"><span data-stu-id="f05ea-118">Color.</span></span> <span data-ttu-id="f05ea-119">Les couleurs spécifiées sont appliquées à la barre des tâches et aux boutons.</span><span class="sxs-lookup"><span data-stu-id="f05ea-119">The specified colors are applied to the taskbar and buttons.</span></span>
-   <span data-ttu-id="f05ea-120">ServiceTask1, ServiceTask2 et ServiceTask3.</span><span class="sxs-lookup"><span data-stu-id="f05ea-120">ServiceTask1, ServiceTask2, and ServiceTask3.</span></span> <span data-ttu-id="f05ea-121">Les éléments enfants ButtonText et ButtonTip sont définis.</span><span class="sxs-lookup"><span data-stu-id="f05ea-121">The ButtonText and ButtonTip child elements are set.</span></span> <span data-ttu-id="f05ea-122">L’attribut URL n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f05ea-122">The URL attribute is not set.</span></span> <span data-ttu-id="f05ea-123">L’URL est définie une fois que l’utilisateur se connecte à Internet et que le lecteur Windows Media récupère sa liste des magasins en ligne de manière normale.</span><span class="sxs-lookup"><span data-stu-id="f05ea-123">URL is set once the user connects to the Internet and Windows Media Player retrieves its list of online stores in the normal fashion.</span></span>
-   <span data-ttu-id="f05ea-124">Image.</span><span class="sxs-lookup"><span data-stu-id="f05ea-124">Image.</span></span> <span data-ttu-id="f05ea-125">Les attributs MenuURL et ServiceLargeURL sont définis.</span><span class="sxs-lookup"><span data-stu-id="f05ea-125">The MenuURL and ServiceLargeURL attributes are set.</span></span> <span data-ttu-id="f05ea-126">Ces URL doivent pointer vers les images que vous avez installées sur le disque dur de l’utilisateur à l’aide du protocole file://.</span><span class="sxs-lookup"><span data-stu-id="f05ea-126">These URLs must point to images you installed on the user's hard disk by using the file:// protocol.</span></span>

<span data-ttu-id="f05ea-127">Lorsque l’utilisateur tente d’afficher le magasin en ligne, le lecteur Windows Media affiche un message informant l’utilisateur qu’une connexion Internet est requise.</span><span class="sxs-lookup"><span data-stu-id="f05ea-127">When the user attempts to view the online store, Windows Media Player displays a message informing the user that an Internet connection is required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f05ea-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f05ea-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f05ea-129">**Color, élément**</span><span class="sxs-lookup"><span data-stu-id="f05ea-129">**Color Element**</span></span>](color-element.md)
</dt> <dt>

[<span data-ttu-id="f05ea-130">**FriendlyName, élément**</span><span class="sxs-lookup"><span data-stu-id="f05ea-130">**FriendlyName Element**</span></span>](friendlyname-element.md)
</dt> <dt>

[<span data-ttu-id="f05ea-131">**Élément Image**</span><span class="sxs-lookup"><span data-stu-id="f05ea-131">**Image Element**</span></span>](image-element.md)
</dt> <dt>

[<span data-ttu-id="f05ea-132">**Informations communes aux magasins en ligne de type 1 et de type 2**</span><span class="sxs-lookup"><span data-stu-id="f05ea-132">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="f05ea-133">**Élément ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="f05ea-133">**ServiceInfo Element**</span></span>](serviceinfo-element.md)
</dt> <dt>

[<span data-ttu-id="f05ea-134">**Élément ServiceTask1**</span><span class="sxs-lookup"><span data-stu-id="f05ea-134">**ServiceTask1 Element**</span></span>](servicetask1-element.md)
</dt> <dt>

[<span data-ttu-id="f05ea-135">**Élément ServiceTask2**</span><span class="sxs-lookup"><span data-stu-id="f05ea-135">**ServiceTask2 Element**</span></span>](servicetask2-element.md)
</dt> <dt>

[<span data-ttu-id="f05ea-136">**Élément ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="f05ea-136">**ServiceTask3 Element**</span></span>](servicetask3-element.md)
</dt> <dt>

[<span data-ttu-id="f05ea-137">**Définition de la boutique en ligne initiale**</span><span class="sxs-lookup"><span data-stu-id="f05ea-137">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> <dt>

[<span data-ttu-id="f05ea-138">**Paramètres de ligne de commande d’installation pour les magasins en ligne**</span><span class="sxs-lookup"><span data-stu-id="f05ea-138">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




