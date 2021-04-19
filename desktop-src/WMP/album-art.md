---
title: Pochette de l’album
description: Pochette de l’album
ms.assetid: a5996232-e1ee-41ae-a6ca-f841321644fe
keywords:
- Windows Media Player Mobile Skins, pochette d’album
- apparences, pochette d’album
- référence pour les habillages, la pochette d’album
- fichiers art pour les habillages, la pochette d’album
- pochette d’album dans des habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0974f8683da98469e75a4472d086dcb1a244c75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509993"
---
# <a name="album-art"></a><span data-ttu-id="d5781-108">Pochette de l’album</span><span class="sxs-lookup"><span data-stu-id="d5781-108">Album Art</span></span>

<span data-ttu-id="d5781-109">Quand vous créez une apparence pour Windows Media Player 10 mobile ou version ultérieure, vous pouvez afficher une pochette d’album qui se réfère à l’élément multimédia en cours de lecture.</span><span class="sxs-lookup"><span data-stu-id="d5781-109">When you create a skin for Windows Media Player 10 Mobile or later, you may want to display album art that relates to the currently playing media item.</span></span> <span data-ttu-id="d5781-110">Lorsque vous concevez votre apparence, vous souhaiterez réserver de l’espace dans l’image d’arrière-plan pour contenir la pochette de l’album.</span><span class="sxs-lookup"><span data-stu-id="d5781-110">When you design your skin, you will want to reserve space in the Background image to contain the album art.</span></span>

<span data-ttu-id="d5781-111">La section de la pochette de l’album du fichier de définition d’apparence doit commencer par la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="d5781-111">The Album Art section of the skin definition file must begin with the following line:</span></span>


```C++
[ Album Art ]

```



<span data-ttu-id="d5781-112">Vous devez ensuite ajouter des informations qui spécifient l’emplacement et la taille de la pochette de l’album dans votre apparence.</span><span class="sxs-lookup"><span data-stu-id="d5781-112">You then must add information that specifies the location and size of the album art in your skin.</span></span> <span data-ttu-id="d5781-113">Vous devez entrer quatre entiers positifs, séparés par des virgules qui définissent la gauche, le haut, la largeur et la hauteur de la pochette de l’album, en pixels, par rapport à l’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="d5781-113">You must enter four positive integers, separated by commas that define the left, top, width, and height of the album art, in pixels, relative to the background image.</span></span> <span data-ttu-id="d5781-114">L’exemple suivant montre comment spécifier des dimensions :</span><span class="sxs-lookup"><span data-stu-id="d5781-114">The following example shows how to specify dimensions:</span></span>


```C++
//  <Location>
//  ----------
   5,37,230,155

```



<span data-ttu-id="d5781-115">Si vous envisagez d’inclure une section vidéo dans votre apparence, vous pouvez utiliser la même taille et l’emplacement de votre pochette pour économiser de l’espace.</span><span class="sxs-lookup"><span data-stu-id="d5781-115">If you plan on including a video section in your skin, you can use the same size and location for your album art to conserve space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5781-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5781-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5781-117">**Référence d’apparence**</span><span class="sxs-lookup"><span data-stu-id="d5781-117">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




