---
title: Utilisation de Direct2D pour le rendu Server-Side
description: Décrit l’utilisation de Direct2D pour le rendu côté serveur.
ms.assetid: 12bf4f14-d86f-40ff-b3d3-15ffb3bd7300
keywords:
- Direct2D, rendu côté serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a35c9df619ee43d11c90c171598c87b6e447dd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382077"
---
# <a name="using-direct2d-for-server-side-rendering"></a><span data-ttu-id="b4eff-104">Utilisation de Direct2D pour le rendu Server-Side</span><span class="sxs-lookup"><span data-stu-id="b4eff-104">Using Direct2D for Server-Side Rendering</span></span>

<span data-ttu-id="b4eff-105">Direct2D est bien adapté aux applications graphiques qui requièrent un rendu côté serveur sur Windows Server.</span><span class="sxs-lookup"><span data-stu-id="b4eff-105">Direct2D is well-suited for graphics applications that require server-side rendering on Windows Server.</span></span> <span data-ttu-id="b4eff-106">Cette vue d’ensemble décrit les principes fondamentaux de l’utilisation de Direct2D pour le rendu côté serveur.</span><span class="sxs-lookup"><span data-stu-id="b4eff-106">This overview describes the basics of using Direct2D for server-side rendering.</span></span> <span data-ttu-id="b4eff-107">Il contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="b4eff-107">It contains the following sections:</span></span>

-   [<span data-ttu-id="b4eff-108">Conditions requises pour le rendu Server-Side</span><span class="sxs-lookup"><span data-stu-id="b4eff-108">Requirements for Server-Side Rendering</span></span>](#requirements-for-server-side-rendering)
-   [<span data-ttu-id="b4eff-109">Options pour les API disponibles</span><span class="sxs-lookup"><span data-stu-id="b4eff-109">Options for Available APIs</span></span>](#options-for-available-apis)
    -   [<span data-ttu-id="b4eff-110">GDI</span><span class="sxs-lookup"><span data-stu-id="b4eff-110">GDI</span></span>](#gdi)
    -   [<span data-ttu-id="b4eff-111">GDI+</span><span class="sxs-lookup"><span data-stu-id="b4eff-111">GDI+</span></span>](#gdi)
    -   [<span data-ttu-id="b4eff-112">Direct2D</span><span class="sxs-lookup"><span data-stu-id="b4eff-112">Direct2D</span></span>](#using-direct2d-for-server-side-rendering)
-   [<span data-ttu-id="b4eff-113">Utilisation de Direct2D pour le rendu Server-Side</span><span class="sxs-lookup"><span data-stu-id="b4eff-113">How to Use Direct2D for Server-Side Rendering</span></span>](#how-to-use-direct2d-for-server-side-rendering)
    -   [<span data-ttu-id="b4eff-114">Rendu logiciel</span><span class="sxs-lookup"><span data-stu-id="b4eff-114">Software Rendering</span></span>](#software-rendering)
    -   [<span data-ttu-id="b4eff-115">Traitement multithread</span><span class="sxs-lookup"><span data-stu-id="b4eff-115">Multithreading</span></span>](#multithreading)
    -   [<span data-ttu-id="b4eff-116">Génération d’un fichier bitmap</span><span class="sxs-lookup"><span data-stu-id="b4eff-116">Generating a Bitmap File</span></span>](#generating-a-bitmap-file)
-   [<span data-ttu-id="b4eff-117">Conclusion</span><span class="sxs-lookup"><span data-stu-id="b4eff-117">Conclusion</span></span>](#conclusion)
-   [<span data-ttu-id="b4eff-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b4eff-118">Related topics</span></span>](#related-topics)

## <a name="requirements-for-server-side-rendering"></a><span data-ttu-id="b4eff-119">Conditions requises pour le rendu Server-Side</span><span class="sxs-lookup"><span data-stu-id="b4eff-119">Requirements for Server-Side Rendering</span></span>

<span data-ttu-id="b4eff-120">Voici un scénario classique pour un serveur de graphique : les graphiques et les graphiques sont rendus sur un serveur et remis en tant que bitmaps en réponse aux requêtes Web.</span><span class="sxs-lookup"><span data-stu-id="b4eff-120">The following is a typical scenario for a chart server: charts and graphics are rendered on a server and delivered as bitmaps in response to Web requests.</span></span> <span data-ttu-id="b4eff-121">Le serveur peut être équipé d’une carte graphique de bas niveau ou d’aucune carte graphique.</span><span class="sxs-lookup"><span data-stu-id="b4eff-121">The server might be equipped with a low-end graphics card or no graphics card at all.</span></span>

<span data-ttu-id="b4eff-122">Ce scénario révèle trois exigences en matière d’applications.</span><span class="sxs-lookup"><span data-stu-id="b4eff-122">This scenario reveals three application requirements.</span></span> <span data-ttu-id="b4eff-123">Tout d’abord, l’application doit gérer efficacement plusieurs requêtes simultanées, en particulier sur les serveurs multicœurs.</span><span class="sxs-lookup"><span data-stu-id="b4eff-123">First, the application must handle multiple concurrent requests efficiently, especially on multicore servers.</span></span> <span data-ttu-id="b4eff-124">Deuxièmement, l’application doit utiliser le rendu logiciel lors de l’exécution sur des serveurs avec une carte graphique de bas niveau ou aucune carte graphique.</span><span class="sxs-lookup"><span data-stu-id="b4eff-124">Second, the application must use software rendering when running on servers with a low-end graphics card or no graphics card.</span></span> <span data-ttu-id="b4eff-125">Enfin, l’application doit s’exécuter en tant que service dans la session 0 afin qu’il ne soit pas nécessaire qu’un utilisateur soit connecté.</span><span class="sxs-lookup"><span data-stu-id="b4eff-125">Finally, the application must run as a service in Session 0 so that it does not require a user to be logged in.</span></span> <span data-ttu-id="b4eff-126">Pour plus d’informations sur la session 0, consultez [impact de l’isolation de la session 0 sur les services et les pilotes dans Windows](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx).</span><span class="sxs-lookup"><span data-stu-id="b4eff-126">For more information about Session 0, see [Impact of Session 0 Isolation on Services and Drivers in Windows](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx).</span></span>

## <a name="options-for-available-apis"></a><span data-ttu-id="b4eff-127">Options pour les API disponibles</span><span class="sxs-lookup"><span data-stu-id="b4eff-127">Options for Available APIs</span></span>

<span data-ttu-id="b4eff-128">Il existe trois options pour le rendu côté serveur : GDI, GDI+ et Direct2D.</span><span class="sxs-lookup"><span data-stu-id="b4eff-128">There are three options for server-side rendering: GDI, GDI+ and Direct2D.</span></span> <span data-ttu-id="b4eff-129">À l’instar de GDI et GDI+, Direct2D est une API de rendu 2D native qui permet aux applications de mieux contrôler l’utilisation des périphériques graphiques.</span><span class="sxs-lookup"><span data-stu-id="b4eff-129">Like GDI and GDI+, Direct2D is a native 2D rendering API that gives applications more control over the use of graphics devices.</span></span> <span data-ttu-id="b4eff-130">En outre, Direct2D prend en charge de façon unique une fabrique à thread unique et une fabrique multithread.</span><span class="sxs-lookup"><span data-stu-id="b4eff-130">In addition, Direct2D uniquely supports a single-threaded and a multithreaded factory.</span></span> <span data-ttu-id="b4eff-131">Les sections suivantes comparent chaque API en termes de qualité de dessin et de rendu multithread côté serveur.</span><span class="sxs-lookup"><span data-stu-id="b4eff-131">The following sections compare each API in terms of drawing qualities and multithreaded server-side rendering.</span></span>

### <a name="gdi"></a><span data-ttu-id="b4eff-132">GDI</span><span class="sxs-lookup"><span data-stu-id="b4eff-132">GDI</span></span>

<span data-ttu-id="b4eff-133">Contrairement à Direct2D et GDI+, GDI ne prend pas en charge les fonctionnalités de dessin de haute qualité.</span><span class="sxs-lookup"><span data-stu-id="b4eff-133">Unlike Direct2D and GDI+, GDI does not support high-quality drawing features.</span></span> <span data-ttu-id="b4eff-134">Par exemple, GDI ne prend pas en charge l’anticrénelage pour créer des courbes lissées et n’a qu’une prise en charge limitée de la transparence.</span><span class="sxs-lookup"><span data-stu-id="b4eff-134">For instance, GDI does not support antialiasing for creating smooth lines and has only limited support for transparency.</span></span> <span data-ttu-id="b4eff-135">En fonction des résultats des tests de performances graphiques sur Windows 7 et Windows Server 2008 R2, la mise à l’échelle de Direct2D est plus efficace que GDI, malgré la reconception des verrous dans GDI.</span><span class="sxs-lookup"><span data-stu-id="b4eff-135">Based on the graphics performance test results on Windows 7 and Windows Server 2008 R2, Direct2D scales more efficiently than GDI, despite the redesign of locks in GDI.</span></span> <span data-ttu-id="b4eff-136">Pour plus d’informations sur ces résultats de tests, consultez [ingénierie des performances graphiques de Windows 7](/archive/blogs/e7/engineering-windows-7-graphics-performance).</span><span class="sxs-lookup"><span data-stu-id="b4eff-136">For more information about these test results, see [Engineering Windows 7 Graphics Performance](/archive/blogs/e7/engineering-windows-7-graphics-performance).</span></span>

<span data-ttu-id="b4eff-137">En outre, les applications utilisant GDI sont limitées aux descripteurs GDI 10240 par processus et 65536 Handles GDI par session.</span><span class="sxs-lookup"><span data-stu-id="b4eff-137">In addition, applications using GDI are limited to 10240 GDI handles per process and 65536 GDI handles per session.</span></span> <span data-ttu-id="b4eff-138">Cela est dû au fait que Windows en interne utilise un mot 16 bits pour stocker l’index des descripteurs pour chaque session.</span><span class="sxs-lookup"><span data-stu-id="b4eff-138">The reason is that internally Windows uses a 16-bit WORD to store the index of handles for each session.</span></span>

### <a name="gdi"></a><span data-ttu-id="b4eff-139">GDI+</span><span class="sxs-lookup"><span data-stu-id="b4eff-139">GDI+</span></span>

<span data-ttu-id="b4eff-140">Bien que GDI+ prenne en charge l’anticrénelage et la fusion alpha pour un dessin de grande qualité, le principal problème avec GDI+ pour les scénarios de serveur est qu’il ne prend pas en charge l’exécution dans la session 0.</span><span class="sxs-lookup"><span data-stu-id="b4eff-140">While GDI+ supports antialiasing and alpha blending for high-quality drawing, the main problem with GDI+ for server-scenarios is that it does not support running in Session 0.</span></span> <span data-ttu-id="b4eff-141">Étant donné que la session 0 ne prend en charge que les fonctionnalités non interactives, les fonctions qui interagissent directement ou indirectement avec les appareils d’affichage recevront donc des erreurs.</span><span class="sxs-lookup"><span data-stu-id="b4eff-141">Since Session 0 only supports non-interactive functionality, functions that directly or indirectly interact with display devices will therefore receive errors.</span></span> <span data-ttu-id="b4eff-142">Les exemples de fonctions spécifiques incluent non seulement ceux qui traitent des appareils d’affichage, mais également ceux qui traitent indirectement des pilotes de périphérique.</span><span class="sxs-lookup"><span data-stu-id="b4eff-142">Specific examples of functions include not only those dealing with display devices, but also those indirectly dealing with device drivers.</span></span>

<span data-ttu-id="b4eff-143">Semblable à GDI, GDI+ est limité par son mécanisme de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="b4eff-143">Similar to GDI, GDI+ is limited by its locking mechanism.</span></span> <span data-ttu-id="b4eff-144">Les mécanismes de verrouillage dans GDI+ sont les mêmes dans Windows 7 et Windows Server 2008 R2, comme dans les versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="b4eff-144">The locking mechanisms in GDI+ are the same in Windows 7 and Windows Server 2008 R2 as in previous versions.</span></span>

### <a name="direct2d"></a><span data-ttu-id="b4eff-145">Direct2D</span><span class="sxs-lookup"><span data-stu-id="b4eff-145">Direct2D</span></span>

<span data-ttu-id="b4eff-146">Direct2D est une API graphique à accélération matérielle, en mode immédiat, en 2D, qui offre des performances élevées et un rendu de haute qualité.</span><span class="sxs-lookup"><span data-stu-id="b4eff-146">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high-quality rendering.</span></span> <span data-ttu-id="b4eff-147">Il offre une fabrique à thread unique et une fabrique multithread, ainsi que la mise à l’échelle linéaire d’un rendu logiciel à granularité de cours.</span><span class="sxs-lookup"><span data-stu-id="b4eff-147">It offers a single-threaded and a multithreaded factory and the linear scaling of course-grained software rendering.</span></span>

<span data-ttu-id="b4eff-148">Pour ce faire, Direct2D définit une interface de fabrique racine.</span><span class="sxs-lookup"><span data-stu-id="b4eff-148">To do this, Direct2D defines a root factory interface.</span></span> <span data-ttu-id="b4eff-149">En règle générale, un objet créé sur une fabrique peut uniquement être utilisé avec d’autres objets créés à partir de la même fabrique.</span><span class="sxs-lookup"><span data-stu-id="b4eff-149">As a rule, an object created on a factory can only be used with other objects created from the same factory.</span></span> <span data-ttu-id="b4eff-150">L’appelant peut demander une fabrique à thread unique ou multithread lorsqu’il est créé.</span><span class="sxs-lookup"><span data-stu-id="b4eff-150">The caller can request either a single-threaded or a multithreaded factory when it is created.</span></span> <span data-ttu-id="b4eff-151">Si une fabrique à thread unique est demandée, aucun verrouillage de threads n’est effectué.</span><span class="sxs-lookup"><span data-stu-id="b4eff-151">If a single-threaded factory is requested, then no locking of threads is performed.</span></span> <span data-ttu-id="b4eff-152">Si l’appelant demande une fabrique multithread, un verrou de thread à l’intérieur de l’usine est acquis à chaque fois qu’un appel est effectué dans Direct2D.</span><span class="sxs-lookup"><span data-stu-id="b4eff-152">If the caller requests a multithreaded factory, then, a factory-wide thread lock is acquired whenever a call is made into Direct2D.</span></span>

<span data-ttu-id="b4eff-153">En outre, le verrouillage des threads dans Direct2D est plus granulaire que dans GDI et GDI+, afin que l’augmentation du nombre de threads ait un impact minimal sur les performances.</span><span class="sxs-lookup"><span data-stu-id="b4eff-153">In addition, the locking of threads in Direct2D is more granular than in GDI and GDI+, so that the increase of the number of threads has minimal impact on the performance.</span></span>

## <a name="how-to-use-direct2d-for-server-side-rendering"></a><span data-ttu-id="b4eff-154">Utilisation de Direct2D pour le rendu Server-Side</span><span class="sxs-lookup"><span data-stu-id="b4eff-154">How to Use Direct2D for Server-Side Rendering</span></span>

<span data-ttu-id="b4eff-155">Les sections suivantes décrivent comment utiliser le rendu logiciel, comment utiliser de façon optimale une fabrique à thread unique et une fabrique multithread, et comment dessiner et enregistrer un dessin complexe dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="b4eff-155">The following sections describe how to use software rendering, how to optimally use a single-threaded and a multithreaded factory, and how to draw and save a complex drawing to a file.</span></span>

### <a name="software-rendering"></a><span data-ttu-id="b4eff-156">Rendu logiciel</span><span class="sxs-lookup"><span data-stu-id="b4eff-156">Software Rendering</span></span>

<span data-ttu-id="b4eff-157">Les applications côté serveur utilisent le rendu logiciel en créant une cible de rendu [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) , avec le type de cible de rendu défini sur le type de cible de rendu d2d1 ou le type de \_ cible de \_ \_ \_ \_ rendu d2d1 \_ \_ \_ par défaut.</span><span class="sxs-lookup"><span data-stu-id="b4eff-157">Server-side applications use software rendering by creating [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target, with the render target type set to either D2D1\_RENDER\_TARGET\_TYPE\_SOFTWARE or D2D1\_RENDER\_TARGET\_TYPE\_DEFAULT.</span></span> <span data-ttu-id="b4eff-158">Pour plus d’informations sur les cibles de rendu [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) , consultez la méthode [**ID2D1Factory :: CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) ; Pour plus d’informations sur les types de cibles de rendu, consultez [**\_ type de \_ cible \_ de rendu d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).</span><span class="sxs-lookup"><span data-stu-id="b4eff-158">For more information about [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render targets, see the [**ID2D1Factory::CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) method; for more information about the render target types, see [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).</span></span>

### <a name="multithreading"></a><span data-ttu-id="b4eff-159">Multithreading</span><span class="sxs-lookup"><span data-stu-id="b4eff-159">Multithreading</span></span>

<span data-ttu-id="b4eff-160">Savoir comment créer et partager des usines et des cibles de rendu sur les threads peut avoir un impact significatif sur les performances d’une application.</span><span class="sxs-lookup"><span data-stu-id="b4eff-160">Knowing how to create and share factories and render targets across threads can significantly impact the performance of an application.</span></span> <span data-ttu-id="b4eff-161">Les trois figures suivantes présentent trois approches différentes.</span><span class="sxs-lookup"><span data-stu-id="b4eff-161">The following three figures show three varied approaches.</span></span> <span data-ttu-id="b4eff-162">L’approche optimale est illustrée à la figure 3.</span><span class="sxs-lookup"><span data-stu-id="b4eff-162">The optimal approach is shown in figure 3.</span></span>

![diagramme multithread de Direct2D avec une seule cible de rendu.](images/server-side-rendering-1.png)

<span data-ttu-id="b4eff-164">Dans la figure 1, les différents threads partagent la même fabrique et la même cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="b4eff-164">In figure 1, different threads share the same factory and the same render target.</span></span> <span data-ttu-id="b4eff-165">Cette approche peut entraîner des résultats imprévisibles lorsque plusieurs threads modifient simultanément l’état de la cible de rendu partagée, par exemple la définition simultanée de la matrice de transformation.</span><span class="sxs-lookup"><span data-stu-id="b4eff-165">This approach can lead to unpredictable results in cases when multiple threads simultaneously change the state of the shared render target, such as simultaneously setting the transformation matrix.</span></span> <span data-ttu-id="b4eff-166">Étant donné que le verrouillage interne dans Direct2D ne synchronise pas une ressource partagée comme les cibles de rendu, cette approche peut provoquer l’échec de l’appel [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) dans le thread 1, car dans le thread 2, l’appel de **BeginDraw** utilise déjà la cible de rendu partagée.</span><span class="sxs-lookup"><span data-stu-id="b4eff-166">As the internal locking in Direct2D does not synchronize a shared resource such as render targets, this approach can cause the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) call to fail in thread 1, because in thread 2, the **BeginDraw** call is already using the shared render target.</span></span>

![diagramme multithread de Direct2D avec plusieurs cibles de rendu.](images/server-side-rendering-2.png)

<span data-ttu-id="b4eff-168">Pour éviter les résultats imprévisibles de la figure 1, la figure 2 illustre une fabrique multithread avec chaque thread ayant sa propre cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="b4eff-168">To avoid the unpredictable results encountered in figure 1, figure 2 shows a multithreaded factory with each thread having its own render target.</span></span> <span data-ttu-id="b4eff-169">Cette approche fonctionne, mais elle fonctionne efficacement comme une application à thread unique.</span><span class="sxs-lookup"><span data-stu-id="b4eff-169">This approach works but it effectively functions as a single-threaded application.</span></span> <span data-ttu-id="b4eff-170">La raison en est que le verrou à l’échelle de l’usine s’applique uniquement au niveau de l’opération de dessin et que tous les appels de dessin dans la même fabrique sont donc sérialisés.</span><span class="sxs-lookup"><span data-stu-id="b4eff-170">The reason is that the factory-wide lock applies only to the drawing-operation level and all the drawing calls in the same factory consequently are serialized.</span></span> <span data-ttu-id="b4eff-171">Par conséquent, le thread 1 est bloqué lors d’une tentative d’entrée d’un appel de dessin, alors que le thread 2 est en train d’exécuter un autre appel de dessin.</span><span class="sxs-lookup"><span data-stu-id="b4eff-171">As a result, thread 1 becomes blocked when trying to enter a drawing call, while thread 2 is in the middle of executing another drawing call.</span></span>

![diagramme multithread de Direct2D avec plusieurs fabriques et plusieurs cibles de rendu.](images/server-side-rendering-3.png)

<span data-ttu-id="b4eff-173">La figure 3 illustre l’approche optimale, où une fabrique à thread unique et une cible de rendu monothread sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="b4eff-173">Figure 3 shows the optimal approach, where a single-threaded factory and a single-threaded render target are used.</span></span> <span data-ttu-id="b4eff-174">Dans la mesure où aucun verrouillage n’est effectué lors de l’utilisation d’une fabrique à thread unique, les opérations de dessin dans chaque thread peuvent s’exécuter simultanément pour obtenir des performances optimales.</span><span class="sxs-lookup"><span data-stu-id="b4eff-174">Since no locking is performed when using a single-threaded factory, drawing operations in each thread can run concurrently to achieve optimal performance.</span></span>

### <a name="generating-a-bitmap-file"></a><span data-ttu-id="b4eff-175">Génération d’un fichier bitmap</span><span class="sxs-lookup"><span data-stu-id="b4eff-175">Generating a Bitmap File</span></span>

<span data-ttu-id="b4eff-176">Pour générer un fichier bitmap à l’aide du rendu logiciel, utilisez une cible de rendu [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="b4eff-176">To generate a bitmap file using software rendering, use an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target.</span></span> <span data-ttu-id="b4eff-177">Utilisez un [IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) pour écrire l’image bitmap dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="b4eff-177">Use an [IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) to write the bitmap to a file.</span></span> <span data-ttu-id="b4eff-178">Utilisez [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) pour encoder la bitmap dans un format d’image spécifié.</span><span class="sxs-lookup"><span data-stu-id="b4eff-178">Use [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) to encode the bitmap into a specified image format.</span></span> <span data-ttu-id="b4eff-179">L’exemple de code suivant montre comment dessiner et enregistrer l’image suivante dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="b4eff-179">The following code example shows how to draw and save the following image to a file.</span></span>

![exemple d’image de sortie.](images/saveasimagefile-sample.png)

<span data-ttu-id="b4eff-181">Cet exemple de code crée d’abord un [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) et une cible de rendu [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="b4eff-181">This code example first creates an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) and an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target.</span></span> <span data-ttu-id="b4eff-182">Il affiche ensuite un dessin avec du texte, une géométrie de tracé représentant une heure et un verre d’heure transformé en bitmap WIC.</span><span class="sxs-lookup"><span data-stu-id="b4eff-182">It then renders a drawing with some text, a path geometry representing an hour glass, and a transformed hour glass into a WIC bitmap.</span></span> <span data-ttu-id="b4eff-183">Il utilise ensuite [IWICStream :: InitializeFromFilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) pour enregistrer l’image bitmap dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="b4eff-183">It then uses [IWICStream::InitializeFromFilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) to save the bitmap to a file.</span></span> <span data-ttu-id="b4eff-184">Si votre application doit enregistrer l’image bitmap en mémoire, utilisez [IWICStream :: InitializeFromMemory](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) à la place.</span><span class="sxs-lookup"><span data-stu-id="b4eff-184">If your application needs to save the bitmap in memory, use [IWICStream::InitializeFromMemory](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) instead.</span></span> <span data-ttu-id="b4eff-185">Enfin, il utilise [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) pour encoder l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="b4eff-185">Finally, it uses [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) to encode the bitmap.</span></span>


```C++
// Create an IWICBitmap and RT
static const UINT sc_bitmapWidth = 640;
static const UINT sc_bitmapHeight = 480;
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateBitmap(
        sc_bitmapWidth,
        sc_bitmapHeight,
        GUID_WICPixelFormat32bppBGR,
        WICBitmapCacheOnLoad,
        &pWICBitmap
        );
}

// Set the render target type to D2D1_RENDER_TARGET_TYPE_DEFAULT to use software rendering.
if (SUCCEEDED(hr))
{
    hr = pD2DFactory->CreateWicBitmapRenderTarget(
        pWICBitmap,
        D2D1::RenderTargetProperties(),
        &pRT
        );
}

// Create text format and a path geometry representing an hour glass. 
if (SUCCEEDED(hr))
{
    static const WCHAR sc_fontName[] = L"Calibri";
    static const FLOAT sc_fontSize = 50;

    hr = pDWriteFactory->CreateTextFormat(
        sc_fontName,
        NULL,
        DWRITE_FONT_WEIGHT_NORMAL,
        DWRITE_FONT_STYLE_NORMAL,
        DWRITE_FONT_STRETCH_NORMAL,
        sc_fontSize,
        L"", //locale
        &pTextFormat
        );
}
if (SUCCEEDED(hr))
{
    pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    hr = pD2DFactory->CreatePathGeometry(&pPathGeometry);
}
if (SUCCEEDED(hr))
{
    hr = pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_ALTERNATE);

    pSink->BeginFigure(
        D2D1::Point2F(0, 0),
        D2D1_FIGURE_BEGIN_FILLED
        );

    pSink->AddLine(D2D1::Point2F(200, 0));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(150, 50),
            D2D1::Point2F(150, 150),
            D2D1::Point2F(200, 200))
        );

    pSink->AddLine(D2D1::Point2F(0, 200));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(50, 150),
            D2D1::Point2F(50, 50),
            D2D1::Point2F(0, 0))
        );

    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}
if (SUCCEEDED(hr))
{
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 1.f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = pRT->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(100, 0),
            D2D1::Point2F(100, 200)),
        D2D1::BrushProperties(),
        pGradientStops,
        &pLGBrush
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        );
}
if (SUCCEEDED(hr))
{
    // Render into the bitmap.
    pRT->BeginDraw();
    pRT->Clear(D2D1::ColorF(D2D1::ColorF::White));
    D2D1_SIZE_F rtSize = pRT->GetSize();

    // Set the world transform to a 45 degree rotation at the center of the render target
    // and write "Hello, World".
    pRT->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45,
            D2D1::Point2F(
                rtSize.width / 2,
                rtSize.height / 2))
            );

    static const WCHAR sc_helloWorld[] = L"Hello, World!";
    pRT->DrawText(
        sc_helloWorld,
        ARRAYSIZE(sc_helloWorld) - 1,
        pTextFormat,
        D2D1::RectF(0, 0, rtSize.width, rtSize.height),
        pBlackBrush);

    // Reset back to the identity transform.
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(0, rtSize.height - 200));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(rtSize.width - 200, 0));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    hr = pRT->EndDraw();
}

if (SUCCEEDED(hr))
{
    // Save the image to a file.
    hr = pWICFactory->CreateStream(&pStream);
}

WICPixelFormatGUID format = GUID_WICPixelFormatDontCare;

// Use InitializeFromFilename to write to a file. If there is need to write inside the memory, use InitializeFromMemory. 
if (SUCCEEDED(hr))
{
    static const WCHAR filename[] = L"output.png";
    hr = pStream->InitializeFromFilename(filename, GENERIC_WRITE);
}
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateEncoder(GUID_ContainerFormatPng, NULL, &pEncoder);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Initialize(pStream, WICBitmapEncoderNoCache);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->CreateNewFrame(&pFrameEncode, NULL);
}
// Use IWICBitmapFrameEncode to encode the bitmap into the picture format you want.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Initialize(NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetSize(sc_bitmapWidth, sc_bitmapHeight);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetPixelFormat(&format);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->WriteSource(pWICBitmap, NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Commit();
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Commit();
}

```



## <a name="conclusion"></a><span data-ttu-id="b4eff-186">Conclusion</span><span class="sxs-lookup"><span data-stu-id="b4eff-186">Conclusion</span></span>

<span data-ttu-id="b4eff-187">Comme indiqué dans l’exemple ci-dessus, l’utilisation de Direct2D pour le rendu côté serveur est simple et directe.</span><span class="sxs-lookup"><span data-stu-id="b4eff-187">As seen from the above, using Direct2D for server-side rendering is simple and straightforward.</span></span> <span data-ttu-id="b4eff-188">En outre, il fournit un rendu de haute qualité et de haut niveau de parallèles qui peut s’exécuter dans des environnements à faibles privilèges du serveur.</span><span class="sxs-lookup"><span data-stu-id="b4eff-188">In addition, it provides high quality and highly parallelizable rendering that can run in low-privilege environments of the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4eff-189">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b4eff-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4eff-190">Référence Direct2D</span><span class="sxs-lookup"><span data-stu-id="b4eff-190">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 