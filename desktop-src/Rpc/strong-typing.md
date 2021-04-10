---
title: Typage fort
description: C est un langage faiblement typé, autrement dit, le compilateur autorise des opérations telles que l’assignation et la comparaison entre les variables de types différents.
ms.assetid: 5f52adcc-22b9-4b4f-b921-5996d278b10e
keywords:
- Appel de procédure distante RPC, description, saisie de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea859e2d5c160048d79e3c371b47af2bc55e0a65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940306"
---
# <a name="strong-typing"></a><span data-ttu-id="18145-104">Typage fort</span><span class="sxs-lookup"><span data-stu-id="18145-104">Strong Typing</span></span>

<span data-ttu-id="18145-105">C est un langage faiblement typé, autrement dit, le compilateur autorise des opérations telles que l’assignation et la comparaison entre les variables de types différents.</span><span class="sxs-lookup"><span data-stu-id="18145-105">C is a weakly typed language, that is, the compiler allows operations such as assignment and comparison among variables of different types.</span></span> <span data-ttu-id="18145-106">Par exemple, C permet d’effectuer un cast de la valeur d’une variable en un autre type.</span><span class="sxs-lookup"><span data-stu-id="18145-106">For example, C allows the value of a variable to be cast to another type.</span></span> <span data-ttu-id="18145-107">La possibilité d’utiliser des variables de types différents dans la même expression favorise la flexibilité et l’efficacité.</span><span class="sxs-lookup"><span data-stu-id="18145-107">The ability to use variables of different types in the same expression promotes flexibility as well as efficiency.</span></span>

<span data-ttu-id="18145-108">Un langage fortement typé impose des restrictions sur les opérations parmi les variables de types différents.</span><span class="sxs-lookup"><span data-stu-id="18145-108">A strongly typed language imposes restrictions on operations among variables of different types.</span></span> <span data-ttu-id="18145-109">Dans ce cas, le compilateur émet une erreur qui interdit l’opération.</span><span class="sxs-lookup"><span data-stu-id="18145-109">In those cases, the compiler issues an error prohibiting the operation.</span></span> <span data-ttu-id="18145-110">Ces recommandations strictes en matière de types de données sont conçues pour éviter les erreurs potentielles.</span><span class="sxs-lookup"><span data-stu-id="18145-110">These strict guidelines regarding data types are designed to avoid potential errors.</span></span>

<span data-ttu-id="18145-111">La difficulté avec l’utilisation d’un langage faiblement typé comme C pour les appels de procédure distante est que les applications distribuées peuvent s’exécuter sur plusieurs ordinateurs différents avec des compilateurs C et des architectures différentes.</span><span class="sxs-lookup"><span data-stu-id="18145-111">The difficulty with using a weakly typed language such as C for remote procedure calls is that distributed applications can run on several different computers with different C compilers and different architectures.</span></span> <span data-ttu-id="18145-112">Quand une application s’exécute sur un seul ordinateur, vous n’avez pas à vous préoccuper du format de données interne, car les données sont gérées de manière cohérente.</span><span class="sxs-lookup"><span data-stu-id="18145-112">When an application runs on only one computer, you don't have to be concerned with the internal data format because the data is handled in a consistent manner.</span></span> <span data-ttu-id="18145-113">Toutefois, dans un environnement informatique distribué, différents ordinateurs peuvent utiliser des définitions différentes pour leurs types de données de base.</span><span class="sxs-lookup"><span data-stu-id="18145-113">However, in a distributed computing environment, different computers can use different definitions for their base data types.</span></span> <span data-ttu-id="18145-114">Par exemple, certains ordinateurs définissent le type **int** , donc sa représentation interne est de 16 bits, tandis que les autres ordinateurs utilisent 32 bits.</span><span class="sxs-lookup"><span data-stu-id="18145-114">For example, some computers define the **int** type, so its internal representation is 16 bits, while other computers use 32 bits.</span></span> <span data-ttu-id="18145-115">Une architecture d’ordinateur, appelée « Little endian », attribue l’octet de données le moins significatif à l’adresse mémoire la plus basse et l’octet le plus significatif à l’adresse la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="18145-115">One computer architecture, known as "little endian," assigns the least significant byte of data to the lowest memory address and the most significant byte to the highest address.</span></span> <span data-ttu-id="18145-116">Une autre architecture, appelée « Big endian », attribue l’octet le moins significatif à l’adresse mémoire la plus élevée associée à ces données.</span><span class="sxs-lookup"><span data-stu-id="18145-116">Another architecture, known as "big endian," assigns the least significant byte to the highest memory address associated with that data.</span></span>

<span data-ttu-id="18145-117">Les appels de procédure distante nécessitent un contrôle strict sur les types de paramètres.</span><span class="sxs-lookup"><span data-stu-id="18145-117">Remote procedure calls require strict control over parameter types.</span></span> <span data-ttu-id="18145-118">Pour gérer la transmission et la conversion des données sur le réseau, MIDL applique strictement les restrictions de type pour les données transférées sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="18145-118">To handle data transmission and conversion over the network, MIDL strictly enforces type restrictions for data transferred over the network.</span></span> <span data-ttu-id="18145-119">Pour cette raison, MIDL comprend un ensemble de [types de base](base-types.md)bien définis.</span><span class="sxs-lookup"><span data-stu-id="18145-119">For this reason, MIDL includes a set of well-defined [base types](base-types.md).</span></span> <span data-ttu-id="18145-120">MIDL applique un typage fort en exigeant l’utilisation de mots clés qui définissent de manière non ambiguë la taille et le type de données.</span><span class="sxs-lookup"><span data-stu-id="18145-120">MIDL enforces strong typing by mandating the use of keywords that unambiguously define the size and type of data.</span></span> <span data-ttu-id="18145-121">L’effet le plus visible du typage fort est que MIDL n’autorise pas les variables de **type \* void**.</span><span class="sxs-lookup"><span data-stu-id="18145-121">The most visible effect of strong typing is that MIDL does not allow variables of the type **void \***.</span></span>

<span data-ttu-id="18145-122">Dans les rubriques suivantes, cette section traite des fonctionnalités de langage MIDL qui garantissent un typage fort des données :</span><span class="sxs-lookup"><span data-stu-id="18145-122">In the following topics, this section discusses the MIDL language features that enforce strong data typing:</span></span>

-   [<span data-ttu-id="18145-123">Types de base</span><span class="sxs-lookup"><span data-stu-id="18145-123">Base Types</span></span>](base-types.md)
-   [<span data-ttu-id="18145-124">Types signés et non signés</span><span class="sxs-lookup"><span data-stu-id="18145-124">Signed and Unsigned Types</span></span>](signed-and-unsigned-types.md)
-   [<span data-ttu-id="18145-125">Types à caractères larges</span><span class="sxs-lookup"><span data-stu-id="18145-125">Wide-Character Types</span></span>](wide-character-types.md)
-   [<span data-ttu-id="18145-126">Structures</span><span class="sxs-lookup"><span data-stu-id="18145-126">Structures</span></span>](structures.md)
-   [<span data-ttu-id="18145-127">Unions</span><span class="sxs-lookup"><span data-stu-id="18145-127">Unions</span></span>](unions.md)
-   [<span data-ttu-id="18145-128">Types énumérés</span><span class="sxs-lookup"><span data-stu-id="18145-128">Enumerated Types</span></span>](enumerated-types.md)
-   [<span data-ttu-id="18145-129">Tableaux</span><span class="sxs-lookup"><span data-stu-id="18145-129">Arrays</span></span>](arrays.md)
-   [<span data-ttu-id="18145-130">Attributs de fonction</span><span class="sxs-lookup"><span data-stu-id="18145-130">Function Attributes</span></span>](function-attributes.md)
-   [<span data-ttu-id="18145-131">Attributs de champ</span><span class="sxs-lookup"><span data-stu-id="18145-131">Field Attributes</span></span>](field-attributes.md)
-   [<span data-ttu-id="18145-132">Trois types pointeur</span><span class="sxs-lookup"><span data-stu-id="18145-132">Three Pointer Types</span></span>](three-pointer-types.md)
-   [<span data-ttu-id="18145-133">Attributs de type</span><span class="sxs-lookup"><span data-stu-id="18145-133">Type Attributes</span></span>](type-attributes.md)

 

 




