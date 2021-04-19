---
description: ICE62 effectue des vérifications approfondies sur la table IsolatedComponent pour les données susceptibles de provoquer un comportement inattendu.
ms.assetid: 649d3989-8121-4303-aa3e-63bc6649f445
title: ICE62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245e205b2d004efa99ae1605ff5255ef69834a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544975"
---
# <a name="ice62"></a><span data-ttu-id="06026-103">ICE62</span><span class="sxs-lookup"><span data-stu-id="06026-103">ICE62</span></span>

<span data-ttu-id="06026-104">ICE62 effectue des vérifications approfondies sur la [table IsolatedComponent](isolatedcomponent-table.md) pour les données susceptibles de provoquer un comportement inattendu.</span><span class="sxs-lookup"><span data-stu-id="06026-104">ICE62 performs extensive checks on the [IsolatedComponent table](isolatedcomponent-table.md) for data that may cause unexpected behavior.</span></span>

<span data-ttu-id="06026-105">Si vous ne corrigez pas une erreur signalée par ICE62, vous risquez de provoquer une défaillance du système de composants isolés de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="06026-105">Failure to fix an error reported by ICE62 can result in a failure of the isolated component system in a wide variety of ways.</span></span> <span data-ttu-id="06026-106">Par exemple, si le bit SharedDllRefCount n’est pas défini pour un composant partagé, l’inscription du composant peut être supprimée lorsqu’une autre application utilise ce ComponentId et est désinstallée.</span><span class="sxs-lookup"><span data-stu-id="06026-106">For example, if the SharedDllRefCount bit is not set for a shared component, the registration for the component could be removed when another application uses that ComponentId and is uninstalled.</span></span>

## <a name="result"></a><span data-ttu-id="06026-107">Résultats</span><span class="sxs-lookup"><span data-stu-id="06026-107">Result</span></span>

<span data-ttu-id="06026-108">ICE62 publie un avertissement ou une erreur lorsqu’il trouve des données dans la table IsolatedComponent qui peuvent produire un comportement inattendu.</span><span class="sxs-lookup"><span data-stu-id="06026-108">ICE62 posts a warning or error when it finds data in the IsolatedComponent table that may produce unexpected behavior.</span></span>

## <a name="example"></a><span data-ttu-id="06026-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="06026-109">Example</span></span>

<span data-ttu-id="06026-110">ICE62 signale les erreurs et avertissements suivants pour les exemples indiqués.</span><span class="sxs-lookup"><span data-stu-id="06026-110">ICE62 reports the following errors and warning for the examples shown.</span></span>

``` syntax
The component 'Component2' is listed as an isolated application 
component in the IsolatedComponent table, but the key path is not a file.
```

<span data-ttu-id="06026-111">COMPONENT2 est listé comme composant d’application pour l’isolation de Composant1.</span><span class="sxs-lookup"><span data-stu-id="06026-111">Component2 is listed as the application component for the isolation of component1.</span></span> <span data-ttu-id="06026-112">Toutefois, COMPONENT2 a un chemin d’accès de clé de Registre et ne fournit pas de chemin d’accès d’exécutable valide à utiliser pour isoler le composant.</span><span class="sxs-lookup"><span data-stu-id="06026-112">However, Component2 has a registry key path, and does not provide a valid executable path to use to isolate the component.</span></span>

<span data-ttu-id="06026-113">Pour corriger cette erreur, utilisez un autre composant que l’application pour le composant isolé Composant1.</span><span class="sxs-lookup"><span data-stu-id="06026-113">To fix this error, use a different component as the application for the isolated component Component1.</span></span>

``` syntax
The component 'Component1' is listed as an isolated shared component in the 
IsolatedComponent table, but is not marked with the SharedDllRefCount component attribute.
```

<span data-ttu-id="06026-114">Composant1 est listé comme un composant partagé isolé, mais le bit SharedDllRefCount n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="06026-114">Component1 is listed as an isolated shared component, but does not have the SharedDllRefCount bit set.</span></span> <span data-ttu-id="06026-115">Cela peut entraîner une inexactitude de la durée de vie du composant.</span><span class="sxs-lookup"><span data-stu-id="06026-115">This could result in the lifetime of the component being incorrect.</span></span> <span data-ttu-id="06026-116">Si une autre application utilise ce composant (isolé ou non) et qu’elle est désinstallée, l’inscription du composant est supprimée, mais la copie isolée de cette application est conservée.</span><span class="sxs-lookup"><span data-stu-id="06026-116">If another application uses this component (isolated or not) and is uninstalled, the registration for the component is removed but this application's isolated copy remains.</span></span> <span data-ttu-id="06026-117">Cela entraîne des problèmes de réparation et de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="06026-117">This causes repair and uninstall problems.</span></span>

<span data-ttu-id="06026-118">Pour corriger cette erreur, définissez le bit SharedDllRefCount pour le composant.</span><span class="sxs-lookup"><span data-stu-id="06026-118">To fix this error, set the SharedDllRefCount bit for the component.</span></span>

``` syntax
The isolated shared component 'Component1' is not installed by the same feature as 
(or a parent feature of) its isolated application component 'Component2' (which is installed by feature 'Feature2').
```

<span data-ttu-id="06026-119">Composant1 et COMPONENT2 sont installés par différentes fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="06026-119">Component1 and Component2 are installed by different features.</span></span> <span data-ttu-id="06026-120">Composant1 est installé par Feature1 et COMPONENT2 est installé par feature2.</span><span class="sxs-lookup"><span data-stu-id="06026-120">Component1 is installed by Feature1, and Component2 is installed by Feature2.</span></span> <span data-ttu-id="06026-121">Feature1 n’est pas un parent de feature2. par conséquent, il est possible d’installer l’application, mais pas le composant isolé, ce qui rompt l’isolation.</span><span class="sxs-lookup"><span data-stu-id="06026-121">Feature1 is not a parent of Feature2, hence it is possible for the application to be installed but not the isolated component, breaking the isolation.</span></span>

<span data-ttu-id="06026-122">Pour corriger cette erreur, ajoutez une entrée à la table FeatureComponents qui lie Composant1 à la même fonctionnalité que (ou une fonctionnalité parente de) la fonctionnalité qui installe COMPONENT2.</span><span class="sxs-lookup"><span data-stu-id="06026-122">To fix this error, add an entry to the FeatureComponents table linking Component1 to the same feature as (or a parent feature of) the feature that installs Component2.</span></span>

``` syntax
WARNING: The isolated shared component 'Component1' (referenced in the IsolatedComponent table) 
is conditionalized. Isolated shared component conditions should never change from TRUE to FALSE after the first install of the product.
```

<span data-ttu-id="06026-123">Composant1 a une condition dans la table des composants.</span><span class="sxs-lookup"><span data-stu-id="06026-123">Component1 has a condition in the Component table.</span></span> <span data-ttu-id="06026-124">Si cette condition passe de TRUE à FALSe pendant la durée de vie d’une installation sur un ordinateur, le composant isolé peut être orphelin sans les informations d’inscription.</span><span class="sxs-lookup"><span data-stu-id="06026-124">If this condition ever changes from TRUE to FALSE during the lifetime of an installation on a computer, the isolated component could be orphaned without registration information.</span></span>

<span data-ttu-id="06026-125">Pour résoudre cet avertissement, supprimez la condition ou créez la condition de sorte qu’elle ne puisse jamais passer de TRUE à FALSe.</span><span class="sxs-lookup"><span data-stu-id="06026-125">To fix this warning, remove the condition, or author the condition so that it can never change from TRUE to FALSE.</span></span>

``` syntax
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component2') that are installed to the directory 'TARGETDIR'.
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component3') that are installed to the directory 'TARGETDIR'.
```

<span data-ttu-id="06026-126">Composant1 est isolé pour COMPONENT2 et Component3, et les deux composants sont également installés dans le même répertoire.</span><span class="sxs-lookup"><span data-stu-id="06026-126">Component1 is isolated for both Component2 and Component3, and the two components are also installed to the same directory.</span></span> <span data-ttu-id="06026-127">Les applications partagent un composant isolé, mais si une application est supprimée, le composant partagé est également supprimé, ce qui entraîne la perte du composant isolé par les autres applications.</span><span class="sxs-lookup"><span data-stu-id="06026-127">The applications share an isolated component, but if one application is removed the shared component is removed as well causing the other applications to lose the isolated component.</span></span>

<span data-ttu-id="06026-128">Pour résoudre cet avertissement, installez les applications dans différents répertoires ou vérifiez si certaines des applications nécessitent véritablement un composant isolé.</span><span class="sxs-lookup"><span data-stu-id="06026-128">To fix this warning, install the applications to different directories or check whether some of the applications truly require an isolated component.</span></span>

[<span data-ttu-id="06026-129">Table IsolatedComponent</span><span class="sxs-lookup"><span data-stu-id="06026-129">IsolatedComponent Table</span></span>](isolatedcomponent-table.md)



| <span data-ttu-id="06026-130">Composant \_ partagé</span><span class="sxs-lookup"><span data-stu-id="06026-130">Component\_Shared</span></span> | <span data-ttu-id="06026-131">Application de composant \_</span><span class="sxs-lookup"><span data-stu-id="06026-131">Component\_Application</span></span> |
|-------------------|------------------------|
| <span data-ttu-id="06026-132">Composant1</span><span class="sxs-lookup"><span data-stu-id="06026-132">Component1</span></span>        | <span data-ttu-id="06026-133">Component2</span><span class="sxs-lookup"><span data-stu-id="06026-133">Component2</span></span>             |
| <span data-ttu-id="06026-134">Composant1</span><span class="sxs-lookup"><span data-stu-id="06026-134">Component1</span></span>        | <span data-ttu-id="06026-135">Component3</span><span class="sxs-lookup"><span data-stu-id="06026-135">Component3</span></span>             |



 

[<span data-ttu-id="06026-136">Table des composants</span><span class="sxs-lookup"><span data-stu-id="06026-136">Component Table</span></span>](component-table.md)



| <span data-ttu-id="06026-137">Composant</span><span class="sxs-lookup"><span data-stu-id="06026-137">Component</span></span>  | <span data-ttu-id="06026-138">ComponentId</span><span class="sxs-lookup"><span data-stu-id="06026-138">ComponentId</span></span> | <span data-ttu-id="06026-139">Répertoire\_</span><span class="sxs-lookup"><span data-stu-id="06026-139">Directory\_</span></span> | <span data-ttu-id="06026-140">Attributs</span><span class="sxs-lookup"><span data-stu-id="06026-140">Attributes</span></span> | <span data-ttu-id="06026-141">Condition</span><span class="sxs-lookup"><span data-stu-id="06026-141">Condition</span></span>   | <span data-ttu-id="06026-142">KeyPath</span><span class="sxs-lookup"><span data-stu-id="06026-142">KeyPath</span></span>   |
|------------|-------------|-------------|------------|-------------|-----------|
| <span data-ttu-id="06026-143">Composant1</span><span class="sxs-lookup"><span data-stu-id="06026-143">Component1</span></span> |             | <span data-ttu-id="06026-144">Dir1</span><span class="sxs-lookup"><span data-stu-id="06026-144">Dir1</span></span>        | <span data-ttu-id="06026-145">0</span><span class="sxs-lookup"><span data-stu-id="06026-145">0</span></span>          | <span data-ttu-id="06026-146">MYCONDITION</span><span class="sxs-lookup"><span data-stu-id="06026-146">MYCONDITION</span></span> | <span data-ttu-id="06026-147">Fichier1</span><span class="sxs-lookup"><span data-stu-id="06026-147">File1</span></span>     |
| <span data-ttu-id="06026-148">Component2</span><span class="sxs-lookup"><span data-stu-id="06026-148">Component2</span></span> |             | <span data-ttu-id="06026-149">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="06026-149">TARGETDIR</span></span>   | <span data-ttu-id="06026-150">4</span><span class="sxs-lookup"><span data-stu-id="06026-150">4</span></span>          |             | <span data-ttu-id="06026-151">Registry2</span><span class="sxs-lookup"><span data-stu-id="06026-151">Registry2</span></span> |
| <span data-ttu-id="06026-152">Component3</span><span class="sxs-lookup"><span data-stu-id="06026-152">Component3</span></span> |             | <span data-ttu-id="06026-153">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="06026-153">TARGETDIR</span></span>   | <span data-ttu-id="06026-154">0</span><span class="sxs-lookup"><span data-stu-id="06026-154">0</span></span>          |             | <span data-ttu-id="06026-155">Fichier3</span><span class="sxs-lookup"><span data-stu-id="06026-155">File3</span></span>     |



 

[<span data-ttu-id="06026-156">FeatureComponentsTable</span><span class="sxs-lookup"><span data-stu-id="06026-156">FeatureComponentsTable</span></span>](featurecomponents-table.md)



| <span data-ttu-id="06026-157">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="06026-157">Feature\_</span></span> | <span data-ttu-id="06026-158">-\_</span><span class="sxs-lookup"><span data-stu-id="06026-158">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="06026-159">Feature1</span><span class="sxs-lookup"><span data-stu-id="06026-159">Feature1</span></span>  | <span data-ttu-id="06026-160">Composant1</span><span class="sxs-lookup"><span data-stu-id="06026-160">Component1</span></span>  |
| <span data-ttu-id="06026-161">Feature2</span><span class="sxs-lookup"><span data-stu-id="06026-161">Feature2</span></span>  | <span data-ttu-id="06026-162">Component2</span><span class="sxs-lookup"><span data-stu-id="06026-162">Component2</span></span>  |
| <span data-ttu-id="06026-163">Feature1</span><span class="sxs-lookup"><span data-stu-id="06026-163">Feature1</span></span>  | <span data-ttu-id="06026-164">Component3</span><span class="sxs-lookup"><span data-stu-id="06026-164">Component3</span></span>  |



 

<span data-ttu-id="06026-165">[Table des fonctionnalités](feature-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="06026-165">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="06026-166">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="06026-166">Feature</span></span>  | <span data-ttu-id="06026-167">Parent de la fonctionnalité \_</span><span class="sxs-lookup"><span data-stu-id="06026-167">Feature\_Parent</span></span> |
|----------|-----------------|
| <span data-ttu-id="06026-168">Feature1</span><span class="sxs-lookup"><span data-stu-id="06026-168">Feature1</span></span> |                 |
| <span data-ttu-id="06026-169">Feature2</span><span class="sxs-lookup"><span data-stu-id="06026-169">Feature2</span></span> |                 |



 

## <a name="related-topics"></a><span data-ttu-id="06026-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="06026-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06026-171">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="06026-171">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



