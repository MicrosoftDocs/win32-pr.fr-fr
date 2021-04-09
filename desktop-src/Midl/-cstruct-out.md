---
title: commutateur/cstruct_out
description: Le commutateur/cstruct_out modifie la définition C d’une interface COM qui retourne des structures pour qu’elles correspondent à l’ABI qu’un implémenteur C++ peut fournir.
keywords:
- /commutateur cstruct_out MIDL
topic_type:
- apiref
api_name:
- /cstruct_out
api_type:
- NA
ms.topic: reference
ms.date: 12/10/2020
ms.openlocfilehash: 535e1630046b424493e2211c29248c18bf1ed798
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844506"
---
# <a name="cstruct_out-switch"></a><span data-ttu-id="9931d-104">\_commutateur/cstruct out</span><span class="sxs-lookup"><span data-stu-id="9931d-104">/cstruct\_out switch</span></span>

<span data-ttu-id="9931d-105">Ce commutateur modifie la définition C d’une interface COM qui retourne des structures correspondant à l’ABI qu’un implémenteur C++ peut fournir.</span><span class="sxs-lookup"><span data-stu-id="9931d-105">This switch modifies the C definition of a COM interface which returns structures to match the ABI a C++ implementer would provide.</span></span>

``` syntax
midl /cstruct_out
```

## <a name="switch-options"></a><span data-ttu-id="9931d-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="9931d-106">Switch Options</span></span>

<span data-ttu-id="9931d-107">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9931d-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="9931d-108">Notes</span><span class="sxs-lookup"><span data-stu-id="9931d-108">Remarks</span></span>

<span data-ttu-id="9931d-109">Certaines définitions d’interface (notamment celles de `d3d12.idl` ) contiennent des `__stdcall` méthodes qui retournent des structures.</span><span class="sxs-lookup"><span data-stu-id="9931d-109">Some interface definitions (notably those in `d3d12.idl`) contain `__stdcall` methods that return structures.</span></span> <span data-ttu-id="9931d-110">Les Abi C et C++ de MSVC diffèrent dans la manière dont ils implémentent les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="9931d-110">The C and C++ ABIs from MSVC differ in how they implement such functions:</span></span>

* <span data-ttu-id="9931d-111">C les traite comme des fonctions brutes qui prennent un `this` pointeur masqué comme premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="9931d-111">C treats them as plain functions that take a hidden `this` pointer as the first parameter.</span></span> <span data-ttu-id="9931d-112">Le compilateur applique une petite optimisation de struct qui autorise les structs inférieurs à 8 octets (ou plus si toutes les valeurs sont à virgule flottante) d’être retournés dans les registres.</span><span class="sxs-lookup"><span data-stu-id="9931d-112">The complier applies a small struct optimization that allows structs smaller than 8 bytes (or larger if all values are floating point) to be returned in registers.</span></span> <span data-ttu-id="9931d-113">Seules les structures plus grandes sont promues pour utiliser un paramètre masqué et une valeur de retour allouée par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="9931d-113">Only larger structures are promoted to use a hidden parameter and caller-allocated return value.</span></span>
* <span data-ttu-id="9931d-114">C++ les traite comme des fonctions membres.</span><span class="sxs-lookup"><span data-stu-id="9931d-114">C++ treats them as member functions.</span></span> <span data-ttu-id="9931d-115">Le compilateur effectue *toujours* cela en insérant un paramètre masqué (pointeur vers une valeur de retour allouée par l’appelant) en tant que deuxième paramètre, après le `this` pointeur.</span><span class="sxs-lookup"><span data-stu-id="9931d-115">The compiler *always* does so by inserting a hidden parameter (a pointer to a caller-allocated return value) as the second parameter, after the `this` pointer.</span></span> <span data-ttu-id="9931d-116">Elle retourne également le même pointeur que sa valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="9931d-116">It also returns that same pointer as its return value.</span></span>

<span data-ttu-id="9931d-117">Ce commutateur force la définition C des interfaces dans l’en-tête résultant à supposer que l’implémenteur utilisait C++ et que le code C doit utiliser à la place explicitement l’ABI C++.</span><span class="sxs-lookup"><span data-stu-id="9931d-117">This switch forces the C definition of interfaces in the resulting header to assume that the implementer was using C++, and that the C code should instead explicitly use the C++ ABI.</span></span> <span data-ttu-id="9931d-118">Cela implique que la fonction inclue un paramètre masqué pour le pointeur de valeur de retour et retourne ce pointeur au lieu de la structure directement.</span><span class="sxs-lookup"><span data-stu-id="9931d-118">This implies that the function includes a hidden parameter for the return value pointer and returns that pointer instead of the structure directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="9931d-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9931d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9931d-120">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="9931d-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>
