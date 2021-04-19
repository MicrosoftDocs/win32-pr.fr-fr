---
description: Cette section décrit le format des enregistrements pour chacun des jetons d’enregistrement. Les informations sont réparties dans les sections suivantes.
ms.assetid: 4fdd8339-f660-4389-878a-e7ab067d8508
title: Enregistrements de jeton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae7e1dcdd36d538ed44205fa51b8e2094d1ff14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514511"
---
# <a name="token-records"></a><span data-ttu-id="85857-104">Enregistrements de jeton</span><span class="sxs-lookup"><span data-stu-id="85857-104">Token Records</span></span>

<span data-ttu-id="85857-105">Cette section décrit le format des enregistrements pour chacun des jetons d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="85857-105">This section describes the format of the records for each of the record-bearing tokens.</span></span> <span data-ttu-id="85857-106">Les informations sont réparties dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="85857-106">Information is divided into the following sections.</span></span>

-   [<span data-ttu-id="85857-107">nom du jeton \_</span><span class="sxs-lookup"><span data-stu-id="85857-107">TOKEN\_NAME</span></span>](/windows)
-   [<span data-ttu-id="85857-108">chaîne de jeton \_</span><span class="sxs-lookup"><span data-stu-id="85857-108">TOKEN\_STRING</span></span>](/windows)
-   [<span data-ttu-id="85857-109">entier de jeton \_</span><span class="sxs-lookup"><span data-stu-id="85857-109">TOKEN\_INTEGER</span></span>](/windows)
-   [<span data-ttu-id="85857-110">GUID du jeton \_</span><span class="sxs-lookup"><span data-stu-id="85857-110">TOKEN\_GUID</span></span>](/windows)
-   [<span data-ttu-id="85857-111">\_liste des entiers de jeton \_</span><span class="sxs-lookup"><span data-stu-id="85857-111">TOKEN\_INTEGER\_LIST</span></span>](/windows)
-   [<span data-ttu-id="85857-112">\_liste flottante de jeton \_</span><span class="sxs-lookup"><span data-stu-id="85857-112">TOKEN\_FLOAT\_LIST</span></span>](/windows)

## <a name="token_name"></a><span data-ttu-id="85857-113">nom du jeton \_</span><span class="sxs-lookup"><span data-stu-id="85857-113">TOKEN\_NAME</span></span>

<span data-ttu-id="85857-114">Enregistrement de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="85857-114">A variable-length record.</span></span> <span data-ttu-id="85857-115">Le jeton est suivi d’une valeur de nombre qui spécifie le nombre d’octets qui suivent dans le champ nom.</span><span class="sxs-lookup"><span data-stu-id="85857-115">The token is followed by a count value that specifies the number of bytes that follow in the name field.</span></span> <span data-ttu-id="85857-116">Un nom ASCII de longueur nombre termine l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="85857-116">An ASCII name of length count completes the record.</span></span>



| <span data-ttu-id="85857-117">Champ</span><span class="sxs-lookup"><span data-stu-id="85857-117">Field</span></span> | <span data-ttu-id="85857-118">Type</span><span class="sxs-lookup"><span data-stu-id="85857-118">Type</span></span>       | <span data-ttu-id="85857-119">Taille (en octets)</span><span class="sxs-lookup"><span data-stu-id="85857-119">Size (bytes)</span></span> | <span data-ttu-id="85857-120">Contenu</span><span class="sxs-lookup"><span data-stu-id="85857-120">Contents</span></span>                       |
|-------|------------|--------------|--------------------------------|
| <span data-ttu-id="85857-121">token</span><span class="sxs-lookup"><span data-stu-id="85857-121">token</span></span> | <span data-ttu-id="85857-122">WORD</span><span class="sxs-lookup"><span data-stu-id="85857-122">WORD</span></span>       | <span data-ttu-id="85857-123">2</span><span class="sxs-lookup"><span data-stu-id="85857-123">2</span></span>            | <span data-ttu-id="85857-124">nom du jeton \_</span><span class="sxs-lookup"><span data-stu-id="85857-124">token\_name</span></span>                    |
| <span data-ttu-id="85857-125">count</span><span class="sxs-lookup"><span data-stu-id="85857-125">count</span></span> | <span data-ttu-id="85857-126">DWORD</span><span class="sxs-lookup"><span data-stu-id="85857-126">DWORD</span></span>      | <span data-ttu-id="85857-127">4</span><span class="sxs-lookup"><span data-stu-id="85857-127">4</span></span>            | <span data-ttu-id="85857-128">Longueur du champ de nom, en octets</span><span class="sxs-lookup"><span data-stu-id="85857-128">Length of name field, in bytes</span></span> |
| <span data-ttu-id="85857-129">name</span><span class="sxs-lookup"><span data-stu-id="85857-129">name</span></span>  | <span data-ttu-id="85857-130">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="85857-130">BYTE array</span></span> | <span data-ttu-id="85857-131">count</span><span class="sxs-lookup"><span data-stu-id="85857-131">count</span></span>        | <span data-ttu-id="85857-132">Nom ASCII</span><span class="sxs-lookup"><span data-stu-id="85857-132">ASCII name</span></span>                     |



 

## <a name="token_string"></a><span data-ttu-id="85857-133">chaîne de jeton \_</span><span class="sxs-lookup"><span data-stu-id="85857-133">TOKEN\_STRING</span></span>

<span data-ttu-id="85857-134">Enregistrement de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="85857-134">A variable-length record.</span></span> <span data-ttu-id="85857-135">Le jeton est suivi d’une valeur de nombre qui spécifie le nombre d’octets qui suivent dans le champ de chaîne.</span><span class="sxs-lookup"><span data-stu-id="85857-135">The token is followed by a count value that specifies the number of bytes that follow in the string field.</span></span> <span data-ttu-id="85857-136">Une chaîne ASCII de nombre de longueurs continue l’enregistrement, qui est terminé par un jeton de fin.</span><span class="sxs-lookup"><span data-stu-id="85857-136">An ASCII string of length count continues the record, which is completed by a terminating token.</span></span> <span data-ttu-id="85857-137">Le choix du terminateur est déterminé par des problèmes de syntaxe abordés ailleurs.</span><span class="sxs-lookup"><span data-stu-id="85857-137">The choice of terminator is determined by syntax issues discussed elsewhere.</span></span>



| <span data-ttu-id="85857-138">Champ</span><span class="sxs-lookup"><span data-stu-id="85857-138">Field</span></span>      | <span data-ttu-id="85857-139">Type</span><span class="sxs-lookup"><span data-stu-id="85857-139">Type</span></span>       | <span data-ttu-id="85857-140">Taille (en octets)</span><span class="sxs-lookup"><span data-stu-id="85857-140">Size (bytes)</span></span> | <span data-ttu-id="85857-141">Contenu</span><span class="sxs-lookup"><span data-stu-id="85857-141">Contents</span></span>                         |
|------------|------------|--------------|----------------------------------|
| <span data-ttu-id="85857-142">token</span><span class="sxs-lookup"><span data-stu-id="85857-142">token</span></span>      | <span data-ttu-id="85857-143">WORD</span><span class="sxs-lookup"><span data-stu-id="85857-143">WORD</span></span>       | <span data-ttu-id="85857-144">2</span><span class="sxs-lookup"><span data-stu-id="85857-144">2</span></span>            | <span data-ttu-id="85857-145">chaîne de jeton \_</span><span class="sxs-lookup"><span data-stu-id="85857-145">token\_string</span></span>                    |
| <span data-ttu-id="85857-146">count</span><span class="sxs-lookup"><span data-stu-id="85857-146">count</span></span>      | <span data-ttu-id="85857-147">DWORD</span><span class="sxs-lookup"><span data-stu-id="85857-147">DWORD</span></span>      | <span data-ttu-id="85857-148">4</span><span class="sxs-lookup"><span data-stu-id="85857-148">4</span></span>            | <span data-ttu-id="85857-149">Longueur du champ de chaîne en octets</span><span class="sxs-lookup"><span data-stu-id="85857-149">Length of string field in bytes</span></span>  |
| <span data-ttu-id="85857-150">Chaîne</span><span class="sxs-lookup"><span data-stu-id="85857-150">strinG</span></span>     | <span data-ttu-id="85857-151">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="85857-151">BYTE array</span></span> | <span data-ttu-id="85857-152">count</span><span class="sxs-lookup"><span data-stu-id="85857-152">count</span></span>        | <span data-ttu-id="85857-153">Chaîne ASCII</span><span class="sxs-lookup"><span data-stu-id="85857-153">ASCII string</span></span>                     |
| <span data-ttu-id="85857-154">terminateur</span><span class="sxs-lookup"><span data-stu-id="85857-154">terminator</span></span> | <span data-ttu-id="85857-155">DWORD</span><span class="sxs-lookup"><span data-stu-id="85857-155">DWORD</span></span>      | <span data-ttu-id="85857-156">4</span><span class="sxs-lookup"><span data-stu-id="85857-156">4</span></span>            | <span data-ttu-id="85857-157">\_point-virgule ou \_ virgule de jeton</span><span class="sxs-lookup"><span data-stu-id="85857-157">tOKEN\_SEMICOLON or TOKEN\_COMMA</span></span> |



 

## <a name="token_integer"></a><span data-ttu-id="85857-158">entier de jeton \_</span><span class="sxs-lookup"><span data-stu-id="85857-158">TOKEN\_INTEGER</span></span>

<span data-ttu-id="85857-159">Enregistrement de longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="85857-159">A fixed length record.</span></span> <span data-ttu-id="85857-160">Le jeton est suivi de la valeur entière requise.</span><span class="sxs-lookup"><span data-stu-id="85857-160">The token is followed by the integer value required.</span></span>



| <span data-ttu-id="85857-161">Champ</span><span class="sxs-lookup"><span data-stu-id="85857-161">Field</span></span> | <span data-ttu-id="85857-162">Type</span><span class="sxs-lookup"><span data-stu-id="85857-162">Type</span></span>  | <span data-ttu-id="85857-163">Taille (en octets)</span><span class="sxs-lookup"><span data-stu-id="85857-163">Size (bytes)</span></span> | <span data-ttu-id="85857-164">Contenu</span><span class="sxs-lookup"><span data-stu-id="85857-164">Contents</span></span>       |
|-------|-------|--------------|----------------|
| <span data-ttu-id="85857-165">token</span><span class="sxs-lookup"><span data-stu-id="85857-165">token</span></span> | <span data-ttu-id="85857-166">WORD</span><span class="sxs-lookup"><span data-stu-id="85857-166">WORD</span></span>  | <span data-ttu-id="85857-167">2</span><span class="sxs-lookup"><span data-stu-id="85857-167">2</span></span>            | <span data-ttu-id="85857-168">entier de jeton \_</span><span class="sxs-lookup"><span data-stu-id="85857-168">tOKEN\_INTEGER</span></span> |
| <span data-ttu-id="85857-169">Ajoutée</span><span class="sxs-lookup"><span data-stu-id="85857-169">valuE</span></span> | <span data-ttu-id="85857-170">DWORD</span><span class="sxs-lookup"><span data-stu-id="85857-170">DWORD</span></span> | <span data-ttu-id="85857-171">4</span><span class="sxs-lookup"><span data-stu-id="85857-171">4</span></span>            | <span data-ttu-id="85857-172">Entier unique</span><span class="sxs-lookup"><span data-stu-id="85857-172">Single integer</span></span> |



 

## <a name="token_guid"></a><span data-ttu-id="85857-173">GUID du jeton \_</span><span class="sxs-lookup"><span data-stu-id="85857-173">TOKEN\_GUID</span></span>

<span data-ttu-id="85857-174">Enregistrement de longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="85857-174">A fixed-length record.</span></span> <span data-ttu-id="85857-175">Le jeton est suivi des quatre champs de données tels qu’ils sont définis par la norme de l’ETCD OSF.</span><span class="sxs-lookup"><span data-stu-id="85857-175">The token is followed by the four data fields as defined by the OSF DCE standard.</span></span>



| <span data-ttu-id="85857-176">Champ</span><span class="sxs-lookup"><span data-stu-id="85857-176">Field</span></span> | <span data-ttu-id="85857-177">Type</span><span class="sxs-lookup"><span data-stu-id="85857-177">Type</span></span>       | <span data-ttu-id="85857-178">Taille (en octets)</span><span class="sxs-lookup"><span data-stu-id="85857-178">Size (bytes)</span></span> | <span data-ttu-id="85857-179">Contenu</span><span class="sxs-lookup"><span data-stu-id="85857-179">Contents</span></span>          |
|-------|------------|--------------|-------------------|
| <span data-ttu-id="85857-180">token</span><span class="sxs-lookup"><span data-stu-id="85857-180">token</span></span> | <span data-ttu-id="85857-181">WORD</span><span class="sxs-lookup"><span data-stu-id="85857-181">WORD</span></span>       | <span data-ttu-id="85857-182">2</span><span class="sxs-lookup"><span data-stu-id="85857-182">2</span></span>            | <span data-ttu-id="85857-183">GUID du jeton \_</span><span class="sxs-lookup"><span data-stu-id="85857-183">tOKEN\_GUID</span></span>       |
| <span data-ttu-id="85857-184">Data1</span><span class="sxs-lookup"><span data-stu-id="85857-184">Data1</span></span> | <span data-ttu-id="85857-185">DWORD</span><span class="sxs-lookup"><span data-stu-id="85857-185">DWORD</span></span>      | <span data-ttu-id="85857-186">4</span><span class="sxs-lookup"><span data-stu-id="85857-186">4</span></span>            | <span data-ttu-id="85857-187">Champ de données UUID 1</span><span class="sxs-lookup"><span data-stu-id="85857-187">UUID data field 1</span></span> |
| <span data-ttu-id="85857-188">Data2</span><span class="sxs-lookup"><span data-stu-id="85857-188">Data2</span></span> | <span data-ttu-id="85857-189">WORD</span><span class="sxs-lookup"><span data-stu-id="85857-189">WORD</span></span>       | <span data-ttu-id="85857-190">2</span><span class="sxs-lookup"><span data-stu-id="85857-190">2</span></span>            | <span data-ttu-id="85857-191">Champ de données UUID 2</span><span class="sxs-lookup"><span data-stu-id="85857-191">UUID data field 2</span></span> |
| <span data-ttu-id="85857-192">Data3</span><span class="sxs-lookup"><span data-stu-id="85857-192">Data3</span></span> | <span data-ttu-id="85857-193">WORD</span><span class="sxs-lookup"><span data-stu-id="85857-193">WORD</span></span>       | <span data-ttu-id="85857-194">2</span><span class="sxs-lookup"><span data-stu-id="85857-194">2</span></span>            | <span data-ttu-id="85857-195">Champ de données UUID 3</span><span class="sxs-lookup"><span data-stu-id="85857-195">UUID data field 3</span></span> |
| <span data-ttu-id="85857-196">Data4</span><span class="sxs-lookup"><span data-stu-id="85857-196">Data4</span></span> | <span data-ttu-id="85857-197">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="85857-197">BYTE array</span></span> | <span data-ttu-id="85857-198">8</span><span class="sxs-lookup"><span data-stu-id="85857-198">8</span></span>            | <span data-ttu-id="85857-199">Champ de données UUID 4</span><span class="sxs-lookup"><span data-stu-id="85857-199">UUID data field 4</span></span> |



 

## <a name="token_integer_list"></a><span data-ttu-id="85857-200">\_liste des entiers de jeton \_</span><span class="sxs-lookup"><span data-stu-id="85857-200">TOKEN\_INTEGER\_LIST</span></span>

<span data-ttu-id="85857-201">Enregistrement de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="85857-201">A variable-length record.</span></span> <span data-ttu-id="85857-202">Le jeton est suivi d’une valeur de nombre qui spécifie le nombre d’entiers figurant dans le champ de liste.</span><span class="sxs-lookup"><span data-stu-id="85857-202">The token is followed by a count value that specifies the number of integers that follow in the list field.</span></span> <span data-ttu-id="85857-203">Pour des performances optimales, les listes d’entiers consécutives doivent être composées en une seule liste.</span><span class="sxs-lookup"><span data-stu-id="85857-203">For efficiency, consecutive integer lists should be compounded into a single list.</span></span>



| <span data-ttu-id="85857-204">Champ</span><span class="sxs-lookup"><span data-stu-id="85857-204">Field</span></span> | <span data-ttu-id="85857-205">Type</span><span class="sxs-lookup"><span data-stu-id="85857-205">Type</span></span>  | <span data-ttu-id="85857-206">Taille (en octets)</span><span class="sxs-lookup"><span data-stu-id="85857-206">Size (bytes)</span></span> | <span data-ttu-id="85857-207">Contenu</span><span class="sxs-lookup"><span data-stu-id="85857-207">Contents</span></span>                         |
|-------|-------|--------------|----------------------------------|
| <span data-ttu-id="85857-208">token</span><span class="sxs-lookup"><span data-stu-id="85857-208">token</span></span> | <span data-ttu-id="85857-209">WORD</span><span class="sxs-lookup"><span data-stu-id="85857-209">WORD</span></span>  | <span data-ttu-id="85857-210">2</span><span class="sxs-lookup"><span data-stu-id="85857-210">2</span></span>            | <span data-ttu-id="85857-211">\_liste des entiers de jeton \_</span><span class="sxs-lookup"><span data-stu-id="85857-211">tOKEN\_INTEGER\_LISt</span></span>             |
| <span data-ttu-id="85857-212">count</span><span class="sxs-lookup"><span data-stu-id="85857-212">count</span></span> | <span data-ttu-id="85857-213">DWORD</span><span class="sxs-lookup"><span data-stu-id="85857-213">DWORD</span></span> | <span data-ttu-id="85857-214">4</span><span class="sxs-lookup"><span data-stu-id="85857-214">4</span></span>            | <span data-ttu-id="85857-215">Nombre d’entiers dans le champ de liste</span><span class="sxs-lookup"><span data-stu-id="85857-215">Number of integers in list field</span></span> |
| <span data-ttu-id="85857-216">list</span><span class="sxs-lookup"><span data-stu-id="85857-216">list</span></span>  | <span data-ttu-id="85857-217">DWORD</span><span class="sxs-lookup"><span data-stu-id="85857-217">DWORD</span></span> | <span data-ttu-id="85857-218">nombre de 4 x</span><span class="sxs-lookup"><span data-stu-id="85857-218">4 x count</span></span>    | <span data-ttu-id="85857-219">Liste d’entiers</span><span class="sxs-lookup"><span data-stu-id="85857-219">Integer list</span></span>                     |



 

## <a name="token_float_list"></a><span data-ttu-id="85857-220">\_liste flottante de jeton \_</span><span class="sxs-lookup"><span data-stu-id="85857-220">TOKEN\_FLOAT\_LIST</span></span>

<span data-ttu-id="85857-221">Enregistrement de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="85857-221">A variable-length record.</span></span> <span data-ttu-id="85857-222">Le jeton est suivi d’une valeur de nombre qui spécifie le nombre de valeurs float ou double qui suivent dans le champ de liste.</span><span class="sxs-lookup"><span data-stu-id="85857-222">The token is followed by a count value that specifies the number of floats or doubles that follow in the list field.</span></span> <span data-ttu-id="85857-223">La taille de la valeur à virgule flottante (float ou double) est déterminée par la valeur de float SizeSpecified dans l’en-tête de fichier.</span><span class="sxs-lookup"><span data-stu-id="85857-223">The size of the floating point value (float or double) is determined by the value of float sizespecified in the file header.</span></span> <span data-ttu-id="85857-224">Pour des performances optimales, les listes de valeurs float de jeton consécutives \_ \_ doivent être composées en une seule liste.</span><span class="sxs-lookup"><span data-stu-id="85857-224">For efficiency, consecutive TOKEN\_FLOAT\_LISTs should be compounded into a single list.</span></span>



| <span data-ttu-id="85857-225">Champ</span><span class="sxs-lookup"><span data-stu-id="85857-225">Field</span></span> | <span data-ttu-id="85857-226">Type</span><span class="sxs-lookup"><span data-stu-id="85857-226">Type</span></span>               | <span data-ttu-id="85857-227">Taille (en octets)</span><span class="sxs-lookup"><span data-stu-id="85857-227">Size (bytes)</span></span>   | <span data-ttu-id="85857-228">Contenu</span><span class="sxs-lookup"><span data-stu-id="85857-228">Contents</span></span>                                  |
|-------|--------------------|----------------|-------------------------------------------|
| <span data-ttu-id="85857-229">token</span><span class="sxs-lookup"><span data-stu-id="85857-229">token</span></span> | <span data-ttu-id="85857-230">WORD</span><span class="sxs-lookup"><span data-stu-id="85857-230">WORD</span></span>               | <span data-ttu-id="85857-231">2</span><span class="sxs-lookup"><span data-stu-id="85857-231">2</span></span>              | <span data-ttu-id="85857-232">\_liste flottante de jeton \_</span><span class="sxs-lookup"><span data-stu-id="85857-232">tOKEN\_FLOAT\_LISt</span></span>                        |
| <span data-ttu-id="85857-233">count</span><span class="sxs-lookup"><span data-stu-id="85857-233">count</span></span> | <span data-ttu-id="85857-234">DWORD</span><span class="sxs-lookup"><span data-stu-id="85857-234">DWORD</span></span>              | <span data-ttu-id="85857-235">4</span><span class="sxs-lookup"><span data-stu-id="85857-235">4</span></span>              | <span data-ttu-id="85857-236">Nombre de valeurs float ou double dans le champ de liste</span><span class="sxs-lookup"><span data-stu-id="85857-236">Number of floats or doubles in list field</span></span> |
| <span data-ttu-id="85857-237">list</span><span class="sxs-lookup"><span data-stu-id="85857-237">list</span></span>  | <span data-ttu-id="85857-238">float/double Array</span><span class="sxs-lookup"><span data-stu-id="85857-238">float/double array</span></span> | <span data-ttu-id="85857-239">nombre de 4 ou 8 x</span><span class="sxs-lookup"><span data-stu-id="85857-239">4 or 8 x count</span></span> | <span data-ttu-id="85857-240">Liste flottante ou double</span><span class="sxs-lookup"><span data-stu-id="85857-240">Float or double list</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="85857-241">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="85857-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85857-242">Encodage Binaire</span><span class="sxs-lookup"><span data-stu-id="85857-242">Binary Encoding</span></span>](binary-encoding.md)
</dt> </dl>

 

 
