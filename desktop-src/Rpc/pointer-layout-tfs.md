---
title: Disposition du pointeur
description: La disposition du pointeur décrit les pointeurs d’une structure ou d’un tableau.
ms.assetid: 1a4984c1-97b9-4e95-a17e-851b67fa94a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a6639b0c4b56c911be1e688995aaf3fb9d2d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840522"
---
# <a name="pointer-layout"></a><span data-ttu-id="319ce-103">Disposition du pointeur</span><span class="sxs-lookup"><span data-stu-id="319ce-103">Pointer Layout</span></span>

<span data-ttu-id="319ce-104">La disposition du pointeur décrit les pointeurs d’une structure ou d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="319ce-104">Pointer layout describes pointers of a structure or an array.</span></span>

## <a name="pointer_layout"></a><span data-ttu-id="319ce-105">disposition du pointeur \_<></span><span class="sxs-lookup"><span data-stu-id="319ce-105">pointer\_layout<></span></span>

<span data-ttu-id="319ce-106">Une disposition de pointeur \_<> champ se compose du bloc de format caractères FC \_ pp FC \_ suivi d’une ou de plusieurs descriptions de pointeur, comme décrit ultérieurement, et se terminant par un \_ caractère de format de fin FC :</span><span class="sxs-lookup"><span data-stu-id="319ce-106">A pointer\_layout<> field consists of the format characters FC\_PP FC\_PAD followed by one or more pointer descriptions, as described later, and terminating with an FC\_END format character:</span></span>

``` syntax
FC_PP
FC_PAD
{ pointer_instance_layout<> }*
FC_END
```

<span data-ttu-id="319ce-107">Une \_ \_ disposition d’instance de pointeur<> champ est une chaîne de format décrivant une ou plusieurs instances de pointeurs.</span><span class="sxs-lookup"><span data-stu-id="319ce-107">A pointer\_instance\_layout<> field is a format string describing single or multiple instances of pointers.</span></span> <span data-ttu-id="319ce-108">Les champs suivants sont utilisés dans ces descripteurs :</span><span class="sxs-lookup"><span data-stu-id="319ce-108">The following fields are used in these descriptors:</span></span>

-   <span data-ttu-id="319ce-109">décalage \_ en \_ mémoire</span><span class="sxs-lookup"><span data-stu-id="319ce-109">offset\_in\_memory</span></span>

    <span data-ttu-id="319ce-110">Décalage signé à l’emplacement du pointeur en mémoire.</span><span class="sxs-lookup"><span data-stu-id="319ce-110">The signed offset to the pointer's location in memory.</span></span> <span data-ttu-id="319ce-111">Pour un pointeur résidant dans une structure, cet offset est un décalage négatif par rapport à la fin de la structure (la fin de la partie non conforme des structures conformes); pour les tableaux, l’offset est à partir du début du tableau.</span><span class="sxs-lookup"><span data-stu-id="319ce-111">For a pointer residing in a structure, this offset is a negative offset from the end of the structure (the end of the nonconformant portion of conformant structures); for arrays, the offset is from the beginning of the array.</span></span>

-   <span data-ttu-id="319ce-112">décalage \_ dans la \_ mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="319ce-112">offset\_in\_buffer</span></span>

    <span data-ttu-id="319ce-113">Offset signé à l’emplacement du pointeur dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="319ce-113">The signed offset to the pointer's location in the buffer.</span></span> <span data-ttu-id="319ce-114">Pour un pointeur résidant dans une structure, cet offset est un décalage négatif à partir de la fin de la structure (la fin de la partie non conforme des structures conformes) : pour les tableaux, l’offset est à partir du début du tableau.</span><span class="sxs-lookup"><span data-stu-id="319ce-114">For a pointer residing in a structure, this offset is a negative offset from the end of the structure (the end of the nonconformant portion of conformant structures): for arrays, the offset is from the beginning of the array.</span></span>

-   <span data-ttu-id="319ce-115">décalage \_ vers le \_ tableau</span><span class="sxs-lookup"><span data-stu-id="319ce-115">offset\_to\_array</span></span>

    <span data-ttu-id="319ce-116">Offset d’une structure englobante vers le tableau incorporé dont les pointeurs sont gérés.</span><span class="sxs-lookup"><span data-stu-id="319ce-116">Offset from an enclosing structure to the embedded array whose pointers are being handled.</span></span> <span data-ttu-id="319ce-117">Pour les tableaux de niveau supérieur, ce champ sera toujours égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="319ce-117">For top-level arrays, this field will always be zero.</span></span>

-   <span data-ttu-id="319ce-118">itérations</span><span class="sxs-lookup"><span data-stu-id="319ce-118">iterations</span></span>

    <span data-ttu-id="319ce-119">Nombre total de pointeurs ayant la même disposition<> décrit.</span><span class="sxs-lookup"><span data-stu-id="319ce-119">Total number of pointers that have the same layout<> described.</span></span>

-   <span data-ttu-id="319ce-120">incrément</span><span class="sxs-lookup"><span data-stu-id="319ce-120">increment</span></span>

    <span data-ttu-id="319ce-121">Incrémentation entre les pointeurs successifs pendant une répétition.</span><span class="sxs-lookup"><span data-stu-id="319ce-121">Increment between successive pointers during a REPEAT.</span></span>

-   <span data-ttu-id="319ce-122">nombre \_ de \_ pointeurs</span><span class="sxs-lookup"><span data-stu-id="319ce-122">number\_of\_pointers</span></span>

    <span data-ttu-id="319ce-123">Nombre de pointeurs différents dans une instance de répétition.</span><span class="sxs-lookup"><span data-stu-id="319ce-123">Number of different pointers in a repeat instance.</span></span>

-   <span data-ttu-id="319ce-124">Description du pointeur \_</span><span class="sxs-lookup"><span data-stu-id="319ce-124">pointer\_description</span></span>

    <span data-ttu-id="319ce-125">Description du pointeur.</span><span class="sxs-lookup"><span data-stu-id="319ce-125">Pointer description.</span></span>

<span data-ttu-id="319ce-126">Toutes les dispositions d’instance de pointeur utilisent l’instance de pointeur unique suivante \_<8> :</span><span class="sxs-lookup"><span data-stu-id="319ce-126">All pointer instance layouts use the following single pointer\_instance<8>:</span></span>

``` syntax
offset_to_pointer_in_memory<2> 
offset_to_pointer_in_buffer<2> 
pointer_description<4>
```

<span data-ttu-id="319ce-127">Voici les descripteurs d’instance :</span><span class="sxs-lookup"><span data-stu-id="319ce-127">The following are instance descriptors:</span></span>

<span data-ttu-id="319ce-128">**Instance unique d’un pointeur vers un type simple :**</span><span class="sxs-lookup"><span data-stu-id="319ce-128">**Single instance of a pointer to a simple type:**</span></span>

``` syntax
FC_NO_REPEAT FC_PAD 
pointer_instance<8>
```

<span data-ttu-id="319ce-129">**Pointeur de répétition fixe :**</span><span class="sxs-lookup"><span data-stu-id="319ce-129">**Fixed repeat pointer:**</span></span>

``` syntax
FC_FIXED_REPEAT FC_PAD 
iterations<2> 
increment<2> 
offset_to_array<2> 
number_of_pointers<2>
{ pointer_instance<8> }*
```

<span data-ttu-id="319ce-130">**Pointeur de répétition de variable :**</span><span class="sxs-lookup"><span data-stu-id="319ce-130">**Variable repeat pointer:**</span></span>

``` syntax
FC_VARIABLE_REPEAT (FC_FIXED_OFFSET | FC_VARIABLE_OFFSET) 
increment<2> 
offset_to_array<2> 
number_of_pointers<2> 
{ pointer_instance<8> }*
```

<span data-ttu-id="319ce-131">Pour les instances de pointeurs REPEAT et variable à répétition fixe, il existe un ensemble de descriptions de décalage et de pointeur pour chaque pointeur de l’instance de répétition.</span><span class="sxs-lookup"><span data-stu-id="319ce-131">For fixed repeat and variable repeat pointer instances there is a set of offset and pointer descriptions for each pointer in the repeat instance.</span></span>

## <a name="pointers-layout-design-issues"></a><span data-ttu-id="319ce-132">Problèmes de conception de la disposition des pointeurs</span><span class="sxs-lookup"><span data-stu-id="319ce-132">Pointers Layout Design Issues</span></span>

<span data-ttu-id="319ce-133">Cette section traite des problèmes liés au traitement des structures conformes et des pointeurs incorporés.</span><span class="sxs-lookup"><span data-stu-id="319ce-133">This section addresses issues related to processing conformant structures and embedded pointers.</span></span> <span data-ttu-id="319ce-134">Le problème est que le compilateur génère des dispositions de pointeur pour les structures et les tableaux avec une certaine redondance.</span><span class="sxs-lookup"><span data-stu-id="319ce-134">The issue is that the compiler generates pointer layouts for structures and arrays with some redundancy.</span></span> <span data-ttu-id="319ce-135">Cela est avantageux, car les informations sont utiles et, par exemple, une structure conforme peut parcourir une disposition de pointeur pour traiter tous les pointeurs de la structure et du tableau conforme faisant partie de la structure conforme.</span><span class="sxs-lookup"><span data-stu-id="319ce-135">This is beneficial, because the information is useful and as such, for example, a conformant structure can walk one pointer layout to service all the pointers from the structure and from the conformant array being part of the conformant structure.</span></span> <span data-ttu-id="319ce-136">Toutefois, il existe certaines situations incorporées qui nécessitent que le moteur de NDR effectue des tâches supplémentaires pour traiter toutes les dispositions de pointeur dans l’ordre approprié, en traitant chaque pointeur exactement une fois.</span><span class="sxs-lookup"><span data-stu-id="319ce-136">However, some embedded situations exist that require the NDR engine to perform additional work to process all the pointer layouts in the proper sequence, processing each pointer exactly once.</span></span>

## <a name="what-the-compiler-generates"></a><span data-ttu-id="319ce-137">Ce que le compilateur génère</span><span class="sxs-lookup"><span data-stu-id="319ce-137">What the Compiler Generates</span></span>

<span data-ttu-id="319ce-138">Chaque objet abordé dans cette section a des pointeurs. par exemple, une structure conforme a des pointeurs dans la partie structure et dans les éléments du tableau.</span><span class="sxs-lookup"><span data-stu-id="319ce-138">Every object discussed in this section has pointers, so for example, a conformant structure has pointers in the structure part as well as in the array elements.</span></span> <span data-ttu-id="319ce-139">L’élément est une structure simple avec un pointeur.</span><span class="sxs-lookup"><span data-stu-id="319ce-139">The element is a simple structure with a pointer.</span></span>

1.  <span data-ttu-id="319ce-140">Structure conforme, niveau unique</span><span class="sxs-lookup"><span data-stu-id="319ce-140">Conformant structure, single level</span></span>

    <span data-ttu-id="319ce-141">Le descripteur conforme a une partie PP dans laquelle tous les pointeurs sont décrits, à la fois à partir de la structure et à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="319ce-141">The conformant descriptor has a PP part where all the pointers are described, both from the structure and from the array.</span></span> <span data-ttu-id="319ce-142">La liste des membres a \_ une valeur FC à la place d’un pointeur.</span><span class="sxs-lookup"><span data-stu-id="319ce-142">The member list has FC\_LONG in lieu of a pointer.</span></span> <span data-ttu-id="319ce-143">Le descripteur de tableau CARRAY possède des éléments via l’utilisation d’un complexe incorporé \_ et aucun descripteur de pointeur.</span><span class="sxs-lookup"><span data-stu-id="319ce-143">The CARRAY array descriptor has elements through the use of an embedded\_complex and no pointer descriptors at all.</span></span> <span data-ttu-id="319ce-144">L’élément a toujours son descripteur de pointeur unique.</span><span class="sxs-lookup"><span data-stu-id="319ce-144">The element still has its single pointer descriptor.</span></span> <span data-ttu-id="319ce-145">La disposition du pointeur précède la disposition des membres dans une structure conforme et des descripteurs de structure simples.</span><span class="sxs-lookup"><span data-stu-id="319ce-145">Pointer layout precedes the member layout in a conformant structure and simple structure descriptors.</span></span>

2.  <span data-ttu-id="319ce-146">Structure conforme, deux niveaux ou plus</span><span class="sxs-lookup"><span data-stu-id="319ce-146">Conformant structure, two or more levels</span></span>

    <span data-ttu-id="319ce-147">La description PP a des pointeurs de tous les niveaux.</span><span class="sxs-lookup"><span data-stu-id="319ce-147">The PP description has pointers from all levels.</span></span> <span data-ttu-id="319ce-148">Elle réutilise la même description de tableau que la structure conforme interne.</span><span class="sxs-lookup"><span data-stu-id="319ce-148">It reuses the same array description as the internal conformant structure.</span></span> <span data-ttu-id="319ce-149">La liste des membres a \_ une valeur FC à la place d’un pointeur.</span><span class="sxs-lookup"><span data-stu-id="319ce-149">The member list has FC\_LONG in lieu of a pointer.</span></span> <span data-ttu-id="319ce-150">Une structure incorporée est utilisée à l’aide d’un complexe incorporé.</span><span class="sxs-lookup"><span data-stu-id="319ce-150">An embedded structure comes through the use of an embedded complex.</span></span> <span data-ttu-id="319ce-151">Le descripteur de structure conforme est réutilisé tel quel.</span><span class="sxs-lookup"><span data-stu-id="319ce-151">The conformant structure descriptor is reused as-is.</span></span> <span data-ttu-id="319ce-152">La taille de la partie plate de la structure est également terminée, ce qui signifie que la taille de la structure de niveau supérieur inclut la taille plate de la structure incorporée.</span><span class="sxs-lookup"><span data-stu-id="319ce-152">The size of the flat portion of the structure comes out complete as well, meaning that the top-level structure size would include embedded structure's flat size.</span></span>

3.  <span data-ttu-id="319ce-153">Structure complexe, niveau simple</span><span class="sxs-lookup"><span data-stu-id="319ce-153">Complex structure, single level</span></span>

    <span data-ttu-id="319ce-154">Les membres de pointeur sont marqués par un \_ pointeur FC.</span><span class="sxs-lookup"><span data-stu-id="319ce-154">Pointer members are marked by FC\_POINTER.</span></span> <span data-ttu-id="319ce-155">La disposition du pointeur est simplifiée de telle sorte qu’il existe un descripteur de pointeur (4 octets) pour chaque \_ entrée de pointeur FC de la liste.</span><span class="sxs-lookup"><span data-stu-id="319ce-155">Pointer layout is simplified such that there is a pointer descriptor (4 bytes) for each FC\_POINTER entry on the list.</span></span> <span data-ttu-id="319ce-156">La disposition du pointeur est parcourue en parallèle avec un parcours de membre, autrement dit, un \_ pointeur FC provoque le traitement de la description suivante du pointeur.</span><span class="sxs-lookup"><span data-stu-id="319ce-156">Pointer layout is walked in parallel with a member walk, that is, an FC\_POINTER causes the next pointer description to be processed.</span></span> <span data-ttu-id="319ce-157">Le tableau CARRAY a une disposition de pointeur avec tous les descripteurs du tableau, puis l’élément, à l’aide d’un complexe incorporé.</span><span class="sxs-lookup"><span data-stu-id="319ce-157">The CARRAY array has pointer layout with all the descriptors of the array, and then element, through the use of an embedded complex.</span></span> <span data-ttu-id="319ce-158">Le descripteur d’élément est réutilisé.</span><span class="sxs-lookup"><span data-stu-id="319ce-158">The element descriptor is reused.</span></span> <span data-ttu-id="319ce-159">La taille de la partie plate de la structure est terminée. en d’autres termes, la taille plate de la structure de niveau supérieur comprend la taille plate de la structure incorporée.</span><span class="sxs-lookup"><span data-stu-id="319ce-159">The size of the flat portion of the structure comes out complete; in other words, the top-level structure's flat size includes the embedded structure's flat size.</span></span> <span data-ttu-id="319ce-160">La disposition des membres précède la disposition du pointeur pour les structures complexes.</span><span class="sxs-lookup"><span data-stu-id="319ce-160">The member layout precedes the pointer layout for complex structures.</span></span>

    <span data-ttu-id="319ce-161">Par conséquent, la génération de description de tableau conforme est différente selon qu’il s’agit d’un tableau à l’intérieur d’une structure conforme ou à l’intérieur d’une structure complexe.</span><span class="sxs-lookup"><span data-stu-id="319ce-161">Hence, the conformant array description generation is different depending on whether it is an array inside of a conformant structure or inside a complex structure.</span></span>

4.  <span data-ttu-id="319ce-162">Structure complexe, 2 niveaux ou plus, complexe en complexe</span><span class="sxs-lookup"><span data-stu-id="319ce-162">Complex structure, 2 or more levels, complex in complex</span></span>

    <span data-ttu-id="319ce-163">La structure complexe de niveau supérieur a ses pointeurs membres, la structure complexe incorporée a ses pointeurs membres.</span><span class="sxs-lookup"><span data-stu-id="319ce-163">Top-level complex structure has its member pointers, embedded complex structure has its member pointers.</span></span> <span data-ttu-id="319ce-164">Le descripteur de structure conforme est réutilisé.</span><span class="sxs-lookup"><span data-stu-id="319ce-164">The conformant structure descriptor is reused.</span></span> <span data-ttu-id="319ce-165">Le descripteur de tableau du haut est le tableau réutilisé à partir de la structure incorporée.</span><span class="sxs-lookup"><span data-stu-id="319ce-165">The array descriptor from the top is the reused array from the embedded structure.</span></span>

5.  <span data-ttu-id="319ce-166">Structure complexe avec une structure conforme incorporée</span><span class="sxs-lookup"><span data-stu-id="319ce-166">Complex structure with an embedded conformant structure</span></span>

    <span data-ttu-id="319ce-167">Top = la structure conforme au niveau a ses pointeurs membres.</span><span class="sxs-lookup"><span data-stu-id="319ce-167">Top=level conformant structure has its member pointers.</span></span> <span data-ttu-id="319ce-168">Le descripteur de structure conforme est réutilisé tel quel.</span><span class="sxs-lookup"><span data-stu-id="319ce-168">The conformant structure descriptor is reused as-is.</span></span> <span data-ttu-id="319ce-169">Le descripteur de tableau est réutilisé à partir de la structure conforme incorporée ; en d’autres termes, il n’a pas de pointeurs au niveau du descripteur de tableau.</span><span class="sxs-lookup"><span data-stu-id="319ce-169">The array descriptor is reused from the embedded conformant structure; in other words, it does not have any pointers at the array descriptor.</span></span> <span data-ttu-id="319ce-170">L’élément a son descripteur de pointeur.</span><span class="sxs-lookup"><span data-stu-id="319ce-170">The element has its pointer descriptor.</span></span>

6.  <span data-ttu-id="319ce-171">Tableaux de structures avec des pointeurs</span><span class="sxs-lookup"><span data-stu-id="319ce-171">Arrays of structures with pointers</span></span>

    <span data-ttu-id="319ce-172">Un tableau de structures simples avec des pointeurs est généré sous la forme d’un SMFARRAY ou d’un CARRAY en fonction de la taille du tableau, mais dans les deux cas, il a une mise en forme de pointeur qui est terminée ( \_ répétition répétée ou variable \_ répétée).</span><span class="sxs-lookup"><span data-stu-id="319ce-172">An array of simple structures with pointers is generated as an SMFARRAY or CARRAY depending whether the array is sized, but in both cases it has a pointer layout that is complete (FIXED\_REPEAT or VARIABLE\_REPEAT).</span></span> <span data-ttu-id="319ce-173">La disposition du pointeur précède la disposition des membres.</span><span class="sxs-lookup"><span data-stu-id="319ce-173">The pointer layout comes before the member layout.</span></span>

    <span data-ttu-id="319ce-174">Un tableau de structures complexes avec des pointeurs est généré sous la forme d’un tableau fictif, qu' \_ il soit fixe ou dimensionné, et dans les deux cas, n’a pas de disposition de pointeur.</span><span class="sxs-lookup"><span data-stu-id="319ce-174">An array of complex structures with pointers is generated as BOGUS\_ARRAY regardless whether it is fixed or sized, and in both cases, does not have any pointer layout.</span></span>

## <a name="what-the-ndr-engine-does"></a><span data-ttu-id="319ce-175">Ce que fait le moteur de NDR</span><span class="sxs-lookup"><span data-stu-id="319ce-175">What the NDR Engine Does</span></span>

<span data-ttu-id="319ce-176">Cette section décrit le comportement du moteur de rapport de non-remise.</span><span class="sxs-lookup"><span data-stu-id="319ce-176">This section describes the NDR engine behavior.</span></span>

<span data-ttu-id="319ce-177">**Passe de marshaling**</span><span class="sxs-lookup"><span data-stu-id="319ce-177">**The marshaling pass**</span></span>

1.  <span data-ttu-id="319ce-178">Structures conformes et structure conforme incorporée.</span><span class="sxs-lookup"><span data-stu-id="319ce-178">Conformant structures and embedded conformant structure.</span></span>

    <span data-ttu-id="319ce-179">La structure de niveau supérieur se comporte comme une structure à un seul niveau.</span><span class="sxs-lookup"><span data-stu-id="319ce-179">The top-level structure behaves like a single-level structure.</span></span>

2.  <span data-ttu-id="319ce-180">Structure complexe incorporée avec tableau conforme</span><span class="sxs-lookup"><span data-stu-id="319ce-180">Embedded complex structure with conformant array</span></span>

    <span data-ttu-id="319ce-181">Toute structure complexe force la structure externe à être une structure complexe.</span><span class="sxs-lookup"><span data-stu-id="319ce-181">Any complex structure forces the outer structure to be a complex structure.</span></span> <span data-ttu-id="319ce-182">La structure incorporée ne marshale jamais son tableau.</span><span class="sxs-lookup"><span data-stu-id="319ce-182">Embedded structure never marshals its array.</span></span> <span data-ttu-id="319ce-183">Chaque structure passe toujours par des pointeurs incorporés en marshalant simplement les membres et un membre qui se trouve comme un \_ pointeur FC.</span><span class="sxs-lookup"><span data-stu-id="319ce-183">Every structure always goes through embedded pointers by simply marshaling members and a member happening to be an FC\_POINTER.</span></span>

3.  <span data-ttu-id="319ce-184">Structure complexe avec une structure conforme</span><span class="sxs-lookup"><span data-stu-id="319ce-184">Complex structure with conformant structure</span></span>

    <span data-ttu-id="319ce-185">La structure conforme incorporée la plus haute marshale le tableau conforme et tous les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="319ce-185">The top-most embedded conformant structure marshals the conformant array and all the pointees.</span></span> <span data-ttu-id="319ce-186">Le moteur de rapport de non-remise ne descend jamais des structures conformes imbriquées, le cas échéant ; Cela simplifie la solution, car une structure conforme est un objet feuille en ce qui concerne le marshaling des objets incorporés.</span><span class="sxs-lookup"><span data-stu-id="319ce-186">The NDR engine never descends to deeper nested conformant structures if there are any; this simplifies the solution, as a conformant structure is a leaf object as far as the marshaling of embedded objects is concerned.</span></span> <span data-ttu-id="319ce-187">La structure complexe de niveau supérieur ignore le marshaling de tableau.</span><span class="sxs-lookup"><span data-stu-id="319ce-187">The top-level complex structure skips the array marshaling.</span></span>

<span data-ttu-id="319ce-188">**Démarshaling, bufsizing et libération des passes**</span><span class="sxs-lookup"><span data-stu-id="319ce-188">**Unmarshaling, bufsizing and freeing passes**</span></span>

<span data-ttu-id="319ce-189">Le démarshaling est symétrique au marshaling ; la première opération effectuée pour les structures complexes consiste à Rechercher l’emplacement des pointeurs dans la mémoire tampon au moyen d’appeler la fonction **NdrComplexStructBufferSize** .</span><span class="sxs-lookup"><span data-stu-id="319ce-189">Unmarshaling is symmetrical to marshaling; the first operation it performs for complex structures is to find out the pointees' location in the buffer by means of calling the **NdrComplexStructBufferSize** function.</span></span> <span data-ttu-id="319ce-190">Il démarshale ensuite les pointeurs en parallèle, ce qui permet d’utiliser le même schéma pour démarshaler correctement les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="319ce-190">It then unmarshals pointees in parallel, enabling the same scheme for unmarshaling the pointees correctly to be used.</span></span> <span data-ttu-id="319ce-191">Il ne doit y avoir aucune confusion en ce qui concerne les objets dimensionnés et les unions. l’image mémoire ne doit pas être utilisée pour les objets dimensionnés et les unions, uniquement pour le contenu de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="319ce-191">There should be no confusion about sized objects and unions; the memory image should not be used for sized objects and unions, just for the buffer contents.</span></span>

<span data-ttu-id="319ce-192">Les indicateurs utilisés pour effectuer correctement le marshaling et le démarshaling sont utilisés de la même façon dans bufsizing et pour s’assurer que les pointeurs sont parcourus une seule fois.</span><span class="sxs-lookup"><span data-stu-id="319ce-192">The flags used to perform marshaling and unmarshaling correctly are used in the same way in bufsizing and freeing to make sure that pointees are walked exactly once.</span></span>

<span data-ttu-id="319ce-193">**Passe de primauté des itérations**</span><span class="sxs-lookup"><span data-stu-id="319ce-193">**Endianess pass**</span></span>

<span data-ttu-id="319ce-194">Au premier abord, le passage d’un niveau d’enprimautément est un peu semblable au marshaling/démarshaling. deux tests sont requis pour traiter des structures complexes.</span><span class="sxs-lookup"><span data-stu-id="319ce-194">At first, the endianess pass is somewhat similar to marshaling/unmarshaling; two passes are required to process complex structures.</span></span> <span data-ttu-id="319ce-195">La première passe convertit la partie plate et recherche l’emplacement des pointeurs dans la mémoire tampon, de la même façon que bufsizing effectue cette opération pour démarshaler.</span><span class="sxs-lookup"><span data-stu-id="319ce-195">First pass converts the flat part and finds the pointees' location in the buffer similar to how bufsizing performs this operation for unmarshaling.</span></span> <span data-ttu-id="319ce-196">La deuxième passe convertit ensuite les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="319ce-196">The second pass then converts the pointees.</span></span>

<span data-ttu-id="319ce-197">Les passes d’un niveau d’inversion varient selon la méthode suivante : chaque structure et chaque membre doivent faire l’élément d’un pas à pas jusqu’à ce que le membre feuille ou l’élément soit un type simple.</span><span class="sxs-lookup"><span data-stu-id="319ce-197">Endianess passes differ in the following manner: every structure and every member has to be stepped until the leaf member or element is a simple type.</span></span> <span data-ttu-id="319ce-198">Cela diffère du démarshaling ; dans le démarshaling, par exemple, il n’est jamais nécessaire de traiter les structures conformes incorporées dans les structures conformes, ou tout membre de la structure conforme, pour cette question.</span><span class="sxs-lookup"><span data-stu-id="319ce-198">This is different from unmarshaling; in unmarshaling, for example, there is never a need to process conformant structures embedded in conformant structures, or any member of the conformant structure, for that matter.</span></span> <span data-ttu-id="319ce-199">Un autre problème est que la conversion n’est pas une opération idempotent. par conséquent, le démarshaling peut rétablir le démarshaling de certains morceaux sans nuire, tandis que la conversion doit être effectuée sur une base strictement unique par type.</span><span class="sxs-lookup"><span data-stu-id="319ce-199">Another issue is that the conversion is not an idempotent operation—hence the unmarshaling pass could redo unmarshaling of some pieces without harm, while conversion has to be performed on a strictly once-per-any-simple-type basis.</span></span>

<span data-ttu-id="319ce-200">Par conséquent, l’algorithme de primauté des valeurs peut être résumé comme suit.</span><span class="sxs-lookup"><span data-stu-id="319ce-200">Hence, the endianess algorithm can be summarized as the following.</span></span> <span data-ttu-id="319ce-201">Le rapport de non-remise a une notion de la structure conforme de niveau supérieur et un indicateur pour marquer cela, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="319ce-201">NDR has a notion of the top-level conformant structure and a flag to mark that, as appropriate.</span></span> <span data-ttu-id="319ce-202">Lorsque vous parcourez la première fois, par exemple pour convertir la partie plate et obtenir l’emplacement des pointeurs, cette notion n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="319ce-202">When walking the first time, such as to convert the flat portion and to obtain the location of the pointees, this notion would not be used.</span></span> <span data-ttu-id="319ce-203">Le rapport de non-remise dépasserait les parties plates de tous les niveaux de structures et n’interviendra jamais dans le traitement des pointeurs.</span><span class="sxs-lookup"><span data-stu-id="319ce-203">NDR would descend through the flat parts of all levels of structures and never venture into pointer processing.</span></span> <span data-ttu-id="319ce-204">Enfin, NDR convertit le tableau au niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="319ce-204">Finally, NDR would flat convert the array at the top-level.</span></span>

<span data-ttu-id="319ce-205">Lorsque vous parcourez la deuxième fois, l’indicateur est utilisé pour marquer la passe du pointeur incorporé afin d’éviter d’entrer des niveaux plus détaillés des structures conformes, puis de la structure conforme la plus haute.</span><span class="sxs-lookup"><span data-stu-id="319ce-205">When walking the second time, the flag would be used to mark the embedded pointer's pass to avoid entering deeper levels of the conformant structures, then the top-most conformant structure.</span></span> <span data-ttu-id="319ce-206">De cette façon, l’indicateur force le comportement de marshaling/démarshaling commun, ce qui évite d’avoir à décroisser les niveaux des structures conformes.</span><span class="sxs-lookup"><span data-stu-id="319ce-206">In this way, the flag would force the common marshaling/unmarshaling behavior, which is to avoid descending into deeper levels of conformant structures.</span></span>

<span data-ttu-id="319ce-207">La deuxième passe pour les structures complexes avec des tableaux conformes fonctionne comme suit : les structures complexes fonctionnent de la manière courante. ce qui signifie que les niveaux les plus approfondis ne verront jamais ou ignorent leur taille conforme ou leurs tableaux conformes, et préfèrent simplement parcourir leurs membres sans toucher au tableau.</span><span class="sxs-lookup"><span data-stu-id="319ce-207">The second pass for complex structures with conformant arrays works as follows: the complex structures work the common way; which means deeper levels would never look at or skip their conformant size or their conformant arrays, and would rather simply walk their members without touching the array.</span></span>

<span data-ttu-id="319ce-208">Pour les structures complexes avec des structures conformes, la structure conforme doit savoir s’il s’agit d’un niveau supérieur et s’il est dans une structure complexe.</span><span class="sxs-lookup"><span data-stu-id="319ce-208">For complex structures with conformant structures, the conformant structure must be aware whether it is top level, and whether it is in a complex structure.</span></span> <span data-ttu-id="319ce-209">La partie plate du tableau est traitée par la structure conforme la plus haute.</span><span class="sxs-lookup"><span data-stu-id="319ce-209">The flat portion of the array is processed by the top-most conformant structure.</span></span> <span data-ttu-id="319ce-210">À la deuxième passe, la structure conforme la plus haute ignore la partie plate et passe par la disposition du pointeur et retourne.</span><span class="sxs-lookup"><span data-stu-id="319ce-210">On the second pass, the top-most conformant structure would skip the flat portion and go through the pointer layout and return.</span></span> <span data-ttu-id="319ce-211">La structure supérieure la plus complexe ignore sa partie plate et ignore également la disposition du pointeur.</span><span class="sxs-lookup"><span data-stu-id="319ce-211">The top-most complex structure would skip its flat portion, and would also skip the pointer layout.</span></span>

<span data-ttu-id="319ce-212">**L’aspect robuste des parcours de primauté des niveaux de l’élément**</span><span class="sxs-lookup"><span data-stu-id="319ce-212">**The robust aspect of the endianess walks**</span></span>

<span data-ttu-id="319ce-213">L’ordre de primauté des erreurs de l’ordre de primauté vérifie les conditions de mémoire tampon inhabituelles et effectue d’autres vérifications de nature non corrélée.</span><span class="sxs-lookup"><span data-stu-id="319ce-213">The endianess walk checks for the usual out-of-the-buffer conditions and performs other checks of an uncorrelated nature.</span></span> <span data-ttu-id="319ce-214">Les vérifications destinées à des valeurs corrélées (telles que l’argument de dimensionnement et la taille conforme) ne peuvent pas être effectuées à l’aide de cette étape. ils sont exécutés plus tard, lors de l’démarshaling.</span><span class="sxs-lookup"><span data-stu-id="319ce-214">The checks aimed at correlated values (such as the sizing argument versus the conformant size) cannot be performed using this step; they are performed later, when unmarshaling.</span></span>

 

 




