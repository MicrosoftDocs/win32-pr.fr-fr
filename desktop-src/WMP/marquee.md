---
title: Chapiteau
description: Chapiteau
ms.assetid: 2715732a-25cc-4ba9-9aa6-181ebb9e1d1c
keywords:
- Windows Media Player Mobile Skins, palissades
- apparences, rectangles de sélection
- informations de référence sur les habillages, les cadres
- textes défilant dans les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7efa2db2c6079d47d207240b18a57ebbf7e41ae1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380174"
---
# <a name="marquee"></a><span data-ttu-id="147f9-107">Chapiteau</span><span class="sxs-lookup"><span data-stu-id="147f9-107">Marquee</span></span>

<span data-ttu-id="147f9-108">Un texte défilant est une zone de texte déroulante qui affiche des informations à partir d’une ou plusieurs zones d’affichage de texte.</span><span class="sxs-lookup"><span data-stu-id="147f9-108">A marquee is a scrolling text display box that displays information from one or more text display boxes.</span></span> <span data-ttu-id="147f9-109">Vous n’avez pas besoin d’ajouter un texte défilant, mais cela peut s’avérer très utile lorsque vous avez des informations détaillées que vous souhaitez afficher à l’utilisateur dans un espace limité.</span><span class="sxs-lookup"><span data-stu-id="147f9-109">You do not need to add a marquee, but it can be very useful when you have detailed information you want to display to the user in a limited space.</span></span>

<span data-ttu-id="147f9-110">Le texte dans le texte défilant défile uniquement si les deux conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="147f9-110">The text in the marquee will scroll only if both of the following conditions are met:</span></span>

-   <span data-ttu-id="147f9-111">Vous avez plus de texte à afficher dans le texte défilant que la largeur de la zone d’affichage du texte défilant.</span><span class="sxs-lookup"><span data-stu-id="147f9-111">You have more text to display in the marquee than the width of the marquee display box.</span></span>
-   <span data-ttu-id="147f9-112">L’élément multimédia est arrêté ou suspendu.</span><span class="sxs-lookup"><span data-stu-id="147f9-112">The media item is either stopped or paused.</span></span>

<span data-ttu-id="147f9-113">La section de texte défilant du fichier de définition d’apparence doit commencer par cette ligne :</span><span class="sxs-lookup"><span data-stu-id="147f9-113">The Marquee section of the skin definition file must begin with this line:</span></span>


```C++
[ Marquee ]

```



> [!Note]  
> <span data-ttu-id="147f9-114">Pour assurer la compatibilité avec les versions de Windows Media Player Mobile antérieures à Windows Media Player 10 mobile, l’utilisation de « marquis » dans un fichier de définition d’apparence est toujours considérée comme valide.</span><span class="sxs-lookup"><span data-stu-id="147f9-114">To maintain compatibility with versions of Windows Media Player Mobile older than Windows Media Player 10 Mobile, using "Marquis" in a skin definition file is still considered valid.</span></span>

 

<span data-ttu-id="147f9-115">Vous devez ensuite ajouter une ou plusieurs lignes qui contiennent des informations sur chacune des zones d’affichage de texte défilant dans votre apparence.</span><span class="sxs-lookup"><span data-stu-id="147f9-115">You then must add one or more lines that contain information about each of the marquee display boxes in your skin.</span></span>


```C++
    3,2,234,20   Tahoma,12,N  255,0,0    Playlist, Time, Filename

```



<span data-ttu-id="147f9-116">Vous pouvez utiliser le modèle suivant pour la section marquee de votre fichier de définition d’apparence :</span><span class="sxs-lookup"><span data-stu-id="147f9-116">You can use the following template for the Marquee section of your skin definition file:</span></span>


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------

```



<span data-ttu-id="147f9-117">Vous devez utiliser l’ordre suivant pour obtenir des informations dans chaque ligne de la section marquee (chaque partie de la ligne est requise) :</span><span class="sxs-lookup"><span data-stu-id="147f9-117">You must use the following order for information in each line of the Marquee section (each part of the line is required):</span></span>

1.  [<span data-ttu-id="147f9-118">Emplacement du texte défilant</span><span class="sxs-lookup"><span data-stu-id="147f9-118">Marquee Location</span></span>](marquee-location.md)
2.  [<span data-ttu-id="147f9-119">Police du texte défilant</span><span class="sxs-lookup"><span data-stu-id="147f9-119">Marquee Font</span></span>](marquee-font.md)
3.  [<span data-ttu-id="147f9-120">Couleur du texte défilant</span><span class="sxs-lookup"><span data-stu-id="147f9-120">Marquee Color</span></span>](marquee-color.md)
4.  [<span data-ttu-id="147f9-121">Combinaisons de texte</span><span class="sxs-lookup"><span data-stu-id="147f9-121">Text Combinations</span></span>](text-combinations.md)

<span data-ttu-id="147f9-122">Pour obtenir un exemple de code de texte défilant, consultez la [section exemple de texte défilant](sample-marquee-section.md).</span><span class="sxs-lookup"><span data-stu-id="147f9-122">For an example of Marquee code, see [Sample Marquee Section](sample-marquee-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="147f9-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="147f9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="147f9-124">**Référence d’apparence**</span><span class="sxs-lookup"><span data-stu-id="147f9-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




