---
title: Chaînes de format de type
description: Les caractères de format dénotent les objets qui intéressent le moteur de NDR.
ms.assetid: 71117082-07b0-4ba4-a920-09be8d8427ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f618d857e487f86e2d28ed18300d82e94b76e3a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029574"
---
# <a name="type-format-strings"></a><span data-ttu-id="ca5e1-103">Chaînes de format de type</span><span class="sxs-lookup"><span data-stu-id="ca5e1-103">Type Format Strings</span></span>

<span data-ttu-id="ca5e1-104">Les caractères de format dénotent les objets qui intéressent le moteur de NDR.</span><span class="sxs-lookup"><span data-stu-id="ca5e1-104">Format characters denote objects of interest to the NDR engine.</span></span> <span data-ttu-id="ca5e1-105">Il existe un caractère de format pour chaque type de base, pour divers types complexes et pour les descriptions des pointeurs, de l’empaquetage, de l’alignement et d’autres objets divers.</span><span class="sxs-lookup"><span data-stu-id="ca5e1-105">There is a format character for each basic type, for various complex types, and for descriptions of pointers, packing, alignment, and other miscellaneous objects.</span></span> <span data-ttu-id="ca5e1-106">Pour les types composés, plusieurs catégories de structures et de tableaux sont reconnues en fonction de leurs propriétés de performances.</span><span class="sxs-lookup"><span data-stu-id="ca5e1-106">For compound types, several categories of structures and arrays are recognized based on their performance properties.</span></span> <span data-ttu-id="ca5e1-107">Une chaîne de format pour chaque catégorie commence par un jeton FC identifiant la chaîne de format particulière.</span><span class="sxs-lookup"><span data-stu-id="ca5e1-107">A format string for each category starts with an FC token identifying the particular format string.</span></span> <span data-ttu-id="ca5e1-108">Les caractères de format pour les structures et les catégories de tableaux peuvent partager les correctifs dans le nom du jeton FC de début indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ca5e1-108">Format characters for structures and arrays categories may share the in-fixes in the name of the leading FC token shown in the following table.</span></span>



| <span data-ttu-id="ca5e1-109">Caractère de format</span><span class="sxs-lookup"><span data-stu-id="ca5e1-109">Format character</span></span> | <span data-ttu-id="ca5e1-110">Description</span><span class="sxs-lookup"><span data-stu-id="ca5e1-110">Description</span></span>                                    |
|------------------|------------------------------------------------|
| <span data-ttu-id="ca5e1-111">C</span><span class="sxs-lookup"><span data-stu-id="ca5e1-111">C</span></span>                | <span data-ttu-id="ca5e1-112">Indique des informations de conformité dans le type.</span><span class="sxs-lookup"><span data-stu-id="ca5e1-112">Indicates conformance information in the type.</span></span> |
| <span data-ttu-id="ca5e1-113">V</span><span class="sxs-lookup"><span data-stu-id="ca5e1-113">V</span></span>                | <span data-ttu-id="ca5e1-114">Indique les informations de variance dans le type.</span><span class="sxs-lookup"><span data-stu-id="ca5e1-114">Indicates variance information in the type.</span></span>    |
| <span data-ttu-id="ca5e1-115">P</span><span class="sxs-lookup"><span data-stu-id="ca5e1-115">P</span></span>                | <span data-ttu-id="ca5e1-116">Indique que les pointeurs font partie du type.</span><span class="sxs-lookup"><span data-stu-id="ca5e1-116">Indicates pointers are a part of the type.</span></span>     |



 

<span data-ttu-id="ca5e1-117">Par exemple, FC \_ CSTRUCT et FC \_ CARRAY identifient la structure conforme et les descripteurs de tableau conformes, respectivement.</span><span class="sxs-lookup"><span data-stu-id="ca5e1-117">For example, FC\_CSTRUCT and FC\_CARRAY identify the conformant structure and conformant array descriptors, respectively.</span></span>

<span data-ttu-id="ca5e1-118">Les caractères de format suivants sont des significations spéciales.</span><span class="sxs-lookup"><span data-stu-id="ca5e1-118">The following are format characters with special meanings.</span></span>



| <span data-ttu-id="ca5e1-119">Caractère de format</span><span class="sxs-lookup"><span data-stu-id="ca5e1-119">Format character</span></span> | <span data-ttu-id="ca5e1-120">Description</span><span class="sxs-lookup"><span data-stu-id="ca5e1-120">Description</span></span>                                                                         |
|------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ca5e1-121">FC \_ pp</span><span class="sxs-lookup"><span data-stu-id="ca5e1-121">FC\_PP</span></span>           | <span data-ttu-id="ca5e1-122">Indique le début de la section de description du pointeur d’une structure ou d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="ca5e1-122">Indicates the beginning of the pointer description section of a structure or array.</span></span> |



 

<span data-ttu-id="ca5e1-123">Les chaînes de format de type NDR RPC sont décrites plus en détail dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="ca5e1-123">RPC NDR type format strings are described in more detail in the following topics:</span></span>

-   [<span data-ttu-id="ca5e1-124">Types simples</span><span class="sxs-lookup"><span data-stu-id="ca5e1-124">Simple Types</span></span>](simple-types-tfs.md)
-   [<span data-ttu-id="ca5e1-125">Pointeurs</span><span class="sxs-lookup"><span data-stu-id="ca5e1-125">Pointers</span></span>](pointers-tfs.md)
-   [<span data-ttu-id="ca5e1-126">Tableaux</span><span class="sxs-lookup"><span data-stu-id="ca5e1-126">Arrays</span></span>](arrays-tfs.md)
-   [<span data-ttu-id="ca5e1-127">Chaînes</span><span class="sxs-lookup"><span data-stu-id="ca5e1-127">Strings</span></span>](strings-tfs.md)
-   [<span data-ttu-id="ca5e1-128">Descripteurs de corrélation</span><span class="sxs-lookup"><span data-stu-id="ca5e1-128">Correlation Descriptors</span></span>](correlation-descriptors-tfs.md)
-   [<span data-ttu-id="ca5e1-129">Structures</span><span class="sxs-lookup"><span data-stu-id="ca5e1-129">Structures</span></span>](structures-tfs.md)
-   [<span data-ttu-id="ca5e1-130">Disposition du pointeur</span><span class="sxs-lookup"><span data-stu-id="ca5e1-130">Pointer Layout</span></span>](pointer-layout-tfs.md)
-   [<span data-ttu-id="ca5e1-131">Unions</span><span class="sxs-lookup"><span data-stu-id="ca5e1-131">Unions</span></span>](unions-tfs.md)
-   [<span data-ttu-id="ca5e1-132">Transmettre \_ en tant que et représenter \_ comme</span><span class="sxs-lookup"><span data-stu-id="ca5e1-132">Transmit\_as and Represent\_as</span></span>](transmit-as-and-represent-as-tfs.md)
-   [<span data-ttu-id="ca5e1-133">Marshal d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="ca5e1-133">User-marshal</span></span>](user-marshal-tfs.md)

 

 




