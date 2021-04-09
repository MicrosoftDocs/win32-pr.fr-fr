---
title: Définition de la boutique en ligne initiale
description: Définition de la boutique en ligne initiale
ms.assetid: 86d98936-8f20-4395-be5f-37800162aa89
keywords:
- Magasins en ligne du lecteur Windows Media, définition des magasins en ligne initiaux
- magasins en ligne, définition des magasins en ligne initiaux
- tapez 1 magasins en ligne, en définissant les magasins en ligne initiaux
- tapez 2 magasins en ligne, en définissant les magasins en ligne initiaux
- Windows Media Player Online stores, premier magasin en ligne affiché
- magasins en ligne, premier magasin en ligne affiché
- tapez 1 magasins en ligne, premier magasin en ligne affiché
- tapez 2 magasins en ligne, premier magasin en ligne affiché
- premier magasin en ligne affiché
- définition des magasins en ligne initiaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fff7dc9b2df43f4b18c257b9b9c36998cbc1334
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840477"
---
# <a name="setting-the-initial-online-store"></a><span data-ttu-id="45334-113">Définition de la boutique en ligne initiale</span><span class="sxs-lookup"><span data-stu-id="45334-113">Setting the Initial Online Store</span></span>

<span data-ttu-id="45334-114">Pour plus d’informations sur la redistribution du logiciel Windows Media Player avec votre application, consultez [redistribution du logiciel Windows Media Player](redistributing-windows-media-player-software.md).</span><span class="sxs-lookup"><span data-stu-id="45334-114">For details about redistributing Windows Media Player software with your application, see [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md).</span></span>

<span data-ttu-id="45334-115">Lorsqu’un utilisateur installe pour la première fois le lecteur Windows Media, l’application d’installation définit la Banque en ligne active initiale sur une valeur par défaut choisie par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="45334-115">When a user first installs Windows Media Player, the setup application sets the initial active online store to a default chosen by Microsoft.</span></span> <span data-ttu-id="45334-116">Les fabricants d’ordinateurs personnels peuvent choisir de modifier ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="45334-116">Personal computer original equipment manufacturers (OEMs) can choose to change this setting.</span></span>

<span data-ttu-id="45334-117">Pour spécifier et configurer le premier magasin en ligne que l’utilisateur voit lorsqu’il installe le lecteur Windows Media, vous devez :</span><span class="sxs-lookup"><span data-stu-id="45334-117">To specify and configure the first online store that the user sees when he or she installs Windows Media Player, you must:</span></span>

-   <span data-ttu-id="45334-118">Créez un document ServiceInfo que vous installez sur le disque dur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="45334-118">Create a ServiceInfo document that you install on the user's hard disk.</span></span> <span data-ttu-id="45334-119">Ce document contient des informations sur la configuration du magasin en ligne actif initial.</span><span class="sxs-lookup"><span data-stu-id="45334-119">This document contains the information about how to configure the initial active online store.</span></span>
-   <span data-ttu-id="45334-120">Ajoutez un ensemble de paramètres de ligne de commande lors de l’exécution de l’application d’installation.</span><span class="sxs-lookup"><span data-stu-id="45334-120">Append a set of command-line parameters when running the setup application.</span></span>

<span data-ttu-id="45334-121">Il existe trois scénarios pour installer le lecteur Windows Media et définir le magasin en ligne initial.</span><span class="sxs-lookup"><span data-stu-id="45334-121">There are three scenarios for installing Windows Media Player and setting the initial online store.</span></span> <span data-ttu-id="45334-122">Les sections suivantes fournissent plus de détails sur chaque scénario :</span><span class="sxs-lookup"><span data-stu-id="45334-122">The following sections provide more details about each scenario:</span></span>

-   [<span data-ttu-id="45334-123">Installation en mode hors connexion</span><span class="sxs-lookup"><span data-stu-id="45334-123">Installing While Offline</span></span>](installing-while-offline.md)
-   [<span data-ttu-id="45334-124">Installation à partir d’un CD-ROM en ligne</span><span class="sxs-lookup"><span data-stu-id="45334-124">Installing from a CD While Online</span></span>](installing-from-a-cd-while-online.md)
-   [<span data-ttu-id="45334-125">Installation à partir du Web en ligne</span><span class="sxs-lookup"><span data-stu-id="45334-125">Installing from the Web While Online</span></span>](installing-from-the-web-while-online.md)

## <a name="related-topics"></a><span data-ttu-id="45334-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="45334-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45334-127">**Informations communes aux magasins en ligne de type 1 et de type 2**</span><span class="sxs-lookup"><span data-stu-id="45334-127">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="45334-128">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="45334-128">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="45334-129">**Paramètres de ligne de commande d’installation pour les magasins en ligne**</span><span class="sxs-lookup"><span data-stu-id="45334-129">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




