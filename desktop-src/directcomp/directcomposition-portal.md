---
title: DirectComposition
description: Cette rubrique décrit l’objectif de Microsoft DirectComposition, identifie ses exigences d’exécution et décrit l’arrière-plan de programmation dont vous avez besoin pour utiliser Microsoft DirectComposition efficacement.
ms.assetid: 40e2d02b-77e8-425f-ac5e-3dcddef08173
keywords:
- DirectComposition
- API DirectComposition
- Microsoft DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb34a4bb3bb7c0ffe370777888e20704fd0165d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309630"
---
# <a name="directcomposition"></a><span data-ttu-id="3d3e4-106">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3d3e4-106">DirectComposition</span></span>

> [!NOTE]
> <span data-ttu-id="3d3e4-107">Pour les applications sur Windows 10, nous vous recommandons d’utiliser des API Windows. UI. composition au lieu de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="3d3e4-107">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="3d3e4-108">Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="3d3e4-108">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

## <a name="purpose"></a><span data-ttu-id="3d3e4-109">Objectif</span><span class="sxs-lookup"><span data-stu-id="3d3e4-109">Purpose</span></span>

<span data-ttu-id="3d3e4-110">Microsoft DirectComposition est un composant Windows qui permet la composition de bitmaps hautes performances avec des transformations, des effets et des animations.</span><span class="sxs-lookup"><span data-stu-id="3d3e4-110">Microsoft DirectComposition is a Windows component that enables high-performance bitmap composition with transforms, effects, and animations.</span></span> <span data-ttu-id="3d3e4-111">Les développeurs d’applications peuvent utiliser l’API DirectComposition pour créer des interfaces utilisateur visuellement attrayantes avec des transitions riches et fluides d’un élément visuel à l’autre.</span><span class="sxs-lookup"><span data-stu-id="3d3e4-111">Application developers can use the DirectComposition API to create visually engaging user interfaces that feature rich and fluid animated transitions from one visual to another.</span></span>

<span data-ttu-id="3d3e4-112">DirectComposition permet d’effectuer des transitions riches et fluides en obtenant une fréquence élevée, en utilisant le matériel graphique et en opérant indépendamment du thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3d3e4-112">DirectComposition enables rich and fluid transitions by achieving a high framerate, using graphics hardware, and operating independently of the UI thread.</span></span> <span data-ttu-id="3d3e4-113">DirectComposition peut accepter le contenu bitmap dessiné par différentes bibliothèques de rendu, y compris les bitmaps Microsoft DirectX, et les bitmaps restitués dans une fenêtre (images bitmap HWND).</span><span class="sxs-lookup"><span data-stu-id="3d3e4-113">DirectComposition can accept bitmap content drawn by different rendering libraries, including Microsoft DirectX bitmaps, and bitmaps rendered to a window (HWND bitmaps).</span></span> <span data-ttu-id="3d3e4-114">En outre, DirectComposition prend en charge diverses transformations, telles que des transformations affines 2D et des transformations de perspective 3D, ainsi que des effets de base tels que le découpage et l’opacité.</span><span class="sxs-lookup"><span data-stu-id="3d3e4-114">Also, DirectComposition supports a variety of transformations, such as 2D affine transforms and 3D perspective transforms, as well as basic effects such as clipping and opacity.</span></span>

<span data-ttu-id="3d3e4-115">DirectComposition est conçu pour simplifier le processus de composition des éléments [*visuels*](directcomposition-glossary.md) et la création de transitions animées.</span><span class="sxs-lookup"><span data-stu-id="3d3e4-115">DirectComposition is designed to simplify the process of composing [*visuals*](directcomposition-glossary.md) and creating animated transitions.</span></span> <span data-ttu-id="3d3e4-116">Si votre application contient déjà du code de rendu ou utilise déjà l’API DirectX recommandée, il vous suffit d’effectuer une quantité minimale de travail pour utiliser DirectComposition efficacement.</span><span class="sxs-lookup"><span data-stu-id="3d3e4-116">If your application already contains rendering code or already uses the recommended DirectX API, you only need to do a minimal amount of work to use DirectComposition effectively.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="3d3e4-117">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="3d3e4-117">Developer audience</span></span>

<span data-ttu-id="3d3e4-118">L’API DirectComposition est conçue pour les développeurs de graphiques expérimentés et très efficaces qui connaissent C/C++, ont une bonne compréhension du modèle COM (Component Object Model) et connaissent les concepts de la programmation Windows.</span><span class="sxs-lookup"><span data-stu-id="3d3e4-118">The DirectComposition API is intended for experienced and highly-capable graphics developers who know C/C++, have a solid understanding of the Component Object Model (COM), and are familiar with Windows programming concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="3d3e4-119">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="3d3e4-119">Run-time requirements</span></span>

<span data-ttu-id="3d3e4-120">DirectComposition a été introduit dans Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3d3e4-120">DirectComposition was introduced in Windows 8.</span></span> <span data-ttu-id="3d3e4-121">Il est inclus dans les plateformes 32 bits, 64 bits et ARM.</span><span class="sxs-lookup"><span data-stu-id="3d3e4-121">It is included in 32-bit, 64-bit, and ARM platforms.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3d3e4-122">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="3d3e4-122">In this section</span></span>



| <span data-ttu-id="3d3e4-123">Rubrique</span><span class="sxs-lookup"><span data-stu-id="3d3e4-123">Topic</span></span>                                                                       | <span data-ttu-id="3d3e4-124">Description</span><span class="sxs-lookup"><span data-stu-id="3d3e4-124">Description</span></span>                                                                                                                                                    |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d3e4-125">Pourquoi utiliser DirectComposition ?</span><span class="sxs-lookup"><span data-stu-id="3d3e4-125">Why use DirectComposition?</span></span>](why-use-directcomposition-.md)<br/>     | <span data-ttu-id="3d3e4-126">Cette rubrique décrit les fonctionnalités et les avantages de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="3d3e4-126">This topic describes the capabilities and benefits of DirectComposition.</span></span> <br/>                                                                           |
| [<span data-ttu-id="3d3e4-127">Utilisation de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3d3e4-127">How to Use DirectComposition</span></span>](how-to-use-directcomposition.md)<br/> | <span data-ttu-id="3d3e4-128">Cette section décrit les meilleures pratiques pour l’utilisation de l’API DirectComposition et montre comment utiliser l’API pour accomplir plusieurs tâches courantes.</span><span class="sxs-lookup"><span data-stu-id="3d3e4-128">This section describes best practices for using the DirectComposition API, and demonstrates how to use the API to accomplish several common tasks.</span></span> <br/> |
| [<span data-ttu-id="3d3e4-129">Concepts DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3d3e4-129">DirectComposition concepts</span></span>](directcomposition-concepts.md)<br/>     | <span data-ttu-id="3d3e4-130">Cette section fournit une vue d’ensemble conceptuelle de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="3d3e4-130">This section provides a conceptual overview of DirectComposition.</span></span><br/>                                                                                   |
| [<span data-ttu-id="3d3e4-131">Référence DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3d3e4-131">DirectComposition reference</span></span>](reference.md)<br/>                     | <span data-ttu-id="3d3e4-132">Cette section fournit des informations de référence détaillées sur les éléments qui composent l’API DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="3d3e4-132">This section provides detailed reference information for the elements that make up the DirectComposition API.</span></span><br/>                                       |
| [<span data-ttu-id="3d3e4-133">Exemples DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3d3e4-133">DirectComposition samples</span></span>](directcomposition-code-samples.md)<br/>  | <span data-ttu-id="3d3e4-134">Les exemples d’applications suivants montrent comment utiliser l’API DirectComposition et illustrer ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="3d3e4-134">The following sample applications show how to use the DirectComposition API and demonstrate its capabilities.</span></span> <br/>                                      |
| [<span data-ttu-id="3d3e4-135">Glossaire DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3d3e4-135">DirectComposition glossary</span></span>](directcomposition-glossary.md)<br/>     | <span data-ttu-id="3d3e4-136">Cette rubrique définit les conditions de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="3d3e4-136">This topic defines DirectComposition terms.</span></span> <br/>                                                                                                        |



 

 

 





