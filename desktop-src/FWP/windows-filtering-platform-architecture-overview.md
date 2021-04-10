---
title: Architecture WFP
description: Cette section fournit une brève vue d’ensemble de l’architecture de la plateforme de filtrage Windows.
ms.assetid: 17a90f5c-ef82-4b14-b7f1-dd025d5f7303
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8740fed254aca97ab77566e2a7f0ace9a6679d56
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104199193"
---
# <a name="wfp-architecture"></a><span data-ttu-id="ef9db-103">Architecture WFP</span><span class="sxs-lookup"><span data-stu-id="ef9db-103">WFP Architecture</span></span>

<span data-ttu-id="ef9db-104">L’illustration suivante montre l’architecture de base de la plateforme de filtrage Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="ef9db-104">The following figure shows the basic architecture of the Windows Filtering Platform (WFP).</span></span>

![architecture de base du diagramme de plateforme de filtrage Windows](images/wfp-architecture.png)

## <a name="filter-engine"></a><span data-ttu-id="ef9db-106">Moteur de filtre</span><span class="sxs-lookup"><span data-stu-id="ef9db-106">Filter Engine</span></span>

<span data-ttu-id="ef9db-107">Le moteur de filtre contient un composant en mode utilisateur et un composant en mode noyau, qui ensemble effectuent toutes les opérations de filtrage sur les données réseau.</span><span class="sxs-lookup"><span data-stu-id="ef9db-107">The filter engine contains a user-mode component and a kernel-mode component, which together perform all of the filtering operations on network data.</span></span> <span data-ttu-id="ef9db-108">Le moteur de filtre contient plusieurs couches de filtrage qui sont mappées librement aux couches de la pile de mise en réseau du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ef9db-108">The filter engine contains multiple filtering layers that map loosely to the operating system's networking stack layers.</span></span> <span data-ttu-id="ef9db-109">Les couches du moteur de filtre sont divisées en couches en mode utilisateur et en couches en mode noyau, en fonction du composant moteur de filtre qui les possède.</span><span class="sxs-lookup"><span data-stu-id="ef9db-109">The filter engine layers are divided into user-mode layers and kernel-mode layers based on the filter engine component that owns them.</span></span>

<span data-ttu-id="ef9db-110">Le composant de mode utilisateur effectue le filtrage RPC et IPsec.</span><span class="sxs-lookup"><span data-stu-id="ef9db-110">The user-mode component performs RPC and IPsec filtering.</span></span> <span data-ttu-id="ef9db-111">Le moteur de filtre contient environ 10 couches de filtrage en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ef9db-111">The filter engine contains approximately 10 user-mode filtering layers.</span></span>

<span data-ttu-id="ef9db-112">Le composant en mode noyau effectue le filtrage au niveau du réseau et des couches de transport de la pile TC/IP.</span><span class="sxs-lookup"><span data-stu-id="ef9db-112">The kernel-mode component performs filtering at the network and transport layers of the TC/IP stack.</span></span> <span data-ttu-id="ef9db-113">Ce composant appelle également les fonctions de légende disponibles pendant le processus de [classification](basic-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ef9db-113">This component also calls the available callout functions during the [classification](basic-operation.md) process.</span></span> <span data-ttu-id="ef9db-114">Le moteur de filtre contient environ 50 couches de filtrage en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="ef9db-114">The filter engine contains approximately 50 kernel-mode filtering layers.</span></span>

<span data-ttu-id="ef9db-115">Pour obtenir une description de chacune des couches du moteur de filtre, consultez [**filtrage des identificateurs de couche**](management-filtering-layer-identifiers-.md) .</span><span class="sxs-lookup"><span data-stu-id="ef9db-115">See [**Filtering Layer Identifiers**](management-filtering-layer-identifiers-.md) for a description of each of the filter engine layers.</span></span>

## <a name="base-filtering-engine"></a><span data-ttu-id="ef9db-116">Moteur de filtrage de base</span><span class="sxs-lookup"><span data-stu-id="ef9db-116">Base Filtering Engine</span></span>

<span data-ttu-id="ef9db-117">Le moteur de filtrage de base (BFE) est un service en mode utilisateur (bfe.dll s’exécutant dans un processus de svchost.exe) qui coordonne les composants WFP.</span><span class="sxs-lookup"><span data-stu-id="ef9db-117">The Base Filtering Engine (BFE) is a user-mode service (bfe.dll running in a svchost.exe process) that coordinates the WFP components.</span></span> <span data-ttu-id="ef9db-118">Les principales tâches effectuées par BFE sont l’ajout et la suppression de filtres du système, le stockage de la configuration du filtre et l’application de la sécurité de la configuration WFP.</span><span class="sxs-lookup"><span data-stu-id="ef9db-118">The principal tasks performed by BFE are adding and removing filters from the system, storing filter configuration, and enforcing WFP configuration security.</span></span> <span data-ttu-id="ef9db-119">Les applications communiquent avec BFE par le biais des [fonctions de gestion WFP](fwp-mgmt-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ef9db-119">Applications communicate with BFE through the [WFP management functions](fwp-mgmt-functions.md).</span></span>

## <a name="callout-drivers"></a><span data-ttu-id="ef9db-120">Pilotes de légende</span><span class="sxs-lookup"><span data-stu-id="ef9db-120">Callout Drivers</span></span>

<span data-ttu-id="ef9db-121">Les pilotes de légende offrent des fonctionnalités de filtrage supplémentaires en ajoutant des fonctions de légende personnalisées au moteur de filtre à une ou plusieurs couches de filtrage en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="ef9db-121">Callout drivers provide additional filtering functionality by adding custom callout functions to the filter engine at one or more of the kernel-mode filtering layers.</span></span> <span data-ttu-id="ef9db-122">Les légendes prennent en charge l’inspection détaillée et les paquets, ainsi que la modification de flux.</span><span class="sxs-lookup"><span data-stu-id="ef9db-122">Callouts support deep inspection and packet as well as stream modification.</span></span> <span data-ttu-id="ef9db-123">Une fois qu’un pilote Callout a ajouté ses fonctions de légende au moteur de filtre, les filtres qui spécifient la fonction de légende d’un pilote donné peuvent être ajoutés au processus de filtrage.</span><span class="sxs-lookup"><span data-stu-id="ef9db-123">After a callout driver has added its callout functions to the filter engine, filters that specify a given driver's callout function can be added to the filtering process.</span></span> <span data-ttu-id="ef9db-124">Ces filtres peuvent être ajoutés soit par une application de gestion en mode utilisateur, soit par le pilote de légende lui-même.</span><span class="sxs-lookup"><span data-stu-id="ef9db-124">Such filters can be added by either a user-mode management application or by the callout driver itself.</span></span> <span data-ttu-id="ef9db-125">L’interface en mode noyau, fournie dans le kit de développement Windows, ne doit être utilisée qu’en cas de besoin et non en remplacement de l’API en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ef9db-125">The kernel-mode interface, delivered in the Windows Development Kit, should only be used where needed and not as a substitute for the user-mode API.</span></span>

> [!Note]  
> <span data-ttu-id="ef9db-126">Pour plus d’informations sur les pilotes de légende, consultez la section plateforme de filtrage Windows du [Kit de développement Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).</span><span class="sxs-lookup"><span data-stu-id="ef9db-126">For more information on callout drivers, see the Windows Filtering Platform section of the [Windows Development Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).</span></span>

 

<span data-ttu-id="ef9db-127">La plateforme de filtrage Windows comprend un certain nombre de fonctions de légende intégrées qui peuvent être utilisées pour la communication sécurisée des données IPsec, les paramètres de filtrage avec état et le filtrage en mode furtif.</span><span class="sxs-lookup"><span data-stu-id="ef9db-127">The Windows Filtering Platform includes a number of built-in callout functions that can be used for IPsec secure data communication, stateful filtering settings, and stealth-mode filtering.</span></span> <span data-ttu-id="ef9db-128">Pour obtenir la liste complète des fonctions de légende intégrées, consultez [**identificateurs de légende intégrés**](built-in-callout-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="ef9db-128">See [**Built-in Callout Identifiers**](built-in-callout-identifiers.md) for a complete list of built-in callout functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef9db-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ef9db-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef9db-130">Modèle objet</span><span class="sxs-lookup"><span data-stu-id="ef9db-130">Object Model</span></span>](object-model.md)
</dt> <dt>

[<span data-ttu-id="ef9db-131">Opération WFP</span><span class="sxs-lookup"><span data-stu-id="ef9db-131">WFP Operation</span></span>](basic-operation.md)
</dt> <dt>

[<span data-ttu-id="ef9db-132">Pilotes de la plateforme de filtrage Windows-Guide de conception</span><span class="sxs-lookup"><span data-stu-id="ef9db-132">Windows Filtering Platform Callout Drivers - Design Guide</span></span>](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[<span data-ttu-id="ef9db-133">Pilotes de la légende de la plateforme de filtrage Windows-référence</span><span class="sxs-lookup"><span data-stu-id="ef9db-133">Windows Filtering Platform Callout Drivers - Reference</span></span>](/windows-hardware/drivers/ddi/_netvista/)
</dt> </dl>

 

 