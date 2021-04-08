---
description: ICE92 vérifie qu’un composant sans GUID d’ID de composant n’est pas également spécifié en tant que composant permanent.
ms.assetid: 5fe8a844-3f96-4b19-baa6-24e2405aff30
title: ICE92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c9cffdfd7ac30313ed24182d8b4cc94f25900f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866089"
---
# <a name="ice92"></a><span data-ttu-id="c6d27-103">ICE92</span><span class="sxs-lookup"><span data-stu-id="c6d27-103">ICE92</span></span>

<span data-ttu-id="c6d27-104">ICE92 vérifie qu’un composant sans GUID d’ID de composant n’est pas également spécifié en tant que composant permanent.</span><span class="sxs-lookup"><span data-stu-id="c6d27-104">ICE92 verifies that a component without a Component Id GUID is not also specified as a permanent component.</span></span> <span data-ttu-id="c6d27-105">Cette action personnalisée ICE vérifie la [table](component-table.md) des composants pour rechercher les composants sans [GUID](guid.md) spécifié dans le champ ComponentID et vérifie que l’indicateur **msidbComponentAttributesPermanent** n’a pas été défini dans le champ attributs.</span><span class="sxs-lookup"><span data-stu-id="c6d27-105">This ICE custom action checks the [Component Table](component-table.md) for components without a [GUID](guid.md) specified in the ComponentId field and verifies that the **msidbComponentAttributesPermanent** flag has not been set in the Attributes field.</span></span> <span data-ttu-id="c6d27-106">ICE92 vérifie également qu’aucun composant n’a à la fois les attributs **msidbComponentAttributesPermanent** et **msidbComponentAttributesUninstallOnSupersedence** .</span><span class="sxs-lookup"><span data-stu-id="c6d27-106">ICE92 also verifies that no component has both the **msidbComponentAttributesPermanent** and **msidbComponentAttributesUninstallOnSupersedence** attributes.</span></span>

<span data-ttu-id="c6d27-107">Si la colonne ComponentId a la valeur null, le programme d’installation n’inscrit pas le composant et le composant ne peut pas être supprimé ou réparé par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="c6d27-107">If the ComponentId column is null, the installer does not register the component and the component cannot be removed or repaired by the installer.</span></span>

## <a name="result"></a><span data-ttu-id="c6d27-108">Résultats</span><span class="sxs-lookup"><span data-stu-id="c6d27-108">Result</span></span>

<span data-ttu-id="c6d27-109">ICE92 publie l’erreur suivante.</span><span class="sxs-lookup"><span data-stu-id="c6d27-109">ICE92 posts the following error.</span></span>



| <span data-ttu-id="c6d27-110">Erreur ICE92</span><span class="sxs-lookup"><span data-stu-id="c6d27-110">ICE92 error</span></span>                                                          | <span data-ttu-id="c6d27-111">Description</span><span class="sxs-lookup"><span data-stu-id="c6d27-111">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d27-112">Le composant' \[ 1 \] 'n’a pas de ComponentID et est marqué comme permanent.</span><span class="sxs-lookup"><span data-stu-id="c6d27-112">The Component '\[1\]' has no ComponentId and is marked as permanent.</span></span> | <span data-ttu-id="c6d27-113">L’entrée de ce composant dans la table des composants a la valeur null dans la colonne ComponentId et contient **msidbComponentAttributesPermanent** dans la colonne attributs.</span><span class="sxs-lookup"><span data-stu-id="c6d27-113">The entry for this component in the Component table has null in the ComponentId column and has **msidbComponentAttributesPermanent** in the Attributes column.</span></span> |



 

<span data-ttu-id="c6d27-114">ICE92 publie l’avertissement suivant.</span><span class="sxs-lookup"><span data-stu-id="c6d27-114">ICE92 posts the following warning.</span></span>



| <span data-ttu-id="c6d27-115">AVERTISSEMENT ICE92</span><span class="sxs-lookup"><span data-stu-id="c6d27-115">ICE92 warning</span></span>                                                                                                                                                           | <span data-ttu-id="c6d27-116">Description</span><span class="sxs-lookup"><span data-stu-id="c6d27-116">Description</span></span>                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d27-117">Le composant « \[ 1 \] » est marqué comme permanent et désinstallation lors du remplacement.</span><span class="sxs-lookup"><span data-stu-id="c6d27-117">The Component '\[1\]' is marked as permanent and uninstall-on-supersedence.</span></span> <span data-ttu-id="c6d27-118">L’attribut Uninstall-on-deremplacement sera ignoré, car le composant est permanent.</span><span class="sxs-lookup"><span data-stu-id="c6d27-118">The uninstall-on-supersedence attribute will be ignored because the component is permanent.</span></span> | <span data-ttu-id="c6d27-119">L’entrée de ce composant dans la [table des composants](component-table.md) a les attributs **msidbComponentAttributesPermanent** et **msidbComponentAttributesUninstallOnSupersedence** spécifiés.</span><span class="sxs-lookup"><span data-stu-id="c6d27-119">The entry for this component in the [Component table](component-table.md) has both the **msidbComponentAttributesPermanent** and **msidbComponentAttributesUninstallOnSupersedence** attributes specified.</span></span> |



 

## <a name="example"></a><span data-ttu-id="c6d27-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="c6d27-120">Example</span></span>

<span data-ttu-id="c6d27-121">ICE92 signale l’erreur suivante pour l’exemple :</span><span class="sxs-lookup"><span data-stu-id="c6d27-121">ICE92 reports the following error for the example:</span></span>

``` syntax
The Component 'Component1' has no ComponentId and is marked as permanent.
```

<span data-ttu-id="c6d27-122">[Table des composants](component-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="c6d27-122">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="c6d27-123">Composant</span><span class="sxs-lookup"><span data-stu-id="c6d27-123">Component</span></span>  | <span data-ttu-id="c6d27-124">ComponentId</span><span class="sxs-lookup"><span data-stu-id="c6d27-124">ComponentId</span></span> | <span data-ttu-id="c6d27-125">Répertoire\_</span><span class="sxs-lookup"><span data-stu-id="c6d27-125">Directory\_</span></span> | <span data-ttu-id="c6d27-126">Attributs</span><span class="sxs-lookup"><span data-stu-id="c6d27-126">Attributes</span></span> | <span data-ttu-id="c6d27-127">KeyPath</span><span class="sxs-lookup"><span data-stu-id="c6d27-127">KeyPath</span></span> |
|------------|-------------|-------------|------------|---------|
| <span data-ttu-id="c6d27-128">Composant1</span><span class="sxs-lookup"><span data-stu-id="c6d27-128">Component1</span></span> |             | <span data-ttu-id="c6d27-129">Annuaire</span><span class="sxs-lookup"><span data-stu-id="c6d27-129">DirectoryA</span></span>  | <span data-ttu-id="c6d27-130">16</span><span class="sxs-lookup"><span data-stu-id="c6d27-130">16</span></span>         | <span data-ttu-id="c6d27-131">Filea</span><span class="sxs-lookup"><span data-stu-id="c6d27-131">FileA</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="c6d27-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c6d27-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6d27-133">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="c6d27-133">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



