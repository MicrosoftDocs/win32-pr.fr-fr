---
title: Vues de l’ordre du rastériseur
description: Les vues triées du rastériseur (ROVs) autorisent le code du nuanceur de pixels à marquer des liaisons UAV avec une déclaration qui modifie les exigences normales pour l’ordre des résultats de la canalisation Graphics pour UAVs.
ms.assetid: 7FCFCD28-E68D-4594-8879-937F57245507
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d891701aeaadd6f4474aeed8303d9b0046d1b656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102081"
---
# <a name="rasterizer-order-views"></a><span data-ttu-id="68b73-103">Vues de l’ordre du rastériseur</span><span class="sxs-lookup"><span data-stu-id="68b73-103">Rasterizer Order Views</span></span>

<span data-ttu-id="68b73-104">Les vues triées du rastériseur (ROVs) autorisent le code du nuanceur de pixels à marquer des liaisons UAV avec une déclaration qui modifie les exigences normales pour l’ordre des résultats de la canalisation Graphics pour UAVs.</span><span class="sxs-lookup"><span data-stu-id="68b73-104">Rasterizer ordered views (ROVs) allow pixel shader code to mark UAV bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span> <span data-ttu-id="68b73-105">Cela permet l’utilisation d’algorithmes OIT (commande Independent transparent), ce qui donne de meilleurs résultats de rendu lorsque plusieurs objets transparents sont alignés les uns avec les autres dans une vue.</span><span class="sxs-lookup"><span data-stu-id="68b73-105">This enables Order Independent Transparency (OIT) algorithms to work, which give much better rendering results when multiple transparent objects are in line with each other in a view.</span></span>

-   [<span data-ttu-id="68b73-106">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="68b73-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="68b73-107">Détails de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="68b73-107">Implementation details</span></span>](#implementation-details)
-   [<span data-ttu-id="68b73-108">API summary</span><span class="sxs-lookup"><span data-stu-id="68b73-108">API summary</span></span>](#api-summary)
-   [<span data-ttu-id="68b73-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="68b73-109">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="68b73-110">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="68b73-110">Overview</span></span>

<span data-ttu-id="68b73-111">Les pipelines graphiques standard peuvent avoir des difficultés à converser correctement ensemble plusieurs textures qui contiennent de la transparence.</span><span class="sxs-lookup"><span data-stu-id="68b73-111">Standard graphics pipelines may have trouble correctly compositing together multiple textures that contain transparency.</span></span> <span data-ttu-id="68b73-112">Les objets tels que les clôtures de câble, les fumées, les incendies, les végétations et les verres de couleur utilisent la transparence pour atteindre l’effet souhaité.</span><span class="sxs-lookup"><span data-stu-id="68b73-112">Objects such as wire fences, smoke, fire, vegetation, and colored glass use transparency to get the desired effect.</span></span> <span data-ttu-id="68b73-113">Des problèmes surviennent lorsque plusieurs textures contenant de la transparence sont alignées les unes avec les autres (fumée devant une clôture devant une couche de verre contenant de la végétation, par exemple).</span><span class="sxs-lookup"><span data-stu-id="68b73-113">Problems arise when multiple textures that contain transparency are in line with each other (smoke in front of a fence in front of a glass building containing vegetation, as an example).</span></span> <span data-ttu-id="68b73-114">Les vues triées du rastériseur (ROVs) permettent aux algorithmes OIT sous-jacents d’utiliser les fonctionnalités du matériel pour tenter de résoudre correctement l’ordre de transparence.</span><span class="sxs-lookup"><span data-stu-id="68b73-114">Rasterizer ordered views (ROVs) enable the underlying OIT algorithms to use features of the hardware to try to resolve the transparency order correctly.</span></span> <span data-ttu-id="68b73-115">La transparence est gérée par le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="68b73-115">Transparency is handled by the pixel shader.</span></span>

<span data-ttu-id="68b73-116">Les vues triées du rastériseur (ROVs) autorisent le code du nuanceur de pixels à marquer des liaisons UAV avec une déclaration qui modifie les exigences normales pour l’ordre des résultats de la canalisation Graphics pour UAVs.</span><span class="sxs-lookup"><span data-stu-id="68b73-116">Rasterizer ordered views (ROVs) allow pixel shader code to mark UAV bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span>

<span data-ttu-id="68b73-117">ROVs garantissent l’ordre des accès à UAV pour toutes les paires d’appels de nuanceur de pixels qui se chevauchent.</span><span class="sxs-lookup"><span data-stu-id="68b73-117">ROVs guarantee the order of UAV accesses for any pair of overlapping pixel shader invocations.</span></span> <span data-ttu-id="68b73-118">Dans ce cas, « se chevauchant » signifie que les appels sont générés par les mêmes appels de dessin et partagent la même coordonnée de pixels en mode d’exécution de fréquence en pixels, et les mêmes coordonnées et coordonnée de l’échantillon en mode échantillonnage-fréquence.</span><span class="sxs-lookup"><span data-stu-id="68b73-118">In this case “overlapping” means that the invocations are generated by the same draw calls and share the same pixel coordinate when in pixel-frequency execution mode, and the same pixel and sample coordinate in sample-frequency mode.</span></span>

<span data-ttu-id="68b73-119">L’ordre dans lequel les accès ROV se chevauchant aux appels de nuanceur de pixels sont exécutés est identique à l’ordre dans lequel la géométrie est soumise.</span><span class="sxs-lookup"><span data-stu-id="68b73-119">The order in which overlapping ROV accesses of pixel shader invocations are executed is identical to the order in which the geometry is submitted.</span></span> <span data-ttu-id="68b73-120">Cela signifie que, pour les appels de nuanceur de pixels qui se chevauchent, les écritures ROV effectuées par un appel de nuanceur de pixels doivent être disponibles pour être lues par un appel ultérieur et ne doivent pas affecter les lectures effectuées par un appel précédent.</span><span class="sxs-lookup"><span data-stu-id="68b73-120">This means that, for overlapping pixel shader invocations, ROV writes performed by a pixel shader invocation must be available to be read by a subsequent invocation and must not affect reads by a previous invocation.</span></span> <span data-ttu-id="68b73-121">Les lectures ROV effectuées par un appel de nuanceur de pixels doivent refléter les écritures par un appel précédent et ne doivent pas refléter les écritures par un appel ultérieur.</span><span class="sxs-lookup"><span data-stu-id="68b73-121">ROV reads performed by a pixel shader invocation must reflect writes by a previous invocation and must not reflect writes by a subsequent invocation.</span></span> <span data-ttu-id="68b73-122">Cela est important pour UAVs, car ils sont explicitement omis des garanties de non-variance de sortie définies normalement par l’ordre fixe des résultats de la canalisation Graphics.</span><span class="sxs-lookup"><span data-stu-id="68b73-122">This is important for UAVs because they are explicitly omitted from the output-invariance guarantees normally set by the fixed order of graphics pipeline results.</span></span>

## <a name="implementation-details"></a><span data-ttu-id="68b73-123">Informations d’implémentation</span><span class="sxs-lookup"><span data-stu-id="68b73-123">Implementation details</span></span>

<span data-ttu-id="68b73-124">Les vues triées du rastériseur (ROVs) sont déclarées avec les nouveaux objets HLSL (High Level Shader Language) suivants, et sont uniquement disponibles pour le nuanceur de pixels :</span><span class="sxs-lookup"><span data-stu-id="68b73-124">Rasterizer ordered views (ROVs) are declared with the following new High Level Shader Language (HLSL) objects, and are only available to the pixel shader:</span></span>

-   `RasterizerOrderedBuffer`
-   `RasterizerOrderedByteAddressBuffer`
-   `RasterizerOrderedStructuredBuffer`
-   `RasterizerOrderedTexture1D`
-   `RasterizerOrderedTexture1DArray`
-   `RasterizerOrderedTexture2D`
-   `RasterizerOrderedTexture2DArray`
-   `RasterizerOrderedTexture3D`

<span data-ttu-id="68b73-125">Utilisez ces objets de la même façon que les autres objets UAV (tels que `RWBuffer` etc.).</span><span class="sxs-lookup"><span data-stu-id="68b73-125">Use these objects in the same manner as other UAV objects (such as `RWBuffer` etc.).</span></span>

## <a name="api-summary"></a><span data-ttu-id="68b73-126">Résumé des API</span><span class="sxs-lookup"><span data-stu-id="68b73-126">API summary</span></span>

<span data-ttu-id="68b73-127">Les ROVs sont une construction en HLSL uniquement qui applique une sémantique de comportement différente à UAVs.</span><span class="sxs-lookup"><span data-stu-id="68b73-127">ROVs are an HLSL-only construct that applies different behavior semantics to UAVs.</span></span> <span data-ttu-id="68b73-128">Toutes les API relatives à UAVs sont également pertinentes pour ROVs.</span><span class="sxs-lookup"><span data-stu-id="68b73-128">All APIs relevant to UAVs are also relevant to ROVs.</span></span> <span data-ttu-id="68b73-129">Notez que la méthode, les structures et la classe d’assistance suivantes référencent le rastériseur :</span><span class="sxs-lookup"><span data-stu-id="68b73-129">Note that the following method, structures, and helper class reference the rasterizer:</span></span>

-   <span data-ttu-id="68b73-130">[**D3d11 \_ RASTÉRISEUR \_ DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : structure contenant la description du rastériseur, en notant la \_ \_ classe d’assistance CD3D12 rastériseur DESC2 pour la création de descriptions de rastériseur.</span><span class="sxs-lookup"><span data-stu-id="68b73-130">[**D3D11\_RASTERIZER\_DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : structure holding the rasterizer description, noting the CD3D12\_RASTERIZER\_DESC2 helper class for creating rasterizer descriptions.</span></span>
-   <span data-ttu-id="68b73-131">[**D3d11 \_ Données de fonctionnalités \_ \_ d3d11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : structure contenant la valeur booléenne `ROVsSupported` , indiquant la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="68b73-131">[**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : structure holding the boolean `ROVsSupported`, indicating the support.</span></span>
-   <span data-ttu-id="68b73-132">[**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : méthode permettant d’accéder aux fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="68b73-132">[**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : method to access the supported features.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68b73-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="68b73-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68b73-134">Fonctionnalités Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="68b73-134">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="68b73-135">Modèle de nuanceur 5,1</span><span class="sxs-lookup"><span data-stu-id="68b73-135">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 