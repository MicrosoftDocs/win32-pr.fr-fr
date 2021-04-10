---
title: Structures (RPC)
description: Description de différents types de structures dans l’appel de procédure distante (RPC).
ms.assetid: edaf547d-d3d1-443c-93dd-8e036bc42944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ccae91f703badd2e0153dfc3d8acff1ace562f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031585"
---
# <a name="structures-rpc"></a><span data-ttu-id="32c8d-103">Structures (RPC)</span><span class="sxs-lookup"><span data-stu-id="32c8d-103">Structures (RPC)</span></span>

<span data-ttu-id="32c8d-104">Il existe plusieurs catégories de structures, progressivement plus compliquées en termes d’actions requises pour le marshaling.</span><span class="sxs-lookup"><span data-stu-id="32c8d-104">There are several categories of structures, progressively more complicated in terms of actions required for marshaling.</span></span> <span data-ttu-id="32c8d-105">Ils commencent par une structure simple qui peut être copiée par bloc dans son ensemble et qui continuent à une structure complexe qui doit être un champ de champ par champ.</span><span class="sxs-lookup"><span data-stu-id="32c8d-105">They begin with a simple structure that can be block-copied as a whole, and continue to a complex structure that has to be serviced field by field.</span></span>

-   [<span data-ttu-id="32c8d-106">Structure simple</span><span class="sxs-lookup"><span data-stu-id="32c8d-106">Simple Structure</span></span>](#simple-structure)
-   [<span data-ttu-id="32c8d-107">Structure simple avec pointeurs</span><span class="sxs-lookup"><span data-stu-id="32c8d-107">Simple Structure with Pointers</span></span>](#simple-structure-with-pointers)
-   [<span data-ttu-id="32c8d-108">Structure conforme</span><span class="sxs-lookup"><span data-stu-id="32c8d-108">Conformant Structure</span></span>](#conformant-structure)
-   [<span data-ttu-id="32c8d-109">Structure conforme avec des pointeurs</span><span class="sxs-lookup"><span data-stu-id="32c8d-109">Conformant Structure with Pointers</span></span>](#conformant-structure-with-pointers)
-   [<span data-ttu-id="32c8d-110">Structure variable conforme (avec ou sans pointeurs)</span><span class="sxs-lookup"><span data-stu-id="32c8d-110">Conformant Varying Structure (with or without Pointers)</span></span>](#conformant-varying-structure-with-or-without-pointers)
-   [<span data-ttu-id="32c8d-111">Structure matérielle</span><span class="sxs-lookup"><span data-stu-id="32c8d-111">Hard Structure</span></span>](#hard-structure)
-   [<span data-ttu-id="32c8d-112">Structure complexe</span><span class="sxs-lookup"><span data-stu-id="32c8d-112">Complex Structure</span></span>](#complex-structure)
-   [<span data-ttu-id="32c8d-113">Description de la disposition des membres de la structure</span><span class="sxs-lookup"><span data-stu-id="32c8d-113">Structure Member Layout Description</span></span>](#structure-member-layout-description)

> [!Note]  
> <span data-ttu-id="32c8d-114">En comparaison avec les catégories de tableau, il devient clair que seules les structures jusqu’à 64 Ko peuvent être décrites (la taille est pour la partie plate de la structure), il n’y a pas d’équivalent des tableaux SM et LG.</span><span class="sxs-lookup"><span data-stu-id="32c8d-114">When compared to array categories, it becomes clear that only structures up to 64k in size can be described (the size is for the flat part of the structure), that is there is no equivalent of SM and LG arrays.</span></span>

 

<span data-ttu-id="32c8d-115">**Membres communs aux structures**</span><span class="sxs-lookup"><span data-stu-id="32c8d-115">**Members Common to Structures**</span></span>

-   <span data-ttu-id="32c8d-116">**repère**</span><span class="sxs-lookup"><span data-stu-id="32c8d-116">**alignment**</span></span>

    <span data-ttu-id="32c8d-117">L’alignement nécessaire de la mémoire tampon avant d’unmarshaler la structure.</span><span class="sxs-lookup"><span data-stu-id="32c8d-117">The necessary alignment of the buffer before unmarshaling the structure.</span></span> <span data-ttu-id="32c8d-118">Les valeurs valides sont 0, 1, 3 et 7 (l’alignement réel moins 1).</span><span class="sxs-lookup"><span data-stu-id="32c8d-118">Valid values are 0, 1, 3, and 7 (the actual alignment minus 1).</span></span>

-   <span data-ttu-id="32c8d-119">**taille de la mémoire \_**</span><span class="sxs-lookup"><span data-stu-id="32c8d-119">**memory\_size**</span></span>

    <span data-ttu-id="32c8d-120">Taille de la structure en octets dans la mémoire ; pour les structures conformes, cette taille n’inclut pas la taille du tableau.</span><span class="sxs-lookup"><span data-stu-id="32c8d-120">Size of the structure in memory in bytes; for conformant structures this size does not include the array's size.</span></span>

-   <span data-ttu-id="32c8d-121">**\_Description du décalage par rapport au \_ tableau \_**</span><span class="sxs-lookup"><span data-stu-id="32c8d-121">**offset\_to\_array\_description**</span></span>

    <span data-ttu-id="32c8d-122">Offset du pointeur de chaîne de format actuel vers la description du tableau conforme contenu dans une structure.</span><span class="sxs-lookup"><span data-stu-id="32c8d-122">Offset from the current format string pointer to the description of the conformant array contained in a structure.</span></span>

-   <span data-ttu-id="32c8d-123">**disposition des membres \_**</span><span class="sxs-lookup"><span data-stu-id="32c8d-123">**member\_layout**</span></span>

    <span data-ttu-id="32c8d-124">Description de chaque élément de la structure.</span><span class="sxs-lookup"><span data-stu-id="32c8d-124">Description of each element of the structure.</span></span> <span data-ttu-id="32c8d-125">Les routines de NDR doivent uniquement examiner cette partie de la chaîne de format d’un type si la transformation endian est nécessaire ou si le type est une structure complexe.</span><span class="sxs-lookup"><span data-stu-id="32c8d-125">The NDR routines only need to examine this portion of a type's format string if endian transformation is needed or if the type is a complex structure.</span></span>

-   <span data-ttu-id="32c8d-126">**disposition du pointeur \_**</span><span class="sxs-lookup"><span data-stu-id="32c8d-126">**pointer\_layout**</span></span>

    <span data-ttu-id="32c8d-127">Consultez la section [disposition du pointeur](pointer-layout-tfs.md) .</span><span class="sxs-lookup"><span data-stu-id="32c8d-127">See the [Pointer Layout](pointer-layout-tfs.md) section.</span></span>

## <a name="simple-structure"></a><span data-ttu-id="32c8d-128">Structure simple</span><span class="sxs-lookup"><span data-stu-id="32c8d-128">Simple Structure</span></span>

<span data-ttu-id="32c8d-129">Une structure simple contient uniquement des types de base, des tableaux fixes et d’autres structures simples.</span><span class="sxs-lookup"><span data-stu-id="32c8d-129">A simple structure contains only base types, fixed arrays, and other simple structures.</span></span> <span data-ttu-id="32c8d-130">La principale fonctionnalité de la structure simple est qu’elle peut être copiée par bloc dans son ensemble.</span><span class="sxs-lookup"><span data-stu-id="32c8d-130">The main feature of the simple structure is that it can be block-copied as a whole.</span></span>

``` syntax
FC_STRUCT alignment<1> 
memory_size<2> 
member_layout<> 
FC_END
```

## <a name="simple-structure-with-pointers"></a><span data-ttu-id="32c8d-131">Structure simple avec pointeurs</span><span class="sxs-lookup"><span data-stu-id="32c8d-131">Simple Structure with Pointers</span></span>

<span data-ttu-id="32c8d-132">Une structure simple avec des pointeurs contient uniquement des types de base, des pointeurs, des tableaux fixes, des structures simples et d’autres structures simples avec des pointeurs.</span><span class="sxs-lookup"><span data-stu-id="32c8d-132">A simple structure with pointers contains only base types, pointers, fixed arrays, simple structures, and other simple structures with pointers.</span></span> <span data-ttu-id="32c8d-133">Étant donné que la<> de disposition ne doit être visitée que lors d’une conversion d’un niveau d’enprimautément, elle est placée à la fin de la description.</span><span class="sxs-lookup"><span data-stu-id="32c8d-133">Because the layout<> will only have to be visited when doing an endianess conversion, it is placed at the end of the description.</span></span>

``` syntax
FC_PSTRUCT alignment<1> 
memory_size<2> 
pointer_layout<> 
member_layout<> 
FC_END
```

## <a name="conformant-structure"></a><span data-ttu-id="32c8d-134">Structure conforme</span><span class="sxs-lookup"><span data-stu-id="32c8d-134">Conformant Structure</span></span>

<span data-ttu-id="32c8d-135">Une structure conforme contient uniquement des types de base, des tableaux fixes et des structures simples, et doit contenir une chaîne conforme ou un tableau conforme.</span><span class="sxs-lookup"><span data-stu-id="32c8d-135">A conformant structure contains only base types, fixed arrays, and simple structures, and must contain either a conformant string or a conformant array.</span></span> <span data-ttu-id="32c8d-136">Ce tableau peut en fait être contenu dans une autre structure conforme ou une structure conforme avec des pointeurs qui est incorporé dans cette structure.</span><span class="sxs-lookup"><span data-stu-id="32c8d-136">This array could actually be contained in another conformant structure or conformant structure with pointers which is embedded in this structure.</span></span>

``` syntax
FC_CSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
member_layout<> 
FC_END
```

## <a name="conformant-structure-with-pointers"></a><span data-ttu-id="32c8d-137">Structure conforme avec des pointeurs</span><span class="sxs-lookup"><span data-stu-id="32c8d-137">Conformant Structure with Pointers</span></span>

<span data-ttu-id="32c8d-138">Une structure conforme avec des pointeurs contient uniquement des types de base, des pointeurs, des tableaux fixes, des structures simples et des structures simples avec des pointeurs ; une structure conforme doit contenir un tableau conforme.</span><span class="sxs-lookup"><span data-stu-id="32c8d-138">A conformant structure with pointers contains only base types, pointers, fixed arrays, simple structures, and simple structures with pointers; a conformant structure must contain a conformant array.</span></span> <span data-ttu-id="32c8d-139">Ce tableau peut en fait être contenu dans une autre structure conforme ou une structure conforme avec des pointeurs incorporés dans cette structure.</span><span class="sxs-lookup"><span data-stu-id="32c8d-139">This array could actually be contained in another conformant structure or conformant structure with pointers that is embedded in this structure.</span></span>

``` syntax
FC_CPSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
pointer_layout<> 
member_layout<> FC_END
```

## <a name="conformant-varying-structure-with-or-without-pointers"></a><span data-ttu-id="32c8d-140">Structure variable conforme (avec ou sans pointeurs)</span><span class="sxs-lookup"><span data-stu-id="32c8d-140">Conformant Varying Structure (with or without Pointers)</span></span>

<span data-ttu-id="32c8d-141">Une structure variable conforme contient uniquement des types simples, des pointeurs, des tableaux fixes, des structures simples et des structures simples avec des pointeurs. une structure variable conforme doit contenir soit une chaîne conforme soit un tableau à variation conforme.</span><span class="sxs-lookup"><span data-stu-id="32c8d-141">A conformant varying structure contains only simple types, pointers, fixed arrays, simple structures, and simple structures with pointers; a conformant varying structure must contain either a conformant string or a conformant-varying array.</span></span> <span data-ttu-id="32c8d-142">La chaîne ou le tableau conforme peut en fait être contenu dans une autre structure conforme ou une structure conforme avec des pointeurs incorporés dans cette structure.</span><span class="sxs-lookup"><span data-stu-id="32c8d-142">The conformant string or array can actually be contained in another conformant structure or conformant structure with pointers that is embedded in this structure.</span></span>

``` syntax
FC_CVSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
[pointer_layout<>] 
layout<> 
FC_END
```

## <a name="hard-structure"></a><span data-ttu-id="32c8d-143">Structure matérielle</span><span class="sxs-lookup"><span data-stu-id="32c8d-143">Hard Structure</span></span>

<span data-ttu-id="32c8d-144">La structure matérielle était un concept visant à éliminer des pénalités en matière de traitement de structures complexes.</span><span class="sxs-lookup"><span data-stu-id="32c8d-144">The hard structure was a concept aimed at eliminating steep penalties related to processing complex structures.</span></span> <span data-ttu-id="32c8d-145">Elle est dérivée d’une observation qu’une structure complexe n’a généralement qu’une ou deux conditions qui empêchent la copie de blocs et, par conséquent, de altérer ses performances par rapport à une structure simple.</span><span class="sxs-lookup"><span data-stu-id="32c8d-145">It is derived from an observation that a complex structure typically has only one or two conditions that prevent block-copying, and therefore spoil its performance compared to a simple structure.</span></span> <span data-ttu-id="32c8d-146">Les coupable sont généralement des unions ou des champs d’énumération.</span><span class="sxs-lookup"><span data-stu-id="32c8d-146">The culprits are usually unions or enumeration fields.</span></span>

<span data-ttu-id="32c8d-147">Une structure matérielle est une structure qui a un enum16, un remplissage de fin en mémoire ou une Union comme dernier membre.</span><span class="sxs-lookup"><span data-stu-id="32c8d-147">A hard structure is a structure that has an enum16, end-padding in memory, or a union as the last member.</span></span> <span data-ttu-id="32c8d-148">Ces trois éléments empêchent la structure de tomber dans l’une des catégories de structures précédentes, qui profitent de la surcharge d’interprétation et du potentiel d’optimisation maximal, mais ne la forcent pas à la catégorie de structure complexe la plus coûteuse.</span><span class="sxs-lookup"><span data-stu-id="32c8d-148">These three elements prevent the structure from falling into one of the previous structure categories, which enjoy small interpretation overhead and maximum optimization potential, but do not force it into the very costly complex structure category.</span></span>

<span data-ttu-id="32c8d-149">Le enum16 ne doit pas provoquer la différence entre la mémoire et la taille des câbles de la structure.</span><span class="sxs-lookup"><span data-stu-id="32c8d-149">The enum16 must not cause the memory and wire sizes of the structure to differ.</span></span> <span data-ttu-id="32c8d-150">La structure ne peut pas avoir de tableau conforme, ni de pointeurs (sauf une partie de l’Union); les seuls autres membres autorisés sont les types de base, les tableaux fixes et les structures simples.</span><span class="sxs-lookup"><span data-stu-id="32c8d-150">The structure cannot have any conformant array, nor any pointers (unless part of the union); the only other members allowed are base types, fixed arrays, and simple structures.</span></span>

``` syntax
FC_HARD_STRUCTURE alignment<1> 
memory_size<2> 
reserved<4> 
enum_offset<2> 
copy_size<2> 
mem_copy_incr<2> 
union_description_offset<2>
member_layout<> 
FC_END
```

<span data-ttu-id="32c8d-151">Le champ décalage de l’énumération \_<2> fournit l’offset du début de la structure en mémoire à un enum16 si celui-ci en contient un ; sinon, le \_ décalage enum<2> champ est – 1.</span><span class="sxs-lookup"><span data-stu-id="32c8d-151">The enum\_offset<2> field provides the offset from the beginning of the structure in memory to an enum16 if it contains one; otherwise the enum\_offset<2> field is –1.</span></span>

<span data-ttu-id="32c8d-152">Le \_ champ Taille de copie<2> fournit le nombre total d’octets dans la structure, qui peuvent être copiés par blocs dans/à partir de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="32c8d-152">The copy\_size<2> field provides the total number of bytes in the structure, which may be block-copied into/from the buffer.</span></span> <span data-ttu-id="32c8d-153">Ce total n’inclut pas d’Union de fin ni de remplissage de fin dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="32c8d-153">This total does not include any trailing union nor any end-padding in memory.</span></span> <span data-ttu-id="32c8d-154">Cette valeur est également la quantité que le pointeur de mémoire tampon doit être incrémenté à la suite de la copie.</span><span class="sxs-lookup"><span data-stu-id="32c8d-154">This value is also the amount the buffer pointer should be incremented following the copy.</span></span>

<span data-ttu-id="32c8d-155">Le \_ \_ champ de> de copie de mem<2 est le nombre d’octets que le pointeur de mémoire doit être incrémenté à la suite de la copie de bloc avant toute Union de fin.</span><span class="sxs-lookup"><span data-stu-id="32c8d-155">The mem\_copy\_incr<2> field is the number of bytes the memory pointer should be incremented following the block-copy before handling any trailing union.</span></span> <span data-ttu-id="32c8d-156">L’incrémentation de cette quantité (et non de la taille de copie \_<2 octets>) produit un pointeur de mémoire approprié à toute Union de fin.</span><span class="sxs-lookup"><span data-stu-id="32c8d-156">Incrementing by this amount (not by copy\_size<2> bytes) yields a proper memory pointer to any trailing union.</span></span>

## <a name="complex-structure"></a><span data-ttu-id="32c8d-157">Structure complexe</span><span class="sxs-lookup"><span data-stu-id="32c8d-157">Complex Structure</span></span>

<span data-ttu-id="32c8d-158">Une structure complexe est une structure qui contient un ou plusieurs champs qui empêchent la structure d’être copiée par bloc ou pour lesquels une vérification supplémentaire doit être effectuée pendant le marshaling ou le démarshaling (par exemple, des contrôles liés sur une énumération).</span><span class="sxs-lookup"><span data-stu-id="32c8d-158">A complex structure is any structure containing one or more fields that either prevent the structure from being block-copied, or for which additional checking must be performed during marshaling or unmarshaling (for example, bound checks on an enumeration).</span></span> <span data-ttu-id="32c8d-159">Les types de NDR suivants appartiennent à cette catégorie :</span><span class="sxs-lookup"><span data-stu-id="32c8d-159">The following NDR types fall in this category:</span></span>

-   <span data-ttu-id="32c8d-160">[types simples](simple-types-tfs.md): ENUM16, \_ \_ INT3264 (sur les plateformes 64 bits uniquement), un intégral avec \[ [ **Range**](/windows/desktop/Midl/range)\]</span><span class="sxs-lookup"><span data-stu-id="32c8d-160">[simple types](simple-types-tfs.md): ENUM16, \_\_INT3264 (on 64-bit platforms only), an integral with \[[**range**](/windows/desktop/Midl/range)\]</span></span>
-   <span data-ttu-id="32c8d-161">remplissage de l’alignement à la fin de la structure</span><span class="sxs-lookup"><span data-stu-id="32c8d-161">alignment padding at the end of the structure</span></span>
-   <span data-ttu-id="32c8d-162">pointeurs d’interface (ils utilisent un complexe intégré)</span><span class="sxs-lookup"><span data-stu-id="32c8d-162">interface pointers (they go using an embedded complex)</span></span>
-   <span data-ttu-id="32c8d-163">pointeurs ignorés (associés à l' \[ attribut [**ignore**](/windows/desktop/Midl/ignore) \] et au jeton FC ignoré \_ )</span><span class="sxs-lookup"><span data-stu-id="32c8d-163">ignored pointers (that is related to \[[**ignore**](/windows/desktop/Midl/ignore)\] attribute and FC\_IGNORE token)</span></span>
-   <span data-ttu-id="32c8d-164">tableaux complexes, tableaux variables, tableaux de chaînes</span><span class="sxs-lookup"><span data-stu-id="32c8d-164">complex arrays, varying arrays, string arrays</span></span>
-   <span data-ttu-id="32c8d-165">tableaux conformes multidimensionnels avec au moins une dimension fixe</span><span class="sxs-lookup"><span data-stu-id="32c8d-165">multidimensional conformant arrays with at least one nonfixed dimension</span></span>
-   <span data-ttu-id="32c8d-166">unions</span><span class="sxs-lookup"><span data-stu-id="32c8d-166">unions</span></span>
-   <span data-ttu-id="32c8d-167">éléments définis avec \[ [**transmettre \_ en tant que**](/windows/desktop/Midl/transmit-as) \] , \[ [**représenter \_ comme**](/windows/desktop/Midl/represent-as) \] , \[ [**\_ marshaleur de câble**](/windows/desktop/Midl/wire-marshal) \] , \[ [**\_ Marshal d’utilisateur**](/windows/desktop/Midl/user-marshal)\]</span><span class="sxs-lookup"><span data-stu-id="32c8d-167">elements defined with \[[**transmit\_as**](/windows/desktop/Midl/transmit-as)\], \[[**represent\_as**](/windows/desktop/Midl/represent-as)\], \[[**wire\_marshal**](/windows/desktop/Midl/wire-marshal)\], \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\]</span></span>
-   <span data-ttu-id="32c8d-168">structures complexes incorporées</span><span class="sxs-lookup"><span data-stu-id="32c8d-168">embedded complex structures</span></span>
-   <span data-ttu-id="32c8d-169">remplissage à la fin de la structure</span><span class="sxs-lookup"><span data-stu-id="32c8d-169">padding at the end of the structure</span></span>

<span data-ttu-id="32c8d-170">Une structure complexe a la description de format suivante :</span><span class="sxs-lookup"><span data-stu-id="32c8d-170">A complex structure has the following format description:</span></span>

``` syntax
FC_BOGUS_STRUCT alignment<1> 
memory_size<2> 
offset_to_conformant_array_description<2> 
offset_to_pointer_layout<2> 
member_layout<> 
FC_END 
[pointer_layout<>]
```

<span data-ttu-id="32c8d-171">La \_ taille de la mémoire<2> champ est la taille de la structure en mémoire, en octets.</span><span class="sxs-lookup"><span data-stu-id="32c8d-171">The memory\_size<2> field is the size of the structure in memory, in bytes.</span></span>

<span data-ttu-id="32c8d-172">Si la structure contient un tableau conforme, le \_ champ offset to \_ conformed \_ array \_ Description<2> champ fournit le décalage à la description du tableau conforme, sinon il est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="32c8d-172">If the structure contains a conformant array, the offset\_to\_conformant\_array\_description<2> field provides the offset to the conformant array's description, otherwise it is zero.</span></span>

<span data-ttu-id="32c8d-173">Si la structure a des pointeurs, le décalage \_ vers la \_ disposition du pointeur \_<2> champ fournit le décalage au-delà de la disposition de la structure jusqu’à la disposition du pointeur, sinon ce champ est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="32c8d-173">If the structure has pointers, the offset\_to\_pointer\_layout<2> field provides the offset past the structure's layout to the pointer layout, otherwise this field is zero.</span></span>

<span data-ttu-id="32c8d-174">La disposition du pointeur \_<> champ d’une structure complexe est gérée de façon légèrement différente de celle des autres structures.</span><span class="sxs-lookup"><span data-stu-id="32c8d-174">The pointer\_layout<> field of a complex structure is handled somewhat differently than for other structures.</span></span> <span data-ttu-id="32c8d-175">La disposition du pointeur \_<> champ d’une structure complexe contient uniquement les descriptions des champs de pointeur réels de la structure elle-même.</span><span class="sxs-lookup"><span data-stu-id="32c8d-175">The pointer\_layout<> field of a complex structure only contains descriptions of actual pointer fields in the structure itself.</span></span> <span data-ttu-id="32c8d-176">Tous les pointeurs contenus dans des tableaux, unions ou structures incorporés ne sont pas décrits dans le champ disposition du pointeur de la structure complexe \_<> .</span><span class="sxs-lookup"><span data-stu-id="32c8d-176">Any pointers contained within any embedded arrays, unions, or structures are not described in the complex structure's pointer\_layout<> field.</span></span>

> [!Note]  
> <span data-ttu-id="32c8d-177">Cela s’oppose à d’autres structures, qui dupliquent la description de tous les pointeurs contenus dans les tableaux ou les structures incorporés dans leur propre disposition de pointeur \_<> champ également.</span><span class="sxs-lookup"><span data-stu-id="32c8d-177">This is in contrast to other structures, which duplicate the description of any pointers contained in embedded arrays or structures in their own pointer \_layout<> field as well.</span></span>

 

<span data-ttu-id="32c8d-178">Le format de la disposition du pointeur d’une structure complexe est également radicalement différent.</span><span class="sxs-lookup"><span data-stu-id="32c8d-178">The format of a complex structure's pointer layout is also radically different.</span></span> <span data-ttu-id="32c8d-179">Étant donné qu’il contient uniquement des descriptions des membres de pointeur réels et qu’une structure complexe est marshalée et démarshalée un champ à la fois, le champ de disposition du pointeur \_<> contient simplement la description du pointeur de tous les membres du pointeur.</span><span class="sxs-lookup"><span data-stu-id="32c8d-179">Because it only contains descriptions of actual pointer members and because a complex structure is marshaled and unmarshaled one field at a time, the pointer\_layout<> field simply contains the pointer description of all pointer members.</span></span> <span data-ttu-id="32c8d-180">Il n’y a pas \_ de point de départ pour le premier plan et aucune des informations de disposition du pointeur habituelle n' \_<> .</span><span class="sxs-lookup"><span data-stu-id="32c8d-180">There is no beginning FC\_PP, and none of the usual pointer\_layout<> information.</span></span>

## <a name="structure-member-layout-description"></a><span data-ttu-id="32c8d-181">Description de la disposition des membres de la structure</span><span class="sxs-lookup"><span data-stu-id="32c8d-181">Structure Member Layout Description</span></span>

<span data-ttu-id="32c8d-182">La description de la disposition d’une structure contient un ou plusieurs des caractères de format suivants :</span><span class="sxs-lookup"><span data-stu-id="32c8d-182">A structure's layout description contains one or more of the following format characters:</span></span>

-   <span data-ttu-id="32c8d-183">N’importe quel caractère de type de base, comme FC \_ Char, etc.</span><span class="sxs-lookup"><span data-stu-id="32c8d-183">Any of the base type characters, like FC\_CHAR, and so on</span></span>
-   <span data-ttu-id="32c8d-184">Directives d’alignement.</span><span class="sxs-lookup"><span data-stu-id="32c8d-184">Alignment directives.</span></span> <span data-ttu-id="32c8d-185">Trois caractères de format spécifient l’alignement du pointeur de mémoire : FC \_ ALIGNM2, FC \_ ALIGNM4 et FC \_ ALIGNM8.</span><span class="sxs-lookup"><span data-stu-id="32c8d-185">There are three format characters specifying alignment of the memory pointer: FC\_ALIGNM2, FC\_ALIGNM4, and FC\_ALIGNM8.</span></span>
    > [!Note]  
    > <span data-ttu-id="32c8d-186">Il existe également des jetons d’alignement de la mémoire tampon, FC \_ ALIGNB2 via FC \_ ALIGNM8 ; ceux-ci ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="32c8d-186">There are also buffer alignment tokens, FC\_ALIGNB2 through FC\_ALIGNM8; these are not used.</span></span>

     

-   <span data-ttu-id="32c8d-187">Remplissage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="32c8d-187">Memory padding.</span></span> <span data-ttu-id="32c8d-188">Elles se produisent uniquement à la fin de la description d’une structure et désignent le nombre d’octets de remplissage dans la mémoire avant le tableau conforme dans la structure : FC \_ STRUCTPADn, où n est le nombre d’octets de remplissage.</span><span class="sxs-lookup"><span data-stu-id="32c8d-188">These occur only at the end of a structure's description and denote the number of bytes of padding in memory before the conformant array in the structure: FC\_STRUCTPADn, where n is the number of bytes of padding.</span></span>
-   <span data-ttu-id="32c8d-189">Tout type non de base incorporé (Notez, toutefois, qu’un tableau conforme ne se produit jamais dans la disposition de la structure).</span><span class="sxs-lookup"><span data-stu-id="32c8d-189">Any embedded nonbase type (note, however, that a conformant array never occurs in the structure layout).</span></span> <span data-ttu-id="32c8d-190">Il comporte une description de 4 octets :</span><span class="sxs-lookup"><span data-stu-id="32c8d-190">This has a 4-byte description:</span></span>

    ``` syntax
    FC_EMBEDDED_COMPLEX memory_pad<1> 
    offset_to_description<2>,
    ```

    <span data-ttu-id="32c8d-191">où l’alignement sur deux octets n’est pas garanti pour l’offset.</span><span class="sxs-lookup"><span data-stu-id="32c8d-191">where the offset is not guaranteed to be 2-byte aligned.</span></span>

    <span data-ttu-id="32c8d-192">\_le bloc de mémoire<1> est un remplissage requis en mémoire avant le champ complexe.</span><span class="sxs-lookup"><span data-stu-id="32c8d-192">memory\_pad<1> is a padding needed in memory before the complex field.</span></span>

    <span data-ttu-id="32c8d-193">décalage \_ vers \_ la description<2> est un décalage de type relatif par rapport au type incorporé.</span><span class="sxs-lookup"><span data-stu-id="32c8d-193">offset\_to\_description<2> is a relative type offset to the embedded type.</span></span>

<span data-ttu-id="32c8d-194">Il peut également y avoir un \_ tampon FC avant l’arrêt de la solution FC, \_ si nécessaire, pour s’assurer que la chaîne de format sera alignée sur une limite de 2 octets à la suite de l' \_ extrémité FC.</span><span class="sxs-lookup"><span data-stu-id="32c8d-194">There may also be an FC\_PAD before the terminating FC\_END if needed to ensure that the format string will be aligned at a 2-byte boundary following the FC\_END.</span></span>

 

 