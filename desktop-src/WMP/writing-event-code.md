---
title: Écriture du code d’événement
description: Écriture du code d’événement
ms.assetid: ce29aa81-1db8-4aea-a3bd-86c6b559fff7
keywords:
- Apparences du lecteur Windows Media, écriture de code
- apparences, écrire du code
- événements, écriture de code
- écriture de code pour les habillages, à propos de
- Apparences du lecteur Windows Media, événements
- apparences, événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d994f4ee111795b8fd2b498d26ab65b8bd44dea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029817"
---
# <a name="writing-event-code"></a><span data-ttu-id="6d87b-109">Écriture du code d’événement</span><span class="sxs-lookup"><span data-stu-id="6d87b-109">Writing Event Code</span></span>

<span data-ttu-id="6d87b-110">Les événements sont traités de la même façon que les attributs.</span><span class="sxs-lookup"><span data-stu-id="6d87b-110">Events are treated similarly to attributes.</span></span> <span data-ttu-id="6d87b-111">Vous devez attribuer une valeur à l’événement, et la valeur est le code que vous souhaitez exécuter lorsque l’événement se produit.</span><span class="sxs-lookup"><span data-stu-id="6d87b-111">You must give the event a value, and the value is the code you want to run when the event happens.</span></span> <span data-ttu-id="6d87b-112">Le mot « on » est ajouté au début du nom de l’événement ; par exemple, l’événement Click deviendra **OnClick**.</span><span class="sxs-lookup"><span data-stu-id="6d87b-112">The word "on" is added to the front of the event name; for example, the click event will become **onclick**.</span></span>

<span data-ttu-id="6d87b-113">La valeur de l’événement est entre guillemets doubles et commence par le mot JScript suivi d’un signe deux-points.</span><span class="sxs-lookup"><span data-stu-id="6d87b-113">The event value is in double quotes and starts with the word JScript followed by a colon.</span></span> <span data-ttu-id="6d87b-114">Le code que vous souhaitez exécuter est ensuite suivi d’un point-virgule et des guillemets doubles fermants.</span><span class="sxs-lookup"><span data-stu-id="6d87b-114">The code you want to run comes next, followed by a semicolon and the closing double quotes.</span></span> <span data-ttu-id="6d87b-115">Par exemple, pour arrêter la diffusion quand l’utilisateur clique sur un bouton, tapez la commande suivante en tant qu’attribut dans votre code d’élément de **bouton** :</span><span class="sxs-lookup"><span data-stu-id="6d87b-115">For example, to stop playing when the user clicks on a button, type the following as an attribute in your **BUTTON** element code:</span></span>


```C++
onclick = "JScript: player.Controls.Stop() ; "
```



<span data-ttu-id="6d87b-116">Si vous avez un code qui requiert des guillemets, utilisez des guillemets simples.</span><span class="sxs-lookup"><span data-stu-id="6d87b-116">If you have a code that requires quotes, use single quotes.</span></span> <span data-ttu-id="6d87b-117">Soyez prudent lorsque vous utilisez des guillemets pour qu’ils soient correctement équilibrés.</span><span class="sxs-lookup"><span data-stu-id="6d87b-117">Care must be taken when using quotation marks so that they are balanced properly.</span></span> <span data-ttu-id="6d87b-118">Voici un exemple d’utilisation des deux types :</span><span class="sxs-lookup"><span data-stu-id="6d87b-118">Here is an example of using both types:</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "
```



<span data-ttu-id="6d87b-119">Vous pouvez également modifier les attributs de votre apparence lors du traitement d’un événement externe.</span><span class="sxs-lookup"><span data-stu-id="6d87b-119">You can also change attributes of your skin when handling an external event.</span></span> <span data-ttu-id="6d87b-120">Par exemple, pour fermer une vue nommée myView, vous pouvez taper :</span><span class="sxs-lookup"><span data-stu-id="6d87b-120">For example, to close a view named myView, you could type:</span></span>


```C++
onclick = "JScript: myView.close() ;"
```



## <a name="related-topics"></a><span data-ttu-id="6d87b-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6d87b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d87b-122">**Gestion des événements**</span><span class="sxs-lookup"><span data-stu-id="6d87b-122">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




