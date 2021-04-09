---
title: Boutons (kit de développement logiciel Windows Media Player)
description: Boutons
ms.assetid: 1212e2d9-e8f8-45d8-8c7f-20865c9c9c94
keywords:
- Windows Media Player Mobile Skins, vue d’ensemble du bouton
- apparences, vue d’ensemble du bouton
- informations de référence sur les apparences, les boutons
- boutons dans des apparences, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f06eb2fe21ee18a24f92e92d4fa760e9c76887
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102757"
---
# <a name="buttons-windows-media-player-sdk"></a><span data-ttu-id="b280c-107">Boutons (kit de développement logiciel Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="b280c-107">Buttons (Windows Media Player SDK)</span></span>

<span data-ttu-id="b280c-108">Vous pouvez utiliser un ou plusieurs boutons dans votre apparence, et chaque bouton doit être défini dans le fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="b280c-108">You will want to use one or more buttons in your skin, and each button must be defined in the skin definition file.</span></span> <span data-ttu-id="b280c-109">Si vous ne définissez pas de bouton dans cette section, votre apparence ne sera pas en mesure de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="b280c-109">If you do not define a button in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="b280c-110">La section Buttons du fichier de définition d’apparence commence par cette ligne :</span><span class="sxs-lookup"><span data-stu-id="b280c-110">The buttons section of the skin definition file begins with this line:</span></span>


```C++
[ Buttons ]

```



<span data-ttu-id="b280c-111">Vous devez ensuite ajouter une ou plusieurs lignes qui contiennent des informations sur chacun des boutons de votre apparence.</span><span class="sxs-lookup"><span data-stu-id="b280c-111">You then must add one or more lines that contain information about each of the buttons in your skin.</span></span> <span data-ttu-id="b280c-112">Une ligne classique peut être :</span><span class="sxs-lookup"><span data-stu-id="b280c-112">A typical line might be:</span></span>


```C++
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98

```



<span data-ttu-id="b280c-113">Notez que ce code doit être tapé sous la forme d’une ligne commençant par « PlayPause » et se terminant par « push @ 160, 98 ».</span><span class="sxs-lookup"><span data-stu-id="b280c-113">Note that this code should be typed as one line starting with "PlayPause" and ending with "Pushed @ 160,98".</span></span>

<span data-ttu-id="b280c-114">Vous pouvez utiliser le modèle suivant pour la section de bouton de votre fichier de définition d’apparence :</span><span class="sxs-lookup"><span data-stu-id="b280c-114">You can use the following template for the Button section of your skin definition file:</span></span>


```C++
//  <Function> <Type>     <Location>     <Push Image Src> <Dis Image Src>    <Hit R,G,B> <Norm 2 Image Src> <Push 2 Image Src>
//  ---------- ------     ----------     ---------------- ---------------    ----------- ------------------ ------------------

```



<span data-ttu-id="b280c-115">Là encore, Notez qu’elles doivent être de type ligne unique, la première commençant par « // <Function> » et se terminant par « &lt; Push 2 image SRC &gt; ».</span><span class="sxs-lookup"><span data-stu-id="b280c-115">Again, note that these should be typed as single lines, the first starting with "// <Function>" and ending with "&lt;Push 2 Image Src&gt;".</span></span> <span data-ttu-id="b280c-116">La deuxième ligne commence par « //---------- » et se termine par « ------------------. ».</span><span class="sxs-lookup"><span data-stu-id="b280c-116">The second line starts with "// ----------" and ends with "------------------."</span></span>

<span data-ttu-id="b280c-117">Les informations de bouton pour chaque ligne dans la section du bouton doivent apparaître dans l’ordre suivant.</span><span class="sxs-lookup"><span data-stu-id="b280c-117">Button information for each line in the Button section must appear in the following order.</span></span> <span data-ttu-id="b280c-118">Seules les six premières parties de la ligne sont requises.</span><span class="sxs-lookup"><span data-stu-id="b280c-118">Only the first six parts of the line are required.</span></span> <span data-ttu-id="b280c-119">Les images secondaires ne sont pas incluses, sauf si elles sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="b280c-119">Secondary images are not included unless they are needed.</span></span>

1.  [<span data-ttu-id="b280c-120">Button, fonction</span><span class="sxs-lookup"><span data-stu-id="b280c-120">Button Function</span></span>](button-function.md)
2.  [<span data-ttu-id="b280c-121">Type de bouton</span><span class="sxs-lookup"><span data-stu-id="b280c-121">Button Type</span></span>](button-type.md)
3.  [<span data-ttu-id="b280c-122">Emplacement du bouton</span><span class="sxs-lookup"><span data-stu-id="b280c-122">Button Location</span></span>](button-location.md)
4.  [<span data-ttu-id="b280c-123">Source de l’image Push</span><span class="sxs-lookup"><span data-stu-id="b280c-123">Pushed Image Source</span></span>](pushed-image-source.md)
5.  [<span data-ttu-id="b280c-124">Source de l’image pour le bouton désactivé</span><span class="sxs-lookup"><span data-stu-id="b280c-124">Image Source for Disabled Button</span></span>](image-source-for-disabled-button.md)
6.  [<span data-ttu-id="b280c-125">Toucher la couleur RVB</span><span class="sxs-lookup"><span data-stu-id="b280c-125">Hit RGB Color</span></span>](hit-rgb-color.md)
7.  [<span data-ttu-id="b280c-126">Source d’image secondaire normale</span><span class="sxs-lookup"><span data-stu-id="b280c-126">Normal Secondary Image Source</span></span>](normal-secondary-image-source.md)
8.  [<span data-ttu-id="b280c-127">Source d’image tertiaire normale</span><span class="sxs-lookup"><span data-stu-id="b280c-127">Normal Tertiary Image Source</span></span>](normal-tertiary-image-source.md)
9.  [<span data-ttu-id="b280c-128">Source d’image secondaire faisant l’objet d’un push</span><span class="sxs-lookup"><span data-stu-id="b280c-128">Pushed Secondary Image Source</span></span>](pushed-secondary-image-source.md)
10. [<span data-ttu-id="b280c-129">Source d’image tertiaire envoyée</span><span class="sxs-lookup"><span data-stu-id="b280c-129">Pushed Tertiary Image Source</span></span>](pushed-tertiary-image-source.md)

<span data-ttu-id="b280c-130">Pour obtenir un exemple de code de bouton, consultez la [section exemple de bouton](sample-button-section.md).</span><span class="sxs-lookup"><span data-stu-id="b280c-130">For an example of button code, see [Sample Button Section](sample-button-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b280c-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b280c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b280c-132">**Référence d’apparence**</span><span class="sxs-lookup"><span data-stu-id="b280c-132">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




