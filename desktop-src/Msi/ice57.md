---
description: ICE57 valide le fait que les composants individuels ne mélangent pas les données par ordinateur et par utilisateur. Cette action personnalisée ICE vérifie les entrées de Registre, les fichiers, les chemins d’accès aux clés de répertoire et les raccourcis non publiés.
ms.assetid: 3c82efa7-9cf3-4bcd-8ec4-b81d1d7aa0a6
title: ICE57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a59d609e5d7de0011666be0b5cc5e76417d8e67d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204189"
---
# <a name="ice57"></a><span data-ttu-id="ff06d-104">ICE57</span><span class="sxs-lookup"><span data-stu-id="ff06d-104">ICE57</span></span>

<span data-ttu-id="ff06d-105">ICE57 valide le fait que les composants individuels ne mélangent pas les données par ordinateur et par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ff06d-105">ICE57 validates that individual components do not mix per-machine and per-user data.</span></span> <span data-ttu-id="ff06d-106">Cette action personnalisée ICE vérifie les entrées de Registre, les fichiers, les chemins d’accès aux clés de répertoire et les raccourcis non publiés.</span><span class="sxs-lookup"><span data-stu-id="ff06d-106">This ICE custom action checks registry entries, files, directory key paths, and non-advertised shortcuts.</span></span>

<span data-ttu-id="ff06d-107">La combinaison de données par utilisateur et par ordinateur dans le même composant peut entraîner une installation partielle du composant pour certains utilisateurs dans un environnement multi-utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ff06d-107">Mixing per-user and per-machine data in the same component could result in only partial installation of the component for some users in a multi-user environment.</span></span>

<span data-ttu-id="ff06d-108">Consultez la propriété [**ALLUSERS**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="ff06d-108">See the [**ALLUSERS**](allusers.md) property.</span></span>

## <a name="result"></a><span data-ttu-id="ff06d-109">Résultats</span><span class="sxs-lookup"><span data-stu-id="ff06d-109">Result</span></span>

<span data-ttu-id="ff06d-110">ICE57 publie une erreur s’il trouve un composant contenant à la fois des entrées de Registre par ordinateur et par utilisateur, des fichiers, des chemins d’accès de clé de répertoire ou des raccourcis non publiés.</span><span class="sxs-lookup"><span data-stu-id="ff06d-110">ICE57 posts an error if it finds any component that contains both a per-machine and per-user registry entries, files, directory key paths, or non-advertised shortcuts.</span></span>

## <a name="example"></a><span data-ttu-id="ff06d-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="ff06d-111">Example</span></span>

<span data-ttu-id="ff06d-112">ICE57reports les erreurs suivantes pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="ff06d-112">ICE57reports the following errors for the example shown.</span></span>

``` syntax
Component 'Component1' has both per-user and per-machine 
    data with a per-machine KeyPath. 
 
WARNING: Component 'Component2' has both per-user and 
    per-machine data with an HKCU Registry KeyPath. 
 
Component 'Component3' has a registry entry that 
    can be either per-user or per-machine and a per-machine KeyPath. 
 
Component 'Component4' has both per-user data and 
    a keypath that can be either per-user or per-machine.
```

<span data-ttu-id="ff06d-113">[Table des composants](component-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="ff06d-113">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="ff06d-114">Composant</span><span class="sxs-lookup"><span data-stu-id="ff06d-114">Component</span></span>  | <span data-ttu-id="ff06d-115">Répertoire</span><span class="sxs-lookup"><span data-stu-id="ff06d-115">Directory</span></span>  | <span data-ttu-id="ff06d-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="ff06d-116">Attributes</span></span> | <span data-ttu-id="ff06d-117">KeyPath</span><span class="sxs-lookup"><span data-stu-id="ff06d-117">KeyPath</span></span> |
|------------|------------|------------|---------|
| <span data-ttu-id="ff06d-118">Composant1</span><span class="sxs-lookup"><span data-stu-id="ff06d-118">Component1</span></span> | <span data-ttu-id="ff06d-119">Annuaire</span><span class="sxs-lookup"><span data-stu-id="ff06d-119">DirectoryA</span></span> | <span data-ttu-id="ff06d-120">0</span><span class="sxs-lookup"><span data-stu-id="ff06d-120">0</span></span>          | <span data-ttu-id="ff06d-121">Filea</span><span class="sxs-lookup"><span data-stu-id="ff06d-121">FileA</span></span>   |
| <span data-ttu-id="ff06d-122">Component2</span><span class="sxs-lookup"><span data-stu-id="ff06d-122">Component2</span></span> | <span data-ttu-id="ff06d-123">Annuaire</span><span class="sxs-lookup"><span data-stu-id="ff06d-123">DirectoryA</span></span> | <span data-ttu-id="ff06d-124">4</span><span class="sxs-lookup"><span data-stu-id="ff06d-124">4</span></span>          | <span data-ttu-id="ff06d-125">RegKeyB</span><span class="sxs-lookup"><span data-stu-id="ff06d-125">RegKeyB</span></span> |
| <span data-ttu-id="ff06d-126">Component3</span><span class="sxs-lookup"><span data-stu-id="ff06d-126">Component3</span></span> | <span data-ttu-id="ff06d-127">Annuaire</span><span class="sxs-lookup"><span data-stu-id="ff06d-127">DirectoryA</span></span> | <span data-ttu-id="ff06d-128">0</span><span class="sxs-lookup"><span data-stu-id="ff06d-128">0</span></span>          | <span data-ttu-id="ff06d-129">FileC</span><span class="sxs-lookup"><span data-stu-id="ff06d-129">FileC</span></span>   |
| <span data-ttu-id="ff06d-130">Component4</span><span class="sxs-lookup"><span data-stu-id="ff06d-130">Component4</span></span> | <span data-ttu-id="ff06d-131">Annuaire</span><span class="sxs-lookup"><span data-stu-id="ff06d-131">DirectoryA</span></span> | <span data-ttu-id="ff06d-132">4</span><span class="sxs-lookup"><span data-stu-id="ff06d-132">4</span></span>          | <span data-ttu-id="ff06d-133">RegKeyD</span><span class="sxs-lookup"><span data-stu-id="ff06d-133">RegKeyD</span></span> |



 

<span data-ttu-id="ff06d-134">[Table du Registre](registry-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="ff06d-134">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="ff06d-135">Registre</span><span class="sxs-lookup"><span data-stu-id="ff06d-135">Registry</span></span> | <span data-ttu-id="ff06d-136">Root</span><span class="sxs-lookup"><span data-stu-id="ff06d-136">Root</span></span> | <span data-ttu-id="ff06d-137">-\_</span><span class="sxs-lookup"><span data-stu-id="ff06d-137">Component\_</span></span> |
|----------|------|-------------|
| <span data-ttu-id="ff06d-138">RegKeyA</span><span class="sxs-lookup"><span data-stu-id="ff06d-138">RegKeyA</span></span>  | <span data-ttu-id="ff06d-139">1</span><span class="sxs-lookup"><span data-stu-id="ff06d-139">1</span></span>    | <span data-ttu-id="ff06d-140">Composant1</span><span class="sxs-lookup"><span data-stu-id="ff06d-140">Component1</span></span>  |
| <span data-ttu-id="ff06d-141">RegKeyB</span><span class="sxs-lookup"><span data-stu-id="ff06d-141">RegKeyB</span></span>  | <span data-ttu-id="ff06d-142">1</span><span class="sxs-lookup"><span data-stu-id="ff06d-142">1</span></span>    | <span data-ttu-id="ff06d-143">Component2</span><span class="sxs-lookup"><span data-stu-id="ff06d-143">Component2</span></span>  |
| <span data-ttu-id="ff06d-144">RegKeyC</span><span class="sxs-lookup"><span data-stu-id="ff06d-144">RegKeyC</span></span>  | <span data-ttu-id="ff06d-145">-1</span><span class="sxs-lookup"><span data-stu-id="ff06d-145">-1</span></span>   | <span data-ttu-id="ff06d-146">Component3</span><span class="sxs-lookup"><span data-stu-id="ff06d-146">Component3</span></span>  |
| <span data-ttu-id="ff06d-147">RegKeyD</span><span class="sxs-lookup"><span data-stu-id="ff06d-147">RegKeyD</span></span>  | <span data-ttu-id="ff06d-148">-1</span><span class="sxs-lookup"><span data-stu-id="ff06d-148">-1</span></span>   | <span data-ttu-id="ff06d-149">Component4</span><span class="sxs-lookup"><span data-stu-id="ff06d-149">Component4</span></span>  |



 

<span data-ttu-id="ff06d-150">[Table de fichiers](file-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="ff06d-150">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="ff06d-151">Fichier</span><span class="sxs-lookup"><span data-stu-id="ff06d-151">File</span></span>  | <span data-ttu-id="ff06d-152">-\_</span><span class="sxs-lookup"><span data-stu-id="ff06d-152">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="ff06d-153">Filea</span><span class="sxs-lookup"><span data-stu-id="ff06d-153">FileA</span></span> | <span data-ttu-id="ff06d-154">Composant1</span><span class="sxs-lookup"><span data-stu-id="ff06d-154">Component1</span></span>  |
| <span data-ttu-id="ff06d-155">FileB</span><span class="sxs-lookup"><span data-stu-id="ff06d-155">FileB</span></span> | <span data-ttu-id="ff06d-156">Component2</span><span class="sxs-lookup"><span data-stu-id="ff06d-156">Component2</span></span>  |
| <span data-ttu-id="ff06d-157">FileC</span><span class="sxs-lookup"><span data-stu-id="ff06d-157">FileC</span></span> | <span data-ttu-id="ff06d-158">Component3</span><span class="sxs-lookup"><span data-stu-id="ff06d-158">Component3</span></span>  |
| <span data-ttu-id="ff06d-159">Classer</span><span class="sxs-lookup"><span data-stu-id="ff06d-159">FileD</span></span> | <span data-ttu-id="ff06d-160">Component4</span><span class="sxs-lookup"><span data-stu-id="ff06d-160">Component4</span></span>  |



 

[<span data-ttu-id="ff06d-161">Table de répertoire</span><span class="sxs-lookup"><span data-stu-id="ff06d-161">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="ff06d-162">Répertoire</span><span class="sxs-lookup"><span data-stu-id="ff06d-162">Directory</span></span>  | <span data-ttu-id="ff06d-163">Répertoire \_ parent</span><span class="sxs-lookup"><span data-stu-id="ff06d-163">Directory\_Parent</span></span> | <span data-ttu-id="ff06d-164">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="ff06d-164">DefaultDir</span></span> |
|------------|-------------------|------------|
| <span data-ttu-id="ff06d-165">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="ff06d-165">TARGETDIR</span></span>  |                   | <span data-ttu-id="ff06d-166">SourceDir</span><span class="sxs-lookup"><span data-stu-id="ff06d-166">SourceDir</span></span>  |
| <span data-ttu-id="ff06d-167">Annuaire</span><span class="sxs-lookup"><span data-stu-id="ff06d-167">DirectoryA</span></span> | <span data-ttu-id="ff06d-168">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="ff06d-168">TARGETDIR</span></span>         | <span data-ttu-id="ff06d-169">Annuaire</span><span class="sxs-lookup"><span data-stu-id="ff06d-169">DirectoryA</span></span> |



 

<span data-ttu-id="ff06d-170">Pour résoudre les erreurs, réorganisez l’application de sorte que chaque composant ne contienne que les ressources par utilisateur ou par ordinateur, et non les deux.</span><span class="sxs-lookup"><span data-stu-id="ff06d-170">To fix the errors, reorganize the application such that each component contains only per-user or per-machine resources, and not both.</span></span>

<span data-ttu-id="ff06d-171">Le premier message d’erreur est publié, car Composant1 contient Filea (par ordinateur) et la clé de Registre HKCU RegKeyA (Per User).</span><span class="sxs-lookup"><span data-stu-id="ff06d-171">The first error message is posted because Component1 contains FileA (per-machine) and the HKCU registry key RegKeyA (per user).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff06d-172">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ff06d-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff06d-173">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="ff06d-173">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



