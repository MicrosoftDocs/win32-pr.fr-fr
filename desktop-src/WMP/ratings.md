---
title: Évaluations
description: Évaluations
ms.assetid: babc9db5-2782-4261-a571-acb7be4ea770
keywords:
- Skins mobiles Windows Media Player, évaluations
- apparences, évaluations
- informations de référence sur les apparences, les évaluations
- évaluations dans les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb90908c725fcb525e0be1547c27c588a4220c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106517969"
---
# <a name="ratings"></a><span data-ttu-id="11d23-107">Évaluations</span><span class="sxs-lookup"><span data-stu-id="11d23-107">Ratings</span></span>

<span data-ttu-id="11d23-108">Lorsque vous créez une apparence pour le lecteur Windows Media 10,1 mobile, vous pouvez afficher l’évaluation associée au contenu Windows Media Audio en cours de lecture.</span><span class="sxs-lookup"><span data-stu-id="11d23-108">When you create a skin for Windows Media Player 10.1 Mobile, you can display the rating associated with Windows Media Audio-based content that is currently playing.</span></span> <span data-ttu-id="11d23-109">L’évaluation est affichée sous la forme d’une étoile avec un chiffre.</span><span class="sxs-lookup"><span data-stu-id="11d23-109">The rating is displayed as a star with a number on it.</span></span> <span data-ttu-id="11d23-110">L’étoile sera numérotée de 1 à 5, indiquant ainsi l’évaluation actuelle de ce contenu.</span><span class="sxs-lookup"><span data-stu-id="11d23-110">The star will be numbered one through five, denoting the current rating for that content.</span></span> <span data-ttu-id="11d23-111">Si le contenu n’est pas évalué, l’étoile sera numérotée à zéro.</span><span class="sxs-lookup"><span data-stu-id="11d23-111">If the content is not rated, the star will be numbered zero.</span></span>

<span data-ttu-id="11d23-112">La section ratings du fichier de définition d’apparence commence par cette ligne :</span><span class="sxs-lookup"><span data-stu-id="11d23-112">The Ratings section of the skin definition file begins with this line:</span></span>


```C++
[ Ratings ]

```



<span data-ttu-id="11d23-113">Vous devez ensuite ajouter une ligne qui contient des informations sur la taille et l’emplacement de votre icône d’évaluation dans votre apparence.</span><span class="sxs-lookup"><span data-stu-id="11d23-113">You then must add a line that contains information about the size and location of your ratings icon in your skin.</span></span>


```C++
147, 3, 22, 21       ratings96S.gif

```



<span data-ttu-id="11d23-114">Vous pouvez utiliser le modèle suivant pour la section évaluations de votre fichier de définition d’apparence :</span><span class="sxs-lookup"><span data-stu-id="11d23-114">You can use the following template for the Ratings section of your skin definition file:</span></span>


```C++
// <Location>           <Image>
// ---------------      --------------------
```



<span data-ttu-id="11d23-115">Vous pouvez également affecter une valeur de classement à un élément multimédia par le biais de l’interface utilisateur dans le lecteur Windows Media 10,1 mobile, et la prochaine fois que l’appareil se synchronise avec un ordinateur, la nouvelle valeur d’évaluation est propagée à cet élément multimédia s’il réside dans la bibliothèque du lecteur Windows Media 10.</span><span class="sxs-lookup"><span data-stu-id="11d23-115">You can also assign a ratings value to a media item through the user interface in Windows Media Player 10.1 Mobile, and the next time the device synchronizes with the a computer, the new ratings value will be propagated to that media item if it resides in the Windows Media Player 10 library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11d23-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="11d23-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11d23-117">**Référence d’apparence**</span><span class="sxs-lookup"><span data-stu-id="11d23-117">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




