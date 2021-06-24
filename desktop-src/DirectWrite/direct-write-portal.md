---
title: DirectWrite (DWrite)
description: Les applications actuelles doivent prendre en charge le rendu de texte de haute qualité, les polices de contour indépendantes de la résolution et la prise en charge complète du texte Unicode et de la disposition. DirectWrite, une API [DirectX](../directx.md) , fournit ces fonctionnalités et bien plus encore.
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6bdc75845c2387a4fa4335fa462d0b97ec5669
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587936"
---
# <a name="directwrite-dwrite"></a><span data-ttu-id="f28cd-104">DirectWrite (DWrite)</span><span class="sxs-lookup"><span data-stu-id="f28cd-104">DirectWrite (DWrite)</span></span>

## <a name="purpose"></a><span data-ttu-id="f28cd-105">Objectif</span><span class="sxs-lookup"><span data-stu-id="f28cd-105">Purpose</span></span>

<span data-ttu-id="f28cd-106">Les applications actuelles doivent prendre en charge le rendu de texte de haute qualité, les polices de contour indépendantes de la résolution et la prise en charge complète du texte Unicode et de la disposition.</span><span class="sxs-lookup"><span data-stu-id="f28cd-106">Today's applications must support high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support.</span></span> <span data-ttu-id="f28cd-107">DirectWrite, une API [DirectX](../directx.md) , fournit ces fonctionnalités et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="f28cd-107">DirectWrite, a [DirectX](../directx.md) API, provides these features and more.</span></span>

- <span data-ttu-id="f28cd-108">Système de disposition de texte indépendant du périphérique qui améliore la lisibilité du texte dans les documents et dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f28cd-108">A device-independent text layout system that improves text readability in documents and in UI.</span></span>
- <span data-ttu-id="f28cd-109">Rendu de texte [Microsoft ClearType](/typography/cleartype/) de haute qualité, sous-pixel, qui peut utiliser [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md)ou la technologie de rendu propre à l’application.</span><span class="sxs-lookup"><span data-stu-id="f28cd-109">High-quality, sub-pixel, [Microsoft ClearType](/typography/cleartype/) text rendering that can use [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md), or application-specific rendering technology.</span></span>
- <span data-ttu-id="f28cd-110">Texte avec accélération matérielle, lorsqu’il est utilisé avec [Direct2D](rendering-by-using-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="f28cd-110">Hardware-accelerated text, when used with [Direct2D](rendering-by-using-direct2d.md).</span></span>
- <span data-ttu-id="f28cd-111">Prise en charge du texte à plusieurs formats.</span><span class="sxs-lookup"><span data-stu-id="f28cd-111">Support for multi-format text.</span></span>
- <span data-ttu-id="f28cd-112">Prise en charge des fonctionnalités typographiques avancées des polices OpenType.</span><span class="sxs-lookup"><span data-stu-id="f28cd-112">Support for the advanced typography features of OpenType fonts.</span></span>
- <span data-ttu-id="f28cd-113">Prise en charge de la disposition et du rendu du texte dans toutes les langues prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f28cd-113">Support for the layout and rendering of text in all supported languages.</span></span>
- <span data-ttu-id="f28cd-114">Mise en page et rendu compatibles [GDI](interoperating-with-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="f28cd-114">[GDI](interoperating-with-gdi.md)-compatible layout and rendering.</span></span>

<span data-ttu-id="f28cd-115">L’API prend en charge la mesure, le dessin et le test d’atteinte du texte à plusieurs formats.</span><span class="sxs-lookup"><span data-stu-id="f28cd-115">The API supports measuring, drawing, and hit-testing of multi-format text.</span></span> <span data-ttu-id="f28cd-116">DirectWrite gère le texte dans toutes les langues prises en charge pour les applications globales et localisées, en se basant sur l’infrastructure de langage clé qui se trouve dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f28cd-116">DirectWrite handles text in all supported languages for global and localized applications, building on the key language infrastructure found in Windows 7.</span></span> <span data-ttu-id="f28cd-117">DirectWrite fournit également une API de rendu de glyphe de bas niveau pour les développeurs désireux de réaliser leurs propres disposition et traitement d’Unicode à glyphe.</span><span class="sxs-lookup"><span data-stu-id="f28cd-117">DirectWrite also provides a low-level glyph rendering API for developers who want to perform their own layout and Unicode-to-glyph processing.</span></span>

> [!NOTE]
> <span data-ttu-id="f28cd-118">Le [Kit de développement logiciel (SDK) d’application Windows](/windows/apps/windows-app-sdk/) introduit une nouvelle version de DirectWrite &mdash; appelée DWriteCore &mdash; qui s’exécute sur des versions de Windows vers Windows 8, et ouvre la porte qui vous permet de l’utiliser sur plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="f28cd-118">[Windows App SDK](/windows/apps/windows-app-sdk/) introduces a new version of DirectWrite&mdash;called DWriteCore&mdash;that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="f28cd-119">Pour plus d’informations, consultez [vue d’ensemble de DWriteCore](dwritecore-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f28cd-119">For more details, see [DWriteCore overview](dwritecore-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="f28cd-120">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="f28cd-120">Run-time requirements</span></span>

- <span data-ttu-id="f28cd-121">Windows 7 ou Windows Vista avec Service Pack 2 (SP2) et mise à jour de la plateforme pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f28cd-121">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista</span></span>
- <span data-ttu-id="f28cd-122">Windows Server 2008 R2 ou Windows Server 2008 avec Service Pack 2 (SP2) et mise à jour de plateforme pour Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f28cd-122">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f28cd-123">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="f28cd-123">In this section</span></span>

| <span data-ttu-id="f28cd-124">Rubrique</span><span class="sxs-lookup"><span data-stu-id="f28cd-124">Topic</span></span> | <span data-ttu-id="f28cd-125">Description</span><span class="sxs-lookup"><span data-stu-id="f28cd-125">Description</span></span> |
|-|-|
| [<span data-ttu-id="f28cd-126">Nouveautés de DirectWrite</span><span class="sxs-lookup"><span data-stu-id="f28cd-126">What's new in DirectWrite</span></span>](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | <span data-ttu-id="f28cd-127">Voici quelques-uns des nouveaux ajouts à DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="f28cd-127">Here are some of the new additions to DirectWrite.</span></span> <br/> |
| [<span data-ttu-id="f28cd-128">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="f28cd-128">Programming Guide</span></span>](programming-guide.md)<br/> | <span data-ttu-id="f28cd-129">Les rubriques suivantes fournissent une vue d’ensemble de l’API DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="f28cd-129">The following topics provide an overview of the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="f28cd-130">Référence sur l’API</span><span class="sxs-lookup"><span data-stu-id="f28cd-130">API Reference</span></span>](reference.md)<br/> | <span data-ttu-id="f28cd-131">Décrit l’API DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="f28cd-131">Describes the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="f28cd-132">Exemple de Code</span><span class="sxs-lookup"><span data-stu-id="f28cd-132">Sample Code</span></span>](samples.md)<br/> | <span data-ttu-id="f28cd-133">Cette section contient des informations sur les exemples de programmes pour DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="f28cd-133">This section contains information about sample programs for DirectWrite.</span></span><br/> |
