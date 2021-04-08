---
description: ICEM06 recherche des références directes non valides aux fonctionnalités par le module.
ms.assetid: 63e63a60-53e5-4881-ad71-efeceb73a70e
title: ICEM06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945d45471ec86605e0fa509fc1855aa1cfd5d698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865762"
---
# <a name="icem06"></a><span data-ttu-id="60ad8-103">ICEM06</span><span class="sxs-lookup"><span data-stu-id="60ad8-103">ICEM06</span></span>

<span data-ttu-id="60ad8-104">ICEM06 recherche des références directes non valides aux fonctionnalités par le module.</span><span class="sxs-lookup"><span data-stu-id="60ad8-104">ICEM06 checks for invalid direct references to features by the module.</span></span>

<span data-ttu-id="60ad8-105">Le module de fusion CIEM est stocké dans un fichier de module de fusion. CUB appelé Mergemod. CUB et non dans le fichier. CUB contenant le CIEM utilisé pour la validation du package.</span><span class="sxs-lookup"><span data-stu-id="60ad8-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="60ad8-106">Résultats</span><span class="sxs-lookup"><span data-stu-id="60ad8-106">Result</span></span>

<span data-ttu-id="60ad8-107">ICEM06 publie une erreur lorsque la base de données du module contient des références directes à une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="60ad8-107">ICEM06 posts an error when the module database contains direct references to a feature.</span></span> <span data-ttu-id="60ad8-108">Les informations sur les fonctionnalités doivent être fournies par l’utilisateur du module.</span><span class="sxs-lookup"><span data-stu-id="60ad8-108">Feature information must be provided by the user of the module.</span></span>

## <a name="example"></a><span data-ttu-id="60ad8-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="60ad8-109">Example</span></span>

<span data-ttu-id="60ad8-110">ICEM06 publie les messages d’erreur suivants pour un module contenant les entrées de base de données présentées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="60ad8-110">ICEM06 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The target of shortcut Shortcut1.GUID1 is not a property and not a null GUID. 
Modules may not directly reference features.
The row GUID2.LocalServer32.Component2 in the Class table has a feature reference 
that is not a null GUID. Modules may not directly reference features.
```

<span data-ttu-id="60ad8-111">[Table de raccourcis](shortcut-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="60ad8-111">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="60ad8-112">Raccourci</span><span class="sxs-lookup"><span data-stu-id="60ad8-112">Shortcut</span></span>          | <span data-ttu-id="60ad8-113">Cible</span><span class="sxs-lookup"><span data-stu-id="60ad8-113">Target</span></span>                                 |
|-------------------|----------------------------------------|
| <span data-ttu-id="60ad8-114">Shortcut1. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="60ad8-114">Shortcut1.*GUID1*</span></span> | <span data-ttu-id="60ad8-115">cmd.exe</span><span class="sxs-lookup"><span data-stu-id="60ad8-115">cmd.exe</span></span>                                |
| <span data-ttu-id="60ad8-116">Shortcut2. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="60ad8-116">Shortcut2.*GUID1*</span></span> | <span data-ttu-id="60ad8-117">\[MyProp\]</span><span class="sxs-lookup"><span data-stu-id="60ad8-117">\[MyProp\]</span></span>                             |
| <span data-ttu-id="60ad8-118">Shortcut3. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="60ad8-118">Shortcut3.*GUID1*</span></span> | {00000000-0000-0000-0000-000000000000} |



 

<span data-ttu-id="60ad8-119">[Table de classe](class-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="60ad8-119">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="60ad8-120">CLSID</span><span class="sxs-lookup"><span data-stu-id="60ad8-120">CLSID</span></span>   | <span data-ttu-id="60ad8-121">Context</span><span class="sxs-lookup"><span data-stu-id="60ad8-121">Context</span></span>       | <span data-ttu-id="60ad8-122">-\_</span><span class="sxs-lookup"><span data-stu-id="60ad8-122">Component\_</span></span> | <span data-ttu-id="60ad8-123">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="60ad8-123">Feature\_</span></span>                              |
|---------|---------------|-------------|----------------------------------------|
| <span data-ttu-id="60ad8-124">*GUID1*</span><span class="sxs-lookup"><span data-stu-id="60ad8-124">*GUID1*</span></span> | <span data-ttu-id="60ad8-125">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="60ad8-125">LocalServer32</span></span> | <span data-ttu-id="60ad8-126">Composant1</span><span class="sxs-lookup"><span data-stu-id="60ad8-126">Component1</span></span>  | {00000000-0000-0000-0000-000000000000} |
| <span data-ttu-id="60ad8-127">*GUID2*</span><span class="sxs-lookup"><span data-stu-id="60ad8-127">*GUID2*</span></span> | <span data-ttu-id="60ad8-128">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="60ad8-128">LocalServer32</span></span> | <span data-ttu-id="60ad8-129">Component2</span><span class="sxs-lookup"><span data-stu-id="60ad8-129">Component2</span></span>  | <span data-ttu-id="60ad8-130">MyFeature</span><span class="sxs-lookup"><span data-stu-id="60ad8-130">MyFeature</span></span>                              |



 

<span data-ttu-id="60ad8-131">ICEM06 signale la première erreur, car le premier enregistrement de la table de raccourcis contient une entrée dans le champ cible qui n’est pas une propriété ou un GUID null.</span><span class="sxs-lookup"><span data-stu-id="60ad8-131">ICEM06 reports the first error because the first record in the Shortcut table has an entry in the Target field that is not a property or a null GUID.</span></span> <span data-ttu-id="60ad8-132">Un module ne peut pas référencer directement une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="60ad8-132">A module cannot reference a feature directly.</span></span> <span data-ttu-id="60ad8-133">Les informations sur les fonctionnalités doivent être fournies par l’utilisateur du module.</span><span class="sxs-lookup"><span data-stu-id="60ad8-133">Feature information must be provided by the user of the module.</span></span> <span data-ttu-id="60ad8-134">Pour corriger cette erreur, les références à une fonctionnalité doivent être remplacées par un GUID null.</span><span class="sxs-lookup"><span data-stu-id="60ad8-134">To fix this error, references to a feature should be replaced by a null GUID.</span></span>

<span data-ttu-id="60ad8-135">ICEM06 signale la deuxième erreur, car le deuxième enregistrement de la table de classe contient une entrée dans le champ Feature qui n’est pas un GUID null.</span><span class="sxs-lookup"><span data-stu-id="60ad8-135">ICEM06 reports the second error because the second record in the Class table has an entry in the Feature field that is not a null GUID.</span></span> <span data-ttu-id="60ad8-136">Un module ne peut pas référencer directement une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="60ad8-136">A module cannot reference a feature directly.</span></span> <span data-ttu-id="60ad8-137">Les informations sur les fonctionnalités doivent être fournies par l’utilisateur du module.</span><span class="sxs-lookup"><span data-stu-id="60ad8-137">Feature information must be provided by the user of the module.</span></span> <span data-ttu-id="60ad8-138">Pour corriger cette erreur, les références à une fonctionnalité doivent être remplacées par un GUID null.</span><span class="sxs-lookup"><span data-stu-id="60ad8-138">To fix this error, references to a feature should be replaced by a null GUID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60ad8-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="60ad8-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60ad8-140">Référence ICE du module de fusion</span><span class="sxs-lookup"><span data-stu-id="60ad8-140">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



