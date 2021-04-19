---
title: Interfaces de la couche de débogage
description: Les interfaces suivantes sont déclarées dans d3d12sdklayers. h.
ms.assetid: 9BD5910A-8FF2-4540-BB8E-8EA5C10528CE
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e37dbe2e3348a500a8898d1e1076d2fafde66768
ms.sourcegitcommit: 0aa1dd7577961438a1b3172f3a92fb11cbf359f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2020
ms.locfileid: "106510453"
---
# <a name="debug-layer-interfaces"></a><span data-ttu-id="f1594-103">Interfaces de couche de débogage</span><span class="sxs-lookup"><span data-stu-id="f1594-103">Debug Layer interfaces</span></span>

<span data-ttu-id="f1594-104">Les interfaces suivantes sont définies dans `d3d12sdklayers.h` .</span><span class="sxs-lookup"><span data-stu-id="f1594-104">The following interfaces are defined in `d3d12sdklayers.h`.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f1594-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="f1594-105">In this section</span></span>

| <span data-ttu-id="f1594-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="f1594-106">Topic</span></span> | <span data-ttu-id="f1594-107">Description</span><span class="sxs-lookup"><span data-stu-id="f1594-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="f1594-108">**ID3D12Debug**</span><span class="sxs-lookup"><span data-stu-id="f1594-108">**ID3D12Debug**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug) | <span data-ttu-id="f1594-109">Une interface de débogage contrôle les paramètres de débogage et valide l’état du pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1594-109">A debug interface controls debug settings and validates pipeline state.</span></span> <span data-ttu-id="f1594-110">Elle ne peut être utilisée que si la couche de débogage est activée.</span><span class="sxs-lookup"><span data-stu-id="f1594-110">It can only be used if the debug layer is turned on.</span></span> |
| [<span data-ttu-id="f1594-111">**ID3D12Debug1**</span><span class="sxs-lookup"><span data-stu-id="f1594-111">**ID3D12Debug1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1) | <span data-ttu-id="f1594-112">Ajoute la validation basée sur GPU et la synchronisation de la file d’attente de commandes dépendante à la couche de débogage.</span><span class="sxs-lookup"><span data-stu-id="f1594-112">Adds GPU-based validation and Dependent Command Queue Synchronization to the debug layer.</span></span> |
| [<span data-ttu-id="f1594-113">**ID3D12Debug2**</span><span class="sxs-lookup"><span data-stu-id="f1594-113">**ID3D12Debug2**</span></span>](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2) | <span data-ttu-id="f1594-114">Ajoute des niveaux configurables de GPU-Based validation.</span><span class="sxs-lookup"><span data-stu-id="f1594-114">Adds configurable levels of GPU-Based Validation.</span></span> |
| [<span data-ttu-id="f1594-115">**ID3D12Debug3**</span><span class="sxs-lookup"><span data-stu-id="f1594-115">**ID3D12Debug3**</span></span>](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug3) | <span data-ttu-id="f1594-116">Ajoute à la couche de débogage la validation basée sur GPU, à la synchronisation de la file d’attente des commandes dépendante et aux niveaux configurables de validation basée sur GPU.</span><span class="sxs-lookup"><span data-stu-id="f1594-116">Adds to the debug layer GPU-based validation, Dependent Command Queue Synchronization, and configurable levels of GPU-based validation.</span></span> |
| [<span data-ttu-id="f1594-117">**ID3D12DebugCommandList**</span><span class="sxs-lookup"><span data-stu-id="f1594-117">**ID3D12DebugCommandList**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist) | <span data-ttu-id="f1594-118">Fournit des méthodes pour surveiller et déboguer une liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="f1594-118">Provides methods to monitor and debug a command list.</span></span> |
| [<span data-ttu-id="f1594-119">**ID3D12DebugCommandList1**</span><span class="sxs-lookup"><span data-stu-id="f1594-119">**ID3D12DebugCommandList1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1) | <span data-ttu-id="f1594-120">Cette interface permet de modifier les paramètres de couche de débogage de la liste de commandes supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f1594-120">This interface enables modification of additional command list debug layer settings.</span></span> |
| [<span data-ttu-id="f1594-121">**ID3D12DebugCommandQueue**</span><span class="sxs-lookup"><span data-stu-id="f1594-121">**ID3D12DebugCommandQueue**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue) | <span data-ttu-id="f1594-122">Fournit des méthodes pour surveiller et déboguer une file d’attente de commandes.</span><span class="sxs-lookup"><span data-stu-id="f1594-122">Provides methods to monitor and debug a command queue.</span></span> |
| [<span data-ttu-id="f1594-123">**ID3D12DebugDevice**</span><span class="sxs-lookup"><span data-stu-id="f1594-123">**ID3D12DebugDevice**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice) | <span data-ttu-id="f1594-124">Cette interface représente un périphérique graphique pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="f1594-124">This interface represents a graphics device for debugging.</span></span> |
| [<span data-ttu-id="f1594-125">**ID3D12DebugDevice1**</span><span class="sxs-lookup"><span data-stu-id="f1594-125">**ID3D12DebugDevice1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1) | <span data-ttu-id="f1594-126">Spécifie les paramètres de la couche de débogage au niveau de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f1594-126">Specifies device-wide debug layer settings.</span></span> |
| [<span data-ttu-id="f1594-127">**ID3D12InfoQueue**</span><span class="sxs-lookup"><span data-stu-id="f1594-127">**ID3D12InfoQueue**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue) | <span data-ttu-id="f1594-128">Une interface d’informations de file d’attente stocke, récupère et filtre les messages de débogage.</span><span class="sxs-lookup"><span data-stu-id="f1594-128">An information-queue interface stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="f1594-129">La file d’attente se compose d’une file d’attente de messages, d’une pile de filtres de stockage facultative et d’une pile de filtres de récupération facultative.</span><span class="sxs-lookup"><span data-stu-id="f1594-129">The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span> |
| [<span data-ttu-id="f1594-130">**ID3D12SharingContract**</span><span class="sxs-lookup"><span data-stu-id="f1594-130">**ID3D12SharingContract**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract) | <span data-ttu-id="f1594-131">Partie d’un contrat entre les couches de diagnostic D3D11On12 et les outils de diagnostic graphique.</span><span class="sxs-lookup"><span data-stu-id="f1594-131">Part of a contract between D3D11On12 diagnostic layers and graphics diagnostics tools.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="f1594-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f1594-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1594-133">Configuration de l’environnement de programmation Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="f1594-133">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)
</dt> <dt>

[<span data-ttu-id="f1594-134">Référence de la couche de débogage</span><span class="sxs-lookup"><span data-stu-id="f1594-134">Debug Layer Reference</span></span>](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[<span data-ttu-id="f1594-135">Référence de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="f1594-135">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>