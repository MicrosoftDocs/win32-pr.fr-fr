---
title: Vue d’ensemble de DWriteCore
description: DWriteCore est l’implémentation de réunion de projet de DirectWrite.
keywords:
- Le noyau de DirectWrite
- DWriteCore
ms.topic: article
ms.date: 04/21/2021
ms.openlocfilehash: 27a34656ce28a65267bd098974b4df9003a80e17
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881838"
---
# <a name="dwritecore-overview"></a><span data-ttu-id="6716c-105">Vue d’ensemble de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="6716c-105">DWriteCore overview</span></span>

<span data-ttu-id="6716c-106">DWriteCore est l’implémentation de [réunion de projet](/windows/apps/project-reunion/) de [DirectWrite](./direct-write-portal.md) (DirectWrite est l’API DirectX pour le rendu de texte de haute qualité, les polices de plan indépendantes de la résolution et la prise en charge complète du texte et de la disposition Unicode).</span><span class="sxs-lookup"><span data-stu-id="6716c-106">DWriteCore is the [Project Reunion](/windows/apps/project-reunion/) implementation of [DirectWrite](./direct-write-portal.md) (DirectWrite is the DirectX API for high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support).</span></span> <span data-ttu-id="6716c-107">DWriteCore est une forme de DirectWrite qui s’exécute sur les versions de Windows jusqu’à Windows 8, et qui vous permet de l’utiliser sur plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="6716c-107">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="6716c-108">Cette rubrique d’introduction décrit ce que DWriteCore est, et montre comment l’installer dans votre environnement de développement et votre programme avec lui.</span><span class="sxs-lookup"><span data-stu-id="6716c-108">This introductory topic describes what DWriteCore is, and shows how to install it into your dev environment and program with it.</span></span>

## <a name="the-value-proposition-of-dwritecore"></a><span data-ttu-id="6716c-109">La proposition de valeur de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="6716c-109">The value proposition of DWriteCore</span></span>

<span data-ttu-id="6716c-110">[DirectWrite](./direct-write-portal.md) prend en charge un large éventail de fonctionnalités qui en font l’outil de rendu des polices de choix sur Windows pour la plupart des applications &mdash; , que ce soit via des appels directs ou via [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="6716c-110">[DirectWrite](./direct-write-portal.md) itself supports a rich array of features that makes it the font-rendering tool of choice on Windows for most apps&mdash;whether that's through direct calls, or via [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="6716c-111">DirectWrite comprend un système de disposition de texte indépendant du périphérique, un rendu de texte [Microsoft ClearType](/typography/cleartype/) de qualité supérieure, du texte accéléré par le matériel, du texte à plusieurs formats, des fonctionnalités avancées de typographie [® OpenType](/typography/opentype/) , une prise en charge de langage large et une disposition et un rendu compatibles [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="6716c-111">DirectWrite includes a device-independent text layout system, high quality sub-pixel [Microsoft ClearType](/typography/cleartype/) text rendering, hardware-accelerated text, multi-format text, advanced [OpenType®](/typography/opentype/) typography features, wide language support, and [GDI](../gdi/windows-gdi.md)-compatible layout and rendering.</span></span> <span data-ttu-id="6716c-112">DirectWrite est disponible depuis Windows Vista SP2 et a évolué au fil des années pour inclure des fonctionnalités plus avancées, telles que des polices variables, qui permettent aux développeurs d’appliquer des styles, des pondérations et d’autres attributs à une police avec une seule ressource de police.</span><span class="sxs-lookup"><span data-stu-id="6716c-112">DirectWrite has been available since Windows Vista SP2, and it has evolved over the years to include more advanced features such as variable fonts, which enables developers to apply styles, weights, and other attributes to a font with only one font resource.</span></span>

<span data-ttu-id="6716c-113">En raison de la longue durée de validité de DirectWrite, toutefois, les avancées en matière de développement ont tendance à conserver des versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="6716c-113">Due to the long lifespan of DirectWrite, however, advances in development have tended to leave older versions of Windows behind.</span></span> <span data-ttu-id="6716c-114">En outre, l’état de DirectWrite en tant que technologie de rendu de texte premier est limité uniquement à Windows, ce qui laisse les applications multiplateformes écrire leur propre pile de rendu de texte, ou s’appuyer sur des solutions tierces.</span><span class="sxs-lookup"><span data-stu-id="6716c-114">In addition, DirectWrite's status as the premier text rendering technology is limited only to Windows, leaving cross-platform applications to either write their own text-rendering stack, or to rely on 3rd-party solutions.</span></span>

<span data-ttu-id="6716c-115">DWriteCore résout les problèmes fondamentaux de la fonctionnalité de la version orpheline et de la compatibilité multiplateforme en supprimant la bibliothèque du système et en ciblant tous les points de terminaison possibles pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6716c-115">DWriteCore solves the fundamental problems of version feature orphaning and cross-platform compatibility by removing the library from the system, and targeting all possible supported endpoints.</span></span> <span data-ttu-id="6716c-116">À cette fin, nous avons intégré DWriteCore dans le projet de réunion avec une API publique qui est prise en charge sur tous les points de terminaison Windows jusqu’à Windows 8, et qui ouvre la porte pour que vous l’utilisiez sur plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="6716c-116">To that end, we've integrated DWriteCore into Project Reunion with a public API that's supported on all Windows endpoints down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="6716c-117">La valeur principale que DWriteCore vous offre, en tant que développeur, dans le projet de réunion, est qu’elle permet d’accéder à toutes les fonctionnalités de DirectWrite actuelles jusqu’à Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6716c-117">The primary value that DWriteCore gives you, as a developer, in Project Reunion is that it provides access to all current DirectWrite features all the way down-level to Windows 8.</span></span> <span data-ttu-id="6716c-118">Toutes les fonctionnalités de DWriteCore fonctionneront de la même façon sur toutes les versions de niveau supérieur. en d’autres termes, toutes les fonctionnalités actuelles fonctionnent sur Windows 8, 8,1 et toutes les versions de Windows 10, sans aucune disparité quant aux fonctionnalités qui peuvent fonctionner sur les versions de.</span><span class="sxs-lookup"><span data-stu-id="6716c-118">All features of DWriteCore will function the same on all down-level versions; in other words, all current features will work on Windows 8, 8.1, and all versions of Windows 10, without any disparity regarding which features might work on which versions.</span></span>

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a><span data-ttu-id="6716c-119">Application de démonstration DWriteCore &mdash; DWriteCoreGallery</span><span class="sxs-lookup"><span data-stu-id="6716c-119">The DWriteCore demo app&mdash;DWriteCoreGallery</span></span>

<span data-ttu-id="6716c-120">DWriteCore est démontré par le biais de l’exemple d’application [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , que vous pouvez maintenant télécharger et étudier.</span><span class="sxs-lookup"><span data-stu-id="6716c-120">DWriteCore is demonstrated by way of the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app, which is available for you now to download and study.</span></span>

## <a name="get-started-with-dwritecore"></a><span data-ttu-id="6716c-121">Prise en main de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="6716c-121">Get started with DWriteCore</span></span>

<span data-ttu-id="6716c-122">DWriteCore fait partie de la [réunion de projet 0,5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span><span class="sxs-lookup"><span data-stu-id="6716c-122">DWriteCore is part of [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span></span> <span data-ttu-id="6716c-123">Cette section décrit comment configurer votre environnement de développement pour la programmation avec DWriteCore.</span><span class="sxs-lookup"><span data-stu-id="6716c-123">This section describes how to set up your development environment for programming with DWriteCore.</span></span>

### <a name="install-the-project-reunion-05-vsix"></a><span data-ttu-id="6716c-124">Installer le projet de réunion 0,5 VSIX</span><span class="sxs-lookup"><span data-stu-id="6716c-124">Install the Project Reunion 0.5 VSIX</span></span>

<span data-ttu-id="6716c-125">Dans Visual Studio, cliquez sur **Extensions**  >  **gérer les extensions**, recherchez *projet de réunion* et téléchargez l’extension de réunion de projet.</span><span class="sxs-lookup"><span data-stu-id="6716c-125">In Visual Studio, click **Extensions** > **Manage Extensions**, search for *Project Reunion*, and download the Project Reunion extension.</span></span> <span data-ttu-id="6716c-126">Fermez et rouvrez Visual Studio, puis suivez les invites pour installer l’extension.</span><span class="sxs-lookup"><span data-stu-id="6716c-126">Close and reopen Visual Studio, and follow the prompts to install the extension.</span></span>

<span data-ttu-id="6716c-127">Pour plus d’informations, consultez [projet REUNION 0,5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)et [créer des applications Windows pour ordinateur de bureau avec la réunion de projet 0,5](/windows/apps/project-reunion/#set-up-your-development-environment).</span><span class="sxs-lookup"><span data-stu-id="6716c-127">For more info, see [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0), and [Build desktop Windows apps with Project Reunion 0.5](/windows/apps/project-reunion/#set-up-your-development-environment).</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="6716c-128">Créer un projet</span><span class="sxs-lookup"><span data-stu-id="6716c-128">Create a new project</span></span>

<span data-ttu-id="6716c-129">Dans Visual Studio, créez un projet à partir du modèle de projet **application vide, empaqueté (WinUI 3 dans le bureau)** .</span><span class="sxs-lookup"><span data-stu-id="6716c-129">In Visual Studio, create a new project from the **Blank App, Packaged (WinUI 3 in Desktop)** project template.</span></span> <span data-ttu-id="6716c-130">Vous pouvez trouver ce modèle de projet en choisissant langue : *C++*; plateforme : *projet REUNION*; type de projet : *Bureau*.</span><span class="sxs-lookup"><span data-stu-id="6716c-130">You can find that project template by choosing language: *C++*; platform: *Project Reunion*; project type: *Desktop*.</span></span>

<span data-ttu-id="6716c-131">Pour plus d’informations, consultez [modèles de projet pour WinUI 3](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3).</span><span class="sxs-lookup"><span data-stu-id="6716c-131">For more info, see [Project templates for WinUI 3](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3).</span></span>

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a><span data-ttu-id="6716c-132">Installer le package NuGet Microsoft. ProjectReunion. DWrite</span><span class="sxs-lookup"><span data-stu-id="6716c-132">Install the Microsoft.ProjectReunion.DWrite NuGet package</span></span>

<span data-ttu-id="6716c-133">Dans Visual Studio, cliquez sur **projet** \> **gérer les packages NuGet...** \> **Parcourir**, tapez ou collez **Microsoft. ProjectReunion. DWrite** dans la zone de recherche, sélectionnez l’élément dans les résultats de la recherche, puis cliquez sur **installer** pour installer le package pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="6716c-133">In Visual Studio, click **Project** \> **Manage NuGet Packages...** \> **Browse**, type or paste **Microsoft.ProjectReunion.DWrite** in the search box, select the item in search results, and then click **Install** to install the package for that project.</span></span>

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a><span data-ttu-id="6716c-134">Vous pouvez également commencer par l’exemple d’application DWriteCoreGallery</span><span class="sxs-lookup"><span data-stu-id="6716c-134">Alternatively, begin with the DWriteCoreGallery sample app</span></span>

<span data-ttu-id="6716c-135">Vous pouvez également programmer avec DWriteCore en commençant par l’exemple de projet d’application [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , et baser votre développement sur ce projet.</span><span class="sxs-lookup"><span data-stu-id="6716c-135">Alternatively, you can program with DWriteCore by beginning with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project, and base your development on that project.</span></span> <span data-ttu-id="6716c-136">Vous pouvez alors librement supprimer le code source (ou les fichiers) existant de cet exemple de projet et ajouter un nouveau code source (ou des fichiers) au projet.</span><span class="sxs-lookup"><span data-stu-id="6716c-136">You can then feel free to remove any existing source code (or files) from that sample project, and to add any new source code (or files) to the project.</span></span>

### <a name="use-dwritecore-in-your-project"></a><span data-ttu-id="6716c-137">Utiliser DWriteCore dans votre projet</span><span class="sxs-lookup"><span data-stu-id="6716c-137">Use DWriteCore in your project</span></span>

<span data-ttu-id="6716c-138">Pour plus d’informations sur la programmation avec DWriteCore, consultez la section [programmation avec DWriteCore](#programming-with-dwritecore) plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="6716c-138">For more info about programming with DWriteCore, see the [Programming with DWriteCore](#programming-with-dwritecore) section later in this topic.</span></span>

## <a name="the-release-phases-of-dwritecore"></a><span data-ttu-id="6716c-139">Phases de publication de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="6716c-139">The release phases of DWriteCore</span></span>

<span data-ttu-id="6716c-140">Le portage de DirectWrite vers DWriteCore est un projet suffisamment volumineux pour s’étendre sur plusieurs cycles de publication Windows.</span><span class="sxs-lookup"><span data-stu-id="6716c-140">Porting DirectWrite to DWriteCore is a sufficiently large project to span multiple Windows release cycles.</span></span> <span data-ttu-id="6716c-141">Ce projet est divisé en plusieurs phases, chacune correspondant à un segment de fonctionnalités fournies dans une version.</span><span class="sxs-lookup"><span data-stu-id="6716c-141">That project is divided into phases, each of which corresponds to a chunk of functionality delivered in a release.</span></span>

### <a name="features-in-the-current-release-of-dwritecore"></a><span data-ttu-id="6716c-142">Fonctionnalités de la version actuelle de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="6716c-142">Features in the current release of DWriteCore</span></span>

<span data-ttu-id="6716c-143">La version de DWriteCore actuellement disponible contient les outils de base que vous, en tant que développeur, devez utiliser DWriteCore, y compris les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="6716c-143">The version of DWriteCore currently available contains the basic tools that you, as a developer, need to consume DWriteCore, including the following features.</span></span>

- <span data-ttu-id="6716c-144">Énumération des polices.</span><span class="sxs-lookup"><span data-stu-id="6716c-144">Font enumeration.</span></span>
- <span data-ttu-id="6716c-145">API de police.</span><span class="sxs-lookup"><span data-stu-id="6716c-145">Font API.</span></span>
- <span data-ttu-id="6716c-146">Shaping.</span><span class="sxs-lookup"><span data-stu-id="6716c-146">Shaping.</span></span>
- <span data-ttu-id="6716c-147">API de rendu de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="6716c-147">Low-level rendering APIs.</span></span> <span data-ttu-id="6716c-148">Cela est partiel au niveau de la phase actuelle &mdash; DWriteCore n’interagit pas avec [Direct2D](../direct2d/direct2d-portal.md), mais vous pouvez utiliser [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) et [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="6716c-148">This is partial at the current phase&mdash;DWriteCore doesn't interoperate with [Direct2D](../direct2d/direct2d-portal.md), but you can use [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) and [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span></span>
- <span data-ttu-id="6716c-149">Fonctionnalités de base de la disposition du texte.</span><span class="sxs-lookup"><span data-stu-id="6716c-149">Basic text layout functionality.</span></span>
- <span data-ttu-id="6716c-150">API de rendu de texte.</span><span class="sxs-lookup"><span data-stu-id="6716c-150">Text-rendering APIs.</span></span>
- <span data-ttu-id="6716c-151">Cible de rendu bitmap.</span><span class="sxs-lookup"><span data-stu-id="6716c-151">Bitmap render target.</span></span>
- <span data-ttu-id="6716c-152">Polices de couleur.</span><span class="sxs-lookup"><span data-stu-id="6716c-152">Color fonts.</span></span>
- <span data-ttu-id="6716c-153">Optimisations diverses (nettoyage du cache des polices, chargeur de police en mémoire, etc.).</span><span class="sxs-lookup"><span data-stu-id="6716c-153">Miscellaneous optimizations (font cache cleanup, in-memory font loader, and so on).</span></span>

<span data-ttu-id="6716c-154">La fonctionnalité de bannière à ce niveau est polices de couleurs.</span><span class="sxs-lookup"><span data-stu-id="6716c-154">The banner feature at this stage is color fonts.</span></span> <span data-ttu-id="6716c-155">Les polices de couleur vous permettent de restituer vos polices avec des fonctionnalités de couleur plus sophistiquées que des couleurs simples simples.</span><span class="sxs-lookup"><span data-stu-id="6716c-155">Color fonts enable you to render your fonts with more sophisticated color functionality beyond simple single colors.</span></span> <span data-ttu-id="6716c-156">Par exemple, les polices de couleur permettent de rendre les polices d’Emoji et d’icône de barre d’outils (la dernière qui est utilisée par Office, par exemple).</span><span class="sxs-lookup"><span data-stu-id="6716c-156">For example, color fonts is what powers the ability to render emoji and toolbar icon fonts (the latter of which is used by Office, for example).</span></span> <span data-ttu-id="6716c-157">Les polices de couleur ont été introduites pour la première fois dans Windows 8.1, mais la fonctionnalité a été largement développée sur Windows 10, version 1607 (mise à jour anniversaire).</span><span class="sxs-lookup"><span data-stu-id="6716c-157">Color fonts were first introduced in Windows 8.1, but the feature was heavily expanded upon in Windows 10, version 1607 (Anniversary Update).</span></span>

<span data-ttu-id="6716c-158">Le travail au nettoyage du cache de polices et le chargeur de police en mémoire permettent un chargement plus rapide des polices et des améliorations de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="6716c-158">The work on cleanup of the font cache, and the in-memory font loader, allow for faster loading of fonts, and memory improvements.</span></span>

<span data-ttu-id="6716c-159">Grâce à ces fonctionnalités, vous pouvez commencer immédiatement à exploiter certaines fonctionnalités de base modernes de DirectWrite &mdash; , telles que les polices variables &mdash; de niveau inférieure vers Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6716c-159">With these features, you can immediately begin to harness some of DirectWrite's modern core functionality&mdash;such as variable fonts&mdash;down-level to Windows 8.</span></span> <span data-ttu-id="6716c-160">Cette itération de la bibliothèque peut également être consommée sur [Android](https://www.android.com/)et **Linux**.</span><span class="sxs-lookup"><span data-stu-id="6716c-160">This iteration of the library can also be consumed on [Android](https://www.android.com/), and **Linux**.</span></span> <span data-ttu-id="6716c-161">Les polices variables sont l’une des fonctionnalités les plus importantes pour les clients de DirectWrite. ils ont été introduits dans Windows 10, version 1709 (automne Creators Update). par conséquent, l’accès aux versions précédentes est une aubaine importante pour vous en tant que développeur.</span><span class="sxs-lookup"><span data-stu-id="6716c-161">Variable fonts are one of the most important features for DirectWrite customers; they were introduced in Windows 10, version 1709 (Fall Creators Update), so accessing them in previous versions is a massive boon to you as a developer.</span></span>

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a><span data-ttu-id="6716c-162">Notre invitation en tant que développeur DirectWrite</span><span class="sxs-lookup"><span data-stu-id="6716c-162">Our invitation to you as a DirectWrite developer</span></span>

<span data-ttu-id="6716c-163">DWriteCore, ainsi que d’autres composants de réunion de projet, seront développés avec les commentaires des développeurs.</span><span class="sxs-lookup"><span data-stu-id="6716c-163">DWriteCore, along with other Project Reunion components, will be developed with openness to developer feedback.</span></span> <span data-ttu-id="6716c-164">Nous vous invitons à commencer à explorer DWriteCore et à fournir des informations ou des demandes dans le développement de fonctionnalités sur notre [référentiel GitHub de réunion de projet](https://github.com/microsoft/ProjectReunion/).</span><span class="sxs-lookup"><span data-stu-id="6716c-164">We invite you to begin exploring DWriteCore, and to provide insights or requests into feature development on our [Project Reunion GitHub repository](https://github.com/microsoft/ProjectReunion/).</span></span>

## <a name="programming-with-dwritecore"></a><span data-ttu-id="6716c-165">Programmation avec DWriteCore</span><span class="sxs-lookup"><span data-stu-id="6716c-165">Programming with DWriteCore</span></span>

<span data-ttu-id="6716c-166">Comme avec [DirectWrite](./direct-write-portal.md), vous programmez avec DWriteCore via son API com-Light, via l’interface [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="6716c-166">Just like with [DirectWrite](./direct-write-portal.md), you program with DWriteCore via its COM-light API, through the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="6716c-167">Pour utiliser DWriteCore, il est nécessaire d’inclure le `dwrite_core.h` fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="6716c-167">To use DWriteCore, it's necessary to include the `dwrite_core.h` header file.</span></span>

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

<span data-ttu-id="6716c-168">Le `dwrite_core.h` fichier d’en-tête définit d’abord le jeton *DWRITE_CORE*, puis il comprend `dwrite_3.h` .</span><span class="sxs-lookup"><span data-stu-id="6716c-168">The `dwrite_core.h` header file first defines the token *DWRITE_CORE*, and then it includes `dwrite_3.h`.</span></span> <span data-ttu-id="6716c-169">Le jeton *DWRITE_CORE* est important, car il dirige tous les en-têtes inclus ultérieurement pour rendre toutes les API DirectWrite disponibles.</span><span class="sxs-lookup"><span data-stu-id="6716c-169">The *DWRITE_CORE* token is important, because it directs any subsequently included headers to make all of the DirectWrite APIs available to you.</span></span> <span data-ttu-id="6716c-170">Une fois votre projet inclus `dwrite_core.h` , vous pouvez continuer à écrire du code, le générer et l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="6716c-170">Once your project has included `dwrite_core.h`, you can then go ahead and write code, build, and run.</span></span>

### <a name="apis-that-are-new-or-different-for-dwritecore"></a><span data-ttu-id="6716c-171">API nouvelles ou différentes pour DWriteCore</span><span class="sxs-lookup"><span data-stu-id="6716c-171">APIs that are new, or different, for DWriteCore</span></span>

<span data-ttu-id="6716c-172">La surface de l’API DWriteCore est la plus similaire à celle de [DirectWrite](/windows/win32/api/_directwrite/).</span><span class="sxs-lookup"><span data-stu-id="6716c-172">The DWriteCore API surface is the largely the same as it is for [DirectWrite](/windows/win32/api/_directwrite/).</span></span> <span data-ttu-id="6716c-173">Mais il existe un petit nombre de nouvelles API qui se trouvent uniquement dans DWriteCore à l’heure actuelle.</span><span class="sxs-lookup"><span data-stu-id="6716c-173">But there are a small number of new APIs that are only in DWriteCore at the present.</span></span>

#### <a name="create-a-restricted-factory-object"></a><span data-ttu-id="6716c-174">Créer un objet de fabrique restreint</span><span class="sxs-lookup"><span data-stu-id="6716c-174">Create a restricted factory object</span></span>

<span data-ttu-id="6716c-175">L’énumération [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) a une nouvelle constante &mdash; **DWRITE_FACTORY_TYPE_ISOLATED2**, indiquant une fabrique restreinte.</span><span class="sxs-lookup"><span data-stu-id="6716c-175">The [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) enumeration has a new constant&mdash;**DWRITE_FACTORY_TYPE_ISOLATED2**, indicating a restricted factory.</span></span> <span data-ttu-id="6716c-176">Une fabrique restreinte est plus verrouillée qu’une fabrique isolée.</span><span class="sxs-lookup"><span data-stu-id="6716c-176">A restricted factory is more locked-down than an isolated factory.</span></span> <span data-ttu-id="6716c-177">Il n’interagit d’aucune manière avec un cache de polices interprocessus ou persistant.</span><span class="sxs-lookup"><span data-stu-id="6716c-177">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="6716c-178">En outre, la collection de polices système retournée par cette fabrique comprend uniquement des polices bien connues.</span><span class="sxs-lookup"><span data-stu-id="6716c-178">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="6716c-179">Voici comment vous pouvez utiliser **DWRITE_FACTORY_TYPE_ISOLATED2** pour créer un objet de fabrique restreint lorsque vous appelez la fonction Free [**DWriteCoreCreateFactory**](/windows/win32/api/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) .</span><span class="sxs-lookup"><span data-stu-id="6716c-179">Here's how you can use **DWRITE_FACTORY_TYPE_ISOLATED2** to create a restricted factory object when you call the [**DWriteCoreCreateFactory**](/windows/win32/api/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) free function.</span></span>

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

<span data-ttu-id="6716c-180">Si vous transmettez **DWRITE_FACTORY_TYPE_ISOLATED2** à une version antérieure de DirectWrite qui ne la prend pas en charge, **DWriteCreateFactory** retourne **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="6716c-180">If you pass **DWRITE_FACTORY_TYPE_ISOLATED2** to an older version of DirectWrite that doesn't support it, then **DWriteCreateFactory** returns **E_INVALIDARG**.</span></span>

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a><span data-ttu-id="6716c-181">Dessin de glyphes dans une bitmap de mémoire système</span><span class="sxs-lookup"><span data-stu-id="6716c-181">Drawing glyphs to a system memory bitmap</span></span>

<span data-ttu-id="6716c-182">DirectWrite a une interface cible de rendu bitmap qui prend en charge le rendu des glyphes à une image bitmap dans la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="6716c-182">DirectWrite has a bitmap render target interface that supports rendering glyphs to a bitmap in system memory.</span></span> <span data-ttu-id="6716c-183">Toutefois, actuellement, la seule façon d’accéder aux données de pixels sous-jacentes est de traverser GDI, et l’API n’est donc pas utilisable sur plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="6716c-183">However, currently the only way to get access to the underlying pixel data is to go through GDI, and so the API is not usable cross-platform.</span></span> <span data-ttu-id="6716c-184">Cela est facilement résolu en ajoutant une méthode pour récupérer les données de pixels.</span><span class="sxs-lookup"><span data-stu-id="6716c-184">This is easily remedied by adding a method to retrieve the pixel data.</span></span>

<span data-ttu-id="6716c-185">DWriteCore introduit l’interface [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) et sa méthode [**IDWriteBitmapRenderTarget2 :: GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span><span class="sxs-lookup"><span data-stu-id="6716c-185">And so DWriteCore introduces the [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) interface, and its method [**IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span></span> <span data-ttu-id="6716c-186">Cette méthode prend un paramètre de type (pointeur vers) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), qui est un nouveau struct.</span><span class="sxs-lookup"><span data-stu-id="6716c-186">That method takes a parameter of (pointer to) type [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), which is a new struct.</span></span>

<span data-ttu-id="6716c-187">Votre application crée une cible de rendu bitmap en appelant [IDWriteGdiInterop :: CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="6716c-187">Your application creates a bitmap render target by calling [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span></span> <span data-ttu-id="6716c-188">Sur Windows, une cible de rendu bitmap encapsule un DC de mémoire GDI avec une bitmap indépendante du périphérique (DIB) GDI sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="6716c-188">On Windows, a bitmap render target encapsulates a GDI memory DC with a GDI device-independent bitmap (DIB) selected into it.</span></span> <span data-ttu-id="6716c-189">[IDWriteBitmapRenderTarget ::D rawglyphrun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) affiche les glyphes dans le dib.</span><span class="sxs-lookup"><span data-stu-id="6716c-189">[IDWriteBitmapRenderTarget::DrawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) renders glyphs to the DIB.</span></span> <span data-ttu-id="6716c-190">DirectWrite rend les glyphes eux-mêmes sans passer par GDI.</span><span class="sxs-lookup"><span data-stu-id="6716c-190">DirectWrite renders the glyphs itself without going through GDI.</span></span> <span data-ttu-id="6716c-191">Votre application peut ensuite obtenir le **HDC** à partir de la cible de rendu bitmap et utiliser [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) pour copier les pixels dans un **HDC** de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6716c-191">Your application can then get the **HDC** from the bitmap render target, and use [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) to copy the pixels to a window **HDC**.</span></span>

<span data-ttu-id="6716c-192">Sur les plateformes non-Windows, votre application peut toujours créer une cible de rendu bitmap, mais elle encapsule simplement un tableau de mémoire système sans **HDC** ni dib.</span><span class="sxs-lookup"><span data-stu-id="6716c-192">On non-Windows platforms, your application can still create a bitmap render target, but it simply encapsulates a system memory array with no **HDC** and no DIB.</span></span> <span data-ttu-id="6716c-193">Sans **HDC**, votre application doit disposer d’une autre méthode pour obtenir les pixels de la bitmap, afin qu’elle puisse les copier ou les utiliser dans d’autres cas.</span><span class="sxs-lookup"><span data-stu-id="6716c-193">Without an **HDC**, there needs to be another way for your application to get the bitmap pixels so that it can copy them, or otherwise use them.</span></span> <span data-ttu-id="6716c-194">Même sur Windows, il est parfois utile d’acquérir les données de pixels réelles, et nous allons montrer la façon actuelle de le faire dans l’exemple de code ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6716c-194">Even on Windows, it's sometimes useful to get the actual pixel data, and we show the current way to do so in the code example below.</span></span>

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

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a><span data-ttu-id="6716c-195">Autres différences d’API entre DWriteCore et DirectWrite</span><span class="sxs-lookup"><span data-stu-id="6716c-195">Other API differences between DWriteCore and DirectWrite</span></span>

<span data-ttu-id="6716c-196">Il existe quelques API qui sont soit des stubs, soit elles se comportent différemment sur des plateformes non-Windows.</span><span class="sxs-lookup"><span data-stu-id="6716c-196">There are a few APIs that are either stubs only, or they behave somewhat differently on non-Windows platforms.</span></span> <span data-ttu-id="6716c-197">Par exemple, [IDWriteGdiInterop :: CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) retourne **E_NOTIMPL** sur les plateformes non-Windows, car il n’y a pas d’autre chose qu’un **HDC** sans [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="6716c-197">For example, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) returns **E_NOTIMPL** on non-Windows platforms, since there's no such thing as an **HDC** without [GDI](../gdi/windows-gdi.md).</span></span>

<span data-ttu-id="6716c-198">Enfin, il existe certaines API Windows qui sont généralement utilisées avec DirectWrite (Direct2D étant un exemple notable).</span><span class="sxs-lookup"><span data-stu-id="6716c-198">And, finally, there are certain other Windows APIs that are typically used together with DirectWrite (Direct2D being a notable example).</span></span> <span data-ttu-id="6716c-199">Toutefois, à l’heure actuelle, Direct2D et DWriteCore n’interagissent pas.</span><span class="sxs-lookup"><span data-stu-id="6716c-199">However, currently, Direct2D and DWriteCore don't interoperate.</span></span> <span data-ttu-id="6716c-200">Par exemple, si vous créez un [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) à l’aide de DWriteCore et que vous le transmettez à [**D2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), l’appel échoue.</span><span class="sxs-lookup"><span data-stu-id="6716c-200">For example, if you create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) using DWriteCore, and pass it to [**D2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), then that call will fail.</span></span>
