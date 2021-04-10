---
title: À propos des types de données .NET Framework
description: À propos des types de données .NET Framework
ms.assetid: 8683888b-889f-4ab2-8eab-dbb79735f13f
keywords:
- Lecteur Windows Media,. NET Framework
- Windows Media Player Object Model, .NET Framework
- modèle objet, .NET Framework
- Windows Media Player Mobile, .NET Framework
- Contrôle ActiveX du lecteur Windows Media, .NET Framework
- Contrôle ActiveX mobile du lecteur Windows Media, .NET Framework
- Contrôle ActiveX, .NET Framework
- .NET Framework, types de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8774f4ee4521628a05bf766c50c8c7609c1107
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029710"
---
# <a name="about-net-framework-data-types"></a><span data-ttu-id="d1897-111">À propos des types de données .NET Framework</span><span class="sxs-lookup"><span data-stu-id="d1897-111">About .NET Framework Data Types</span></span>

<span data-ttu-id="d1897-112">Cette section contient les informations dont vous avez besoin pour traduire la référence du modèle objet orienté script en types de données de base Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="d1897-112">This section contains the information you need to translate the script-oriented Object Model Reference into Microsoft .NET Framework base data types.</span></span> <span data-ttu-id="d1897-113">La référence du script du lecteur Windows Media a presque toutes les informations dont vous avez besoin pour utiliser le contrôle du lecteur Windows Media dans un programme .NET Framework. dans la plupart des cas, la syntaxe sera similaire à celle des autres langages de script tels que Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="d1897-113">The Windows Media Player script reference has almost all the information you need to use the Windows Media Player control in a .NET Framework-based program, and in most cases, the syntax will be similar to that of other scripting languages such as Microsoft JScript.</span></span>

<span data-ttu-id="d1897-114">La référence du lecteur Windows Media fournit le type de données JScript et, si nécessaire, la conversion C++.</span><span class="sxs-lookup"><span data-stu-id="d1897-114">The Windows Media Player reference provides the JScript data type and, if necessary, the C++ conversion.</span></span> <span data-ttu-id="d1897-115">Par exemple, un **nombre** peut être retourné par une méthode.</span><span class="sxs-lookup"><span data-stu-id="d1897-115">For example, a **Number** might be returned by a method.</span></span> <span data-ttu-id="d1897-116">JScript traite tous les nombres de la même manière, mais d’autres langages distinguent les différents types de nombres (entier, virgule flottante, etc.).</span><span class="sxs-lookup"><span data-stu-id="d1897-116">JScript treats all numbers in the same way, but other languages distinguish between different types of numbers (integer, floating point, and so on).</span></span> <span data-ttu-id="d1897-117">La référence fournit la conversion C++ pour les types de données numériques, car les nombres peuvent être traités différemment par C++.</span><span class="sxs-lookup"><span data-stu-id="d1897-117">The reference gives the C++ conversion for number data types because numbers can be processed differently by C++.</span></span> <span data-ttu-id="d1897-118">Par exemple, C++ utilise le type de données **int** pour les opérations arithmétiques sur les entiers et **float** pour la virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="d1897-118">For example, C++ uses the **int** data type for integer arithmetic and **float** for floating point.</span></span>

<span data-ttu-id="d1897-119">Le .NET Framework utilise un système de types de données de base légèrement différent.</span><span class="sxs-lookup"><span data-stu-id="d1897-119">The .NET Framework uses a slightly different system of base data types.</span></span> <span data-ttu-id="d1897-120">Le tableau suivant présente les différences entre les types de données courants que vous êtes susceptible d’utiliser.</span><span class="sxs-lookup"><span data-stu-id="d1897-120">The following table shows the differences in the common data types you are likely to use.</span></span> <span data-ttu-id="d1897-121">Pour plus d’informations sur les types de données de base .NET Framework et la conversion vers d’autres systèmes de type de données, consultez le Guide du développeur .NET Framework présentation des types de données de base de l’espace de noms System.</span><span class="sxs-lookup"><span data-stu-id="d1897-121">For more information on .NET Framework base data types and the conversion to other data type systems, see the .NET Framework Developer's Guide discussion of System Namespace base data types.</span></span>

<span data-ttu-id="d1897-122">Ce tableau indique le nom de la classe .NET Framework et le type de données C#.</span><span class="sxs-lookup"><span data-stu-id="d1897-122">This table gives the .NET Framework class name and the C# data type.</span></span> <span data-ttu-id="d1897-123">Les types de données pour d’autres langages sont définis pour chaque langue dans leurs références de langue respectives.</span><span class="sxs-lookup"><span data-stu-id="d1897-123">Data types for other languages are defined for each language in their respective language references.</span></span>



| <span data-ttu-id="d1897-124">Type de données de script</span><span class="sxs-lookup"><span data-stu-id="d1897-124">Script data type</span></span> | <span data-ttu-id="d1897-125">Type de données C++</span><span class="sxs-lookup"><span data-stu-id="d1897-125">C++ data type</span></span>     | <span data-ttu-id="d1897-126">.NET Framework, classe (type de données C#)</span><span class="sxs-lookup"><span data-stu-id="d1897-126">.NET Framework class (C# data type )</span></span> |
|------------------|-------------------|---------------------------------------|
| <span data-ttu-id="d1897-127">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d1897-127">**Number**</span></span>       | <span data-ttu-id="d1897-128">**int**</span><span class="sxs-lookup"><span data-stu-id="d1897-128">**int**</span></span>           | <span data-ttu-id="d1897-129">**Int32** (**entier**)</span><span class="sxs-lookup"><span data-stu-id="d1897-129">**Int32** (**int**)</span></span>                   |
| <span data-ttu-id="d1897-130">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d1897-130">**Number**</span></span>       | <span data-ttu-id="d1897-131">**long**</span><span class="sxs-lookup"><span data-stu-id="d1897-131">**long**</span></span>          | <span data-ttu-id="d1897-132">**Int32** (**entier**)</span><span class="sxs-lookup"><span data-stu-id="d1897-132">**Int32** (**int**)</span></span>                   |
| <span data-ttu-id="d1897-133">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d1897-133">**Number**</span></span>       | <span data-ttu-id="d1897-134">**double**</span><span class="sxs-lookup"><span data-stu-id="d1897-134">**double**</span></span>        | <span data-ttu-id="d1897-135">**Double** (**double**)</span><span class="sxs-lookup"><span data-stu-id="d1897-135">**Double** (**double**)</span></span>               |
| <span data-ttu-id="d1897-136">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d1897-136">**Number**</span></span>       | <span data-ttu-id="d1897-137">**float**</span><span class="sxs-lookup"><span data-stu-id="d1897-137">**float**</span></span>         | <span data-ttu-id="d1897-138">**Single** (**float**)</span><span class="sxs-lookup"><span data-stu-id="d1897-138">**Single** (**float**)</span></span>                |
| <span data-ttu-id="d1897-139">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1897-139">**String**</span></span>       | <span data-ttu-id="d1897-140">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="d1897-140">**BSTR**</span></span>          | <span data-ttu-id="d1897-141">**Chaîne** (**String**)</span><span class="sxs-lookup"><span data-stu-id="d1897-141">**String** (**string**)</span></span>               |
| <span data-ttu-id="d1897-142">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="d1897-142">**Boolean**</span></span>      | <span data-ttu-id="d1897-143">**VARIANT \_ booléen**</span><span class="sxs-lookup"><span data-stu-id="d1897-143">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="d1897-144">**Boolean** (**booléen**)</span><span class="sxs-lookup"><span data-stu-id="d1897-144">**Boolean** (**bool**)</span></span>                |
| <span data-ttu-id="d1897-145">**Object**</span><span class="sxs-lookup"><span data-stu-id="d1897-145">**Object**</span></span>       | <span data-ttu-id="d1897-146">**Object**</span><span class="sxs-lookup"><span data-stu-id="d1897-146">**Object**</span></span>        | <span data-ttu-id="d1897-147">**Object** (**objet**)</span><span class="sxs-lookup"><span data-stu-id="d1897-147">**Object** (**object**)</span></span>               |



 

<span data-ttu-id="d1897-148">Si vous utilisez Visual Studio, vous pouvez utiliser la technologie Microsoft IntelliSense pour déterminer le type de données attendu pour une fonction spécifique.</span><span class="sxs-lookup"><span data-stu-id="d1897-148">If you are using Visual Studio, you can use the Microsoft IntelliSense technology to determine what data type is expected for a specific function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1897-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d1897-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1897-150">**Intégration du contrôle du lecteur Windows Media dans une solution .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="d1897-150">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[<span data-ttu-id="d1897-151">**Référence du modèle objet pour l’écriture de scripts**</span><span class="sxs-lookup"><span data-stu-id="d1897-151">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




