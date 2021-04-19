---
title: Vue d’ensemble de la couche de débogage Direct2D
description: .
ms.assetid: 7c28e00b-ebb9-4b79-939c-64eade1351ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df560595ea0ae6c7a56c3fa568f2f94ae56652ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511001"
---
# <a name="direct2d-debug-layer-overview"></a><span data-ttu-id="ce942-103">Vue d’ensemble de la couche de débogage Direct2D</span><span class="sxs-lookup"><span data-stu-id="ce942-103">Direct2D Debug Layer Overview</span></span>

<span data-ttu-id="ce942-104">La couche de débogage Direct2D fournit des messages de débogage au moment du design pour réduire l’échec de l’application Runtime.</span><span class="sxs-lookup"><span data-stu-id="ce942-104">The Direct2D debug layer provides design-time debug messages for you to minimize runtime application failure.</span></span> <span data-ttu-id="ce942-105">Cette vue d’ensemble décrit les principes fondamentaux de la couche de débogage Direct2D.</span><span class="sxs-lookup"><span data-stu-id="ce942-105">This overview describes the basics of the Direct2D debug layer.</span></span> <span data-ttu-id="ce942-106">Il part du principe que vous êtes familiarisé avec la création d’applications Direct2D de base.</span><span class="sxs-lookup"><span data-stu-id="ce942-106">It assumes that you are familiar with creating basic Direct2D applications.</span></span>

<span data-ttu-id="ce942-107">Cette vue d’ensemble contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="ce942-107">This overview contains the following sections.</span></span>

-   [<span data-ttu-id="ce942-108">Qu’est-ce que la couche de débogage Direct2D ?</span><span class="sxs-lookup"><span data-stu-id="ce942-108">What Is the Direct2D Debug Layer</span></span>](#what-is-the-direct2d-debug-layer)
-   [<span data-ttu-id="ce942-109">Installation de la couche de débogage Direct2D</span><span class="sxs-lookup"><span data-stu-id="ce942-109">Installing the Direct2D Debug Layer</span></span>](#installing-the-direct2d-debug-layer)
-   [<span data-ttu-id="ce942-110">Activation de la couche de débogage</span><span class="sxs-lookup"><span data-stu-id="ce942-110">Enabling the Debug Layer</span></span>](#enabling-the-debug-layer)
-   [<span data-ttu-id="ce942-111">Niveaux de débogage</span><span class="sxs-lookup"><span data-stu-id="ce942-111">Debug Levels</span></span>](#debug-levels)
-   [<span data-ttu-id="ce942-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ce942-112">Related topics</span></span>](#related-topics)

## <a name="what-is-the-direct2d-debug-layer"></a><span data-ttu-id="ce942-113">Qu’est-ce que la couche de débogage Direct2D ?</span><span class="sxs-lookup"><span data-stu-id="ce942-113">What Is the Direct2D Debug Layer</span></span>

<span data-ttu-id="ce942-114">La couche de débogage Direct2D, implémentée séparément de Direct2D dans sa propre DLL nommée d2d1debug.dll, fournit des messages de débogage pour vous permettre d’utiliser avec précision les fonctions Direct2D.</span><span class="sxs-lookup"><span data-stu-id="ce942-114">The Direct2D debug layer, implemented separately from Direct2D in its own DLL named d2d1debug.dll, provides debug messages to enable you to accurately use Direct2D functions.</span></span> <span data-ttu-id="ce942-115">Les messages de débogage résultent souvent de violations de contrat d’API telles que les paramètres non valides (qui peuvent être liés à Direct3D), de ressources non valides, de violations de thread et de problèmes de performances, tels que l’utilisation d’une couche quand un clip suffit.</span><span class="sxs-lookup"><span data-stu-id="ce942-115">The debug messages often result from API contract violations such as invalid parameters (could be Direct3D-related), invalid resources, threading violations, and performance issues such as using a layer when a clip would suffice.</span></span> <span data-ttu-id="ce942-116">Pour spécifier la quantité d’informations qui est tracée par la couche de débogage, vous pouvez spécifier l’un des trois niveaux de débogage : information, avertissement et erreur. et un message d’erreur de niveau déclenche le point d’arrêt pour vous aider à effectuer le débogage.</span><span class="sxs-lookup"><span data-stu-id="ce942-116">To specify how much information is traced by the debug layer, you can specify one of the three debug levels: information, warning, and error; and a message of level error triggers the breakpoint to help you debug.</span></span>

## <a name="installing-the-direct2d-debug-layer"></a><span data-ttu-id="ce942-117">Installation de la couche de débogage Direct2D</span><span class="sxs-lookup"><span data-stu-id="ce942-117">Installing the Direct2D Debug Layer</span></span>

<span data-ttu-id="ce942-118">Pour obtenir des instructions sur l’installation de la couche de débogage, consultez [installation de la couche de débogage Direct2D](installing-the-direct2d-debug-layer.md).</span><span class="sxs-lookup"><span data-stu-id="ce942-118">For instructions on installing the debug layer, see [Installing the Direct2D Debug Layer](installing-the-direct2d-debug-layer.md).</span></span>

## <a name="enabling-the-debug-layer"></a><span data-ttu-id="ce942-119">Activation de la couche de débogage</span><span class="sxs-lookup"><span data-stu-id="ce942-119">Enabling the Debug Layer</span></span>

<span data-ttu-id="ce942-120">Pour activer la couche de débogage dans votre application, spécifiez une valeur de [**\_ \_ niveau de débogage d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) autre que le niveau de débogage **d2d1 \_ \_ \_ aucun** lorsque vous créez une fabrique avec la fonction [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) .</span><span class="sxs-lookup"><span data-stu-id="ce942-120">To enable the debug layer in your application, specify a [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) value other than **D2D1\_DEBUG\_LEVEL\_NONE** when you create a factory with the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function.</span></span>

> [!Note]  
> <span data-ttu-id="ce942-121">Si la couche de débogage Direct2D est activée, l’effet de gestion des couleurs Direct2D (CLSID \_ D2D1ColorManagement) peut entraîner une violation d’accès lors de la définition d’un contexte de couleur.</span><span class="sxs-lookup"><span data-stu-id="ce942-121">If the Direct2D debug layer is enabled, the Direct2D color management effect (CLSID\_D2D1ColorManagement) may cause an access violation when setting a color context.</span></span> <span data-ttu-id="ce942-122">La solution de contournement consiste à désactiver la couche de débogage lors de l’utilisation de l’effet de gestion des couleurs</span><span class="sxs-lookup"><span data-stu-id="ce942-122">The workaround is to disable the debug layer when using the color management effect</span></span>

 

<span data-ttu-id="ce942-123">L’activation de la couche de débogage pour une fabrique active également les informations de débogage pour tout objet créé par cette fabrique.</span><span class="sxs-lookup"><span data-stu-id="ce942-123">Enabling the debug layer for a factory also enables debugging information for any object created by that factory.</span></span>

<span data-ttu-id="ce942-124">L’exemple suivant active la couche de débogage pour une fabrique lorsque l’application est compilée pour la configuration de build DEBUG.</span><span class="sxs-lookup"><span data-stu-id="ce942-124">The following example enables the debug layer for a factory when the application is compiled for the DEBUG build configuration.</span></span>


```C++
        // If you set the options.debugLevel to D2D1_DEBUG_LEVEL_NONE,
        // the debug layer is not enabled.
#if defined(DEBUG) || defined(_DEBUG)
        D2D1_FACTORY_OPTIONS options;
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;

        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory
            );
#else
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
#endif
```



> [!Note]  
> <span data-ttu-id="ce942-125">Si aucune option de fabrique n’est spécifiée ou si un niveau de débogage de « None » est spécifié, la couche de débogage n’est pas appelée.</span><span class="sxs-lookup"><span data-stu-id="ce942-125">If no factory options are specified or a debug level of "none" is specified, the debug layer is not invoked.</span></span> <span data-ttu-id="ce942-126">La couche de débogage ne doit jamais être active dans la version Release d’une application.</span><span class="sxs-lookup"><span data-stu-id="ce942-126">The debug layer should never be active in the release version of an application.</span></span>

 

<span data-ttu-id="ce942-127">La section suivante décrit les différents niveaux de débogage définis par l’énumération de [**\_ \_ niveau de débogage d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) .</span><span class="sxs-lookup"><span data-stu-id="ce942-127">The next section describes the different debug levels defined by the [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) enumeration.</span></span>

## <a name="debug-levels"></a><span data-ttu-id="ce942-128">Niveaux de débogage</span><span class="sxs-lookup"><span data-stu-id="ce942-128">Debug Levels</span></span>

<span data-ttu-id="ce942-129">L’énumération de [**\_ \_ niveau de débogage d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) spécifie trois niveaux de débogage : erreur de niveau de débogage d2d1 \_ \_ \_ (erreur), d2d1 \_ avertissement de niveau de débogage \_ \_ (avertissement) et \_ informations de niveau de débogage d2d1 \_ \_ (informations).</span><span class="sxs-lookup"><span data-stu-id="ce942-129">The [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) enumeration specifies three debug levels: D2D1\_DEBUG\_LEVEL\_ERROR (error), D2D1\_DEBUG\_LEVEL\_WARNING (warning), and D2D1\_DEBUG\_LEVEL\_INFORMATION (information).</span></span> <span data-ttu-id="ce942-130">Ces niveaux sont interprétés comme suit :</span><span class="sxs-lookup"><span data-stu-id="ce942-130">These levels are interpreted as follows:</span></span>

-   <span data-ttu-id="ce942-131">**Erreur :** Direct2D envoie des messages d’erreur graves à la couche de débogage.</span><span class="sxs-lookup"><span data-stu-id="ce942-131">**Error:** Direct2D sends severe error messages to the debug layer.</span></span> <span data-ttu-id="ce942-132">Par exemple, l’interruption d’une contrainte de thread génère une erreur grave.</span><span class="sxs-lookup"><span data-stu-id="ce942-132">For example, breaking a threading constraint will generate a severe error.</span></span>

-   <span data-ttu-id="ce942-133">**Avertissement :** Direct2D envoie des messages d’erreur et des avertissements à la couche de débogage pour vous permettre de traiter l’un de ces messages.</span><span class="sxs-lookup"><span data-stu-id="ce942-133">**Warning:** Direct2D sends error messages and warnings to the debug layer so that you can address any of these messages.</span></span>

-   <span data-ttu-id="ce942-134">**Informations :** Direct2D envoie des messages d’erreur, des avertissements et des informations de diagnostic supplémentaires à la couche de débogage.</span><span class="sxs-lookup"><span data-stu-id="ce942-134">**Information:** Direct2D sends error messages, warnings, and additional diagnostic information to the debug layer.</span></span> <span data-ttu-id="ce942-135">Par exemple, les messages d’amélioration des performances seront envoyés à ce niveau de débogage.</span><span class="sxs-lookup"><span data-stu-id="ce942-135">For example, performance improvement messages will be sent at this debug level.</span></span>

<span data-ttu-id="ce942-136">La valeur D2D1 \_ niveau de débogage \_ \_ aucun (aucune) indique que Direct2D ne fournit pas de sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="ce942-136">The value D2D1\_DEBUG\_LEVEL\_NONE (none) indicates that Direct2D does not provide any debugging output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce942-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ce942-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce942-138">Messages de débogage</span><span class="sxs-lookup"><span data-stu-id="ce942-138">Debug Messages</span></span>](direct2ddebuglayer-debugmessages.md)
</dt> </dl>

 

 




