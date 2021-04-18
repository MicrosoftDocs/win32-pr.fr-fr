---
title: Combinaisons de texte
description: Combinaisons de texte
ms.assetid: 0220b77e-5f1e-4569-a8fe-5085e0c16338
keywords:
- Windows Media Player Mobile Skins, palissades
- apparences, rectangles de sélection
- informations de référence sur les habillages, les cadres
- textes défilant dans les apparences, combinaisons de texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5668a9e18555b871c82bae7ed1826766ec9429e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507283"
---
# <a name="text-combinations"></a><span data-ttu-id="7877b-107">Combinaisons de texte</span><span class="sxs-lookup"><span data-stu-id="7877b-107">Text Combinations</span></span>

<span data-ttu-id="7877b-108">Cette valeur est une liste de combinaisons de zones d’affichage de texte, séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="7877b-108">This value is a list of text display box combinations, separated by commas.</span></span> <span data-ttu-id="7877b-109">Les zones d’affichage de texte peuvent être jointes par un caractère plus pour créer une nouvelle valeur d’affichage de texte défilant et tout type de texte défini dans la section type de texte peut être utilisé dans votre texte défilant.</span><span class="sxs-lookup"><span data-stu-id="7877b-109">Text display boxes can be joined together by a plus character to create a new marquee display value and any text type defined in the Text Type section can be used in your marquee.</span></span>

<span data-ttu-id="7877b-110">Lorsque vous déterminez ce qui doit être affiché, le lecteur Windows Media Mobile évalue chaque élément de la liste pour voir si toutes les parties sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="7877b-110">When determining what to display, Windows Media Player Mobile evaluates each item in the list to see if all parts are available.</span></span> <span data-ttu-id="7877b-111">Si ce n’est pas le cas, l’élément suivant est évalué, et ainsi de suite, jusqu’à ce que toutes les parties disponibles aient été trouvées.</span><span class="sxs-lookup"><span data-stu-id="7877b-111">If not, the next item is evaluated, and so on, until all the available parts have been found.</span></span> <span data-ttu-id="7877b-112">Par exemple, si vous souhaitez afficher l’auteur et le titre, mais que vous ne savez pas si les deux sont disponibles, utilisez la valeur suivante :</span><span class="sxs-lookup"><span data-stu-id="7877b-112">For example, if you want to display Author and Title, but you're not sure whether both are available, use the following value:</span></span>


```C++
Title+Author, Title, Author

```



<span data-ttu-id="7877b-113">Dans l’exemple précédent, le titre et l’auteur s’affichent si le titre et l’auteur ont été définis pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="7877b-113">In the preceding example, the Title+Author will be displayed if the title and author have been defined for the media item.</span></span> <span data-ttu-id="7877b-114">Si les deux ne sont pas définis, le titre est évalué et affiché s’il est défini.</span><span class="sxs-lookup"><span data-stu-id="7877b-114">If both are not defined, the Title is evaluated and displayed if defined.</span></span> <span data-ttu-id="7877b-115">Si le titre n’est pas défini, l’auteur est affiché s’il est défini.</span><span class="sxs-lookup"><span data-stu-id="7877b-115">If the Title is not defined, the Author is displayed if defined.</span></span> <span data-ttu-id="7877b-116">Si aucun n’est défini, rien ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="7877b-116">If neither is defined, then nothing is displayed.</span></span>

<span data-ttu-id="7877b-117">Lorsque vous utilisez le signe plus pour la concaténation, veillez à ne pas avoir d’espaces de part et d’autre du signe plus.</span><span class="sxs-lookup"><span data-stu-id="7877b-117">When using the plus sign for concatenation, be sure you have no spaces on either side of the plus sign.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7877b-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7877b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7877b-119">**Chapiteau**</span><span class="sxs-lookup"><span data-stu-id="7877b-119">**Marquee**</span></span>](marquee.md)
</dt> <dt>

[<span data-ttu-id="7877b-120">**Type de texte**</span><span class="sxs-lookup"><span data-stu-id="7877b-120">**Text Type**</span></span>](text-type.md)
</dt> </dl>

 

 




