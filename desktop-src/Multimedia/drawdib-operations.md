---
title: Opérations DrawDib
description: Opérations DrawDib
ms.assetid: 785ad42e-0c77-44a4-b4ef-be2a0ee2b563
keywords:
- DrawDib, à propos de
- DrawDib, accès
- DrawDib, ouverture
- DrawDib, opérations
- DrawDib, contexte de périphérique (DC)
- DC (contexte de périphérique)
- DrawDibOpen fonction)
- DrawDibClose fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc366287cdf481d70ef03aa82df5ea248673280b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462462"
---
# <a name="drawdib-operations"></a><span data-ttu-id="9da7b-111">Opérations DrawDib</span><span class="sxs-lookup"><span data-stu-id="9da7b-111">DrawDib Operations</span></span>

<span data-ttu-id="9da7b-112">Vous pouvez accéder à l’ensemble du groupe de fonctions DrawDib à l’aide de la fonction [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) .</span><span class="sxs-lookup"><span data-stu-id="9da7b-112">You can access the entire group of DrawDib functions by using the [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) function.</span></span> <span data-ttu-id="9da7b-113">Cette fonction charge la bibliothèque de liens dynamiques (DLL), alloue des ressources mémoire, crée un contexte de périphérique (DC) DrawDib et conserve un décompte de références du nombre de contrôleurs de rôle qui sont initialisés.</span><span class="sxs-lookup"><span data-stu-id="9da7b-113">This function loads the dynamic-link library (DLL), allocates memory resources, creates a DrawDib device context (DC), and maintains a reference count of the number of DCs that are initialized.</span></span> <span data-ttu-id="9da7b-114">**DrawDibOpen** retourne également un handle du nouveau contrôleur de périphérique que vous utilisez avec les autres fonctions DrawDib.</span><span class="sxs-lookup"><span data-stu-id="9da7b-114">**DrawDibOpen** also returns a handle of the new DC that you use with the other DrawDib functions.</span></span>

<span data-ttu-id="9da7b-115">Vous pouvez libérer un contrôleur de DrawDib quand vous avez fini de l’utiliser à l’aide de la fonction [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) .</span><span class="sxs-lookup"><span data-stu-id="9da7b-115">You can release a DrawDib DC when you finish using it by using the [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) function.</span></span> <span data-ttu-id="9da7b-116">**DrawDibClose** décrémente également le décompte de références des applications qui accèdent à la dll.</span><span class="sxs-lookup"><span data-stu-id="9da7b-116">**DrawDibClose** also decrements the reference count of the applications accessing the DLL.</span></span> <span data-ttu-id="9da7b-117">L’appel à **DrawDibClose** doit être la dernière fonction DrawDib dans votre application.</span><span class="sxs-lookup"><span data-stu-id="9da7b-117">The call to **DrawDibClose** should be the last DrawDib function in your application.</span></span>

<span data-ttu-id="9da7b-118">Vous pouvez créer autant de contrôleurs de DrawDib que vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="9da7b-118">You can create as many DrawDib DCs as you want.</span></span> <span data-ttu-id="9da7b-119">Vous pouvez utiliser plusieurs contrôleurs de DrawDib pour créer plusieurs bitmaps simultanément.</span><span class="sxs-lookup"><span data-stu-id="9da7b-119">You can use multiple DrawDib DCs to draw several bitmaps simultaneously.</span></span> <span data-ttu-id="9da7b-120">Vous pouvez également créer plusieurs contrôleurs de DrawDib, chacun avec des caractéristiques uniques, afin que votre application puisse choisir, puis utiliser le DC avec les paramètres les plus appropriés.</span><span class="sxs-lookup"><span data-stu-id="9da7b-120">You can also create multiple DrawDib DCs, each with unique characteristics, so your application can choose and then use the DC with the most appropriate settings.</span></span> <span data-ttu-id="9da7b-121">Par exemple, vous pouvez créer deux contrôleurs de DrawDib dans une application : un qui affiche une image à sa résolution normale et l’autre qui affiche une partie agrandie de l’image.</span><span class="sxs-lookup"><span data-stu-id="9da7b-121">For example, you can create two DrawDib DCs in an application: one that displays an image at its normal resolution, and the other that displays an enlarged portion of the image.</span></span>

<span data-ttu-id="9da7b-122">Pour s’exécuter efficacement, les fonctions DrawDib requièrent des informations sur la carte d’affichage et son pilote.</span><span class="sxs-lookup"><span data-stu-id="9da7b-122">To run efficiently, DrawDib functions require information about the display adapter and its driver.</span></span> <span data-ttu-id="9da7b-123">Le profil d’affichage est obtenu en exécutant une série de tests sur la carte d’affichage la première fois que la DLL contenant les fonctions DrawDib est accédée.</span><span class="sxs-lookup"><span data-stu-id="9da7b-123">The display profile is obtained by running a series of tests on the display adapter the first time the DLL containing the DrawDib functions is accessed.</span></span> <span data-ttu-id="9da7b-124">Les fonctions DrawDib utilisent ces informations pour toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="9da7b-124">The DrawDib functions use this information for all applications.</span></span> <span data-ttu-id="9da7b-125">Vous pouvez répéter ces tests si nécessaire à l’aide de la fonction [**DrawDibProfileDisplay**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) .</span><span class="sxs-lookup"><span data-stu-id="9da7b-125">You can repeat these tests when necessary by using the [**DrawDibProfileDisplay**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) function.</span></span>

> [!Note]  
> <span data-ttu-id="9da7b-126">La récupération et le stockage du profil d’affichage est généralement une occurrence unique.</span><span class="sxs-lookup"><span data-stu-id="9da7b-126">Retrieving and storing the display profile is typically a one-time occurrence.</span></span> <span data-ttu-id="9da7b-127">Toutefois, si les informations de profil sont supprimées ou si un autre pilote d’affichage est installé dans le système, DrawDib réexécute les tests.</span><span class="sxs-lookup"><span data-stu-id="9da7b-127">If, however, the profile information is deleted or another display driver is installed in the system, DrawDib reruns the tests.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9da7b-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9da7b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9da7b-129">À propos des fonctions DrawDib</span><span class="sxs-lookup"><span data-stu-id="9da7b-129">About the DrawDib Functions</span></span>](about-the-drawdib-functions.md)
</dt> </dl>

 

 




