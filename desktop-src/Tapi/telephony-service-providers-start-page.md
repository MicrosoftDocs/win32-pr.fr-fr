---
description: Un fournisseur de services de téléphonie (TSP) est une bibliothèque de liens dynamiques (DLL) qui prend en charge le contrôle des appareils de communication via un ensemble de fonctions de service exportées.
ms.assetid: 276c27ac-b6ee-42a7-8327-33dfd87e69bd
title: Fournisseurs de services de téléphonie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3c8887723cc74a1bf0d77bcdcfd06c8468a4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868145"
---
# <a name="telephony-service-providers"></a><span data-ttu-id="f3db6-103">Fournisseurs de services de téléphonie</span><span class="sxs-lookup"><span data-stu-id="f3db6-103">Telephony Service Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="f3db6-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="f3db6-104">Purpose</span></span>

<span data-ttu-id="f3db6-105">Un fournisseur de services de téléphonie (TSP) est une bibliothèque de liens dynamiques (DLL) qui prend en charge le contrôle des appareils de communication via un ensemble de fonctions de service exportées.</span><span class="sxs-lookup"><span data-stu-id="f3db6-105">A telephony service provider (TSP) is a dynamic-link library (DLL) that supports communications device control through a set of exported service functions.</span></span> <span data-ttu-id="f3db6-106">Une application TAPI utilise des commandes standardisées, TAPI transmet des informations au fournisseur de services de téléphonie et le TSP gère les commandes spécifiques qui doivent être échangées avec l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f3db6-106">A TAPI application uses standardized commands, TAPI passes information to the telephony service provider, and the TSP handles the specific commands that must be exchanged with the device.</span></span>

<span data-ttu-id="f3db6-107">Un TSP doit se conformer à l’interface TSPI (Telephony Service Provider Interface) pour fonctionner en tant que fournisseur de services au sein de l’environnement de téléphonie Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f3db6-107">A TSP must conform to the Telephony Service Provider Interface (TSPI) to function as a service provider within the Microsoft Telephony environment.</span></span> <span data-ttu-id="f3db6-108">TSPI définit les fonctions externes exposées par un fournisseur de services de téléphonie fourni avec l’équipement de communication.</span><span class="sxs-lookup"><span data-stu-id="f3db6-108">TSPI defines the external functions exposed by a telephony service provider supplied with communications equipment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="f3db6-109">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="f3db6-109">Developer audience</span></span>

<span data-ttu-id="f3db6-110">Vous pouvez écrire des applications compatibles TAPI dans de nombreux langages, notamment Java, Visual Basic et C/C++.</span><span class="sxs-lookup"><span data-stu-id="f3db6-110">You can write TAPI-enabled applications in many languages, including Java, Visual Basic, and C/C++.</span></span> <span data-ttu-id="f3db6-111">L’expérience de développement précédente avec les télécommunications ou d’autres applications de téléphonie est utile, mais pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f3db6-111">Previous development experience with telecommunications or other telephony applications is helpful but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="f3db6-112">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="f3db6-112">Run-time requirements</span></span>

<span data-ttu-id="f3db6-113">TSPI permet le développement de TSPs pour toutes les versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="f3db6-113">TSPI enables development of TSPs for all versions of Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f3db6-114">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="f3db6-114">In this section</span></span>



| <span data-ttu-id="f3db6-115">Rubrique</span><span class="sxs-lookup"><span data-stu-id="f3db6-115">Topic</span></span>                                                                | <span data-ttu-id="f3db6-116">Description</span><span class="sxs-lookup"><span data-stu-id="f3db6-116">Description</span></span>                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="f3db6-117">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="f3db6-117">Overview</span></span>](about-the-telephony-service-provider-tsp-.md)<br/> | <span data-ttu-id="f3db6-118">Informations générales sur l’architecture et les composants de TSPI.</span><span class="sxs-lookup"><span data-stu-id="f3db6-118">General information about TSPI's architecture and components.</span></span><br/> |
| [<span data-ttu-id="f3db6-119">Référence</span><span class="sxs-lookup"><span data-stu-id="f3db6-119">Reference</span></span>](tspi-reference.md)<br/>                           | <span data-ttu-id="f3db6-120">Documentation pour les interfaces TSPI.</span><span class="sxs-lookup"><span data-stu-id="f3db6-120">Documentation for the TSPI interfaces.</span></span><br/>                        |



 

## <a name="related-topics"></a><span data-ttu-id="f3db6-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f3db6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3db6-122">Vue d’ensemble de la téléphonie Microsoft</span><span class="sxs-lookup"><span data-stu-id="f3db6-122">Microsoft Telephony Overview</span></span>](./microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="f3db6-123">Fournisseurs de services de média</span><span class="sxs-lookup"><span data-stu-id="f3db6-123">Media Service Providers</span></span>](./media-service-providers-start-page.md)
</dt> <dt>

[<span data-ttu-id="f3db6-124">TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="f3db6-124">TAPI 2.2</span></span>](./tapi-2-2-start-page.md)
</dt> <dt>

[<span data-ttu-id="f3db6-125">TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="f3db6-125">TAPI 3.1</span></span>](./tapi-3-1-start-page.md)
</dt> </dl>

 

