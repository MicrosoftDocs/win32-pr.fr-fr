---
title: StreamSelectOperation, classe
description: Inscrit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par GetMuteAsync se termine, et fournit une méthode qui retourne les résultats de l’opération. | StreamSelectOperation, classe
ms.assetid: 681142B4-AECD-42D0-A2D4-494E69A29025
keywords:
- API de diffusion multimédia en continu de la classe StreamSelectOperation
- API de diffusion multimédia en continu de la classe StreamSelectOperation, décrite
topic_type:
- apiref
api_name:
- StreamSelectOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4a19ff2826f0f2ea3e5ef01841ce482d2f293a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211535"
---
# <a name="streamselectoperation-class"></a><span data-ttu-id="e69c1-106">StreamSelectOperation, classe</span><span class="sxs-lookup"><span data-stu-id="e69c1-106">StreamSelectOperation class</span></span>

<span data-ttu-id="e69c1-107">Inscrit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) se termine, et fournit une méthode qui retourne les résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e69c1-107">Registers an event handler that is invoked when the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) completes, and provides a method that returns the results of the operation.</span></span>

<span data-ttu-id="e69c1-108">**StreamSelectOperation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e69c1-108">**StreamSelectOperation** has these types of members:</span></span>

-   [<span data-ttu-id="e69c1-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e69c1-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="e69c1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e69c1-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e69c1-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e69c1-111">Methods</span></span>

<span data-ttu-id="e69c1-112">La classe **StreamSelectOperation** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e69c1-112">The **StreamSelectOperation** class has these methods.</span></span>



| <span data-ttu-id="e69c1-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="e69c1-113">Method</span></span>                                                 | <span data-ttu-id="e69c1-114">Description</span><span class="sxs-lookup"><span data-stu-id="e69c1-114">Description</span></span>                                                                                                                                       |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e69c1-115">**GetResults**</span><span class="sxs-lookup"><span data-stu-id="e69c1-115">**GetResults**</span></span>](streamselectoperation-getresults.md) | <span data-ttu-id="e69c1-116">Retourne les résultats de l’opération asynchrone démarrée par [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e69c1-116">Returns the results of the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e69c1-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e69c1-117">Properties</span></span>

<span data-ttu-id="e69c1-118">La classe **StreamSelectOperation** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e69c1-118">The **StreamSelectOperation** class has these properties.</span></span>



| <span data-ttu-id="e69c1-119">Propriété</span><span class="sxs-lookup"><span data-stu-id="e69c1-119">Property</span></span>                                                        | <span data-ttu-id="e69c1-120">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="e69c1-120">Access type</span></span>           | <span data-ttu-id="e69c1-121">Description</span><span class="sxs-lookup"><span data-stu-id="e69c1-121">Description</span></span>                                                                                                                                                                             |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e69c1-122">**Completed**</span><span class="sxs-lookup"><span data-stu-id="e69c1-122">**Completed**</span></span>](streamselectoperation-completed.md)<br/> | <span data-ttu-id="e69c1-123">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e69c1-123">Read/write</span></span><br/> | <span data-ttu-id="e69c1-124">Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) est terminée.</span><span class="sxs-lookup"><span data-stu-id="e69c1-124">Gets or sets an event handler that is invoked when the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) is completed.</span></span><br/> |



 

 

