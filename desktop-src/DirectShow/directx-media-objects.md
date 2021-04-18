---
description: Objets multimédia DirectX
ms.assetid: e4424740-31b9-4317-8791-6a9aebb0c7e6
title: Objets multimédia DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2119fc8cce602bc1cc085886edd6852320aca180
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522874"
---
# <a name="directx-media-objects"></a><span data-ttu-id="bbc2a-103">Objets multimédia DirectX</span><span class="sxs-lookup"><span data-stu-id="bbc2a-103">DirectX Media Objects</span></span>

> [!Note]  
> <span data-ttu-id="bbc2a-104">Les DMOs ont été remplacés par [Media Foundation transformations](/windows/desktop/medfound/media-foundation-transforms) (MFTS).</span><span class="sxs-lookup"><span data-stu-id="bbc2a-104">DMOs have been superseded by [Media Foundation Transforms](/windows/desktop/medfound/media-foundation-transforms) (MFTs).</span></span> <span data-ttu-id="bbc2a-105">Les interfaces DMO sont toujours prises en charge.</span><span class="sxs-lookup"><span data-stu-id="bbc2a-105">The DMO interfaces are still supported.</span></span> <span data-ttu-id="bbc2a-106">Toutefois, si vous écrivez un codec personnalisé ou un plug-in de traitement audio/vidéo, vous devez envisager de l’implémenter en tant que table MFT.</span><span class="sxs-lookup"><span data-stu-id="bbc2a-106">However, if you are writing a custom codec or audio/video processing plug-in, you should consider implementing it as an MFT.</span></span>

 

<span data-ttu-id="bbc2a-107">Les objets DMOs (DirectX Media Objects) sont des composants de diffusion en continu de données COM.</span><span class="sxs-lookup"><span data-stu-id="bbc2a-107">DirectX Media Objects (DMOs) are COM-based data-streaming components.</span></span> <span data-ttu-id="bbc2a-108">À certains égards, les DMOs sont similaires aux filtres Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="bbc2a-108">In some respects, DMOs are similar to Microsoft DirectShow filters.</span></span> <span data-ttu-id="bbc2a-109">À l’instar des filtres DirectShow, DMOs prend les données d’entrée et les utilise pour produire des données de sortie.</span><span class="sxs-lookup"><span data-stu-id="bbc2a-109">Like DirectShow filters, DMOs take input data and use it to produce output data.</span></span> <span data-ttu-id="bbc2a-110">Toutefois, les interfaces de programmation d’applications (API) pour DMOs sont bien plus simples que les API correspondantes pour DirectShow.</span><span class="sxs-lookup"><span data-stu-id="bbc2a-110">However, the application programming interfaces (APIs) for DMOs are much simpler than the corresponding APIs for DirectShow.</span></span> <span data-ttu-id="bbc2a-111">Par conséquent, les DMOs sont plus faciles à créer, à tester et à utiliser.</span><span class="sxs-lookup"><span data-stu-id="bbc2a-111">As a result, DMOs are easier to create, test, and use.</span></span> <span data-ttu-id="bbc2a-112">DMOs peut être utilisé dans de nombreux scénarios :</span><span class="sxs-lookup"><span data-stu-id="bbc2a-112">DMOs can be used in many scenarios:</span></span>

-   <span data-ttu-id="bbc2a-113">Les applications basées sur DirectShow peuvent utiliser DMOs via un filtre DirectShow appelé filtre de [wrappers DMO](dmo-wrapper-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="bbc2a-113">Applications based on DirectShow can use DMOs through a DirectShow filter called the [DMO Wrapper](dmo-wrapper-filter.md) filter.</span></span> <span data-ttu-id="bbc2a-114">La distinction entre les filtres et les DMOs est transparente pour l’application.</span><span class="sxs-lookup"><span data-stu-id="bbc2a-114">The distinction between filters and DMOs is transparent to the application.</span></span> <span data-ttu-id="bbc2a-115">L’application n’appelle pas directement les API DMO.</span><span class="sxs-lookup"><span data-stu-id="bbc2a-115">The application does not directly call the DMO APIs.</span></span>
-   <span data-ttu-id="bbc2a-116">Les applications basées sur Microsoft DirectSound peuvent utiliser l’effet audio DMOs.</span><span class="sxs-lookup"><span data-stu-id="bbc2a-116">Applications based on Microsoft DirectSound can use audio effect DMOs.</span></span> <span data-ttu-id="bbc2a-117">Là encore, l’application est protégée des API DMO de bas niveau par les API DirectSound de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="bbc2a-117">Again, the application is shielded from the low-level DMO APIs by the higher-level DirectSound APIs.</span></span>
-   <span data-ttu-id="bbc2a-118">Les applications peuvent utiliser DMOs directement.</span><span class="sxs-lookup"><span data-stu-id="bbc2a-118">Applications can use DMOs directly.</span></span>

<span data-ttu-id="bbc2a-119">Ainsi, en écrivant un DMO, vous créez un composant qui peut être utilisé dans un large éventail d’applications.</span><span class="sxs-lookup"><span data-stu-id="bbc2a-119">Thus, by writing a DMO, you create a component that can be used in a wide range of applications.</span></span> <span data-ttu-id="bbc2a-120">Cette documentation contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="bbc2a-120">This documentation contains the following sections:</span></span>

-   [<span data-ttu-id="bbc2a-121">À propos de DMOs</span><span class="sxs-lookup"><span data-stu-id="bbc2a-121">About DMOs</span></span>](about-dmos.md)
-   [<span data-ttu-id="bbc2a-122">Utilisation de DMOs</span><span class="sxs-lookup"><span data-stu-id="bbc2a-122">Using DMOs</span></span>](using-dmos.md)
-   [<span data-ttu-id="bbc2a-123">Écriture d’un DMO</span><span class="sxs-lookup"><span data-stu-id="bbc2a-123">Writing a DMO</span></span>](writing-a-dmo.md)
-   [<span data-ttu-id="bbc2a-124">Paramètres de média</span><span class="sxs-lookup"><span data-stu-id="bbc2a-124">Media Parameters</span></span>](media-parameters.md)
-   [<span data-ttu-id="bbc2a-125">Référence DMO</span><span class="sxs-lookup"><span data-stu-id="bbc2a-125">DMO Reference</span></span>](dmo-reference.md)

## <a name="related-topics"></a><span data-ttu-id="bbc2a-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bbc2a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbc2a-127">DirectShow</span><span class="sxs-lookup"><span data-stu-id="bbc2a-127">DirectShow</span></span>](directshow.md)
</dt> </dl>

 

 
