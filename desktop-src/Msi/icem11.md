---
description: ICEM11 vérifie qu’un module de fusion configurable répertorie la table ModuleConfiguration et la table ModuleSubstitution dans la table ModuleIgnoreTable du module.
ms.assetid: f0199137-0a40-40ca-b3cf-ff8eef4309cc
title: ICEM11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403a36435ce2367fc356934740e6d022f5457698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203778"
---
# <a name="icem11"></a><span data-ttu-id="7f811-103">ICEM11</span><span class="sxs-lookup"><span data-stu-id="7f811-103">ICEM11</span></span>

<span data-ttu-id="7f811-104">ICEM11 vérifie qu’un module de fusion configurable répertorie la [table ModuleConfiguration](moduleconfiguration-table.md) et la [table ModuleSubstitution](modulesubstitution-table.md) dans la [table ModuleIgnoreTable](moduleignoretable-table.md) du module.</span><span class="sxs-lookup"><span data-stu-id="7f811-104">ICEM11 verifies that a Configurable Merge Module lists the [ModuleConfiguration table](moduleconfiguration-table.md) and [ModuleSubstitution table](modulesubstitution-table.md) in the [ModuleIgnoreTable table](moduleignoretable-table.md) of the module.</span></span> <span data-ttu-id="7f811-105">Cela permet de s’assurer que les outils de fusion qui ne reconnaissent pas les modules de fusion configurables (inférieurs à la version 2,0) ne copient pas ces tables dans la base de données cible.</span><span class="sxs-lookup"><span data-stu-id="7f811-105">This ensures that merge tools that do not recognize configurable merge modules(less than version 2.0) do not copy these tables into the target database.</span></span>

<span data-ttu-id="7f811-106">Ce ICEM est disponible dans le fichier Mergemod. CUB fourni dans le kit de développement logiciel (SDK) Windows Installer 2,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7f811-106">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="7f811-107">Pour plus d’informations, consultez [SDK Windows Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="7f811-107">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="7f811-108">Résultats</span><span class="sxs-lookup"><span data-stu-id="7f811-108">Result</span></span>

<span data-ttu-id="7f811-109">ICEM11 publie une erreur si le module contient une table ModuleConfiguration ou ModuleSubstitution non listée dans le tableau ModuleIgnoreTable.</span><span class="sxs-lookup"><span data-stu-id="7f811-109">ICEM11 posts an error if the module contains a ModuleConfiguration or ModuleSubstitution table not listed in the ModuleIgnoreTable table.</span></span>

## <a name="example"></a><span data-ttu-id="7f811-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="7f811-110">Example</span></span>

<span data-ttu-id="7f811-111">ICEM11 publie les messages d’erreur suivants pour un module contenant les entrées de base de données présentées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7f811-111">ICEM11 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
Error The module contains a ModuleConfiguration or ModuleSubstitution 
table. These tables must be listed in the ModuleIgnoreTable table.
```

<span data-ttu-id="7f811-112">[ModuleConfiguration](moduleconfiguration-table.md) (partiel)</span><span class="sxs-lookup"><span data-stu-id="7f811-112">[ModuleConfiguration](moduleconfiguration-table.md) (partial)</span></span>



| <span data-ttu-id="7f811-113">Nom</span><span class="sxs-lookup"><span data-stu-id="7f811-113">Name</span></span>     | <span data-ttu-id="7f811-114">Format</span><span class="sxs-lookup"><span data-stu-id="7f811-114">Format</span></span> | <span data-ttu-id="7f811-115">Type</span><span class="sxs-lookup"><span data-stu-id="7f811-115">Type</span></span>   | <span data-ttu-id="7f811-116">ContextData</span><span class="sxs-lookup"><span data-stu-id="7f811-116">ContextData</span></span> | <span data-ttu-id="7f811-117">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7f811-117">DefaultValue</span></span> |
|----------|--------|--------|-------------|--------------|
| <span data-ttu-id="7f811-118">IconKey1</span><span class="sxs-lookup"><span data-stu-id="7f811-118">IconKey1</span></span> | <span data-ttu-id="7f811-119">1</span><span class="sxs-lookup"><span data-stu-id="7f811-119">1</span></span>      | <span data-ttu-id="7f811-120">Binary</span><span class="sxs-lookup"><span data-stu-id="7f811-120">Binary</span></span> | <span data-ttu-id="7f811-121">Icône</span><span class="sxs-lookup"><span data-stu-id="7f811-121">Icon</span></span>        | <span data-ttu-id="7f811-122">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="7f811-122">DefaultIcon</span></span>  |



 

[<span data-ttu-id="7f811-123">ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="7f811-123">ModuleSubstitution</span></span>](modulesubstitution-table.md)



| <span data-ttu-id="7f811-124">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="7f811-124">Table</span></span>   | <span data-ttu-id="7f811-125">Ligne</span><span class="sxs-lookup"><span data-stu-id="7f811-125">Row</span></span>              | <span data-ttu-id="7f811-126">Colonne</span><span class="sxs-lookup"><span data-stu-id="7f811-126">Column</span></span> | <span data-ttu-id="7f811-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f811-127">Value</span></span>        |
|---------|------------------|--------|--------------|
| <span data-ttu-id="7f811-128">Contrôler</span><span class="sxs-lookup"><span data-stu-id="7f811-128">Control</span></span> | <span data-ttu-id="7f811-129">Dialog1; Control1</span><span class="sxs-lookup"><span data-stu-id="7f811-129">Dialog1;Control1</span></span> | <span data-ttu-id="7f811-130">Texte</span><span class="sxs-lookup"><span data-stu-id="7f811-130">Text</span></span>   | <span data-ttu-id="7f811-131">\[IconKey1\]</span><span class="sxs-lookup"><span data-stu-id="7f811-131">\[IconKey1\]</span></span> |



 

[<span data-ttu-id="7f811-132">ModuleIgnoreTable</span><span class="sxs-lookup"><span data-stu-id="7f811-132">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)



| <span data-ttu-id="7f811-133">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="7f811-133">Table</span></span>               |
|---------------------|
| <span data-ttu-id="7f811-134">ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f811-134">ModuleConfiguration</span></span> |



 

<span data-ttu-id="7f811-135">Pour corriger cette erreur, vous pouvez inclure les tables ModuleSubstitution et ModuleConfiguration dans la table ModuleIgnoreTable.</span><span class="sxs-lookup"><span data-stu-id="7f811-135">To fix this error include both the ModuleSubstitution and ModuleConfiguration tables in the ModuleIgnoreTable table.</span></span>

## <a name="table-used-during-execution"></a><span data-ttu-id="7f811-136">Table utilisée pendant l’exécution</span><span class="sxs-lookup"><span data-stu-id="7f811-136">Table Used During Execution</span></span>

[<span data-ttu-id="7f811-137">ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="7f811-137">ModuleSubstitution</span></span>](modulesubstitution-table.md)

[<span data-ttu-id="7f811-138">ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f811-138">ModuleConfiguration</span></span>](moduleconfiguration-table.md)

[<span data-ttu-id="7f811-139">ModuleIgnoreTable</span><span class="sxs-lookup"><span data-stu-id="7f811-139">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)

## <a name="related-topics"></a><span data-ttu-id="7f811-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7f811-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f811-141">Référence ICE du module de fusion</span><span class="sxs-lookup"><span data-stu-id="7f811-141">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



