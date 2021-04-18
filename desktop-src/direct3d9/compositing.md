---
description: Votre application peut utiliser la mémoire tampon de stencil pour les images 2D ou 3D composite sur une scène 3D.
ms.assetid: 9233d15d-fa99-41a2-a253-22f5ae5bf788
title: Composition (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bca61559d2773bd1e4f7dc345e9ad4c1fb6fcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512906"
---
# <a name="compositing-direct3d-9"></a><span data-ttu-id="7ed9e-103">Composition (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7ed9e-103">Compositing (Direct3D 9)</span></span>

<span data-ttu-id="7ed9e-104">Votre application peut utiliser la mémoire tampon de stencil pour les images 2D ou 3D composite sur une scène 3D.</span><span class="sxs-lookup"><span data-stu-id="7ed9e-104">Your application can use the stencil buffer to composite 2D or 3D images onto a 3D scene.</span></span> <span data-ttu-id="7ed9e-105">Un masque dans le tampon de stencil est utilisé pour occultait une zone de la surface cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="7ed9e-105">A mask in the stencil buffer is used to occlude an area of the rendering target surface.</span></span> <span data-ttu-id="7ed9e-106">Des informations 2D stockées, telles que du texte ou des bitmaps, peuvent ensuite être écrites dans la zone bloqués.</span><span class="sxs-lookup"><span data-stu-id="7ed9e-106">Stored 2D information, such as text or bitmaps, can then be written to the occluded area.</span></span> <span data-ttu-id="7ed9e-107">Votre application peut également restituer des primitives 3D supplémentaires dans la région masquée du stencil de la surface cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="7ed9e-107">Alternately, your application can render additional 3D primitives to the stencil-masked region of the rendering target surface.</span></span> <span data-ttu-id="7ed9e-108">Il peut même rendre une scène entière.</span><span class="sxs-lookup"><span data-stu-id="7ed9e-108">It can even render an entire scene.</span></span>

<span data-ttu-id="7ed9e-109">Les jeux composent souvent plusieurs scènes 3D ensemble.</span><span class="sxs-lookup"><span data-stu-id="7ed9e-109">Games often composite multiple 3D scenes together.</span></span> <span data-ttu-id="7ed9e-110">Par exemple, la conduite des jeux affiche généralement un miroir en mode arrière.</span><span class="sxs-lookup"><span data-stu-id="7ed9e-110">For instance, driving games typically display a rear-view mirror.</span></span> <span data-ttu-id="7ed9e-111">Le miroir contient la vue de la scène 3D derrière le pilote.</span><span class="sxs-lookup"><span data-stu-id="7ed9e-111">The mirror contains the view of the 3D scene behind the driver.</span></span> <span data-ttu-id="7ed9e-112">Il s’agit essentiellement d’une deuxième scène 3D composite avec la vue d’avance du pilote.</span><span class="sxs-lookup"><span data-stu-id="7ed9e-112">It is essentially a second 3D scene composited with the driver's forward view.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ed9e-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7ed9e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ed9e-114">Techniques de tampon de stencil</span><span class="sxs-lookup"><span data-stu-id="7ed9e-114">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



