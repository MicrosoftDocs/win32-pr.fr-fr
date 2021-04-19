---
description: Le retournement de page est essentiel dans les logiciels multimédia, d’animation et de jeu ; elle est analogue à la façon dont vous pouvez effectuer une animation avec un bloc de papier.
ms.assetid: b6824962-c7cb-4e7f-8731-2971b0d9a2b0
title: Mise en mémoire tampon de basculement et de page (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bffad581c5d4250c7f36980ba1f278a9f770912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515122"
---
# <a name="page-flipping-and-back-buffering-direct3d-9"></a><span data-ttu-id="fc660-103">Mise en mémoire tampon de basculement et de page (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fc660-103">Page Flipping and Back Buffering (Direct3D 9)</span></span>

<span data-ttu-id="fc660-104">Le retournement de page est essentiel dans les logiciels multimédia, d’animation et de jeu ; elle est analogue à la façon dont vous pouvez effectuer une animation avec un bloc de papier.</span><span class="sxs-lookup"><span data-stu-id="fc660-104">Page flipping is key in multimedia, animation, and game software; it is analogous to the way you can do animation with a pad of paper.</span></span> <span data-ttu-id="fc660-105">Sur chaque page, l’artiste change légèrement la figure, de sorte que lorsque vous retournez rapidement entre les feuilles, le dessin apparaît animé.</span><span class="sxs-lookup"><span data-stu-id="fc660-105">On each page, the artist changes the figure slightly, so that when you flip rapidly between sheets, the drawing appears animated.</span></span>

<span data-ttu-id="fc660-106">Le basculement de page dans le logiciel est similaire à celui de ce processus.</span><span class="sxs-lookup"><span data-stu-id="fc660-106">Page flipping in software is similar to this process.</span></span> <span data-ttu-id="fc660-107">Direct3D implémente la fonctionnalité de retournement de page par le biais d’une chaîne de permutation, qui est une propriété de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fc660-107">Direct3D implements page flipping functionality through a swap chain, which is a property of the device.</span></span> <span data-ttu-id="fc660-108">Initialement, vous configurez une série de mémoires tampons Direct3D qui s’affichent à l’écran de la façon dont le papier de l’artiste bascule sur la page suivante.</span><span class="sxs-lookup"><span data-stu-id="fc660-108">Initially, you set up a series of Direct3D buffers that flip to the screen in the way that the artist's paper flips to the next page.</span></span> <span data-ttu-id="fc660-109">La première mémoire tampon est appelée « mémoire tampon d’avant ».</span><span class="sxs-lookup"><span data-stu-id="fc660-109">The first buffer is referred to as the color front buffer.</span></span> <span data-ttu-id="fc660-110">Les mémoires tampons sous-jacentes sont appelées mémoires tampons d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="fc660-110">The buffers behind it are called back buffers.</span></span> <span data-ttu-id="fc660-111">Votre application écrit dans une mémoire tampon d’arrière-plan, puis retourne la mémoire tampon d’arrière-plan de la couleur afin que la mémoire tampon d’arrière-plan apparaisse à l’écran.</span><span class="sxs-lookup"><span data-stu-id="fc660-111">Your application writes to a back buffer and then flips the color front buffer so that the back buffer appears on screen.</span></span> <span data-ttu-id="fc660-112">Lorsque le système affiche l’image, votre logiciel écrit à nouveau dans une mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="fc660-112">While the system displays the image, your software is again writing to a back buffer.</span></span> <span data-ttu-id="fc660-113">Le processus se poursuit aussi longtemps que vous animez, ce qui vous permet d’animer les images efficacement.</span><span class="sxs-lookup"><span data-stu-id="fc660-113">The process continues as long as you are animating, enabling you to animate images efficiently.</span></span>

<span data-ttu-id="fc660-114">Direct3D facilite la configuration des schémas de retournement de page à partir d’un simple schéma à double mise en mémoire tampon (une mémoire tampon d’arrière-plan de couleur avec une seule mémoire tampon d’arrière-plan) vers des schémas plus sophistiqués avec des mémoires tampons d’arrière-plan supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="fc660-114">Direct3D makes it easy to set up page flipping schemes - from a simple double-buffered scheme (a color front buffer with one back buffer) to more sophisticated schemes with additional back buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc660-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc660-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc660-116">Surfaces Direct3D</span><span class="sxs-lookup"><span data-stu-id="fc660-116">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="fc660-117">Qu’est-ce qu’une chaîne de permutation ? (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fc660-117">What Is a Swap Chain? (Direct3D 9)</span></span>](what-is-a-swap-chain-.md)
</dt> </dl>

 

 



