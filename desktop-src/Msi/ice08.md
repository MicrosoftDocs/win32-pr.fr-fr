---
description: ICE08 vérifie que la table des composants ne contient pas de GUID en double. Chaque composant doit avoir un GUID unique. Aucune validation n’est effectuée si la table de composants n’existe pas.
ms.assetid: c8ff53f3-6587-479d-afb8-b09d0df3b673
title: ICE08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051f32aa983fdae39fc3717d3c9036b542f14369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520010"
---
# <a name="ice08"></a><span data-ttu-id="097a8-105">ICE08</span><span class="sxs-lookup"><span data-stu-id="097a8-105">ICE08</span></span>

<span data-ttu-id="097a8-106">ICE08 vérifie que la [table des composants](component-table.md) ne contient pas de [GUID](guid.md)en double.</span><span class="sxs-lookup"><span data-stu-id="097a8-106">ICE08 validates that the [Component table](component-table.md) contains no duplicate [GUIDs](guid.md).</span></span> <span data-ttu-id="097a8-107">Chaque composant doit avoir un GUID unique.</span><span class="sxs-lookup"><span data-stu-id="097a8-107">Every component must have a unique GUID.</span></span> <span data-ttu-id="097a8-108">Aucune validation n’est effectuée si la table de composants n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="097a8-108">No validation is done if the Component table does not exist.</span></span>

## <a name="result"></a><span data-ttu-id="097a8-109">Résultats</span><span class="sxs-lookup"><span data-stu-id="097a8-109">Result</span></span>

<span data-ttu-id="097a8-110">ICE08 publie un message d’erreur si au moins deux entrées de la colonne ComponentId de la table des composants contiennent le même GUID.</span><span class="sxs-lookup"><span data-stu-id="097a8-110">ICE08 posts an error message if two or more entries in the ComponentId column of the Component table contain the same GUID.</span></span>

## <a name="example"></a><span data-ttu-id="097a8-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="097a8-111">Example</span></span>

<span data-ttu-id="097a8-112">Dans l’exemple suivant, ICE08 publie un message indiquant que les composants Red et Green comportent des GUID en double.</span><span class="sxs-lookup"><span data-stu-id="097a8-112">For the following example, ICE08 would post a message stating that components Red and Green have duplicate GUIDs.</span></span>

<span data-ttu-id="097a8-113">[Table des composants](component-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="097a8-113">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="097a8-114">Composant</span><span class="sxs-lookup"><span data-stu-id="097a8-114">Component</span></span> | <span data-ttu-id="097a8-115">ComponentId</span><span class="sxs-lookup"><span data-stu-id="097a8-115">ComponentId</span></span>                            |
|-----------|----------------------------------------|
| <span data-ttu-id="097a8-116">Rouge</span><span class="sxs-lookup"><span data-stu-id="097a8-116">Red</span></span>       | <span data-ttu-id="097a8-117">{0000000A-0003-0000-0000-624474736554}</span><span class="sxs-lookup"><span data-stu-id="097a8-117">{0000000A-0003-0000-0000-624474736554}</span></span> |
| <span data-ttu-id="097a8-118">Bleu</span><span class="sxs-lookup"><span data-stu-id="097a8-118">Blue</span></span>      | <span data-ttu-id="097a8-119">{0000000A-0003-0000-0000-624474736354}</span><span class="sxs-lookup"><span data-stu-id="097a8-119">{0000000A-0003-0000-0000-624474736354}</span></span> |
| <span data-ttu-id="097a8-120">Vert</span><span class="sxs-lookup"><span data-stu-id="097a8-120">Green</span></span>     | <span data-ttu-id="097a8-121">{0000000A-0003-0000-0000-624474736554}</span><span class="sxs-lookup"><span data-stu-id="097a8-121">{0000000A-0003-0000-0000-624474736554}</span></span> |



 

<span data-ttu-id="097a8-122">Pour corriger cette erreur, modifiez l’un des GUID dupliqués.</span><span class="sxs-lookup"><span data-stu-id="097a8-122">To fix this error, change either of the duplicate GUIDs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="097a8-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="097a8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="097a8-124">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="097a8-124">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



