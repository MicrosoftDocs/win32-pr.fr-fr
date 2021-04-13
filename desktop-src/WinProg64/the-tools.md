---
title: Les outils
description: Cette rubrique décrit les outils que vous pouvez utiliser pour rendre votre application 64 bits prête. Windows 10 est disponible pour les processeurs x64 et ARM64.
ms.assetid: 457b7cc1-8517-4a36-9a0c-cf191ff3b374
keywords:
- Guide de programmation Windows 64 bits, programmation Windows 64 bits, outils
- outils de programmation Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87fb315200ae32eb1e1441ed330be49aa02d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380232"
---
# <a name="the-tools"></a><span data-ttu-id="c430e-106">Les outils</span><span class="sxs-lookup"><span data-stu-id="c430e-106">The Tools</span></span>

<span data-ttu-id="c430e-107">Cette rubrique décrit les outils que vous pouvez utiliser pour rendre votre application 64 bits prête.</span><span class="sxs-lookup"><span data-stu-id="c430e-107">This topic describes the tools available for you to use in making your application 64-bit ready.</span></span> <span data-ttu-id="c430e-108">Windows 10 est disponible pour les processeurs x64 et ARM64.</span><span class="sxs-lookup"><span data-stu-id="c430e-108">Windows 10 is available for both x64 and ARM64 based processors.</span></span>

## <a name="include-files"></a><span data-ttu-id="c430e-109">Fichiers include</span><span class="sxs-lookup"><span data-stu-id="c430e-109">Include Files</span></span>

<span data-ttu-id="c430e-110">Les éléments d’API sont pratiquement identiques entre les fenêtres 32 et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c430e-110">The API elements are virtually identical between 32- and 64-bit Windows.</span></span> <span data-ttu-id="c430e-111">Les fichiers d’en-tête Windows ont été modifiés afin de pouvoir être utilisés pour le code 32 et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c430e-111">The Windows header files have been modified so that they can be used for both 32- and 64-bit code.</span></span> <span data-ttu-id="c430e-112">Les nouveaux types et macros 64 bits sont définis dans un nouveau fichier d’en-tête, Basetsd. h, qui se trouve dans le jeu de fichiers d’en-tête inclus dans Windows. h.</span><span class="sxs-lookup"><span data-stu-id="c430e-112">The new 64-bit types and macros are defined in a new header file, Basetsd.h, which is in the set of header files included by Windows.h.</span></span> <span data-ttu-id="c430e-113">Basetsd. h comprend les nouvelles définitions de type de données pour faciliter la création d’une taille de mot de code source indépendante.</span><span class="sxs-lookup"><span data-stu-id="c430e-113">Basetsd.h includes the new data-type definitions to assist in making source code word-size independent.</span></span>

## <a name="new-data-types"></a><span data-ttu-id="c430e-114">Nouveaux types de données</span><span class="sxs-lookup"><span data-stu-id="c430e-114">New Data Types</span></span>

<span data-ttu-id="c430e-115">Les fichiers d’en-tête Windows contiennent de nouveaux types de données.</span><span class="sxs-lookup"><span data-stu-id="c430e-115">The Windows header files contain new data types.</span></span> <span data-ttu-id="c430e-116">Ces types sont principalement destinés à la compatibilité de type avec les types de données 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c430e-116">These types are primarily for type compatibility with the 32-bit data types.</span></span> <span data-ttu-id="c430e-117">Les nouveaux types fournissent exactement le même type que les types existants, tout en assurant la prise en charge des fenêtres 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c430e-117">The new types provide exactly the same typing as the existing types, while at the same time providing support for the 64-bit Windows.</span></span> <span data-ttu-id="c430e-118">Pour plus d’informations, consultez [les nouveaux types de données](the-new-data-types.md) ou le fichier d’en-tête Basetsd. h.</span><span class="sxs-lookup"><span data-stu-id="c430e-118">For more information, see [The New Data Types](the-new-data-types.md) or the Basetsd.h header file.</span></span>

## <a name="predefined-macros"></a><span data-ttu-id="c430e-119">Macros prédéfinies</span><span class="sxs-lookup"><span data-stu-id="c430e-119">Predefined Macros</span></span>

<span data-ttu-id="c430e-120">Le compilateur définit les macros suivantes pour identifier la plateforme.</span><span class="sxs-lookup"><span data-stu-id="c430e-120">The compiler defines the following macros to identify the platform.</span></span>



| <span data-ttu-id="c430e-121">Macro</span><span class="sxs-lookup"><span data-stu-id="c430e-121">Macro</span></span>   | <span data-ttu-id="c430e-122">Signification</span><span class="sxs-lookup"><span data-stu-id="c430e-122">Meaning</span></span>                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c430e-123">\_WIN64</span><span class="sxs-lookup"><span data-stu-id="c430e-123">\_WIN64</span></span> | <span data-ttu-id="c430e-124">Une plateforme 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c430e-124">A 64-bit platform.</span></span> <span data-ttu-id="c430e-125">Cela comprend à la fois x64 et ARM64.</span><span class="sxs-lookup"><span data-stu-id="c430e-125">This includes both x64 and ARM64.</span></span>                                                        |
| <span data-ttu-id="c430e-126">\_32</span><span class="sxs-lookup"><span data-stu-id="c430e-126">\_WIN32</span></span> | <span data-ttu-id="c430e-127">Une plateforme 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c430e-127">A 32-bit platform.</span></span> <span data-ttu-id="c430e-128">Cette valeur est également définie par le compilateur 64 bits pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="c430e-128">This value is also defined by the 64-bit compiler for backward compatibility.</span></span><br/> |
| <span data-ttu-id="c430e-129">\_WIN16</span><span class="sxs-lookup"><span data-stu-id="c430e-129">\_WIN16</span></span> | <span data-ttu-id="c430e-130">Plateforme 16 bits</span><span class="sxs-lookup"><span data-stu-id="c430e-130">A 16-bit platform</span></span>                                                                                           |



 

<span data-ttu-id="c430e-131">Les macros suivantes sont spécifiques à l’architecture.</span><span class="sxs-lookup"><span data-stu-id="c430e-131">The following macros are specific to the architecture.</span></span>



| <span data-ttu-id="c430e-132">Macro</span><span class="sxs-lookup"><span data-stu-id="c430e-132">Macro</span></span>      | <span data-ttu-id="c430e-133">Signification</span><span class="sxs-lookup"><span data-stu-id="c430e-133">Meaning</span></span>                |
|------------|------------------------|
| <span data-ttu-id="c430e-134">\_M \_ ia64</span><span class="sxs-lookup"><span data-stu-id="c430e-134">\_M\_IA64</span></span>  | <span data-ttu-id="c430e-135">Plateforme Intel Itanium</span><span class="sxs-lookup"><span data-stu-id="c430e-135">Intel Itanium platform</span></span> |
| <span data-ttu-id="c430e-136">\_M \_ ix86</span><span class="sxs-lookup"><span data-stu-id="c430e-136">\_M\_IX86</span></span>  | <span data-ttu-id="c430e-137">plateforme x86</span><span class="sxs-lookup"><span data-stu-id="c430e-137">x86 platform</span></span>           |
| <span data-ttu-id="c430e-138">\_M \_ x64</span><span class="sxs-lookup"><span data-stu-id="c430e-138">\_M\_X64</span></span>   | <span data-ttu-id="c430e-139">plateforme x64</span><span class="sxs-lookup"><span data-stu-id="c430e-139">x64 platform</span></span>           |
| <span data-ttu-id="c430e-140">\_M \_ ARM64</span><span class="sxs-lookup"><span data-stu-id="c430e-140">\_M\_ARM64</span></span> | <span data-ttu-id="c430e-141">Plateforme ARM64</span><span class="sxs-lookup"><span data-stu-id="c430e-141">ARM64 platform</span></span>         |



 

<span data-ttu-id="c430e-142">N’utilisez pas ces macros, à l’exception du code propre à l’architecture, à la place, utilisez \_ Win64, Win32 et Win16 dans la mesure du \_ \_ possible.</span><span class="sxs-lookup"><span data-stu-id="c430e-142">Do not use these macros except with architecture-specific code, instead, use \_WIN64, \_WIN32, and \_WIN16 whenever possible.</span></span>

## <a name="helper-functions"></a><span data-ttu-id="c430e-143">Fonctions d’assistance</span><span class="sxs-lookup"><span data-stu-id="c430e-143">Helper Functions</span></span>

<span data-ttu-id="c430e-144">Les fonctions inline suivantes (définies dans Basetsd. h) peuvent vous aider à convertir en toute sécurité des valeurs d’un type vers un autre.</span><span class="sxs-lookup"><span data-stu-id="c430e-144">The following inline functions (defined in Basetsd.h) can help you safely convert values from one type to another.</span></span>

``` syntax
void            * Handle64ToHandle( const void * POINTER_64 h ) 
void * POINTER_64 HandleToHandle64( const void *h )
long              HandleToLong(     const void *h )
unsigned long     HandleToUlong(    const void *h )
void            * IntToPtr(         const int i )
void            * LongToHandle(     const long h )
void            * LongToPtr(        const long l )
void            * Ptr64ToPtr(       const void * POINTER_64 p )
int               PtrToInt(         const void *p )
long              PtrToLong(        const void *p )
void * POINTER_64 PtrToPtr64(       const void *p )
short             PtrToShort(       const void *p )
unsigned int      PtrToUint(        const void *p )
unsigned long     PtrToUlong(       const void *p )
unsigned short    PtrToUshort(      const void *p )
void            * UIntToPtr(        const unsigned int ui )
void            * ULongToPtr(       const unsigned long ul )
```

> [!WARNING]
> <span data-ttu-id="c430e-145">**IntToPtr** signe-étend la valeur **int** , **UIntToPtr** zéro étend la valeur **unsigned int** , **LongToPtr** signe étend la valeur **long** et **ULongToPtr** zéro-étend la valeur **long non signée** .</span><span class="sxs-lookup"><span data-stu-id="c430e-145">**IntToPtr** sign-extends the **int** value, **UIntToPtr** zero-extends the **unsigned int** value, **LongToPtr** sign-extends the **long** value, and **ULongToPtr** zero-extends the **unsigned long** value.</span></span>

 

## <a name="64-bit-compiler"></a><span data-ttu-id="c430e-146">Compilateur 64 bits</span><span class="sxs-lookup"><span data-stu-id="c430e-146">64-bit Compiler</span></span>

<span data-ttu-id="c430e-147">Les compilateurs 64 bits peuvent être utilisés pour identifier la troncation de pointeur, les casts de type incorrects et d’autres problèmes spécifiques à 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c430e-147">The 64-bit compilers can be used to identify pointer truncation, improper type casts, and other 64-bit-specific problems.</span></span>

<span data-ttu-id="c430e-148">Lorsque le compilateur est exécuté pour la première fois, il génère probablement de nombreux avertissements de troncation de pointeur ou d’incompatibilité de type, comme suit :</span><span class="sxs-lookup"><span data-stu-id="c430e-148">When the compiler is first run, it will probably generate many pointer truncation or type mismatch warnings, such as the following:</span></span>

`warning C4311: 'type cast' : pointer truncation from 'unsigned char *' to 'unsigned long '`

<span data-ttu-id="c430e-149">Utilisez ces avertissements comme guide pour rendre le code plus robuste.</span><span class="sxs-lookup"><span data-stu-id="c430e-149">Use these warnings as a guide to make the code more robust.</span></span> <span data-ttu-id="c430e-150">Il est conseillé d’éliminer tous les avertissements, en particulier les avertissements de troncation de pointeur.</span><span class="sxs-lookup"><span data-stu-id="c430e-150">It is good practice to eliminate all warnings, especially pointer-truncation warnings.</span></span>

## <a name="64-bit-compiler-switches-and-warnings"></a><span data-ttu-id="c430e-151">Avertissements et commutateurs du compilateur 64 bits</span><span class="sxs-lookup"><span data-stu-id="c430e-151">64-bit Compiler Switches and Warnings</span></span>

<span data-ttu-id="c430e-152">Notez que ce compilateur active le modèle de données LLP64.</span><span class="sxs-lookup"><span data-stu-id="c430e-152">Note that this compiler enables the LLP64 data model.</span></span>

<span data-ttu-id="c430e-153">Il existe une option d’avertissement pour faciliter le portage vers LLP64.</span><span class="sxs-lookup"><span data-stu-id="c430e-153">There is a warning option to assist porting to LLP64.</span></span> <span data-ttu-id="c430e-154">Le commutateur-Wp64-W3 active les avertissements suivants :</span><span class="sxs-lookup"><span data-stu-id="c430e-154">The -Wp64 -W3 switch enables the following warnings:</span></span>

-   <span data-ttu-id="c430e-155">C4305 : avertissement de troncation.</span><span class="sxs-lookup"><span data-stu-id="c430e-155">C4305: Truncation warning.</span></span> <span data-ttu-id="c430e-156">Par exemple, « Return » : troncation de « unsigned int64 » à « long ».</span><span class="sxs-lookup"><span data-stu-id="c430e-156">For example, "return": truncation from "unsigned int64" to "long."</span></span>
-   <span data-ttu-id="c430e-157">C4311 : avertissement de troncation.</span><span class="sxs-lookup"><span data-stu-id="c430e-157">C4311: Truncation warning.</span></span> <span data-ttu-id="c430e-158">Par exemple, « cast de type » : troncation de pointeur de « int \* \_ ptr64 » à « int ».</span><span class="sxs-lookup"><span data-stu-id="c430e-158">For example, "type cast": pointer truncation from "int\*\_ptr64" to "int."</span></span>
-   <span data-ttu-id="c430e-159">C4312 : conversion en avertissement de taille supérieure.</span><span class="sxs-lookup"><span data-stu-id="c430e-159">C4312: Conversion to bigger-size warning.</span></span> <span data-ttu-id="c430e-160">Par exemple, « cast de type » : conversion de « int » en « int \* \_ ptr64 » d’une plus grande taille.</span><span class="sxs-lookup"><span data-stu-id="c430e-160">For example, "type cast": conversion from "int" to "int\*\_ptr64" of greater size.</span></span>
-   <span data-ttu-id="c430e-161">C4318 : passage de longueur nulle.</span><span class="sxs-lookup"><span data-stu-id="c430e-161">C4318: Passing zero length.</span></span> <span data-ttu-id="c430e-162">Par exemple, le passage de la constante zéro comme longueur à la fonction **memset** .</span><span class="sxs-lookup"><span data-stu-id="c430e-162">For example, passing constant zero as the length to the **memset** function.</span></span>
-   <span data-ttu-id="c430e-163">C4319 : opérateur NOT.</span><span class="sxs-lookup"><span data-stu-id="c430e-163">C4319: Not operator.</span></span> <span data-ttu-id="c430e-164">Par exemple, « ~ » : zéro étendant « unsigned long » à « unsigned \_ Int64 » d’une taille supérieure.</span><span class="sxs-lookup"><span data-stu-id="c430e-164">For example, "~": zero extending "unsigned long" to "unsigned \_int64" of greater size.</span></span>
-   <span data-ttu-id="c430e-165">C4313 : appel de la famille de fonctions **printf** avec des spécificateurs et des arguments de type de conversion conflictuels.</span><span class="sxs-lookup"><span data-stu-id="c430e-165">C4313: Calling the **printf** family of functions with conflicting conversion type specifiers and arguments.</span></span> <span data-ttu-id="c430e-166">Par exemple, « printf » : « % p » dans la chaîne de mise en forme est en conflit avec l’argument 2 de type « \_ Int64 ».</span><span class="sxs-lookup"><span data-stu-id="c430e-166">For example, "printf": "%p" in format string conflicts with argument 2 of type "\_int64."</span></span> <span data-ttu-id="c430e-167">Un autre exemple est l’appel de printf ("% x", valeur de pointeur \_ ); cela provoque une troncation des 32 bits supérieurs.</span><span class="sxs-lookup"><span data-stu-id="c430e-167">Another example is the call printf("%x", pointer\_value); this causes a truncation of the upper 32 bits.</span></span> <span data-ttu-id="c430e-168">L’appel correct est printf ("% p", valeur du pointeur \_ ).</span><span class="sxs-lookup"><span data-stu-id="c430e-168">The correct call is printf("%p", pointer\_value).</span></span>
-   <span data-ttu-id="c430e-169">C4244 : identique à l’C4242 d’avertissement existant.</span><span class="sxs-lookup"><span data-stu-id="c430e-169">C4244: Same as the existing warning C4242.</span></span> <span data-ttu-id="c430e-170">Par exemple, « Return » : conversion de « \_ Int64 » en « unsigned int », perte possible de données.</span><span class="sxs-lookup"><span data-stu-id="c430e-170">For example, "return": conversion from "\_int64" to "unsigned int," possible loss of data.</span></span>

## <a name="64-bit-linker-and-libraries"></a><span data-ttu-id="c430e-171">Bibliothèques et éditeur de liens 64 bits</span><span class="sxs-lookup"><span data-stu-id="c430e-171">64-bit Linker and Libraries</span></span>

<span data-ttu-id="c430e-172">Pour générer des applications, utilisez l’éditeur de liens et les bibliothèques fournis par le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="c430e-172">To build applications, use the linker and libraries provided by the Windows SDK.</span></span> <span data-ttu-id="c430e-173">La plupart des bibliothèques 32 bits ont une version 64 bits correspondante, mais certaines bibliothèques héritées sont disponibles uniquement dans les versions 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c430e-173">Most 32-bit libraries have a corresponding 64-bit version, but certain legacy libraries are available only in 32-bit versions.</span></span> <span data-ttu-id="c430e-174">Le code qui appelle ces bibliothèques n’est pas lié lorsque l’application est générée pour Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c430e-174">Code that calls into these libraries will not link when the application is built for 64-bit Windows.</span></span>

 

 





