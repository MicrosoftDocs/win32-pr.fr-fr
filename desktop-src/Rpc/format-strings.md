---
title: Chaînes de format
description: Une chaîne de format est un jeton interprété que le moteur de NDR comprend. Les chaînes de format sont souvent appelées éléments MOP ; Cette documentation utilise le terme chaîne de format dans tout.
ms.assetid: 548283bd-023a-41dd-b1d0-661305d019e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563dd9e4145a7d83b2e49f180329c05c1d55155d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673818"
---
# <a name="format-strings"></a><span data-ttu-id="c45ca-104">Chaînes de format</span><span class="sxs-lookup"><span data-stu-id="c45ca-104">Format Strings</span></span>

<span data-ttu-id="c45ca-105">Une chaîne de format est un jeton interprété que le moteur de NDR comprend.</span><span class="sxs-lookup"><span data-stu-id="c45ca-105">A format string is an interpreted token that the NDR engine understands.</span></span> <span data-ttu-id="c45ca-106">Les chaînes de format sont souvent appelées éléments MOP ; Cette documentation utilise le terme chaîne de format dans tout.</span><span class="sxs-lookup"><span data-stu-id="c45ca-106">Format strings are often referred to as MOPs; this documentation uses the term format string throughout.</span></span>

<span data-ttu-id="c45ca-107">Pour être plus précis, un caractère de format est un jeton interprétable (atomique) individuel.</span><span class="sxs-lookup"><span data-stu-id="c45ca-107">To be more precise, a format character is an individual (atomic) interpretable token.</span></span> <span data-ttu-id="c45ca-108">Chaque caractère de format est d’une taille d’un octet.</span><span class="sxs-lookup"><span data-stu-id="c45ca-108">Each format character is one byte in size.</span></span> <span data-ttu-id="c45ca-109">Une chaîne de format est une séquence de caractères de format ou de caractères de format et de données numériques.</span><span class="sxs-lookup"><span data-stu-id="c45ca-109">A format string is a sequence of format characters or format characters and numerical data.</span></span> <span data-ttu-id="c45ca-110">Le descripteur de terme est également utilisé pour nommer des séquences courantes. par exemple, une chaîne de format de paramètre ou un descripteur de paramètre est une chaîne de format utilisée pour décrire un paramètre d’une routine.</span><span class="sxs-lookup"><span data-stu-id="c45ca-110">The term descriptor is also used for naming common sequences; for example, a parameter format string or a parameter descriptor is a format string used to describe a parameter of a routine.</span></span>

<span data-ttu-id="c45ca-111">Les caractères de format ont des noms symboliques de type « Fibre Channel » \_ ou « struct FC » \_ .</span><span class="sxs-lookup"><span data-stu-id="c45ca-111">Format characters have suggestive symbolic names like FC\_LONG or FC\_STRUCT.</span></span> <span data-ttu-id="c45ca-112">Tous les caractères de chaîne de format utilisés par MIDL et le moteur de NDR sont définis dans le fichier Ndrtypes. h.</span><span class="sxs-lookup"><span data-stu-id="c45ca-112">All format string characters used by MIDL and the NDR engine are defined in the Ndrtypes.h file.</span></span>

## <a name="format-string-tables"></a><span data-ttu-id="c45ca-113">Tables de chaînes de format</span><span class="sxs-lookup"><span data-stu-id="c45ca-113">Format String Tables</span></span>

<span data-ttu-id="c45ca-114">Deux tables de chaînes de format principales sont utilisées par le moteur : la table de format de procédure, **\_ \_ MIDL \_ ProcFormatString**, qui conserve les descripteurs de procédure ; et la table de chaînes de format de type, **\_ \_ MIDL \_ TypeFormatString**, qui conserve les descripteurs de type de données.</span><span class="sxs-lookup"><span data-stu-id="c45ca-114">Two primary format string tables are used by the engine: the procedure format string table, **\_\_MIDL\_ProcFormatString**, that keeps the procedure descriptors; and the type format string table, **\_\_MIDL\_TypeFormatString**, that keeps the data type descriptors.</span></span> <span data-ttu-id="c45ca-115">Le compilateur génère les deux dans les fichiers stub principaux ( \* \_ c. c, \* \_ s. c, \* \_ p. c).</span><span class="sxs-lookup"><span data-stu-id="c45ca-115">The compiler generates both into the main stub files (\*\_c.c, \*\_s.c, \*\_p.c).</span></span> <span data-ttu-id="c45ca-116">La table de chaînes de format de procédure est utilisée principalement par différents interpréteurs, mais elle est également utilisée pour la conversion de mémoire tampon, quel que soit le mode du compilateur.</span><span class="sxs-lookup"><span data-stu-id="c45ca-116">The procedure format string table is used mostly by various interpreters but it is also used for the buffer conversion regardless of the compiler mode.</span></span> <span data-ttu-id="c45ca-117">Le type de table de chaînes de format est utilisé lors de l’appel du moteur de rapport de données principal pour indiquer les types de données spécifiques sur lesquels travailler.</span><span class="sxs-lookup"><span data-stu-id="c45ca-117">The type format string table is used when calling the core NDR engine to indicate specific data types to be worked on.</span></span>

## <a name="format-string-notation"></a><span data-ttu-id="c45ca-118">Notation de chaîne de format</span><span class="sxs-lookup"><span data-stu-id="c45ca-118">Format String Notation</span></span>

<span data-ttu-id="c45ca-119">La notation utilisée dans ce document suit des indications de description de programmation courantes, avec une barre ( \| ) utilisée pour désigner d’autres constructions et crochets ( \[ \] ) utilisés pour indiquer des éléments facultatifs.</span><span class="sxs-lookup"><span data-stu-id="c45ca-119">The notation used in this document follows common programming description guidelines, with a bar ( \| ) used to denote alternative constructs and square brackets ( \[ \] ) used to indicate optional elements.</span></span> <span data-ttu-id="c45ca-120">Les chaînes de format sont fréquemment empilées pour des raisons de lisibilité (responsabilisation).</span><span class="sxs-lookup"><span data-stu-id="c45ca-120">Format strings are frequently stacked up for readability (accountability).</span></span> <span data-ttu-id="c45ca-121">Dans ce document, FC désigne un caractère de format unique.</span><span class="sxs-lookup"><span data-stu-id="c45ca-121">Throughout this document, FC denotes a single format character.</span></span> <span data-ttu-id="c45ca-122">Les caractères de format sont présentés en MAJUSCULEs, à l’aide de leurs noms symboliques réels.</span><span class="sxs-lookup"><span data-stu-id="c45ca-122">Format characters are presented in all CAPS, using their actual symbolic names.</span></span> <span data-ttu-id="c45ca-123">D’autres champs arbitraires sont représentés par un nom et une taille.</span><span class="sxs-lookup"><span data-stu-id="c45ca-123">Other arbitrary fields are represented by a name and a size.</span></span>

<span data-ttu-id="c45ca-124">Les chevrons ( <> ) sont utilisés pour indiquer la taille des descripteurs.</span><span class="sxs-lookup"><span data-stu-id="c45ca-124">Angle brackets ( <> ) are used to denote sizes of the descriptors.</span></span> <span data-ttu-id="c45ca-125">Les conventions présentées dans le tableau suivant sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="c45ca-125">The conventions shown in the following table are employed.</span></span>



| <span data-ttu-id="c45ca-126">Notation</span><span class="sxs-lookup"><span data-stu-id="c45ca-126">Notation</span></span>     | <span data-ttu-id="c45ca-127">Signification</span><span class="sxs-lookup"><span data-stu-id="c45ca-127">Meaning</span></span>                                                   |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="c45ca-128"><*n*></span><span class="sxs-lookup"><span data-stu-id="c45ca-128"><*n*></span></span>  | <span data-ttu-id="c45ca-129">La taille du descripteur est de n octets.</span><span class="sxs-lookup"><span data-stu-id="c45ca-129">The size of descriptor is n bytes.</span></span>                        |
| <>     | <span data-ttu-id="c45ca-130">La taille du descripteur varie.</span><span class="sxs-lookup"><span data-stu-id="c45ca-130">The size of descriptor varies.</span></span>                            |
| <span data-ttu-id="c45ca-131">{<>}\*</span><span class="sxs-lookup"><span data-stu-id="c45ca-131">{<>}\*</span></span> | <span data-ttu-id="c45ca-132">Le descripteur est répété un nombre quelconque de fois (0, 1, 2...).</span><span class="sxs-lookup"><span data-stu-id="c45ca-132">The descriptor is repeated any number of times (0,1,2 …).</span></span> |



 

<span data-ttu-id="c45ca-133">Les caractères de format suivants ont une signification particulière.</span><span class="sxs-lookup"><span data-stu-id="c45ca-133">The following format characters have a special meaning.</span></span>



| <span data-ttu-id="c45ca-134">Caractère</span><span class="sxs-lookup"><span data-stu-id="c45ca-134">Character</span></span> | <span data-ttu-id="c45ca-135">Signification</span><span class="sxs-lookup"><span data-stu-id="c45ca-135">Meaning</span></span>                                   |
|-----------|-------------------------------------------|
| <span data-ttu-id="c45ca-136">\_fin FC</span><span class="sxs-lookup"><span data-stu-id="c45ca-136">FC\_END</span></span>   | <span data-ttu-id="c45ca-137">Indique la fin de certaines chaînes de format.</span><span class="sxs-lookup"><span data-stu-id="c45ca-137">Indicates the end of some format strings.</span></span> |
| <span data-ttu-id="c45ca-138">\_boîtier FC</span><span class="sxs-lookup"><span data-stu-id="c45ca-138">FC\_PAD</span></span>   | <span data-ttu-id="c45ca-139">Caractère de remplissage non interprété.</span><span class="sxs-lookup"><span data-stu-id="c45ca-139">Uninterpreted pad character.</span></span>              |



 

 

 




