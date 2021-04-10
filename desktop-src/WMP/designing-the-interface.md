---
title: Conception de l’interface
description: Conception de l’interface
ms.assetid: 7b87bab4-8246-461a-a9cd-2d348e7f0d48
keywords:
- Windows Media Player Mobile Skins, interfaces utilisateur
- apparences, interfaces utilisateur
- création d’apparences, d’interfaces utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8070ef6fd4589f762624d7a0b5ee1d380a264066
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100773"
---
# <a name="designing-the-interface"></a><span data-ttu-id="1ae55-106">Conception de l’interface</span><span class="sxs-lookup"><span data-stu-id="1ae55-106">Designing the Interface</span></span>

<span data-ttu-id="1ae55-107">Une fois les fonctions choisies, l’interface peut être conçue.</span><span class="sxs-lookup"><span data-stu-id="1ae55-107">Once the functions have been chosen, the interface can be designed.</span></span> <span data-ttu-id="1ae55-108">Une interface simple a été choisie pour correspondre à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1ae55-108">A simple interface was chosen to match the functionality.</span></span> <span data-ttu-id="1ae55-109">Les symboles des contrôles ont été choisis dans les contrôles de magnétoscope standard.</span><span class="sxs-lookup"><span data-stu-id="1ae55-109">Symbols for the controls were chosen from standard VCR controls.</span></span>

<span data-ttu-id="1ae55-110">L’illustration suivante montre à quoi ressemblera l’interface.</span><span class="sxs-lookup"><span data-stu-id="1ae55-110">The following image shows what the interface will look like.</span></span>

![exemple d’interface](images/ceswmful.png)

-   <span data-ttu-id="1ae55-112">**Bouton PlayPause ou PlayPauseStop.**</span><span class="sxs-lookup"><span data-stu-id="1ae55-112">**PlayPause or PlayPauseStop button.**</span></span> <span data-ttu-id="1ae55-113">L’utilisateur aura le plus de toucher, donc vous pouvez envisager un plus grand bouton.</span><span class="sxs-lookup"><span data-stu-id="1ae55-113">The user will be tapping this the most, so you might consider a larger button.</span></span> <span data-ttu-id="1ae55-114">L’angle supérieur droit constitue un bon emplacement que l’utilisateur peut trouver rapidement.</span><span class="sxs-lookup"><span data-stu-id="1ae55-114">The upper-right corner makes a good location that the user can find quickly.</span></span> <span data-ttu-id="1ae55-115">Une flèche pleine est utilisée pour indiquer que la lecture et les deux barres verticales (qui ne sont pas affichées ici) seront utilisées pour indiquer une pause.</span><span class="sxs-lookup"><span data-stu-id="1ae55-115">A solid arrow is used to indicate play and two vertical bars (not shown here) will be used to indicate pause.</span></span>
    > [!Note]  
    > <span data-ttu-id="1ae55-116">Le bouton PlayPauseStop peut uniquement être utilisé lors de la création d’une apparence pour le lecteur Windows Media 10 mobile ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1ae55-116">The PlayPauseStop button can only be used when creating a skin for Windows Media Player 10 Mobile or later.</span></span>

     

-   <span data-ttu-id="1ae55-117">**Bouton arrêter.**</span><span class="sxs-lookup"><span data-stu-id="1ae55-117">**Stop button.**</span></span> <span data-ttu-id="1ae55-118">Pour faciliter la recherche, elle est placée dans l’angle supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="1ae55-118">To make this easy to find, it is placed at the upper-left corner.</span></span> <span data-ttu-id="1ae55-119">Un carré est utilisé pour indiquer l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="1ae55-119">A square is used to indicate stop.</span></span> <span data-ttu-id="1ae55-120">Si vous créez une apparence pour Windows Media Player 10 mobile ou version ultérieure, le bouton PlayPauseStop fournit déjà cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1ae55-120">If you are creating a skin for Windows Media Player 10 Mobile or later, the PlayPauseStop button already provides this functionality.</span></span>
-   <span data-ttu-id="1ae55-121">**Boutons suivant et préc.**</span><span class="sxs-lookup"><span data-stu-id="1ae55-121">**Next and Prev buttons.**</span></span> <span data-ttu-id="1ae55-122">Étant donné qu’elles ne seront pas utilisées aussi souvent, elles sont placées sur la gauche.</span><span class="sxs-lookup"><span data-stu-id="1ae55-122">Since these will not be used as often, they are placed on the left.</span></span> <span data-ttu-id="1ae55-123">Le suivant se trouve au-dessus du bouton précédent, car il est plus probable que les utilisateurs veulent avancer dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="1ae55-123">The Next is above the Prev button because people will more likely want to move forward in a playlist.</span></span> <span data-ttu-id="1ae55-124">Les symboles à deux flèches sont utilisés, car ils sont similaires en fonction d’un contrôle d’avance rapide.</span><span class="sxs-lookup"><span data-stu-id="1ae55-124">The double-arrow symbols are used because they are similar in function to a fast-forward control.</span></span>
-   <span data-ttu-id="1ae55-125">**TrackBar du volume.**</span><span class="sxs-lookup"><span data-stu-id="1ae55-125">**Volume trackbar.**</span></span> <span data-ttu-id="1ae55-126">Il est placé en bas de l’écran et il s’agit d’une simple ligne avec un bouton Thumb.</span><span class="sxs-lookup"><span data-stu-id="1ae55-126">This is placed at the bottom of the screen and is a simple line with a thumb button on top of it.</span></span>
-   <span data-ttu-id="1ae55-127">**Zone de texte de texte défilant.**</span><span class="sxs-lookup"><span data-stu-id="1ae55-127">**Marquee text box.**</span></span> <span data-ttu-id="1ae55-128">Elle est placée sous le bouton PlayPause ou PlayPauseStop pour qu’elle soit facile à voir.</span><span class="sxs-lookup"><span data-stu-id="1ae55-128">This is placed under the PlayPause or PlayPauseStop button so that it is easy to see.</span></span>

<span data-ttu-id="1ae55-129">Vous pouvez le faire tout d’abord et expérimenter le placement de chaque élément d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1ae55-129">You may want to sketch this first and experiment with the placement of each user interface element.</span></span> <span data-ttu-id="1ae55-130">La conception présentée ici a été choisie pour des raisons de simplicité et de facilité d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="1ae55-130">The design shown here was chosen for simplicity and ease of use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ae55-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ae55-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ae55-132">**Repère d’apparence**</span><span class="sxs-lookup"><span data-stu-id="1ae55-132">**Skin Guide**</span></span>](skin-guide.md)
</dt> </dl>

 

 




