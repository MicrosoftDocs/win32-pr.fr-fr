---
title: Implémentation du rendu
description: Implémentation du rendu
ms.assetid: 9b3a64f6-6803-457c-8e63-e8a799089e18
keywords:
- visualisations, événements chronométrés
- visualisations personnalisées, événements chronométrés
- visualisations, fonction Render
- visualisations personnalisées, fonction Render
- visualisations, fonction RenderWindow
- visualisations personnalisées, fonction RenderWindow
- Fonction Render, paramètres
- RenderWindow fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99db0a96a07c361d18de579fb0235befa11838c8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030809"
---
# <a name="implementing-render"></a><span data-ttu-id="7128e-111">Implémentation du rendu</span><span class="sxs-lookup"><span data-stu-id="7128e-111">Implementing Render</span></span>

<span data-ttu-id="7128e-112">La façon la plus simple de considérer la programmation de la visualisation est que vous créez un gestionnaire pour un événement chronométré.</span><span class="sxs-lookup"><span data-stu-id="7128e-112">The easiest way to think of visualization programming is that you are creating a handler for a timed event.</span></span> <span data-ttu-id="7128e-113">À des intervalles spécifiques, le lecteur Windows Media prend un instantané des données audio qu’il lit et fournit les données de capture instantanée à la visualisation actuellement chargée.</span><span class="sxs-lookup"><span data-stu-id="7128e-113">At specific intervals, Windows Media Player takes a snapshot of the audio data it is playing, and provides the snapshot data to the currently loaded visualization.</span></span> <span data-ttu-id="7128e-114">Cela est similaire à la programmation pilotée par les événements et fait partie du modèle de programmation de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7128e-114">This is similar to event-driven programming and is part of the programming model of Microsoft Windows.</span></span> <span data-ttu-id="7128e-115">Vous écrivez du code et attendez qu’il soit appelé par un événement particulier.</span><span class="sxs-lookup"><span data-stu-id="7128e-115">You write code and wait for it to be called by a particular event.</span></span>

<span data-ttu-id="7128e-116">Si votre code est une implémentation de la fonction [IWMPEffects :: Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) pour le rendu en mode sans fenêtre, il reçoit les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7128e-116">If your code is an implementation of the [IWMPEffects::Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) function for rendering in windowless mode, it receives the following parameters:</span></span>

<span data-ttu-id="7128e-117">*TimedLevel*</span><span class="sxs-lookup"><span data-stu-id="7128e-117">*TimedLevel*</span></span>

<span data-ttu-id="7128e-118">Il s’agit d’une structure qui définit les données audio que votre code analysera.</span><span class="sxs-lookup"><span data-stu-id="7128e-118">This is a structure that defines the audio data your code will be analyzing.</span></span> <span data-ttu-id="7128e-119">La structure est composée de deux tableaux.</span><span class="sxs-lookup"><span data-stu-id="7128e-119">The structure is composed of two arrays.</span></span> <span data-ttu-id="7128e-120">Le premier tableau est basé sur les informations de fréquence et contient un instantané du spectre audio divisé en portions de 1024.</span><span class="sxs-lookup"><span data-stu-id="7128e-120">The first array is based on frequency information and contains a snapshot of the audio spectrum divided into 1024 portions.</span></span> <span data-ttu-id="7128e-121">Chaque cellule du tableau contient une valeur comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="7128e-121">Each cell of the array contains a value from 0 to 255.</span></span> <span data-ttu-id="7128e-122">La première cellule commence à 20 Hz et la dernière à 22050 Hz.</span><span class="sxs-lookup"><span data-stu-id="7128e-122">The first cell starts at 20 Hz and the last at 22050 Hz.</span></span> <span data-ttu-id="7128e-123">Le tableau est en deux dimensions pour représenter l’audio stéréo.</span><span class="sxs-lookup"><span data-stu-id="7128e-123">The array is two dimensional to represent stereo audio.</span></span> <span data-ttu-id="7128e-124">Le deuxième tableau est basé sur les informations de forme d’onde et correspond à la puissance audio, où le plus fort de l’onde est, plus la valeur est grande.</span><span class="sxs-lookup"><span data-stu-id="7128e-124">The second array is based on waveform information and corresponds to audio power, where the stronger the wave is, the larger the value.</span></span> <span data-ttu-id="7128e-125">Le tableau de forme d’onde est un instantané granulaire des 1024 dernières tranches de puissance audio prises à des intervalles de temps très petits.</span><span class="sxs-lookup"><span data-stu-id="7128e-125">The waveform array is a granular snapshot of the last 1024 slices of audio power taken at very small time intervals.</span></span> <span data-ttu-id="7128e-126">Ce tableau est également à deux dimensions pour représenter l’audio stéréo.</span><span class="sxs-lookup"><span data-stu-id="7128e-126">This array also is two dimensional to represent stereo audio.</span></span>

<span data-ttu-id="7128e-127">*HDC*</span><span class="sxs-lookup"><span data-stu-id="7128e-127">*HDC*</span></span>

<span data-ttu-id="7128e-128">Il s’agit d’un handle Microsoft Windows vers un contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="7128e-128">This is a Microsoft Windows handle to a device context.</span></span> <span data-ttu-id="7128e-129">Cela donne un moyen d’identifier la surface de dessin sur Windows.</span><span class="sxs-lookup"><span data-stu-id="7128e-129">This gives a way to identify the drawing surface to Windows.</span></span> <span data-ttu-id="7128e-130">Vous n’avez pas besoin de la créer, il vous suffit de l’utiliser pour des appels de fonction de dessin spécifiques.</span><span class="sxs-lookup"><span data-stu-id="7128e-130">You do not need to create it, you just need to use it for specific drawing function calls.</span></span>

<span data-ttu-id="7128e-131">*RECTANGULAIRE*</span><span class="sxs-lookup"><span data-stu-id="7128e-131">*RECT*</span></span>

<span data-ttu-id="7128e-132">Il s’agit d’un rectangle Microsoft Windows qui définit la taille d’une surface de dessin.</span><span class="sxs-lookup"><span data-stu-id="7128e-132">This is a Microsoft Windows rectangle that defines the size of a drawing surface.</span></span> <span data-ttu-id="7128e-133">Il s’agit d’un rectangle simple avec quatre propriétés : **gauche**, **droite**, **haut** et **bas**.</span><span class="sxs-lookup"><span data-stu-id="7128e-133">This is a simple rectangle with four properties: **left**, **right**, **top**, and **bottom**.</span></span> <span data-ttu-id="7128e-134">Les valeurs réelles sont fournies par le lecteur Windows Media pour vous permettre de déterminer comment le développeur de l’utilisateur ou de la peau a dimensionné la fenêtre sur laquelle vous allez dessiner.</span><span class="sxs-lookup"><span data-stu-id="7128e-134">The actual values are supplied by Windows Media Player so that you can determine how the user or skin developer has sized the window you will draw on.</span></span> <span data-ttu-id="7128e-135">Elle détermine également la position sur le HDC sur laquelle l’effet est supposé être rendu.</span><span class="sxs-lookup"><span data-stu-id="7128e-135">It also determines the position on the HDC that the effect is supposed to render on.</span></span>

<span data-ttu-id="7128e-136">Si votre code est une implémentation de la fonction **IWMPEffects2 :: RenderWindowed** pour le rendu dans une fenêtre, il reçoit les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7128e-136">If your code is an implementation of the **IWMPEffects2::RenderWindowed** function for rendering in a window, it receives the following parameters:</span></span>

<span data-ttu-id="7128e-137">*TimedLevel*</span><span class="sxs-lookup"><span data-stu-id="7128e-137">*TimedLevel*</span></span>

<span data-ttu-id="7128e-138">Il s’agit des mêmes informations que celles reçues par la fonction **Render** .</span><span class="sxs-lookup"><span data-stu-id="7128e-138">This is the same information that the **Render** function receives.</span></span>

<span data-ttu-id="7128e-139">*fRequiredRender*</span><span class="sxs-lookup"><span data-stu-id="7128e-139">*fRequiredRender*</span></span>

<span data-ttu-id="7128e-140">Le paramètre *fRequiredRender* vous informe que votre visualisation doit se redessiner, par exemple, lorsqu’une autre fenêtre est glissée au-dessus.</span><span class="sxs-lookup"><span data-stu-id="7128e-140">The *fRequiredRender* parameter informs you that your visualization must repaint itself—for example, when another window is dragged over it.</span></span> <span data-ttu-id="7128e-141">Lorsque cette valeur est false, vous pouvez ignorer en toute sécurité le code de rendu si l’élément multimédia actuel est arrêté ou suspendu.</span><span class="sxs-lookup"><span data-stu-id="7128e-141">When this value is false, you can safely skip over the rendering code if the current media item is stopped or paused.</span></span> <span data-ttu-id="7128e-142">Cela vous permet d’éviter de consommer inutilement des cycles d’UC.</span><span class="sxs-lookup"><span data-stu-id="7128e-142">This lets you avoid consuming CPU cycles unnecessarily.</span></span>

<span data-ttu-id="7128e-143">L’exemple de plug-in généré par l’Assistant de plug-in ne fournit pas d’implémentation personnalisée pour **RenderWindowed**.</span><span class="sxs-lookup"><span data-stu-id="7128e-143">The sample plug-in generated by the Plug-in Wizard does not provide a custom implementation for **RenderWindowed**.</span></span> <span data-ttu-id="7128e-144">Au lieu de cela, l’exemple de code de plug-in récupère le contexte de périphérique à partir de la fenêtre parente fournie par le lecteur Windows Media dans [IWMPEffects2 :: Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create), puis récupère les dimensions de la fenêtre parente comme une structure Rect, puis appelle pour effectuer le **rendu** à l’aide du contexte de périphérique, du Rect et du pointeur de niveau chronométré à partir de **RenderWindowed**.</span><span class="sxs-lookup"><span data-stu-id="7128e-144">Instead, the sample plug-in code retrieves the device context from the parent window provided by Windows Media Player in [IWMPEffects2::Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create), then retrieves the dimensions of the parent window as a RECT structure, and then calls through to **Render** using the device context, the RECT, and the timed level pointer from **RenderWindowed**.</span></span>

<span data-ttu-id="7128e-145">Les sections suivantes fournissent plus d’informations sur l’implémentation du **rendu**:</span><span class="sxs-lookup"><span data-stu-id="7128e-145">The following sections provide more information about implementing **Render**:</span></span>

-   [<span data-ttu-id="7128e-146">Utilisation de niveaux chronométrés</span><span class="sxs-lookup"><span data-stu-id="7128e-146">Using Timed Levels</span></span>](using-timed-levels.md)
-   [<span data-ttu-id="7128e-147">Utilisation des contextes de périphérique</span><span class="sxs-lookup"><span data-stu-id="7128e-147">Using Device Contexts</span></span>](using-device-contexts.md)
-   [<span data-ttu-id="7128e-148">Utilisation de rectangles</span><span class="sxs-lookup"><span data-stu-id="7128e-148">Using Rectangles</span></span>](using-rectangles.md)
-   [<span data-ttu-id="7128e-149">Exemple de code de rendu</span><span class="sxs-lookup"><span data-stu-id="7128e-149">Sample Render Code</span></span>](sample-render-code.md)

## <a name="related-topics"></a><span data-ttu-id="7128e-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7128e-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7128e-151">**Implémentation de votre code**</span><span class="sxs-lookup"><span data-stu-id="7128e-151">**Implementing Your Code**</span></span>](implementing-your-code.md)
</dt> </dl>

 

 




