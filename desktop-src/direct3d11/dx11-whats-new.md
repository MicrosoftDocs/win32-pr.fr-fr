---
title: Nouveautés du kit de développement logiciel (SDK) Windows 7/Direct3D 11 d’août 2009
description: Cette version de Windows 7/Direct3D 11 est fournie avec le kit de développement logiciel (SDK) DirectX et contient de nouvelles fonctionnalités, des outils et de la documentation.
ms.assetid: c2dc3726-70a0-49ff-bbad-8ef774bc4868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5e600e5dff679129bb9d007b9f1659bfd018d1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103731557"
---
# <a name="whats-new-in-the-august-2009-windows-7direct3d-11-sdk"></a><span data-ttu-id="8e9b0-103">Nouveautés du kit de développement logiciel (SDK) Windows 7/Direct3D 11 d’août 2009</span><span class="sxs-lookup"><span data-stu-id="8e9b0-103">What's New in the August 2009 Windows 7/Direct3D 11 SDK</span></span>

<span data-ttu-id="8e9b0-104">Cette version de Windows 7/Direct3D 11 est fournie avec le kit de développement logiciel (SDK) DirectX et contient de nouvelles fonctionnalités, des outils et de la documentation.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-104">This version of Windows 7/Direct3D 11 ships as part of the DirectX SDK and contains new features, tools, and documentation.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e9b0-105">Élément</span><span class="sxs-lookup"><span data-stu-id="8e9b0-105">Item</span></span></th>
<th><span data-ttu-id="8e9b0-106">Description</span><span class="sxs-lookup"><span data-stu-id="8e9b0-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8e9b0-107"><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D</span><span class="sxs-lookup"><span data-stu-id="8e9b0-107"><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D</span></span><br/></td>
<td><span data-ttu-id="8e9b0-108">Direct2D est une API graphique à accélération matérielle, en mode immédiat, en 2D, qui offre des performances élevées et un rendu de haute qualité pour la géométrie 2D, les bitmaps et le texte.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-108">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="8e9b0-109">L’API Direct2D est conçue pour interagir correctement avec Direct3D et GDI.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-109">The Direct2D API is designed to interoperate well with Direct3D and GDI.</span></span> <span data-ttu-id="8e9b0-110">Ce kit de développement logiciel (SDK) permet aux développeurs d’évaluer l’API et d’écrire des applications simples, avec certaines des fonctionnalités les plus avancées possibles sur les ordinateurs configurés correctement.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-110">This SDK allows developers to evaluate the API and write simple applications, with some of the more advanced functionality possible on properly configured machines.</span></span> <br/> <span data-ttu-id="8e9b0-111"><a href="/windows/win32/direct2d/direct2d-portal">La documentation</a> et les <a href="/previous-versions//dd372354(v=vs.85)">exemples</a> de Direct2D sont actuellement disponibles sur MSDN.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-111"><a href="/windows/win32/direct2d/direct2d-portal">Documentation</a> and <a href="/previous-versions//dd372354(v=vs.85)">samples</a> for Direct2D are currently available on MSDN.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e9b0-112"><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite</span><span class="sxs-lookup"><span data-stu-id="8e9b0-112"><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite</span></span><br/></td>
<td><span data-ttu-id="8e9b0-113">DirectWrite prend en charge le rendu de texte de haute qualité, les polices de contour indépendantes de la résolution, la prise en charge complète du texte Unicode et de la disposition, et bien plus encore :</span><span class="sxs-lookup"><span data-stu-id="8e9b0-113">DirectWrite provides support for high-quality text rendering, resolution-independent outline fonts, full Unicode text and layout support, and much, much more:</span></span><br/>
<ul>
<li><span data-ttu-id="8e9b0-114">Système de disposition de texte indépendant du périphérique qui améliore la lisibilité du texte dans les documents et dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-114">A device-independent text layout system that improves text readability in documents and in UI.</span></span><br/></li>
<li><span data-ttu-id="8e9b0-115">Rendu de texte ClearType de haute qualité, sous-pixel, qui peut utiliser l’interface GDI Direct3D, Direct2D ou la technologie de rendu propre à l’application.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-115">High-quality, sub-pixel, ClearType text rendering that can use GDI Direct3D, Direct2D, or application-specific rendering technology.</span></span><br/></li>
<li><span data-ttu-id="8e9b0-116">Prise en charge du texte à plusieurs formats.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-116">Support for multi-format text.</span></span> <br/></li>
<li><span data-ttu-id="8e9b0-117">Prise en charge des fonctionnalités typographiques avancées des polices OpenType.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-117">Support for the advanced typography features of OpenType fonts.</span></span><br/></li>
<li><span data-ttu-id="8e9b0-118">Prise en charge de la disposition et du rendu du texte dans toutes les langues prises en charge par Windows.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-118">Support for the layout and rendering of text in all languages supported by Windows.</span></span><br/></li>
</ul>
<span data-ttu-id="8e9b0-119">Ce kit de développement logiciel (SDK) permet aux développeurs d’évaluer l’API et d’écrire des applications de base à des fins de démonstration uniquement.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-119">This SDK allows developers to evaluate the API and write basic applications for demonstration purposes only.</span></span><br/> <span data-ttu-id="8e9b0-120"><a href="/windows/win32/directwrite/direct-write-portal">La documentation</a> et les <a href="/windows/win32/directwrite/samples">exemples</a> de DirectWrite sont actuellement disponibles sur MSDN.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-120"><a href="/windows/win32/directwrite/direct-write-portal">Documentation</a> and <a href="/windows/win32/directwrite/samples">samples</a> for DirectWrite are currently available on MSDN.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e9b0-121"><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1,1</span><span class="sxs-lookup"><span data-stu-id="8e9b0-121"><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1.1</span></span><br/></td>
<td><span data-ttu-id="8e9b0-122"><a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">DXGI 1,1</a> s’appuie sur DXGI 1,0 et sera disponible sur Windows Vista et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-122"><a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">DXGI 1.1</a> builds on DXGI 1.0 and will be available on both Windows Vista and Windows 7.</span></span> <span data-ttu-id="8e9b0-123">DXGI 1,1 ajoute plusieurs nouvelles fonctionnalités :</span><span class="sxs-lookup"><span data-stu-id="8e9b0-123">DXGI 1.1 adds several new features:</span></span><br/>
<ul>
<li><span data-ttu-id="8e9b0-124">Prise en charge des surfaces partagées synchronisées.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-124">Synchronized Shared Surfaces Support.</span></span> <span data-ttu-id="8e9b0-125">Cela permet un partage des surfaces de lecture et d’écriture efficace entre plusieurs périphériques D3D (entre D3D10 et D3D11).</span><span class="sxs-lookup"><span data-stu-id="8e9b0-125">This enables efficient read and write surface sharing between multiple D3D (could be between D3D10 and D3D11) devices.</span></span><br/></li>
<li><span data-ttu-id="8e9b0-126">Prise en charge du format BGRA.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-126">BGRA format support.</span></span> <span data-ttu-id="8e9b0-127">Cela permet à GDI de s’afficher sur la même surface DXGI ciblée par un appareil Direct2D, Direct3D 10,1 ou Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-127">This allows GDI to render to the same DXGI surface targeted by a Direct2D, Direct3D 10.1 or Direct3D 11 device.</span></span> <br/></li>
<li><span data-ttu-id="8e9b0-128">Latence de trame maximale.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-128">Maximum Frame Latency.</span></span> <span data-ttu-id="8e9b0-129">À l’aide de <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1 :: SetMaximumFrameLatency</strong></a> et <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1 :: GetMaximumFrameLatency</strong></a>, les titres peuvent contrôler le nombre de frames qui sont autorisés à être stockés dans une file d’attente avant leur envoi.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-129">Using <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1::SetMaximumFrameLatency</strong></a> and <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1::GetMaximumFrameLatency</strong></a>, titles can control the number of frames that are allowed to be stored in a queue, before submission for rendering.</span></span> <span data-ttu-id="8e9b0-130">La latence est souvent utilisée pour contrôler la façon dont l’UC choisit de répondre aux entrées d’utilisateur et aux trames qui se trouvent dans la file d’attente de rendu.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-130">Latency is often used to control how the CPU chooses between responding to user input and frames that are in the render queue.</span></span><br/></li>
<li><span data-ttu-id="8e9b0-131">Énumération des adaptateurs.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-131">Adapter Enumeration.</span></span> <span data-ttu-id="8e9b0-132">À l’aide de <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1 :: EnumAdapters1</strong></a>, Titles peut énumérer des adaptateurs locaux sans moniteurs ou sorties attachés, ainsi que des adaptateurs avec des sorties attachées.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-132">Using <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1::EnumAdapters1</strong></a>, titles can enumerates local adapters without any monitors or outputs attached, as well as adapters with outputs attached.</span></span><br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e9b0-133"><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Exemples mis à jour</span><span class="sxs-lookup"><span data-stu-id="8e9b0-133"><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Updated Samples</span></span><br/></td>
<td><span data-ttu-id="8e9b0-134">Cette version comporte plusieurs exemples nouveaux et mis à jour.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-134">This release has several new and updated samples.</span></span><br/>
<ul>
<li><span data-ttu-id="8e9b0-135">Le nouveau <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> est une illustration de techniques de traitement de nuanceur de calcul avancées qui peuvent être exécutées sur un GPU D3D10 ou d3d11.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-135">The new <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> is an illustration of more advanced compute shader processing techniques that can be run on a D3D10 or D3D11 GPU.</span></span></li>
<li><span data-ttu-id="8e9b0-136">L' <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">exemple HDRToneMappingCS11</a> a été développé pour implémenter des effets de flou et de floraison (en plus du mappage de tons) à l’aide du nuanceur de calcul, ainsi que des implémentations de nuanceur de pixels pour la comparaison.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-136">The <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11 sample</a> has been expanded to implement blur and bloom effects (in addition to tone mapping) using compute shader, as well as providing pixel shader implementations for comparison.</span></span></li>
<li><span data-ttu-id="8e9b0-137">L' <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">exemple MultithreadedRendering11</a> a été considérablement mis à jour, avec des ressources artistiques plus complexes et un traitement par thread plus intensif.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-137">The <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">MultithreadedRendering11 sample</a> has been significantly updated, with more complex art assets and more intensive per-thread processing.</span></span></li>
<li><span data-ttu-id="8e9b0-138">L' <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">exemple SubD11</a> a été mis à jour avec un nouveau modèle facial, et l’exemple tire parti de la fonctionnalité de calcul contiguïté de l’exportateur de contenu Samples.</span><span class="sxs-lookup"><span data-stu-id="8e9b0-138">The <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">SubD11 sample</a> has been updated with a new facial model, and the sample now leverages the adjacency computation feature of the Samples Content Exporter.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="8e9b0-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e9b0-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e9b0-140">Fonctionnalités introduites dans les versions précédentes</span><span class="sxs-lookup"><span data-stu-id="8e9b0-140">Features Introduced In Previous Releases</span></span>](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

