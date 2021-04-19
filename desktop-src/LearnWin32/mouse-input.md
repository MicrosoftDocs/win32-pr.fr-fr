---
title: Entrée de la souris (prise en main de Win32 et C++)
description: Entrée de la souris
ms.assetid: EB074CB6-2BB3-4593-A843-8EE25CA028BE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71a560baf110892ba1b8f277c55fc124888b62b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106509483"
---
# <a name="mouse-input-get-started-with-win32-and-c"></a><span data-ttu-id="c4e5a-103">Entrée de la souris (prise en main de Win32 et C++)</span><span class="sxs-lookup"><span data-stu-id="c4e5a-103">Mouse Input (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="c4e5a-104">Windows prend en charge la souris avec un maximum de cinq boutons : gauche, milieu et droite, ainsi que deux autres boutons appelés le bouton XButton1 et XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="c4e5a-104">Windows supports mice with up to five buttons: left, middle, and right, plus two additional buttons called XBUTTON1 and XBUTTON2.</span></span>

![illustration qui montre les boutons gauche (1), droite (2), milieu (3) et le bouton XButton1 (4).](images/mouse.png)

<span data-ttu-id="c4e5a-106">La plupart des souris pour Windows ont au moins les boutons gauche et droit.</span><span class="sxs-lookup"><span data-stu-id="c4e5a-106">Most mice for Windows have at least the left and right buttons.</span></span> <span data-ttu-id="c4e5a-107">Le bouton gauche de la souris est utilisé pour le pointage, la sélection, le glissement, etc.</span><span class="sxs-lookup"><span data-stu-id="c4e5a-107">The left mouse button is used for pointing, selecting, dragging, and so forth.</span></span> <span data-ttu-id="c4e5a-108">Le bouton droit de la souris affiche généralement un menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="c4e5a-108">The right mouse button typically displays a context menu.</span></span> <span data-ttu-id="c4e5a-109">Certaines souris disposent d’une roulette de défilement située entre les boutons gauche et droit.</span><span class="sxs-lookup"><span data-stu-id="c4e5a-109">Some mice have a scroll wheel located between the left and right buttons.</span></span> <span data-ttu-id="c4e5a-110">Selon la souris, la roulette de défilement peut également être cliquable, ce qui en fait le bouton central.</span><span class="sxs-lookup"><span data-stu-id="c4e5a-110">Depending on the mouse, the scroll wheel might also be clickable, making it the middle button.</span></span>

<span data-ttu-id="c4e5a-111">Les boutons le bouton XButton1 et XBUTTON2 sont souvent situés sur les côtés de la souris, près de la base.</span><span class="sxs-lookup"><span data-stu-id="c4e5a-111">The XBUTTON1 and XBUTTON2 buttons are often located on the sides of the mouse, near the base.</span></span> <span data-ttu-id="c4e5a-112">Ces boutons supplémentaires ne sont pas présents sur toutes les souris.</span><span class="sxs-lookup"><span data-stu-id="c4e5a-112">These extra buttons are not present on all mice.</span></span> <span data-ttu-id="c4e5a-113">S’il est présent, les boutons le bouton XButton1 et XBUTTON2 sont souvent mappés à une fonction d’application, telle que la navigation vers l’avant et vers l’arrière dans un navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="c4e5a-113">If present, the XBUTTON1 and XBUTTON2 buttons are often mapped to an application function, such as forward and backward navigation in a Web browser.</span></span>

<span data-ttu-id="c4e5a-114">Les utilisateurs de gauche trouvent souvent plus à l’aise pour échanger les fonctions des boutons gauche et droit, en utilisant le bouton droit comme pointeur et le bouton gauche pour afficher le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="c4e5a-114">Left-handed users often find it more comfortable to swap the functions of the left and right buttons—using the right button as the pointer, and the left button to show the context menu.</span></span> <span data-ttu-id="c4e5a-115">Pour cette raison, la documentation d’aide de Windows utilise le *bouton principal* termes et le *bouton secondaire*, qui font référence à la fonction logique plutôt qu’à l’emplacement physique.</span><span class="sxs-lookup"><span data-stu-id="c4e5a-115">For this reason, the Windows help documentation uses the terms *primary button* and *secondary button*, which refer to logical function rather than physical placement.</span></span> <span data-ttu-id="c4e5a-116">Dans le paramètre par défaut (droitier), le bouton gauche est le bouton principal et la droite est le bouton secondaire.</span><span class="sxs-lookup"><span data-stu-id="c4e5a-116">In the default (right-handed) setting, the left button is the primary button and the right is the secondary button.</span></span> <span data-ttu-id="c4e5a-117">Toutefois, les conditions de clic droit et de *clic* *droit* font référence aux actions logiques.</span><span class="sxs-lookup"><span data-stu-id="c4e5a-117">However, the terms *right click* and *left click* refer to logical actions.</span></span> <span data-ttu-id="c4e5a-118">*Cliquez avec le bouton droit* sur le bouton principal, que ce bouton se trouve physiquement à droite ou à gauche de la souris.</span><span class="sxs-lookup"><span data-stu-id="c4e5a-118">*Right clicking* means clicking the primary button, whether that button is physically on the right or left side of the mouse.</span></span>

<span data-ttu-id="c4e5a-119">Quelle que soit la façon dont l’utilisateur configure la souris, Windows convertit automatiquement les messages de la souris afin qu’ils soient cohérents.</span><span class="sxs-lookup"><span data-stu-id="c4e5a-119">Regardless of how the user configures the mouse, Windows automatically translates mouse messages so they are consistent.</span></span> <span data-ttu-id="c4e5a-120">L’utilisateur peut échanger les boutons principal et secondaire au milieu de l’utilisation de votre programme, et il n’a aucune incidence sur le comportement de votre programme.</span><span class="sxs-lookup"><span data-stu-id="c4e5a-120">The user can swap the primary and secondary buttons in the middle of using your program, and it will not affect how your program behaves.</span></span>

<span data-ttu-id="c4e5a-121">La documentation MSDN utilise le bouton *droit* et le bouton *gauche* pour signifier les boutons *principal* et *secondaire* .</span><span class="sxs-lookup"><span data-stu-id="c4e5a-121">MSDN documentation uses the terms *right button* and *left button* to mean *primary* and *secondary* button.</span></span> <span data-ttu-id="c4e5a-122">Cette terminologie est cohérente avec les noms des messages de fenêtre pour l’entrée de la souris.</span><span class="sxs-lookup"><span data-stu-id="c4e5a-122">This terminology is consistent with the names of the window messages for mouse input.</span></span> <span data-ttu-id="c4e5a-123">Rappelez-vous simplement que les boutons physiques gauche et droit peuvent être permutés.</span><span class="sxs-lookup"><span data-stu-id="c4e5a-123">Just remember that the physical left and right buttons might be swapped.</span></span>

## <a name="next"></a><span data-ttu-id="c4e5a-124">Suivant</span><span class="sxs-lookup"><span data-stu-id="c4e5a-124">Next</span></span>

[<span data-ttu-id="c4e5a-125">Réponse aux clics de souris</span><span class="sxs-lookup"><span data-stu-id="c4e5a-125">Responding to Mouse Clicks</span></span>](mouse-clicks.md)

 

 




