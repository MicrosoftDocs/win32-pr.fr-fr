---
title: Utilisation de rectangles (Windows Media Player SDK)
description: Utilisation de rectangles
ms.assetid: b3fc16b4-dc93-43c0-a97d-5234e36437c8
keywords:
- visualisations, rectangles
- visualisations personnalisées, rectangles
- visualisations, fonction Render
- visualisations personnalisées, fonction Render
- Render, fonction, rectangles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b48f16888d8e71c052d216a838683f2b7127e75
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106510512"
---
# <a name="using-rectangles-windows-media-player-sdk"></a><span data-ttu-id="856b7-108">Utilisation de rectangles (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="856b7-108">Using Rectangles (Windows Media Player SDK)</span></span>

<span data-ttu-id="856b7-109">Les rectangles sont utilisés pour spécifier des zones rectangulaires dans Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="856b7-109">Rectangles are used to specify rectangular areas in Microsoft Windows.</span></span> <span data-ttu-id="856b7-110">Vous pouvez créer de nombreux rectangles dans votre fenêtre, mais le lecteur Windows Media fournit les valeurs d’un rectangle via la fonction [IWMPEffects :: Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) .</span><span class="sxs-lookup"><span data-stu-id="856b7-110">You can create many rectangles in your window, but Windows Media Player supplies the values of one rectangle through the [IWMPEffects::Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) function.</span></span> <span data-ttu-id="856b7-111">Si votre plug-in est restitué à l’aide d’une fenêtre, le rectangle est la zone cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="856b7-111">If your plug-in renders using a window, the rectangle is the client area of the window.</span></span> <span data-ttu-id="856b7-112">C’est ce que l’on appelle le rectangle PRC et définit le rectangle par lequel le lecteur Windows Media affiche votre visualisation.</span><span class="sxs-lookup"><span data-stu-id="856b7-112">This is called the prc rectangle, and it defines the rectangle that Windows Media Player will display your visualization through.</span></span> <span data-ttu-id="856b7-113">Utilisez cette fréquence pour être certain de ne pas dessiner au-delà des étendues du rectangle fourni par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="856b7-113">Use this frequently to be sure you do not draw beyond the extents of the rectangle supplied by Windows Media Player.</span></span>

<span data-ttu-id="856b7-114">Un rectangle a quatre valeurs qui le définissent.</span><span class="sxs-lookup"><span data-stu-id="856b7-114">A rectangle has four values that define it.</span></span> <span data-ttu-id="856b7-115">Ils sont gauche, haut, droit et bas.</span><span class="sxs-lookup"><span data-stu-id="856b7-115">They are left, top, right, and bottom.</span></span> <span data-ttu-id="856b7-116">L’angle supérieur gauche du rectangle est défini par des gauches et des haut, et le coin inférieur droit du rectangle est défini par le bas et la droite.</span><span class="sxs-lookup"><span data-stu-id="856b7-116">The top, left corner of the rectangle is defined by left and top, and the bottom, right corner of the rectangle is defined by bottom and right.</span></span>

<span data-ttu-id="856b7-117">Utilisez le code suivant pour récupérer les étendues de votre rectangle de dessin.</span><span class="sxs-lookup"><span data-stu-id="856b7-117">Use the following code to get the extents of your drawing rectangle.</span></span> <span data-ttu-id="856b7-118">Vous devez effectuer cette opération, car l’utilisateur peut redimensionner la fenêtre et vous voulez être sûr que vous dessinez toujours dans une zone que l’utilisateur peut voir.</span><span class="sxs-lookup"><span data-stu-id="856b7-118">You need to do this because the user may resize the window, and you want to be sure that you are always drawing in an area the user can see.</span></span>


```C++
int leftside = prc->left;
int rightside = prc->right;
int topside = prc->top;
int bottomside = prc->bottom;

```



<span data-ttu-id="856b7-119">Par exemple, pour dessiner de gauche à droite, en haut de la fenêtre, utilisez un code similaire à celui-ci :</span><span class="sxs-lookup"><span data-stu-id="856b7-119">For example, to draw from left to right, along the top of the window, use code like this:</span></span>


```C++
::MoveToEx( hdc, prc->left, prc->top, NULL );  
::LineTo(hdc, prc->right, prc->top);

```



## <a name="related-topics"></a><span data-ttu-id="856b7-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="856b7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="856b7-121">**Implémentation du rendu**</span><span class="sxs-lookup"><span data-stu-id="856b7-121">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




