---
title: Description (Windows Media Player SDK)
description: Description
ms.assetid: 940ef0bf-d651-411a-b36d-99dcc01d8508
keywords:
- Windows Media Player Mobile Skins, section Description
- apparences, section Description
- référence pour les apparences, section Description
- Section Description dans les apparences
- fichiers de définition d’apparence, section Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a1b714fb917f9d13ee710509cfc5bf696e3eef
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383679"
---
# <a name="description-windows-media-player-sdk"></a><span data-ttu-id="433c0-108">Description (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="433c0-108">Description (Windows Media Player SDK)</span></span>

<span data-ttu-id="433c0-109">Quand vous créez une apparence pour Windows Media Player 9 Series pour Windows Mobile 2003 ou version ultérieure, vous devez inclure une section Description.</span><span class="sxs-lookup"><span data-stu-id="433c0-109">When you create a skin for Windows Media Player 9 Series for Windows Mobile 2003 or later, you must include a Description section.</span></span> <span data-ttu-id="433c0-110">La section Description vous permet de spécifier la largeur et la hauteur de l’affichage, la résolution d’affichage et l’orientation d’affichage pour laquelle l’apparence a été conçue.</span><span class="sxs-lookup"><span data-stu-id="433c0-110">The Description section enables you to specify the width and height of the display, the display resolution, and the display orientation for which the skin was designed.</span></span> <span data-ttu-id="433c0-111">La section Description doit apparaître dans le fichier de définition d’apparence avant toute autre section, et juste après la déclaration de version initiale.</span><span class="sxs-lookup"><span data-stu-id="433c0-111">The Description section must appear in the skin definition file before any other section, and just after the initial version declaration.</span></span>

<span data-ttu-id="433c0-112">La section Description du fichier de définition d’apparence doit commencer par la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="433c0-112">The Description section of the skin definition file must begin with the following line:</span></span>


```C++
[ Description ]

```



<span data-ttu-id="433c0-113">Vous devez ensuite ajouter des informations sur les dimensions de l’apparence et la résolution d’affichage.</span><span class="sxs-lookup"><span data-stu-id="433c0-113">You then must add information about the dimensions of the skin and the display resolution.</span></span> <span data-ttu-id="433c0-114">L’exemple suivant montre comment spécifier des dimensions :</span><span class="sxs-lookup"><span data-stu-id="433c0-114">The following example shows how to specify dimensions:</span></span>


```C++
//              <X,Y>       <DPI>

//              -------     -----

    Dimensions  240,320      96

```



<span data-ttu-id="433c0-115">Cela spécifie que vous avez conçu l’apparence pour afficher 240 pixels de large, 320 pixels de haut et avec une résolution d’affichage de 96 ppp.</span><span class="sxs-lookup"><span data-stu-id="433c0-115">This specifies that you designed the skin to be displayed 240 pixels wide, 320 pixels high, and using 96 DPI display resolution.</span></span> <span data-ttu-id="433c0-116">Notez que cela implique une orientation en mode portrait.</span><span class="sxs-lookup"><span data-stu-id="433c0-116">Note that this implies a portrait mode orientation.</span></span>

<span data-ttu-id="433c0-117">Vous pouvez éventuellement spécifier le mode d’orientation pour lequel vous avez conçu l’apparence dans la section Description.</span><span class="sxs-lookup"><span data-stu-id="433c0-117">You may optionally specify the orientation mode for which you designed the skin in the description section.</span></span> <span data-ttu-id="433c0-118">L’exemple suivant montre comment spécifier l’orientation :</span><span class="sxs-lookup"><span data-stu-id="433c0-118">The following example shows how to specify orientation:</span></span>


```C++
//     <Orientation>

//     -------------

    Orientation Portrait

```



<span data-ttu-id="433c0-119">Le tableau suivant répertorie les valeurs que vous pouvez utiliser pour l’orientation.</span><span class="sxs-lookup"><span data-stu-id="433c0-119">The following table lists the values you may use for Orientation.</span></span>



| <span data-ttu-id="433c0-120">Orientation</span><span class="sxs-lookup"><span data-stu-id="433c0-120">Orientation</span></span> | <span data-ttu-id="433c0-121">Description</span><span class="sxs-lookup"><span data-stu-id="433c0-121">Description</span></span>                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="433c0-122">Paysage</span><span class="sxs-lookup"><span data-stu-id="433c0-122">Landscape</span></span>   | <span data-ttu-id="433c0-123">La largeur de l’apparence est supérieure à la hauteur de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="433c0-123">The width of the skin is greater than height of the skin.</span></span> <span data-ttu-id="433c0-124">L’affichage est orienté horizontalement.</span><span class="sxs-lookup"><span data-stu-id="433c0-124">The display is oriented in a horizontal fashion.</span></span>   |
| <span data-ttu-id="433c0-125">Portrait</span><span class="sxs-lookup"><span data-stu-id="433c0-125">Portrait</span></span>    | <span data-ttu-id="433c0-126">La hauteur de l’apparence est supérieure à la largeur de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="433c0-126">The height of the skin is greater than the width of the skin.</span></span> <span data-ttu-id="433c0-127">L’affichage est orienté verticalement.</span><span class="sxs-lookup"><span data-stu-id="433c0-127">The display is oriented in a vertical fashion.</span></span> |
| <span data-ttu-id="433c0-128">Carré</span><span class="sxs-lookup"><span data-stu-id="433c0-128">Square</span></span>      | <span data-ttu-id="433c0-129">La hauteur de l’apparence est égale à la largeur de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="433c0-129">The height of the skin is equal to the width of the skin.</span></span> <span data-ttu-id="433c0-130">L’affichage n’a aucune orientation.</span><span class="sxs-lookup"><span data-stu-id="433c0-130">The display has no orientation.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="433c0-131">Le lecteur Windows Media 9 Series pour Windows Mobile 2003 affiche uniquement une apparence particulière lorsque la section Description spécifiée dans le fichier de définition d’apparence correspond à l’état actuel de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="433c0-131">Windows Media Player 9 Series for Windows Mobile 2003 will only display a particular skin when the description section specified in the skin definition file matches the current state of the device.</span></span>

 

<span data-ttu-id="433c0-132">Veillez à toujours spécifier les dimensions, la résolution et l’orientation appropriées pour lesquelles votre apparence a été créée.</span><span class="sxs-lookup"><span data-stu-id="433c0-132">You should be careful to always specify the correct dimensions, resolution, and orientation for which your skin was authored.</span></span> <span data-ttu-id="433c0-133">Par exemple, si les dimensions spécifiées par votre apparence décrivent une orientation paysage, votre apparence n’est pas disponible lorsque l’appareil est en mode portrait, même si vous spécifiez portrait dans la ligne orientation.</span><span class="sxs-lookup"><span data-stu-id="433c0-133">For example, if the dimensions specified by your skin describe a landscape orientation, your skin will not be available when the device is in portrait mode, even if you specify Portrait in the orientation line.</span></span>

## <a name="related-topics"></a><span data-ttu-id="433c0-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="433c0-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="433c0-135">**Référence d’apparence**</span><span class="sxs-lookup"><span data-stu-id="433c0-135">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




