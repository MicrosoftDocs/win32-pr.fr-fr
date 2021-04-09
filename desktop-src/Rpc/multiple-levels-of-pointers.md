---
title: Plusieurs niveaux de pointeurs
description: Utilisation de plusieurs niveaux de pointeurs dans l’appel de procédure distante (RPC).
ms.assetid: d45b9b20-3b21-4d46-9097-8aacb4e4e921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61a917ee29c982505c601d7b0dd0721e94e4678
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941208"
---
# <a name="multiple-levels-of-pointers"></a><span data-ttu-id="79062-103">Plusieurs niveaux de pointeurs</span><span class="sxs-lookup"><span data-stu-id="79062-103">Multiple Levels of Pointers</span></span>

<span data-ttu-id="79062-104">Lorsqu’il existe plusieurs niveaux de pointeurs, les attributs sont associés au pointeur le plus proche du nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="79062-104">When there are multiple levels of pointers, the attributes are associated with the pointer closest to the variable name.</span></span> <span data-ttu-id="79062-105">Le client est toujours responsable de l’allocation de toute mémoire associée à la réponse.</span><span class="sxs-lookup"><span data-stu-id="79062-105">The client is still responsible for allocating any memory associated with the response.</span></span>

<span data-ttu-id="79062-106">L’exemple suivant permet au stub d’appeler le serveur sans savoir à l’avance la quantité de données qui seront retournées :</span><span class="sxs-lookup"><span data-stu-id="79062-106">The following example allows the stub to call the server without knowing in advance how much data will be returned:</span></span>

``` syntax
[
    uuid( ...),
    version(3.3),
]
interface AnInterface
{
    HRESULT GetBars([out] long * pSize,
             [out, size_is( , *pSize)]
             BAR ** ppBar);//BAR type defined elsewhere
}
```

<span data-ttu-id="79062-107">Dans cet exemple, le stub transmet au serveur un pointeur unique, que le serveur Initialise à la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="79062-107">In this example, the stub passes the server a unique pointer, which the server initializes to **NULL**.</span></span> <span data-ttu-id="79062-108">Le serveur alloue ensuite un bloc de barres, définit le pointeur, définit l’argument de taille et retourne.</span><span class="sxs-lookup"><span data-stu-id="79062-108">The server then allocates a block of BARs, sets the pointer, sets the size argument and returns.</span></span> <span data-ttu-id="79062-109">Notez que, pour que le serveur ait un effet sur l’appelant, vous devez passer un \[ \] pointeur Ref à un \[ [](/windows/desktop/Midl/unique) \] pointeur unique vers vos données.</span><span class="sxs-lookup"><span data-stu-id="79062-109">Note that in order for the server to have an effect on the caller you must pass a \[ref\] pointer to a \[[**unique**](/windows/desktop/Midl/unique)\] pointer to your data.</span></span> <span data-ttu-id="79062-110">Notez également que la taille de la virgule \[ [**\_ est**](/windows/desktop/Midl/size-is)(, \* psize), ce qui \] indique que le pointeur de niveau supérieur n’est pas un pointeur de taille, mais que le pointeur de niveau inférieur est.</span><span class="sxs-lookup"><span data-stu-id="79062-110">Also note the comma in \[[**size\_is**](/windows/desktop/Midl/size-is)( , \*pSize )\], which indicates that the top-level pointer is not a sized pointer, but that the lower-level pointer is.</span></span>

<span data-ttu-id="79062-111">Côté client, le stub affecte la \* **valeur null** à ppBar avant d’appeler la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="79062-111">On the client side, the stub sets \*ppBar to **NULL** before calling the remote procedure.</span></span> <span data-ttu-id="79062-112">Le stub alloue ensuite et démarshale le tableau en d’objets de la barre.</span><span class="sxs-lookup"><span data-stu-id="79062-112">The stub then allocates and unmarshals the arry of BAR objects.</span></span> <span data-ttu-id="79062-113">L’argument Size indique la taille du bloc (et le nombre de barres non marshalées).</span><span class="sxs-lookup"><span data-stu-id="79062-113">The size argument indicates the size of the block (and the number of unmarshaled BARs).</span></span> <span data-ttu-id="79062-114">Le client doit libérer le tableau retourné d’objets de barre lorsqu’il n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="79062-114">The client must free the returned array of BAR objects when it is no longer required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79062-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="79062-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79062-116">**la taille \_ est**</span><span class="sxs-lookup"><span data-stu-id="79062-116">**size\_is**</span></span>](/windows/desktop/Midl/size-is)
</dt> </dl>

 

 