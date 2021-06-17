---
title: Vue d’ensemble de DWriteCore
description: DWriteCore est l’implémentation de réunion de projet de DirectWrite.
keywords:
- Le noyau de DirectWrite
- DWriteCore
ms.topic: article
ms.date: 04/22/2021
ms.openlocfilehash: 0f908f000d340f9cc9f374e036919422c4a940a6
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262641"
---
# <a name="dwritecore-overview"></a><span data-ttu-id="b4644-105">Vue d’ensemble de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="b4644-105">DWriteCore overview</span></span>

<span data-ttu-id="b4644-106">DWriteCore est l’implémentation de [réunion de projet](/windows/apps/project-reunion/) de [DirectWrite](./direct-write-portal.md) (DirectWrite est l’API DirectX pour le rendu de texte de haute qualité, les polices de plan indépendantes de la résolution et la prise en charge complète du texte et de la disposition Unicode).</span><span class="sxs-lookup"><span data-stu-id="b4644-106">DWriteCore is the [Project Reunion](/windows/apps/project-reunion/) implementation of [DirectWrite](./direct-write-portal.md) (DirectWrite is the DirectX API for high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support).</span></span> <span data-ttu-id="b4644-107">DWriteCore est une forme de DirectWrite qui s’exécute sur les versions de Windows jusqu’à Windows 10, version 1809 (10,0 ; Build 17763), et ouvre la porte qui vous permet de l’utiliser sur plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="b4644-107">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 10, version 1809 (10.0; Build 17763), and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="b4644-108">Cette rubrique d’introduction décrit ce que DWriteCore est, et montre comment l’installer dans votre environnement de développement et votre programme avec lui.</span><span class="sxs-lookup"><span data-stu-id="b4644-108">This introductory topic describes what DWriteCore is, and shows how to install it into your dev environment and program with it.</span></span>

> [!TIP]
> <span data-ttu-id="b4644-109">Pour obtenir des descriptions et des liens vers des composants DirectX dans le développement actif, consultez le billet de blog [page d’accueil de DirectX](https://devblogs.microsoft.com/directx/landing-page/).</span><span class="sxs-lookup"><span data-stu-id="b4644-109">For descriptions of and links to DirectX components in active development, see the blog post [DirectX Landing Page](https://devblogs.microsoft.com/directx/landing-page/).</span></span>

## <a name="the-value-proposition-of-dwritecore"></a><span data-ttu-id="b4644-110">La proposition de valeur de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="b4644-110">The value proposition of DWriteCore</span></span>

<span data-ttu-id="b4644-111">[DirectWrite](./direct-write-portal.md) prend en charge un large éventail de fonctionnalités qui en font l’outil de rendu des polices de choix sur Windows pour la plupart des applications &mdash; , que ce soit via des appels directs ou via [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="b4644-111">[DirectWrite](./direct-write-portal.md) itself supports a rich array of features that makes it the font-rendering tool of choice on Windows for most apps&mdash;whether that's through direct calls, or via [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="b4644-112">DirectWrite comprend un système de disposition de texte indépendant du périphérique, un rendu de texte [Microsoft ClearType](/typography/cleartype/) de qualité supérieure, du texte accéléré par le matériel, du texte à plusieurs formats, des fonctionnalités avancées de typographie [® OpenType](/typography/opentype/) , une prise en charge de langage large et une disposition et un rendu compatibles [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="b4644-112">DirectWrite includes a device-independent text layout system, high quality sub-pixel [Microsoft ClearType](/typography/cleartype/) text rendering, hardware-accelerated text, multi-format text, advanced [OpenType®](/typography/opentype/) typography features, wide language support, and [GDI](../gdi/windows-gdi.md)-compatible layout and rendering.</span></span> <span data-ttu-id="b4644-113">DirectWrite est disponible depuis Windows Vista SP2 et a évolué au fil des années pour inclure des fonctionnalités plus avancées, telles que des polices variables, qui vous permettent d’appliquer des styles, des pondérations et d’autres attributs à une police avec une seule ressource de police.</span><span class="sxs-lookup"><span data-stu-id="b4644-113">DirectWrite has been available since Windows Vista SP2, and it has evolved over the years to include more advanced features such as variable fonts, which enables you to apply styles, weights, and other attributes to a font with only one font resource.</span></span>

<span data-ttu-id="b4644-114">En raison de la longue durée de validité de DirectWrite, toutefois, les avancées en matière de développement ont tendance à conserver des versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="b4644-114">Due to the long lifespan of DirectWrite, however, advances in development have tended to leave older versions of Windows behind.</span></span> <span data-ttu-id="b4644-115">En outre, l’état de DirectWrite en tant que technologie de rendu de texte premier est limité uniquement à Windows, ce qui laisse les applications multiplateformes écrire leur propre pile de rendu de texte, ou s’appuyer sur des solutions tierces.</span><span class="sxs-lookup"><span data-stu-id="b4644-115">In addition, DirectWrite's status as the premier text rendering technology is limited only to Windows, leaving cross-platform applications to either write their own text-rendering stack, or to rely on 3rd-party solutions.</span></span>

<span data-ttu-id="b4644-116">DWriteCore résout les problèmes fondamentaux de la fonctionnalité de la version orpheline et de la compatibilité multiplateforme en supprimant la bibliothèque du système et en ciblant tous les points de terminaison possibles pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b4644-116">DWriteCore solves the fundamental problems of version feature orphaning and cross-platform compatibility by removing the library from the system, and targeting all possible supported endpoints.</span></span> <span data-ttu-id="b4644-117">À cette fin, nous avons intégré DWriteCore dans le projet REUNION.</span><span class="sxs-lookup"><span data-stu-id="b4644-117">To that end, we've integrated DWriteCore into Project Reunion.</span></span>

<span data-ttu-id="b4644-118">La valeur principale que DWriteCore vous offre, en tant que développeur, dans le projet de réunion, est qu’elle permet d’accéder à de nombreuses fonctionnalités DirectWrite (et finalement).</span><span class="sxs-lookup"><span data-stu-id="b4644-118">The primary value that DWriteCore gives you, as a developer, in Project Reunion is that it provides access to many (and eventually all) DirectWrite features.</span></span> <span data-ttu-id="b4644-119">Toutes les fonctionnalités de DWriteCore fonctionneront de la même façon sur toutes les versions de niveau inférieure sans aucune disparité quant aux fonctionnalités qui peuvent fonctionner sur les versions.</span><span class="sxs-lookup"><span data-stu-id="b4644-119">All features of DWriteCore will function the same on all down-level versions without any disparity regarding which features might work on which versions.</span></span>

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a><span data-ttu-id="b4644-120">Application de démonstration DWriteCore &mdash; DWriteCoreGallery</span><span class="sxs-lookup"><span data-stu-id="b4644-120">The DWriteCore demo app&mdash;DWriteCoreGallery</span></span>

<span data-ttu-id="b4644-121">DWriteCore est démontré par le biais de l’exemple d’application [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , que vous pouvez maintenant télécharger et étudier.</span><span class="sxs-lookup"><span data-stu-id="b4644-121">DWriteCore is demonstrated by way of the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app, which is available for you now to download and study.</span></span>

## <a name="get-started-with-dwritecore"></a><span data-ttu-id="b4644-122">Prise en main de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="b4644-122">Get started with DWriteCore</span></span>

<span data-ttu-id="b4644-123">DWriteCore fait partie de la [réunion de projet 0,5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span><span class="sxs-lookup"><span data-stu-id="b4644-123">DWriteCore is part of [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span></span> <span data-ttu-id="b4644-124">Cette section décrit comment configurer votre environnement de développement pour la programmation avec DWriteCore.</span><span class="sxs-lookup"><span data-stu-id="b4644-124">This section describes how to set up your development environment for programming with DWriteCore.</span></span>

### <a name="install-the-project-reunion-05-vsix"></a><span data-ttu-id="b4644-125">Installer le projet de réunion 0,5 VSIX</span><span class="sxs-lookup"><span data-stu-id="b4644-125">Install the Project Reunion 0.5 VSIX</span></span>

<span data-ttu-id="b4644-126">Dans Visual Studio, cliquez sur **Extensions**  >  **gérer les extensions**, recherchez *projet de réunion* et téléchargez l’extension de réunion de projet.</span><span class="sxs-lookup"><span data-stu-id="b4644-126">In Visual Studio, click **Extensions** > **Manage Extensions**, search for *Project Reunion*, and download the Project Reunion extension.</span></span> <span data-ttu-id="b4644-127">Fermez et rouvrez Visual Studio, puis suivez les invites pour installer l’extension.</span><span class="sxs-lookup"><span data-stu-id="b4644-127">Close and reopen Visual Studio, and follow the prompts to install the extension.</span></span>

<span data-ttu-id="b4644-128">Pour plus d’informations, consultez [projet REUNION 0,5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)et [configurer votre environnement de développement (pour la réunion de projet)](/windows/apps/project-reunion/get-started-with-project-reunion#set-up-your-development-environment).</span><span class="sxs-lookup"><span data-stu-id="b4644-128">For more info, see [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0), and [Set up your development environment (for Project Reunion)](/windows/apps/project-reunion/get-started-with-project-reunion#set-up-your-development-environment).</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="b4644-129">Création d'un projet</span><span class="sxs-lookup"><span data-stu-id="b4644-129">Create a new project</span></span>

<span data-ttu-id="b4644-130">Dans Visual Studio, créez un projet à partir du modèle de projet **application vide, empaqueté (WinUI 3 dans le bureau)** .</span><span class="sxs-lookup"><span data-stu-id="b4644-130">In Visual Studio, create a new project from the **Blank App, Packaged (WinUI 3 in Desktop)** project template.</span></span> <span data-ttu-id="b4644-131">Vous pouvez trouver ce modèle de projet en choisissant langue : *C++*; plateforme : *projet REUNION*; type de projet : *Bureau*.</span><span class="sxs-lookup"><span data-stu-id="b4644-131">You can find that project template by choosing language: *C++*; platform: *Project Reunion*; project type: *Desktop*.</span></span>

<span data-ttu-id="b4644-132">Pour plus d’informations, consultez [prise en main de WinUI 3 pour les applications de bureau](/windows/apps/winui/winui3/get-started-winui3-for-desktop).</span><span class="sxs-lookup"><span data-stu-id="b4644-132">For more info, see [Get started with WinUI 3 for desktop apps](/windows/apps/winui/winui3/get-started-winui3-for-desktop).</span></span>

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a><span data-ttu-id="b4644-133">Installer le package NuGet Microsoft. ProjectReunion. DWrite</span><span class="sxs-lookup"><span data-stu-id="b4644-133">Install the Microsoft.ProjectReunion.DWrite NuGet package</span></span>

<span data-ttu-id="b4644-134">Dans Visual Studio, cliquez sur **projet** \> **gérer les packages NuGet...** \> **Parcourir**, tapez ou collez **Microsoft. ProjectReunion. DWrite** dans la zone de recherche, sélectionnez l’élément dans les résultats de la recherche, puis cliquez sur **installer** pour installer le package pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="b4644-134">In Visual Studio, click **Project** \> **Manage NuGet Packages...** \> **Browse**, type or paste **Microsoft.ProjectReunion.DWrite** in the search box, select the item in search results, and then click **Install** to install the package for that project.</span></span>

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a><span data-ttu-id="b4644-135">Vous pouvez également commencer par l’exemple d’application DWriteCoreGallery</span><span class="sxs-lookup"><span data-stu-id="b4644-135">Alternatively, begin with the DWriteCoreGallery sample app</span></span>

<span data-ttu-id="b4644-136">Vous pouvez également programmer avec DWriteCore en commençant par l’exemple de projet d’application [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , et baser votre développement sur ce projet.</span><span class="sxs-lookup"><span data-stu-id="b4644-136">Alternatively, you can program with DWriteCore by beginning with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project, and base your development on that project.</span></span> <span data-ttu-id="b4644-137">Vous pouvez alors librement supprimer le code source (ou les fichiers) existant de cet exemple de projet et ajouter un nouveau code source (ou des fichiers) au projet.</span><span class="sxs-lookup"><span data-stu-id="b4644-137">You can then feel free to remove any existing source code (or files) from that sample project, and to add any new source code (or files) to the project.</span></span>

### <a name="use-dwritecore-in-your-project"></a><span data-ttu-id="b4644-138">Utiliser DWriteCore dans votre projet</span><span class="sxs-lookup"><span data-stu-id="b4644-138">Use DWriteCore in your project</span></span>

<span data-ttu-id="b4644-139">Pour plus d’informations sur la programmation avec DWriteCore, consultez la section [programmation avec DWriteCore](#programming-with-dwritecore) plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="b4644-139">For more info about programming with DWriteCore, see the [Programming with DWriteCore](#programming-with-dwritecore) section later in this topic.</span></span>

## <a name="the-release-phases-of-dwritecore"></a><span data-ttu-id="b4644-140">Phases de publication de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="b4644-140">The release phases of DWriteCore</span></span>

<span data-ttu-id="b4644-141">Le portage de DirectWrite vers DWriteCore est un projet suffisamment volumineux pour s’étendre sur plusieurs cycles de publication Windows.</span><span class="sxs-lookup"><span data-stu-id="b4644-141">Porting DirectWrite to DWriteCore is a sufficiently large project to span multiple Windows release cycles.</span></span> <span data-ttu-id="b4644-142">Ce projet est divisé en plusieurs phases, chacune correspondant à un segment de fonctionnalités fournies dans une version.</span><span class="sxs-lookup"><span data-stu-id="b4644-142">That project is divided into phases, each of which corresponds to a chunk of functionality delivered in a release.</span></span>

### <a name="features-in-the-current-release-of-dwritecore"></a><span data-ttu-id="b4644-143">Fonctionnalités de la version actuelle de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="b4644-143">Features in the current release of DWriteCore</span></span>

<span data-ttu-id="b4644-144">La version de DWriteCore actuellement disponible fait partie de la [réunion de projet 0,5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span><span class="sxs-lookup"><span data-stu-id="b4644-144">The version of DWriteCore currently available is part of [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span></span> <span data-ttu-id="b4644-145">Il contient les outils de base que vous, en tant que développeur, devez utiliser DWriteCore, y compris les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4644-145">It contains the basic tools that you, as a developer, need to consume DWriteCore, including the following features.</span></span>

- <span data-ttu-id="b4644-146">Énumération des polices.</span><span class="sxs-lookup"><span data-stu-id="b4644-146">Font enumeration.</span></span>
- <span data-ttu-id="b4644-147">API de police.</span><span class="sxs-lookup"><span data-stu-id="b4644-147">Font API.</span></span>
- <span data-ttu-id="b4644-148">Shaping.</span><span class="sxs-lookup"><span data-stu-id="b4644-148">Shaping.</span></span>
- <span data-ttu-id="b4644-149">API de rendu de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="b4644-149">Low-level rendering APIs.</span></span> <span data-ttu-id="b4644-150">Cela est partiel au niveau de la phase actuelle &mdash; DWriteCore n’interagit pas avec [Direct2D](../direct2d/direct2d-portal.md), mais vous pouvez utiliser [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) et [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="b4644-150">This is partial at the current phase&mdash;DWriteCore doesn't interoperate with [Direct2D](../direct2d/direct2d-portal.md), but you can use [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) and [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span></span>
- <span data-ttu-id="b4644-151">Fonctionnalités de base de la disposition du texte.</span><span class="sxs-lookup"><span data-stu-id="b4644-151">Basic text layout functionality.</span></span>
- <span data-ttu-id="b4644-152">API de rendu de texte.</span><span class="sxs-lookup"><span data-stu-id="b4644-152">Text-rendering APIs.</span></span>
- <span data-ttu-id="b4644-153">Cible de rendu bitmap.</span><span class="sxs-lookup"><span data-stu-id="b4644-153">Bitmap render target.</span></span>
- <span data-ttu-id="b4644-154">Polices de couleur.</span><span class="sxs-lookup"><span data-stu-id="b4644-154">Color fonts.</span></span>
- <span data-ttu-id="b4644-155">Optimisations diverses (nettoyage du cache des polices, chargeur de police en mémoire, etc.).</span><span class="sxs-lookup"><span data-stu-id="b4644-155">Miscellaneous optimizations (font cache cleanup, in-memory font loader, and so on).</span></span>

<span data-ttu-id="b4644-156">Une fonctionnalité de bannière est une police de couleurs.</span><span class="sxs-lookup"><span data-stu-id="b4644-156">A banner feature is color fonts.</span></span> <span data-ttu-id="b4644-157">Les polices de couleur vous permettent de restituer vos polices avec des fonctionnalités de couleur plus sophistiquées que des couleurs simples simples.</span><span class="sxs-lookup"><span data-stu-id="b4644-157">Color fonts enable you to render your fonts with more sophisticated color functionality beyond simple single colors.</span></span> <span data-ttu-id="b4644-158">Par exemple, les polices de couleur permettent de rendre les polices d’Emoji et d’icône de barre d’outils (la dernière qui est utilisée par Office, par exemple).</span><span class="sxs-lookup"><span data-stu-id="b4644-158">For example, color fonts is what powers the ability to render emoji and toolbar icon fonts (the latter of which is used by Office, for example).</span></span> <span data-ttu-id="b4644-159">Les polices de couleur ont été introduites pour la première fois dans Windows 8.1, mais la fonctionnalité a été largement développée sur Windows 10, version 1607 (mise à jour anniversaire).</span><span class="sxs-lookup"><span data-stu-id="b4644-159">Color fonts were first introduced in Windows 8.1, but the feature was heavily expanded upon in Windows 10, version 1607 (Anniversary Update).</span></span>

<span data-ttu-id="b4644-160">Le travail au nettoyage du cache de polices et le chargeur de police en mémoire permettent un chargement plus rapide des polices et des améliorations de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="b4644-160">The work on cleanup of the font cache, and the in-memory font loader, allow for faster loading of fonts, and memory improvements.</span></span>

<span data-ttu-id="b4644-161">Grâce à ces fonctionnalités, vous pouvez commencer immédiatement à exploiter certaines fonctionnalités de base modernes de DirectWrite &mdash; , telles que les polices variables.</span><span class="sxs-lookup"><span data-stu-id="b4644-161">With these features, you can immediately begin to harness some of DirectWrite's modern core functionality&mdash;such as variable fonts.</span></span> <span data-ttu-id="b4644-162">Les polices variables sont l’une des fonctionnalités les plus importantes pour les clients de DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="b4644-162">Variable fonts are one of the most important features for DirectWrite customers.</span></span>

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a><span data-ttu-id="b4644-163">Notre invitation en tant que développeur DirectWrite</span><span class="sxs-lookup"><span data-stu-id="b4644-163">Our invitation to you as a DirectWrite developer</span></span>

<span data-ttu-id="b4644-164">DWriteCore, ainsi que d’autres composants de réunion de projet, seront développés avec les commentaires des développeurs.</span><span class="sxs-lookup"><span data-stu-id="b4644-164">DWriteCore, along with other Project Reunion components, will be developed with openness to developer feedback.</span></span> <span data-ttu-id="b4644-165">Nous vous invitons à commencer à explorer DWriteCore et à fournir des informations ou des demandes dans le développement de fonctionnalités sur notre [référentiel GitHub de réunion de projet](https://github.com/microsoft/ProjectReunion/).</span><span class="sxs-lookup"><span data-stu-id="b4644-165">We invite you to begin exploring DWriteCore, and to provide insights or requests into feature development on our [Project Reunion GitHub repository](https://github.com/microsoft/ProjectReunion/).</span></span>

## <a name="programming-with-dwritecore"></a><span data-ttu-id="b4644-166">Programmation avec DWriteCore</span><span class="sxs-lookup"><span data-stu-id="b4644-166">Programming with DWriteCore</span></span>

<span data-ttu-id="b4644-167">Comme avec [DirectWrite](./direct-write-portal.md), vous programmez avec DWriteCore via son API com-Light, via l’interface [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="b4644-167">Just like with [DirectWrite](./direct-write-portal.md), you program with DWriteCore via its COM-light API, through the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="b4644-168">Pour utiliser DWriteCore, il est nécessaire d’inclure le `dwrite_core.h` fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="b4644-168">To use DWriteCore, it's necessary to include the `dwrite_core.h` header file.</span></span>

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

<span data-ttu-id="b4644-169">Le `dwrite_core.h` fichier d’en-tête définit d’abord le jeton *DWRITE_CORE*, puis il comprend le `dwrite_3.h` fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="b4644-169">The `dwrite_core.h` header file first defines the token *DWRITE_CORE*, and then it includes the `dwrite_3.h` header file.</span></span> <span data-ttu-id="b4644-170">Le jeton *DWRITE_CORE* est important, car il dirige tous les en-têtes inclus ultérieurement pour rendre toutes les API DirectWrite disponibles.</span><span class="sxs-lookup"><span data-stu-id="b4644-170">The *DWRITE_CORE* token is important, because it directs any subsequently included headers to make all of the DirectWrite APIs available to you.</span></span> <span data-ttu-id="b4644-171">Une fois votre projet inclus `dwrite_core.h` , vous pouvez continuer à écrire du code, le générer et l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="b4644-171">Once your project has included `dwrite_core.h`, you can then go ahead and write code, build, and run.</span></span>

### <a name="apis-that-are-new-or-different-for-dwritecore"></a><span data-ttu-id="b4644-172">API nouvelles ou différentes pour DWriteCore</span><span class="sxs-lookup"><span data-stu-id="b4644-172">APIs that are new, or different, for DWriteCore</span></span>

<span data-ttu-id="b4644-173">La surface de l’API DWriteCore est la plus similaire à celle de [DirectWrite](/windows/win32/api/_directwrite/).</span><span class="sxs-lookup"><span data-stu-id="b4644-173">The DWriteCore API surface is the largely the same as it is for [DirectWrite](/windows/win32/api/_directwrite/).</span></span> <span data-ttu-id="b4644-174">Mais il existe un petit nombre de nouvelles API qui se trouvent uniquement dans DWriteCore à l’heure actuelle.</span><span class="sxs-lookup"><span data-stu-id="b4644-174">But there are a small number of new APIs that are only in DWriteCore at the present.</span></span>

#### <a name="create-a-factory-object"></a><span data-ttu-id="b4644-175">Créer un objet de fabrique</span><span class="sxs-lookup"><span data-stu-id="b4644-175">Create a factory object</span></span>

<span data-ttu-id="b4644-176">La fonction Free [**DWriteCoreCreateFactory**](./dwrite_core/nf-dwrite_core-dwritecorecreatefactory.md) crée un objet de fabrique qui est utilisé pour la création suivante d’objets DWriteCore individuels.</span><span class="sxs-lookup"><span data-stu-id="b4644-176">The [**DWriteCoreCreateFactory**](./dwrite_core/nf-dwrite_core-dwritecorecreatefactory.md) free function creates a factory object that is used for subsequent creation of individual DWriteCore objects.</span></span>

<span data-ttu-id="b4644-177">**DWriteCoreCreateFactory** fonctionne de la même façon que la fonction [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) exportée par la version système de DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="b4644-177">**DWriteCoreCreateFactory** is functionally the same as the [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function exported by the system version of DirectWrite.</span></span> <span data-ttu-id="b4644-178">La fonction DWriteCore a un nom différent pour éviter toute ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="b4644-178">The DWriteCore function has a different name to avoid ambiguity.</span></span>

#### <a name="create-a-restricted-factory-object"></a><span data-ttu-id="b4644-179">Créer un objet de fabrique restreint</span><span class="sxs-lookup"><span data-stu-id="b4644-179">Create a restricted factory object</span></span>

<span data-ttu-id="b4644-180">L’énumération [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) a une nouvelle constante &mdash; **DWRITE_FACTORY_TYPE_ISOLATED2**, indiquant une fabrique restreinte.</span><span class="sxs-lookup"><span data-stu-id="b4644-180">The [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) enumeration has a new constant&mdash;**DWRITE_FACTORY_TYPE_ISOLATED2**, indicating a restricted factory.</span></span> <span data-ttu-id="b4644-181">Une fabrique restreinte est plus verrouillée qu’une fabrique isolée.</span><span class="sxs-lookup"><span data-stu-id="b4644-181">A restricted factory is more locked-down than an isolated factory.</span></span> <span data-ttu-id="b4644-182">Il n’interagit d’aucune manière avec un cache de polices interprocessus ou persistant.</span><span class="sxs-lookup"><span data-stu-id="b4644-182">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="b4644-183">En outre, la collection de polices système retournée par cette fabrique comprend uniquement des polices bien connues.</span><span class="sxs-lookup"><span data-stu-id="b4644-183">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="b4644-184">Voici comment vous pouvez utiliser **DWRITE_FACTORY_TYPE_ISOLATED2** pour créer un objet de fabrique restreint lorsque vous appelez la fonction Free [**DWriteCoreCreateFactory**](./dwrite_core/nf-dwrite_core-dwritecorecreatefactory.md) .</span><span class="sxs-lookup"><span data-stu-id="b4644-184">Here's how you can use **DWRITE_FACTORY_TYPE_ISOLATED2** to create a restricted factory object when you call the [**DWriteCoreCreateFactory**](./dwrite_core/nf-dwrite_core-dwritecorecreatefactory.md) free function.</span></span>

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCoreCreateFactory(
    DWRITE_FACTORY_TYPE_ISOLATED2,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

<span data-ttu-id="b4644-185">Si vous transmettez **DWRITE_FACTORY_TYPE_ISOLATED2** à une version antérieure de DirectWrite qui ne la prend pas en charge, **DWriteCreateFactory** retourne **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="b4644-185">If you pass **DWRITE_FACTORY_TYPE_ISOLATED2** to an older version of DirectWrite that doesn't support it, then **DWriteCreateFactory** returns **E_INVALIDARG**.</span></span>

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a><span data-ttu-id="b4644-186">Dessin de glyphes dans une bitmap de mémoire système</span><span class="sxs-lookup"><span data-stu-id="b4644-186">Drawing glyphs to a system memory bitmap</span></span>

<span data-ttu-id="b4644-187">DirectWrite a une interface cible de rendu bitmap qui prend en charge le rendu des glyphes à une image bitmap dans la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="b4644-187">DirectWrite has a bitmap render target interface that supports rendering glyphs to a bitmap in system memory.</span></span> <span data-ttu-id="b4644-188">Toutefois, actuellement, la seule façon d’accéder aux données de pixels sous-jacentes est de traverser GDI, et l’API n’est donc pas utilisable sur plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="b4644-188">However, currently the only way to get access to the underlying pixel data is to go through GDI, and so the API is not usable cross-platform.</span></span> <span data-ttu-id="b4644-189">Cela est facilement résolu en ajoutant une méthode pour récupérer les données de pixels.</span><span class="sxs-lookup"><span data-stu-id="b4644-189">This is easily remedied by adding a method to retrieve the pixel data.</span></span>

<span data-ttu-id="b4644-190">DWriteCore introduit l’interface [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) et sa méthode [**IDWriteBitmapRenderTarget2 :: GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span><span class="sxs-lookup"><span data-stu-id="b4644-190">And so DWriteCore introduces the [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) interface, and its method [**IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span></span> <span data-ttu-id="b4644-191">Cette méthode prend un paramètre de type (pointeur vers) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), qui est un nouveau struct.</span><span class="sxs-lookup"><span data-stu-id="b4644-191">That method takes a parameter of (pointer to) type [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), which is a new struct.</span></span>

<span data-ttu-id="b4644-192">Votre application crée une cible de rendu bitmap en appelant [IDWriteGdiInterop :: CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="b4644-192">Your application creates a bitmap render target by calling [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span></span> <span data-ttu-id="b4644-193">Sur Windows, une cible de rendu bitmap encapsule un DC de mémoire GDI avec une bitmap indépendante du périphérique (DIB) GDI sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="b4644-193">On Windows, a bitmap render target encapsulates a GDI memory DC with a GDI device-independent bitmap (DIB) selected into it.</span></span> <span data-ttu-id="b4644-194">[IDWriteBitmapRenderTarget ::D rawglyphrun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) affiche les glyphes dans le dib.</span><span class="sxs-lookup"><span data-stu-id="b4644-194">[IDWriteBitmapRenderTarget::DrawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) renders glyphs to the DIB.</span></span> <span data-ttu-id="b4644-195">DirectWrite rend les glyphes eux-mêmes sans passer par GDI.</span><span class="sxs-lookup"><span data-stu-id="b4644-195">DirectWrite renders the glyphs itself without going through GDI.</span></span> <span data-ttu-id="b4644-196">Votre application peut ensuite obtenir le **HDC** à partir de la cible de rendu bitmap et utiliser [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) pour copier les pixels dans un **HDC** de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b4644-196">Your application can then get the **HDC** from the bitmap render target, and use [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) to copy the pixels to a window **HDC**.</span></span>

<span data-ttu-id="b4644-197">Sur les plateformes non-Windows, votre application peut toujours créer une cible de rendu bitmap, mais elle encapsule simplement un tableau de mémoire système sans **HDC** ni dib.</span><span class="sxs-lookup"><span data-stu-id="b4644-197">On non-Windows platforms, your application can still create a bitmap render target, but it simply encapsulates a system memory array with no **HDC** and no DIB.</span></span> <span data-ttu-id="b4644-198">Sans **HDC**, votre application doit disposer d’une autre méthode pour obtenir les pixels de la bitmap, afin qu’elle puisse les copier ou les utiliser dans d’autres cas.</span><span class="sxs-lookup"><span data-stu-id="b4644-198">Without an **HDC**, there needs to be another way for your application to get the bitmap pixels so that it can copy them, or otherwise use them.</span></span> <span data-ttu-id="b4644-199">Même sur Windows, il est parfois utile d’acquérir les données de pixels réelles, et nous allons montrer la façon actuelle de le faire dans l’exemple de code ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b4644-199">Even on Windows, it's sometimes useful to get the actual pixel data, and we show the current way to do so in the code example below.</span></span>

```cppwinrt
// pch.h
#pragma once

#include <windows.h>
#include <Unknwn.h>
#include <winrt/Windows.Foundation.h>

// WinMain.cpp
#include "pch.h"
#include <dwrite_core.h>
#pragma comment(lib, "Gdi32")

class TextRenderer
{
    DWRITE_BITMAP_DATA_BGRA32 m_targetBitmapData;

public:
    void InitializeBitmapData(winrt::com_ptr<IDWriteBitmapRenderTarget> const& renderTarget)
    {
        // Query the bitmap render target for the new interface. 
        winrt::com_ptr<IDWriteBitmapRenderTarget2> renderTarget2;
        renderTarget2 = renderTarget.try_as<IDWriteBitmapRenderTarget2>();

        if (renderTarget2)
        {
            // IDWriteBitmapRenderTarget2 exists, so we can get the bitmap the easy way. 
            winrt::check_hresult(renderTarget2->GetBitmapData(OUT & m_targetBitmapData));
        }
        else
        {
            // We're using an older version that doesn't implement IDWriteBitmapRenderTarget2, 
            // so we have to get the bitmap by going through GDI. First get the bitmap handle. 
            HDC hdc = renderTarget->GetMemoryDC();
            winrt::handle dibHandle{ GetCurrentObject(hdc, OBJ_BITMAP) };
            winrt::check_bool(bool{ dibHandle });

            // Call a GDI function to fill in the DIBSECTION structure for the bitmap. 
            DIBSECTION dib;
            winrt::check_bool(GetObject(dibHandle.get(), sizeof(dib), &dib));

            m_targetBitmapData.width = dib.dsBm.bmWidth;
            m_targetBitmapData.height = dib.dsBm.bmHeight;
            m_targetBitmapData.pixels = static_cast<uint32_t*>(dib.dsBm.bmBits);
        }
    }
};

int __stdcall wWinMain(HINSTANCE, HINSTANCE, LPWSTR, int)
{
    TextRenderer textRenderer;
    winrt::com_ptr<IDWriteBitmapRenderTarget> renderTarget{ /* ... */ };
    textRenderer.InitializeBitmapData(renderTarget);
}
```

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a><span data-ttu-id="b4644-200">Autres différences d’API entre DWriteCore et DirectWrite</span><span class="sxs-lookup"><span data-stu-id="b4644-200">Other API differences between DWriteCore and DirectWrite</span></span>

<span data-ttu-id="b4644-201">Il existe quelques API qui sont soit des stubs, soit elles se comportent différemment sur des plateformes non-Windows.</span><span class="sxs-lookup"><span data-stu-id="b4644-201">There are a few APIs that are either stubs only, or they behave somewhat differently on non-Windows platforms.</span></span> <span data-ttu-id="b4644-202">Par exemple, [IDWriteGdiInterop :: CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) retourne **E_NOTIMPL** sur les plateformes non-Windows, car il n’y a pas d’autre chose qu’un **HDC** sans [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="b4644-202">For example, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) returns **E_NOTIMPL** on non-Windows platforms, since there's no such thing as an **HDC** without [GDI](../gdi/windows-gdi.md).</span></span>

<span data-ttu-id="b4644-203">Enfin, il existe certaines API Windows qui sont généralement utilisées avec DirectWrite (Direct2D étant un exemple notable).</span><span class="sxs-lookup"><span data-stu-id="b4644-203">And, finally, there are certain other Windows APIs that are typically used together with DirectWrite (Direct2D being a notable example).</span></span> <span data-ttu-id="b4644-204">Toutefois, à l’heure actuelle, Direct2D et DWriteCore n’interagissent pas.</span><span class="sxs-lookup"><span data-stu-id="b4644-204">However, currently, Direct2D and DWriteCore don't interoperate.</span></span> <span data-ttu-id="b4644-205">Par exemple, si vous créez un [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) à l’aide de DWriteCore et que vous le transmettez à [**D2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), l’appel échoue.</span><span class="sxs-lookup"><span data-stu-id="b4644-205">For example, if you create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) using DWriteCore, and pass it to [**D2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), then that call will fail.</span></span>
