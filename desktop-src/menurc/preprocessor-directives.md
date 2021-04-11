---
title: Directives de préprocesseur (menus et autres ressources)
description: Vous pouvez utiliser les directives décrites dans le tableau suivant en fonction des besoins dans votre script de ressources. Ils indiquent à RC d’effectuer des actions ou d’assigner des valeurs à des noms.
ms.assetid: 162f946e-54d8-4e23-9aa7-8e91eda4ee68
keywords:
- compilateur de ressources, directives de préprocesseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e8c32f1d32dab784d5d947fdf64b7018451a5a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317073"
---
# <a name="preprocessor-directives-menus-and-other-resources"></a><span data-ttu-id="be280-105">Directives de préprocesseur (menus et autres ressources)</span><span class="sxs-lookup"><span data-stu-id="be280-105">Preprocessor Directives (Menus and Other Resources)</span></span>

<span data-ttu-id="be280-106">Vous pouvez utiliser les directives décrites dans le tableau suivant en fonction des besoins dans votre script de ressources.</span><span class="sxs-lookup"><span data-stu-id="be280-106">You can use the directives described in the following table as needed in your resource script.</span></span> <span data-ttu-id="be280-107">Ils indiquent à RC d’effectuer des actions ou d’assigner des valeurs à des noms.</span><span class="sxs-lookup"><span data-stu-id="be280-107">They instruct RC to perform actions or to assign values to names.</span></span>



| <span data-ttu-id="be280-108">Directive</span><span class="sxs-lookup"><span data-stu-id="be280-108">Directive</span></span>                     | <span data-ttu-id="be280-109">Description</span><span class="sxs-lookup"><span data-stu-id="be280-109">Description</span></span>                                                           |
|-------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="be280-110">**\#définition**</span><span class="sxs-lookup"><span data-stu-id="be280-110">**\#define**</span></span>](-define.md)   | <span data-ttu-id="be280-111">Définit un nom spécifié en lui assignant une valeur donnée.</span><span class="sxs-lookup"><span data-stu-id="be280-111">Defines a specified name by assigning it a given value.</span></span>               |
| [<span data-ttu-id="be280-112">**\#elif**</span><span class="sxs-lookup"><span data-stu-id="be280-112">**\#elif**</span></span>](-elif.md)       | <span data-ttu-id="be280-113">Marque une clause facultative d’un bloc de compilation conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="be280-113">Marks an optional clause of a conditional-compilation block.</span></span>          |
| [<span data-ttu-id="be280-114">**\#else**</span><span class="sxs-lookup"><span data-stu-id="be280-114">**\#else**</span></span>](-else.md)       | <span data-ttu-id="be280-115">Marque la dernière clause facultative d’un bloc de compilation conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="be280-115">Marks the last optional clause of a conditional-compilation block.</span></span>    |
| [<span data-ttu-id="be280-116">**\#endif**</span><span class="sxs-lookup"><span data-stu-id="be280-116">**\#endif**</span></span>](-endif.md)     | <span data-ttu-id="be280-117">Marque la fin d’un bloc de compilation conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="be280-117">Marks the end of a conditional-compilation block.</span></span>                     |
| [<span data-ttu-id="be280-118">**\#que**</span><span class="sxs-lookup"><span data-stu-id="be280-118">**\#if**</span></span>](-if.md)           | <span data-ttu-id="be280-119">Compile conditionnellement le script si une expression spécifiée a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="be280-119">Conditionally compiles the script if a specified expression is true.</span></span>  |
| [<span data-ttu-id="be280-120">**\#ifdef**</span><span class="sxs-lookup"><span data-stu-id="be280-120">**\#ifdef**</span></span>](-ifdef.md)     | <span data-ttu-id="be280-121">Compile conditionnellement le script si un nom spécifié est défini.</span><span class="sxs-lookup"><span data-stu-id="be280-121">Conditionally compiles the script if a specified name is defined.</span></span>     |
| [<span data-ttu-id="be280-122">**\#ifndef**</span><span class="sxs-lookup"><span data-stu-id="be280-122">**\#ifndef**</span></span>](-ifndef.md)   | <span data-ttu-id="be280-123">Compile conditionnellement le script si un nom spécifié n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="be280-123">Conditionally compiles the script if a specified name is not defined.</span></span> |
| [<span data-ttu-id="be280-124">**\#inclusion**</span><span class="sxs-lookup"><span data-stu-id="be280-124">**\#include**</span></span>](-include.md) | <span data-ttu-id="be280-125">Copie le contenu d’un fichier dans le fichier de définition de ressource.</span><span class="sxs-lookup"><span data-stu-id="be280-125">Copies the contents of a file into the resource-definition file.</span></span>      |
| [<span data-ttu-id="be280-126">**\#undef**</span><span class="sxs-lookup"><span data-stu-id="be280-126">**\#undef**</span></span>](-undef.md)     | <span data-ttu-id="be280-127">Supprime la définition du nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="be280-127">Removes the definition of the specified name.</span></span>                         |



 

<span data-ttu-id="be280-128">Pour définir des symboles pour vos identificateurs de ressource, utilisez la directive **\# define** pour les définir dans un fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="be280-128">To define symbols for your resource identifiers, use the **\#define** directive to define them in a header file.</span></span> <span data-ttu-id="be280-129">Incluez cet en-tête dans le script de ressources et le code source de votre application.</span><span class="sxs-lookup"><span data-stu-id="be280-129">Include this header both in the resource script and your application source code.</span></span> <span data-ttu-id="be280-130">De même, vous définissez les valeurs des attributs de ressource et des styles en incluant Windows. h dans le script de ressources.</span><span class="sxs-lookup"><span data-stu-id="be280-130">Similarly, you define the values for resource attributes and styles by including Windows.h in the resource script.</span></span>

<span data-ttu-id="be280-131">RC traite les fichiers avec les extensions. c et. h d’une manière spéciale.</span><span class="sxs-lookup"><span data-stu-id="be280-131">RC treats files with the .c and .h extensions in a special manner.</span></span> <span data-ttu-id="be280-132">Il part du principe qu’un fichier avec l’une de ces extensions ne contient pas de ressources.</span><span class="sxs-lookup"><span data-stu-id="be280-132">It assumes that a file with one of these extensions does not contain resources.</span></span> <span data-ttu-id="be280-133">Si un fichier a l’extension de nom de fichier. c ou. h, RC ignore toutes les lignes du fichier, à l’exception des directives de préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="be280-133">If a file has the .c or .h file name extension, RC ignores all lines in the file except the preprocessor directives.</span></span> <span data-ttu-id="be280-134">Par conséquent, pour inclure un fichier qui contient des ressources dans un autre script de ressources, indiquez au fichier d’inclure une extension autre que. c ou. h.</span><span class="sxs-lookup"><span data-stu-id="be280-134">Therefore, to include a file that contains resources in another resource script, give the file to be included an extension other than .c or .h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be280-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be280-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be280-136">Directives pragma</span><span class="sxs-lookup"><span data-stu-id="be280-136">Pragma Directives</span></span>](pragma-directives.md)
</dt> </dl>

 

 




