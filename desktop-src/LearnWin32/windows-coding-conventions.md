---
title: Conventions de codage Windows
description: Si vous débutez avec la programmation Windows, il peut être déconcerté quand vous consultez un programme Windows pour la première fois.
ms.assetid: 466a66db-7681-4fce-9672-07849cd1b096
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c8509d7cb799bafdfa70c326f1074b64d93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106518003"
---
# <a name="windows-coding-conventions"></a><span data-ttu-id="d5cdc-103">Conventions de codage Windows</span><span class="sxs-lookup"><span data-stu-id="d5cdc-103">Windows Coding Conventions</span></span>

<span data-ttu-id="d5cdc-104">Si vous débutez avec la programmation Windows, il peut être déconcerté quand vous consultez un programme Windows pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-104">If you are new to Windows programming, it can be disconcerting when you first see a Windows program.</span></span> <span data-ttu-id="d5cdc-105">Le code est rempli avec des définitions de type étrange comme **DWORD \_ ptr** et **LPRECT**, et les variables ont des noms tels que *HWND* et *PWSZ* (appelé notation hongroise).</span><span class="sxs-lookup"><span data-stu-id="d5cdc-105">The code is filled with strange type definitions like **DWORD\_PTR** and **LPRECT**, and variables have names like *hWnd* and *pwsz* (called Hungarian notation).</span></span> <span data-ttu-id="d5cdc-106">Il est judicieux de prendre un moment pour apprendre certaines des conventions de codage Windows.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-106">It's worth taking a moment to learn some of the Windows coding conventions.</span></span>

<span data-ttu-id="d5cdc-107">La grande majorité des API Windows consistent en des fonctions ou des interfaces COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="d5cdc-107">The vast majority of Windows APIs consist of either functions or Component Object Model (COM) interfaces.</span></span> <span data-ttu-id="d5cdc-108">Très peu d’API Windows sont fournies en tant que classes C++.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-108">Very few Windows APIs are provided as C++ classes.</span></span> <span data-ttu-id="d5cdc-109">(Une exception notable est GDI+, l’une des API graphiques 2D.)</span><span class="sxs-lookup"><span data-stu-id="d5cdc-109">(A notable exception is GDI+, one of the 2-D graphics APIs.)</span></span>

## <a name="typedefs"></a><span data-ttu-id="d5cdc-110">Typedefs</span><span class="sxs-lookup"><span data-stu-id="d5cdc-110">Typedefs</span></span>

<span data-ttu-id="d5cdc-111">Les en-têtes Windows contiennent un grand nombre de typedefs.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-111">The Windows headers contain a lot of typedefs.</span></span> <span data-ttu-id="d5cdc-112">Un grand nombre d’entre eux sont définis dans le fichier d’en-tête WinDef. h.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-112">Many of these are defined in the header file WinDef.h.</span></span> <span data-ttu-id="d5cdc-113">Voici quelques-uns que vous rencontrerez souvent.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-113">Here are some that you will encounter often.</span></span>

### <a name="integer-types"></a><span data-ttu-id="d5cdc-114">Types d'entier</span><span class="sxs-lookup"><span data-stu-id="d5cdc-114">Integer types</span></span>



| <span data-ttu-id="d5cdc-115">Type de données</span><span class="sxs-lookup"><span data-stu-id="d5cdc-115">Data type</span></span>     | <span data-ttu-id="d5cdc-116">Taille</span><span class="sxs-lookup"><span data-stu-id="d5cdc-116">Size</span></span>    | <span data-ttu-id="d5cdc-117">Abonné?</span><span class="sxs-lookup"><span data-stu-id="d5cdc-117">Signed?</span></span>  |
|---------------|---------|----------|
| <span data-ttu-id="d5cdc-118">**BYTE**</span><span class="sxs-lookup"><span data-stu-id="d5cdc-118">**BYTE**</span></span>      | <span data-ttu-id="d5cdc-119">8 bits</span><span class="sxs-lookup"><span data-stu-id="d5cdc-119">8 bits</span></span>  | <span data-ttu-id="d5cdc-120">Non signé</span><span class="sxs-lookup"><span data-stu-id="d5cdc-120">Unsigned</span></span> |
| <span data-ttu-id="d5cdc-121">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="d5cdc-121">**DWORD**</span></span>     | <span data-ttu-id="d5cdc-122">32 bits</span><span class="sxs-lookup"><span data-stu-id="d5cdc-122">32 bits</span></span> | <span data-ttu-id="d5cdc-123">Non signé</span><span class="sxs-lookup"><span data-stu-id="d5cdc-123">Unsigned</span></span> |
| <span data-ttu-id="d5cdc-124">**ENTIER**</span><span class="sxs-lookup"><span data-stu-id="d5cdc-124">**INT32**</span></span>     | <span data-ttu-id="d5cdc-125">32 bits</span><span class="sxs-lookup"><span data-stu-id="d5cdc-125">32 bits</span></span> | <span data-ttu-id="d5cdc-126">Signé</span><span class="sxs-lookup"><span data-stu-id="d5cdc-126">Signed</span></span>   |
| <span data-ttu-id="d5cdc-127">**INT64**</span><span class="sxs-lookup"><span data-stu-id="d5cdc-127">**INT64**</span></span>     | <span data-ttu-id="d5cdc-128">64 bits</span><span class="sxs-lookup"><span data-stu-id="d5cdc-128">64 bits</span></span> | <span data-ttu-id="d5cdc-129">Signé</span><span class="sxs-lookup"><span data-stu-id="d5cdc-129">Signed</span></span>   |
| <span data-ttu-id="d5cdc-130">**LONG**</span><span class="sxs-lookup"><span data-stu-id="d5cdc-130">**LONG**</span></span>      | <span data-ttu-id="d5cdc-131">32 bits</span><span class="sxs-lookup"><span data-stu-id="d5cdc-131">32 bits</span></span> | <span data-ttu-id="d5cdc-132">Signé</span><span class="sxs-lookup"><span data-stu-id="d5cdc-132">Signed</span></span>   |
| <span data-ttu-id="d5cdc-133">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="d5cdc-133">**LONGLONG**</span></span>  | <span data-ttu-id="d5cdc-134">64 bits</span><span class="sxs-lookup"><span data-stu-id="d5cdc-134">64 bits</span></span> | <span data-ttu-id="d5cdc-135">Signé</span><span class="sxs-lookup"><span data-stu-id="d5cdc-135">Signed</span></span>   |
| <span data-ttu-id="d5cdc-136">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d5cdc-136">**UINT32**</span></span>    | <span data-ttu-id="d5cdc-137">32 bits</span><span class="sxs-lookup"><span data-stu-id="d5cdc-137">32 bits</span></span> | <span data-ttu-id="d5cdc-138">Non signé</span><span class="sxs-lookup"><span data-stu-id="d5cdc-138">Unsigned</span></span> |
| <span data-ttu-id="d5cdc-139">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="d5cdc-139">**UINT64**</span></span>    | <span data-ttu-id="d5cdc-140">64 bits</span><span class="sxs-lookup"><span data-stu-id="d5cdc-140">64 bits</span></span> | <span data-ttu-id="d5cdc-141">Non signé</span><span class="sxs-lookup"><span data-stu-id="d5cdc-141">Unsigned</span></span> |
| <span data-ttu-id="d5cdc-142">**CORRESPONDANTE**</span><span class="sxs-lookup"><span data-stu-id="d5cdc-142">**ULONG**</span></span>     | <span data-ttu-id="d5cdc-143">32 bits</span><span class="sxs-lookup"><span data-stu-id="d5cdc-143">32 bits</span></span> | <span data-ttu-id="d5cdc-144">Non signé</span><span class="sxs-lookup"><span data-stu-id="d5cdc-144">Unsigned</span></span> |
| <span data-ttu-id="d5cdc-145">**ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="d5cdc-145">**ULONGLONG**</span></span> | <span data-ttu-id="d5cdc-146">64 bits</span><span class="sxs-lookup"><span data-stu-id="d5cdc-146">64 bits</span></span> | <span data-ttu-id="d5cdc-147">Non signé</span><span class="sxs-lookup"><span data-stu-id="d5cdc-147">Unsigned</span></span> |
| <span data-ttu-id="d5cdc-148">**WORD**</span><span class="sxs-lookup"><span data-stu-id="d5cdc-148">**WORD**</span></span>      | <span data-ttu-id="d5cdc-149">16 bits</span><span class="sxs-lookup"><span data-stu-id="d5cdc-149">16 bits</span></span> | <span data-ttu-id="d5cdc-150">Non signé</span><span class="sxs-lookup"><span data-stu-id="d5cdc-150">Unsigned</span></span> |



 

<span data-ttu-id="d5cdc-151">Comme vous pouvez le voir, il existe une certaine redondance dans ces typedefs.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-151">As you can see, there is a certain amount of redundancy in these typedefs.</span></span> <span data-ttu-id="d5cdc-152">Une partie de ce chevauchement est simplement due à l’historique des API Windows.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-152">Some of this overlap is simply due to the history of the Windows APIs.</span></span> <span data-ttu-id="d5cdc-153">Les types répertoriés ici ont une taille fixe et les tailles sont les mêmes dans les applications 32 bits et 64.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-153">The types listed here have fixed size, and the sizes are the same in both 32-bit and 64-applications.</span></span> <span data-ttu-id="d5cdc-154">Par exemple, le type **DWORD** est toujours de 32 bits de largeur.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-154">For example, the **DWORD** type is always 32 bits wide.</span></span>

### <a name="boolean-type"></a><span data-ttu-id="d5cdc-155">Type booléen</span><span class="sxs-lookup"><span data-stu-id="d5cdc-155">Boolean Type</span></span>

<span data-ttu-id="d5cdc-156">**Bool** est un typedef pour une valeur entière qui est utilisée dans un contexte booléen.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-156">**BOOL** is a typedef for an integer value that is used in a Boolean context.</span></span> <span data-ttu-id="d5cdc-157">Le fichier d’en-tête WinDef. h définit également deux valeurs à utiliser avec **bool**.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-157">The header file WinDef.h also defines two values for use with **BOOL**.</span></span>


```C++
#define FALSE    0 
#define TRUE     1
```



<span data-ttu-id="d5cdc-158">Toutefois, en dépit de cette définition de **true**, la plupart des fonctions qui retournent un type **bool** peuvent retourner toute valeur différente de zéro pour indiquer la vérité booléenne.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-158">Despite this definition of **TRUE**, however, most functions that return a **BOOL** type can return any non-zero value to indicate Boolean truth.</span></span> <span data-ttu-id="d5cdc-159">Par conséquent, vous devez toujours écrire ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="d5cdc-159">Therefore, you should always write this:</span></span>


```C++
// Right way.
BOOL result = SomeFunctionThatReturnsBoolean();
if (result) 
{ 
    ...
}
```



<span data-ttu-id="d5cdc-160">et non :</span><span class="sxs-lookup"><span data-stu-id="d5cdc-160">and not this:</span></span>


```C++
// Wrong!
if (result == TRUE) 
{
    ... 
}
```



<span data-ttu-id="d5cdc-161">N’oubliez pas que **bool** est un type entier et qu’il n’est pas interchangeable avec le type **bool** C++.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-161">Be aware that **BOOL** is an integer type and is not interchangeable with the C++ **bool** type.</span></span>

### <a name="pointer-types"></a><span data-ttu-id="d5cdc-162">Types pointeur</span><span class="sxs-lookup"><span data-stu-id="d5cdc-162">Pointer Types</span></span>

<span data-ttu-id="d5cdc-163">Windows définit de nombreux types de données de la forme *pointeur vers X*.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-163">Windows defines many data types of the form *pointer-to-X*.</span></span> <span data-ttu-id="d5cdc-164">Ils ont généralement le préfixe *P* ou *LP* dans le nom.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-164">These usually have the prefix *P-* or *LP-* in the name.</span></span> <span data-ttu-id="d5cdc-165">Par exemple, **LPRECT** est un pointeur vers [**Rect**](/previous-versions//dd162897(v=vs.85)), où **Rect** est une structure qui décrit un rectangle.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-165">For example, **LPRECT** is a pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)), where **RECT** is a structure that describes a rectangle.</span></span> <span data-ttu-id="d5cdc-166">Les déclarations de variables suivantes sont équivalentes.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-166">The following variable declarations are equivalent.</span></span>


```C++
RECT*  rect;  // Pointer to a RECT structure.
LPRECT rect;  // The same
PRECT  rect;  // Also the same.
```



<span data-ttu-id="d5cdc-167">Historiquement, *P* correspond à « pointeur » et la *LP* à « pointeur long ».</span><span class="sxs-lookup"><span data-stu-id="d5cdc-167">Historically, *P* stands for "pointer" and *LP* stands for "long pointer".</span></span> <span data-ttu-id="d5cdc-168">Les pointeurs longs (également appelés *pointeurs Far*) sont un holdover de Windows 16 bits, lorsqu’ils étaient nécessaires pour adresser des plages de mémoire en dehors du segment actuel.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-168">Long pointers (also called *far pointers*) are a holdover from 16-bit Windows, when they were needed to address memory ranges outside the current segment.</span></span> <span data-ttu-id="d5cdc-169">Le préfixe *LP* a été conservé pour faciliter le portage du code 16 bits vers Windows 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-169">The *LP* prefix was preserved to make it easier to port 16-bit code to 32-bit Windows.</span></span> <span data-ttu-id="d5cdc-170">À l’heure actuelle, il n’existe aucune distinction : un pointeur est un pointeur.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-170">Today there is no distinction — a pointer is a pointer.</span></span>

### <a name="pointer-precision-types"></a><span data-ttu-id="d5cdc-171">Types de précision des pointeurs</span><span class="sxs-lookup"><span data-stu-id="d5cdc-171">Pointer Precision Types</span></span>

<span data-ttu-id="d5cdc-172">Les types de données suivants sont toujours la taille d’un pointeur, c’est-à-dire 32 bits de largeur dans les applications 32 bits et 64 bits de largeur dans les applications 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-172">The following data types are always the size of a pointer—that is, 32 bits wide in 32-bit applications, and 64 bits wide in 64-bit applications.</span></span> <span data-ttu-id="d5cdc-173">La taille est déterminée au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-173">The size is determined at compile time.</span></span> <span data-ttu-id="d5cdc-174">Quand une application 32 bits s’exécute sur Windows 64 bits, ces types de données ont toujours une largeur de 4 octets.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-174">When a 32-bit application runs on 64-bit Windows, these data types are still 4 bytes wide.</span></span> <span data-ttu-id="d5cdc-175">(Une application 64 bits ne peut pas s’exécuter sous Windows 32 bits, donc la situation inverse ne se produit pas.)</span><span class="sxs-lookup"><span data-stu-id="d5cdc-175">(A 64-bit application cannot run on 32-bit Windows, so the reverse situation does not occur.)</span></span>

-   <span data-ttu-id="d5cdc-176">**\_ptr DWORD**</span><span class="sxs-lookup"><span data-stu-id="d5cdc-176">**DWORD\_PTR**</span></span>
-   <span data-ttu-id="d5cdc-177">**\_pointeur int**</span><span class="sxs-lookup"><span data-stu-id="d5cdc-177">**INT\_PTR**</span></span>
-   <span data-ttu-id="d5cdc-178">**\_ptr long**</span><span class="sxs-lookup"><span data-stu-id="d5cdc-178">**LONG\_PTR**</span></span>
-   <span data-ttu-id="d5cdc-179">**ULONG ( \_ PTR)**</span><span class="sxs-lookup"><span data-stu-id="d5cdc-179">**ULONG\_PTR**</span></span>
-   <span data-ttu-id="d5cdc-180">**UINT \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="d5cdc-180">**UINT\_PTR**</span></span>

<span data-ttu-id="d5cdc-181">Ces types sont utilisés dans les situations où un entier peut être casté en un pointeur.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-181">These types are used in situations where an integer might be cast to a pointer.</span></span> <span data-ttu-id="d5cdc-182">Elles servent également à définir des variables pour les opérations arithmétiques sur les pointeurs et à définir des compteurs de boucle qui effectuent une itération sur la plage complète d’octets dans les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-182">They are also used to define variables for pointer arithmetic and to define loop counters that iterate over the full range of bytes in memory buffers.</span></span> <span data-ttu-id="d5cdc-183">Plus généralement, elles apparaissent à des endroits où une valeur 32 bits existante a été étendue à 64 bits sur Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-183">More generally, they appear in places where an existing 32-bit value was expanded to 64 bits on 64-bit Windows.</span></span>

## <a name="hungarian-notation"></a><span data-ttu-id="d5cdc-184">Notation hongroise</span><span class="sxs-lookup"><span data-stu-id="d5cdc-184">Hungarian Notation</span></span>

<span data-ttu-id="d5cdc-185">La *notation hongroise* est la pratique consistant à ajouter des préfixes aux noms de variables, afin de fournir des informations supplémentaires sur la variable.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-185">*Hungarian notation* is the practice of adding prefixes to the names of variables, to give additional information about the variable.</span></span> <span data-ttu-id="d5cdc-186">(L’invente de la notation, Charles Simonyi, était hongrois, donc son nom).</span><span class="sxs-lookup"><span data-stu-id="d5cdc-186">(The notation's inventor, Charles Simonyi, was Hungarian, hence its name).</span></span>

<span data-ttu-id="d5cdc-187">Dans sa forme d’origine, la notation hongroise fournit des informations *sémantiques* sur une variable, en vous indiquant l’utilisation prévue.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-187">In its original form, Hungarian notation gives *semantic* information about a variable, telling you the intended use.</span></span> <span data-ttu-id="d5cdc-188">Par exemple, *je* signifie un index, *CB* signifie une taille en octets (« nombre d’octets ») et les numéros de ligne et de colonne pour les colonnes *RW* et *col* .</span><span class="sxs-lookup"><span data-stu-id="d5cdc-188">For example, *i* means an index, *cb* means a size in bytes ("count of bytes"), and *rw* and *col* mean row and column numbers.</span></span> <span data-ttu-id="d5cdc-189">Ces préfixes sont conçus pour éviter l’utilisation accidentelle d’une variable dans un contexte incorrect.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-189">These prefixes are designed to avoid the accidental use of a variable in the wrong context.</span></span> <span data-ttu-id="d5cdc-190">Par exemple, si vous avez vu l’expression `rwPosition +  cbTable` , vous savez qu’un numéro de ligne est ajouté à une taille, ce qui est presque certainement un bogue dans le code</span><span class="sxs-lookup"><span data-stu-id="d5cdc-190">For example, if you saw the expression `rwPosition +  cbTable`, you would know that a row number is being added to a size, which is almost certainly a bug in the code</span></span>

<span data-ttu-id="d5cdc-191">Une forme plus courante de notation hongroise utilise des préfixes pour fournir des informations de *type* , par exemple, *DW* pour **DWORD** et *w* pour **Word**.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-191">A more common form of Hungarian notation uses prefixes to give *type* information—for example, *dw* for **DWORD** and *w* for **WORD**.</span></span>

<span data-ttu-id="d5cdc-192">Si vous recherchez « notation hongroise » sur le Web, vous trouverez un grand nombre d’opinions indiquant si la notation hongroise est correcte ou incorrecte.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-192">If you search the Web for "Hungarian notation," you will find a lot of opinions about whether Hungarian notation is good or bad.</span></span> <span data-ttu-id="d5cdc-193">Certains programmeurs ont une plus forte non-notation hongroise.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-193">Some programmers have an intense dislike for Hungarian notation.</span></span> <span data-ttu-id="d5cdc-194">D’autres le trouvent utiles.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-194">Others find it helpful.</span></span> <span data-ttu-id="d5cdc-195">Quoi qu’il en soit, un grand nombre d’exemples de code sur MSDN utilisent la notation hongroise, mais vous n’avez pas besoin de mémoriser les préfixes pour comprendre le code.</span><span class="sxs-lookup"><span data-stu-id="d5cdc-195">Regardless, many of the code examples on MSDN use Hungarian notation, but you don't need to memorize the prefixes to understand the code.</span></span>

## <a name="next"></a><span data-ttu-id="d5cdc-196">Suivant</span><span class="sxs-lookup"><span data-stu-id="d5cdc-196">Next</span></span>

[<span data-ttu-id="d5cdc-197">Utilisation de chaînes</span><span class="sxs-lookup"><span data-stu-id="d5cdc-197">Working with Strings</span></span>](working-with-strings.md)

 

 