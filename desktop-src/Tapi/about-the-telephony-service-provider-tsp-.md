---
description: Un fournisseur de services de téléphonie TAPI (TSP) est une bibliothèque de liens dynamiques (DLL) qui prend en charge le contrôle des appareils de communication via un ensemble de fonctions de service exportées.
ms.assetid: 6e4fb295-940e-4f76-ad43-fad7da90094a
title: À propos du fournisseur de services de téléphonie (TSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5200a4291bdd91aba9f93a5552fecf4b52d24ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750789"
---
# <a name="about-the-telephony-service-provider-tsp"></a><span data-ttu-id="44a49-103">À propos du fournisseur de services de téléphonie (TSP)</span><span class="sxs-lookup"><span data-stu-id="44a49-103">About the Telephony Service Provider (TSP)</span></span>

<span data-ttu-id="44a49-104">\[ Les TSPs H323 et IPConf ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="44a49-104">\[ The H323 and IPConf TSPs are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="44a49-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="44a49-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="44a49-106">Un fournisseur de services de téléphonie TAPI (TSP) est une bibliothèque de liens dynamiques (DLL) qui prend en charge le contrôle des appareils de communication via un ensemble de fonctions de service exportées.</span><span class="sxs-lookup"><span data-stu-id="44a49-106">A TAPI telephony service provider (TSP) is a dynamic-link library (DLL) that supports communications device control through a set of exported service functions.</span></span> <span data-ttu-id="44a49-107">Une application TAPI utilise des commandes standardisées, TAPI passe en formation au fournisseur de services de téléphonie et le TSP gère les commandes spécifiques qui doivent être échangées avec l’appareil.</span><span class="sxs-lookup"><span data-stu-id="44a49-107">A TAPI application uses standardized commands, TAPI passes in formation to the telephony service provider, and the TSP handles the specific commands that must be exchanged with the device.</span></span>

<span data-ttu-id="44a49-108">Les sections suivantes décrivent brièvement les TSPs fournis avec Microsoft Windows :</span><span class="sxs-lookup"><span data-stu-id="44a49-108">The following sections briefly describe the TSPs provided with Microsoft Windows:</span></span>

-   [<span data-ttu-id="44a49-109">TSP H323</span><span class="sxs-lookup"><span data-stu-id="44a49-109">H323 TSP</span></span>](h323-tsp.md)
-   [<span data-ttu-id="44a49-110">TSP IPConf</span><span class="sxs-lookup"><span data-stu-id="44a49-110">IPConf TSP</span></span>](ipconf-tsp.md)
-   [<span data-ttu-id="44a49-111">TSP pilote de périphérique en mode noyau</span><span class="sxs-lookup"><span data-stu-id="44a49-111">Kernel-Mode Device Driver TSP</span></span>](kernel-mode-device-driver-tsp.md)
-   [<span data-ttu-id="44a49-112">TSP proxy NDIS</span><span class="sxs-lookup"><span data-stu-id="44a49-112">NDIS Proxy TSP</span></span>](ndis-proxy-tsp.md)
-   [<span data-ttu-id="44a49-113">TSP distant</span><span class="sxs-lookup"><span data-stu-id="44a49-113">Remote TSP</span></span>](remote-tsp.md)
-   [<span data-ttu-id="44a49-114">TSP tiers</span><span class="sxs-lookup"><span data-stu-id="44a49-114">Third-Party TSP</span></span>](third-party-tsp.md)
-   [<span data-ttu-id="44a49-115">TSP Unimodem</span><span class="sxs-lookup"><span data-stu-id="44a49-115">Unimodem TSP</span></span>](unimodem-tsp.md)

<span data-ttu-id="44a49-116">Pour plus d’informations, consultez le kit de ressources pour le système d’exploitation cible.</span><span class="sxs-lookup"><span data-stu-id="44a49-116">For detailed information, please see the Resource Kit for the target operating system.</span></span> <span data-ttu-id="44a49-117">Les TSPs tiers pour les appareils de communication spécialisés sont généralement fournis par le fabricant et sont installés avec l’appareil.</span><span class="sxs-lookup"><span data-stu-id="44a49-117">Third-party TSPs for specialized communications devices will typically be provided by the manufacturer and will be installed with the device.</span></span>

<span data-ttu-id="44a49-118">Les rubriques suivantes décrivent comment créer un TSP qui fonctionnera correctement dans l’environnement de téléphonie Microsoft, et comment créer une paire TSP/MSP :</span><span class="sxs-lookup"><span data-stu-id="44a49-118">The following topics describe how to create a TSP that will function properly within the Microsoft Telephony environment, and how to create a TSP/MSP pair:</span></span>

-   [<span data-ttu-id="44a49-119">Interface du fournisseur de services de téléphonie (TSPI)</span><span class="sxs-lookup"><span data-stu-id="44a49-119">Telephony Service Provider Interface (TSPI)</span></span>](telephony-service-provider-interface-tspi-.md)
-   [<span data-ttu-id="44a49-120">Référence TSPI</span><span class="sxs-lookup"><span data-stu-id="44a49-120">TSPI Reference</span></span>](tspi-reference.md)
-   [<span data-ttu-id="44a49-121">Fournisseurs de services de média</span><span class="sxs-lookup"><span data-stu-id="44a49-121">Media Service Providers</span></span>](./media-service-providers-start-page.md)

> [!Note]  
> <span data-ttu-id="44a49-122">Un TSP est une DLL créée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="44a49-122">A TSP is a user-created DLL.</span></span> <span data-ttu-id="44a49-123">Si vous créez un TSP pour une plateforme Windows 64 bits, vous devez le compiler en tant que DLL 64 bits ou dll.</span><span class="sxs-lookup"><span data-stu-id="44a49-123">If you are creating a TSP for a 64-bit Windows platform, you must compile it as a 64-bit DLL or DLLs.</span></span>

 

 

 
