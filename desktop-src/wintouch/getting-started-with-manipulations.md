---
title: Manipulations
description: Cette section explique la manipulation d’objets pour Windows Touch.
ms.assetid: 7f905c36-7804-422c-8a60-a281e03c5e15
keywords:
- Tactile Windows, manipulations
- manipulations, à propos de
- manipulations, différences de mouvements
- mouvements, différences de manipulation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10fe65494de990305e4268aa4191b5dabaa267f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309349"
---
# <a name="manipulations"></a><span data-ttu-id="76ef2-107">Manipulations</span><span class="sxs-lookup"><span data-stu-id="76ef2-107">Manipulations</span></span>

<span data-ttu-id="76ef2-108">Cette section explique la manipulation d’objets pour Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="76ef2-108">This section explains object manipulation for Windows Touch.</span></span>

## <a name="manipulation-overview"></a><span data-ttu-id="76ef2-109">Vue d’ensemble de la manipulation</span><span class="sxs-lookup"><span data-stu-id="76ef2-109">Manipulation Overview</span></span>

<span data-ttu-id="76ef2-110">Un moyen pratique de réfléchir aux manipulations consiste à les considérer comme un sur-ensemble de gestes.</span><span class="sxs-lookup"><span data-stu-id="76ef2-110">A convenient way to think about manipulations is to consider them a superset of gestures.</span></span> <span data-ttu-id="76ef2-111">Ce que vous pouvez faire avec les gestes, vous pouvez le faire avec davantage de flexibilité et avec une précision plus fine en utilisant des manipulations.</span><span class="sxs-lookup"><span data-stu-id="76ef2-111">What you can do with gestures, you can do with more flexibility and with finer precision by using manipulations.</span></span> <span data-ttu-id="76ef2-112">La différence entre les manipulations et les gestes est illustrée par un exemple simple.</span><span class="sxs-lookup"><span data-stu-id="76ef2-112">The difference between manipulations and gestures is best demonstrated with a simple example.</span></span> <span data-ttu-id="76ef2-113">Vous pouvez développer un objet et le traduire en même temps à l’aide de manipulations. avec les gestes, vous ne pouvez effectuer qu’un seul à la fois.</span><span class="sxs-lookup"><span data-stu-id="76ef2-113">You can expand an object and at the same time translate it using manipulations; with gestures, you can do only one at a time.</span></span> <span data-ttu-id="76ef2-114">Cette capacité à manipuler un objet en temps réel rend les applications plus intuitives aux utilisateurs en offrant une expérience plus réaliste.</span><span class="sxs-lookup"><span data-stu-id="76ef2-114">This ability to manipulate an object in real time makes applications more intuitive to users by enabling a more realistic experience.</span></span>

<span data-ttu-id="76ef2-115">Les API de manipulation sont utilisées pour simplifier les opérations de transformation sur les objets pour les applications tactiles.</span><span class="sxs-lookup"><span data-stu-id="76ef2-115">The Manipulation APIs are used to simplify transformation operations on objects for touch-enabled applications.</span></span> <span data-ttu-id="76ef2-116">Les manipulations sont effectuées dans Windows 7 par le biais de l’objet COM de manipulations.</span><span class="sxs-lookup"><span data-stu-id="76ef2-116">Manipulations are performed in Windows 7 through the manipulations COM object.</span></span> <span data-ttu-id="76ef2-117">En utilisant des manipulations, les développeurs peuvent prendre en charge l’inertie plus facilement (physique des objets) et peuvent facilement effectuer des transformations sur les objets d’une manière qui est cohérente avec les autres applications.</span><span class="sxs-lookup"><span data-stu-id="76ef2-117">By using manipulations, developers can more easily support inertia (object physics) and can easily perform transformations on objects in a way that is consistent with other applications.</span></span> <span data-ttu-id="76ef2-118">Les sections suivantes expliquent les différentes façons dont vous pouvez effectuer des manipulations.</span><span class="sxs-lookup"><span data-stu-id="76ef2-118">The following sections explain various ways that you can perform manipulations.</span></span>



| <span data-ttu-id="76ef2-119">Section</span><span class="sxs-lookup"><span data-stu-id="76ef2-119">Section</span></span>                                                                                            | <span data-ttu-id="76ef2-120">Description</span><span class="sxs-lookup"><span data-stu-id="76ef2-120">Description</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76ef2-121">Ajout de la prise en charge de manipulation au code non managé</span><span class="sxs-lookup"><span data-stu-id="76ef2-121">Adding Manipulation Support to Unmanaged Code</span></span>](adding-manipulation-support-in-unmanaged-code.md) | <span data-ttu-id="76ef2-122">Explique comment implémenter un récepteur d’événements pour l’interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) et ajouter des gestionnaires d’événements à votre code.</span><span class="sxs-lookup"><span data-stu-id="76ef2-122">Explains how to implement an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface and add event handlers to your code.</span></span> |
| [<span data-ttu-id="76ef2-123">Manipulations avancées</span><span class="sxs-lookup"><span data-stu-id="76ef2-123">Advanced Manipulations</span></span>](advanced-manipulations.md)                                               | <span data-ttu-id="76ef2-124">Explique comment effectuer des manipulations complexes.</span><span class="sxs-lookup"><span data-stu-id="76ef2-124">Explains how to perform complex manipulations.</span></span>                                                                                                       |
| [<span data-ttu-id="76ef2-125">Rotation d’un seul doigt</span><span class="sxs-lookup"><span data-stu-id="76ef2-125">Single Finger Rotation</span></span>](single-finger-rotation.md)                                               | <span data-ttu-id="76ef2-126">Explique comment faire pivoter un objet à l’aide d’un point pivot et du processeur de manipulation.</span><span class="sxs-lookup"><span data-stu-id="76ef2-126">Explains how to rotate an object by using a pivot point and the manipulation processor.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="76ef2-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="76ef2-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76ef2-128">Manipulations et inertie</span><span class="sxs-lookup"><span data-stu-id="76ef2-128">Manipulations and Inertia</span></span>](manipulation-and-inertia.md)
</dt> </dl>

 

 




