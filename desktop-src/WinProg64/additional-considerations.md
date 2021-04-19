---
title: Considérations supplémentaires
description: Lorsque vous transférez votre code, tenez compte des points suivants.
ms.assetid: 2d649a09-b593-477a-9b4f-d2404784f4b0
keywords:
- conseils sur le portage-programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7607685f4b4ba04b86da276c38090a48ce0fead
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106542206"
---
# <a name="additional-considerations"></a><span data-ttu-id="e4db8-104">Considérations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e4db8-104">Additional Considerations</span></span>

<span data-ttu-id="e4db8-105">Lorsque vous transférez votre code, tenez compte des points suivants :</span><span class="sxs-lookup"><span data-stu-id="e4db8-105">When porting your code, consider the following points:</span></span>

- <span data-ttu-id="e4db8-106">L’hypothèse suivante n’est plus valide :</span><span class="sxs-lookup"><span data-stu-id="e4db8-106">The following assumption is no longer valid:</span></span>

   ```syntax
   #ifdef _WIN32 // Win32 code
      ...
   #else         // Win16 code
      ...
   #endif
   ```

   <span data-ttu-id="e4db8-107">Toutefois, le compilateur 64 bits définit \_ Win32 pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="e4db8-107">However, the 64-bit compiler defines \_WIN32 for backward compatibility.</span></span>

- <span data-ttu-id="e4db8-108">L’hypothèse suivante n’est plus valide :</span><span class="sxs-lookup"><span data-stu-id="e4db8-108">The following assumption is no longer valid:</span></span>

   ```syntax
   #ifdef _WIN16 // Win16 code
      ...
   #else         // Win32 code
      ...
   #endif
   ```

   <span data-ttu-id="e4db8-109">Dans ce cas, la clause else peut représenter \_ Win32 ou \_ Win64.</span><span class="sxs-lookup"><span data-stu-id="e4db8-109">In this case, the else clause can represent \_WIN32 or \_WIN64.</span></span>

- <span data-ttu-id="e4db8-110">Soyez vigilant avec l’alignement des types de données.</span><span class="sxs-lookup"><span data-stu-id="e4db8-110">Be careful with data-type alignment.</span></span> <span data-ttu-id="e4db8-111">La **macro \_ alignement de type** retourne les exigences d’alignement d’un type de données.</span><span class="sxs-lookup"><span data-stu-id="e4db8-111">The **TYPE\_ALIGNMENT** macro returns the alignment requirements of a data type.</span></span> <span data-ttu-id="e4db8-112">Par exemple : `TYPE_ALIGNMENT( KFLOATING_SAVE )` = = 4 sur x86, 8 sur processeur Intel Itanium `TYPE_ALIGNMENT( UCHAR )` = = 1 partout</span><span class="sxs-lookup"><span data-stu-id="e4db8-112">For example: `TYPE_ALIGNMENT( KFLOATING_SAVE )` == 4 on x86, 8 on Intel Itanium processor`TYPE_ALIGNMENT( UCHAR )` == 1 everywhere</span></span>

    <span data-ttu-id="e4db8-113">Par exemple, le code du noyau qui se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="e4db8-113">As an example, kernel code that currently looks like this:</span></span>

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, sizeof(ULONG) );
    ```

    <span data-ttu-id="e4db8-114">doit probablement être remplacé par :</span><span class="sxs-lookup"><span data-stu-id="e4db8-114">should probably be changed to:</span></span>

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, TYPE_ALIGNMENT(IOCTL_STRUC) );
    ```

    <span data-ttu-id="e4db8-115">Les correctifs automatiques des exceptions d’alignement en mode noyau sont désactivés pour les systèmes Intel Itanium.</span><span class="sxs-lookup"><span data-stu-id="e4db8-115">Automatic fixes of kernel-mode alignment exceptions are disabled for Intel Itanium systems.</span></span>

- <span data-ttu-id="e4db8-116">Soyez vigilant avec les opérations NOT.</span><span class="sxs-lookup"><span data-stu-id="e4db8-116">Be careful with NOT operations.</span></span> <span data-ttu-id="e4db8-117">Tenez compte des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e4db8-117">Consider the following:</span></span>

    ```syntax
    UINT_PTR a; 
    ULONG b;
    a = a & ~(b - 1);
    ```

    <span data-ttu-id="e4db8-118">Le problème est que ~ (b – 1) produit « 0x0000 0000 xxxx xxxx » et non pas « 0xFFFF FFFF xxxx xxxx ».</span><span class="sxs-lookup"><span data-stu-id="e4db8-118">The problem is that ~(b–1) produces "0x0000 0000 xxxx xxxx" and not "0xFFFF FFFF xxxx xxxx".</span></span> <span data-ttu-id="e4db8-119">Le compilateur ne détecte pas cela.</span><span class="sxs-lookup"><span data-stu-id="e4db8-119">The compiler will not detect this.</span></span> <span data-ttu-id="e4db8-120">Pour résoudre ce problème, modifiez le code comme suit :</span><span class="sxs-lookup"><span data-stu-id="e4db8-120">To fix this, change the code as follows:</span></span>

    ```syntax
    a = a & ~((UINT_PTR)b - 1);
    ```

- <span data-ttu-id="e4db8-121">Effectuez des opérations non signées et signées avec prudence.</span><span class="sxs-lookup"><span data-stu-id="e4db8-121">Be careful performing unsigned and signed operations.</span></span> <span data-ttu-id="e4db8-122">Tenez compte des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e4db8-122">Consider the following:</span></span>

    ```syntax
    LONG a;
    ULONG b;
    LONG c;

    a = -10;
    b = 2;
    c = a / b;
    ```

    <span data-ttu-id="e4db8-123">Le résultat est de taille inattendue.</span><span class="sxs-lookup"><span data-stu-id="e4db8-123">The result is unexpectedly large.</span></span> <span data-ttu-id="e4db8-124">La règle est que si l’un des opérandes n’est pas signé, le résultat est non signé.</span><span class="sxs-lookup"><span data-stu-id="e4db8-124">The rule is that if either operand is unsigned, the result is unsigned.</span></span> <span data-ttu-id="e4db8-125">Dans l’exemple précédent, une est convertie en valeur non signée, divisée par b et le résultat est stocké en c.</span><span class="sxs-lookup"><span data-stu-id="e4db8-125">In the preceding example, a is converted to an unsigned value, divided by b, and the result stored in c.</span></span> <span data-ttu-id="e4db8-126">La conversion n’implique aucune manipulation numérique.</span><span class="sxs-lookup"><span data-stu-id="e4db8-126">The conversion involves no numeric manipulation.</span></span>

    <span data-ttu-id="e4db8-127">Voici un autre exemple :</span><span class="sxs-lookup"><span data-stu-id="e4db8-127">As another example, consider the following:</span></span>

    ```syntax
    ULONG x;
    LONG y;
    LONG *pVar1;
    LONG *pVar2;

    pVar2 = pVar1 + y * (x - 1);
    ```

    <span data-ttu-id="e4db8-128">Le problème survient car x n’est pas signé, ce qui rend l’expression entière non signée.</span><span class="sxs-lookup"><span data-stu-id="e4db8-128">The problem arises because x is unsigned, which makes the entire expression unsigned.</span></span> <span data-ttu-id="e4db8-129">Cela fonctionne bien sauf si y est négatif.</span><span class="sxs-lookup"><span data-stu-id="e4db8-129">This works fine unless y is negative.</span></span> <span data-ttu-id="e4db8-130">Dans ce cas, y est converti en une valeur non signée, l’expression est évaluée à l’aide de la précision 32 bits, mise à l’échelle et ajoutée à pVar1.</span><span class="sxs-lookup"><span data-stu-id="e4db8-130">In this case, y is converted to an unsigned value, the expression is evaluated using 32-bit precision, scaled, and added to pVar1.</span></span> <span data-ttu-id="e4db8-131">Un nombre négatif non signé 32 bits devient un grand nombre positif de 64 bits, ce qui donne un résultat erroné.</span><span class="sxs-lookup"><span data-stu-id="e4db8-131">A 32-bit unsigned negative number becomes a large 64-bit positive number, which gives the wrong result.</span></span> <span data-ttu-id="e4db8-132">Pour résoudre ce problème, déclarez x comme valeur signée ou convertissez-le explicitement en **long** dans l’expression.</span><span class="sxs-lookup"><span data-stu-id="e4db8-132">To fix this problem, declare x as a signed value or explicitly typecast it to **LONG** in the expression.</span></span>

- <span data-ttu-id="e4db8-133">Soyez prudent lorsque vous effectuez des allocations de taille fragmentaire.</span><span class="sxs-lookup"><span data-stu-id="e4db8-133">Be careful when making piecemeal size allocations.</span></span> <span data-ttu-id="e4db8-134">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e4db8-134">For example:</span></span>

    ```syntax
    struct xx {
       DWORD NumberOfPointers;
       PVOID Pointers[100];
    };
    ```

    <span data-ttu-id="e4db8-135">Le code suivant est incorrect, car le compilateur remplit la structure avec un 4 octets supplémentaires pour effectuer l’alignement sur 8 octets :</span><span class="sxs-lookup"><span data-stu-id="e4db8-135">The following code is wrong because the compiler will pad the structure with an additional 4 bytes to make the 8-byte alignment:</span></span>

    ```syntax
    malloc(sizeof(DWORD) + 100*sizeof(PVOID));
    ```

    <span data-ttu-id="e4db8-136">Le code suivant est correct :</span><span class="sxs-lookup"><span data-stu-id="e4db8-136">The following code is correct:</span></span>

    ```syntax
    malloc(offsetof(struct xx, Pointers) + 100*sizeof(PVOID));
    ```

- <span data-ttu-id="e4db8-137">Ne pas passer `(HANDLE)0xFFFFFFFF` à des fonctions telles que [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga).</span><span class="sxs-lookup"><span data-stu-id="e4db8-137">Do not pass `(HANDLE)0xFFFFFFFF` to functions such as [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga).</span></span> <span data-ttu-id="e4db8-138">Utilisez plutôt une **\_ \_ valeur de handle non valide**.</span><span class="sxs-lookup"><span data-stu-id="e4db8-138">Instead, use **INVALID\_HANDLE\_VALUE**.</span></span>
- <span data-ttu-id="e4db8-139">Utilisez les spécificateurs de format appropriés lors de l’impression d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="e4db8-139">Use the proper format specifiers when printing a string.</span></span> <span data-ttu-id="e4db8-140">Utilisez% p pour imprimer des pointeurs au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="e4db8-140">Use %p to print pointers in hexadecimal.</span></span> <span data-ttu-id="e4db8-141">C’est le meilleur choix pour les pointeurs d’impression.</span><span class="sxs-lookup"><span data-stu-id="e4db8-141">This is the best choice for printing pointers.</span></span> <span data-ttu-id="e4db8-142">Microsoft Visual C++ prend en charge% I pour imprimer des données polymorphes.</span><span class="sxs-lookup"><span data-stu-id="e4db8-142">Microsoft Visual C++ supports %I to print polymorphic data.</span></span> <span data-ttu-id="e4db8-143">Visual C++ prend également en charge% I64 pour imprimer des valeurs de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e4db8-143">Visual C++ also supports %I64 to print values that are 64 bits.</span></span>

 

 