---
description: ICE46 recherche des propriétés personnalisées dans les conditions, le texte mis en forme et d’autres emplacements qui diffèrent d’une propriété définie par le système uniquement par la casse d’un ou plusieurs caractères.
ms.assetid: 892d7462-0222-4fa0-b14c-17742a266c0a
title: ICE46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e24a76560b02a3a0ce3afa681c7ba74fcc7a2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756225"
---
# <a name="ice46"></a><span data-ttu-id="b6755-103">ICE46</span><span class="sxs-lookup"><span data-stu-id="b6755-103">ICE46</span></span>

<span data-ttu-id="b6755-104">ICE46 recherche des propriétés personnalisées dans les conditions, le texte mis en forme et d’autres emplacements qui diffèrent d’une propriété définie par le système uniquement par la casse d’un ou plusieurs caractères.</span><span class="sxs-lookup"><span data-stu-id="b6755-104">ICE46 checks for custom properties in conditions, formatted text, and other locations that differ from a system defined property only by the case of one or more characters.</span></span>

## <a name="result"></a><span data-ttu-id="b6755-105">Résultats</span><span class="sxs-lookup"><span data-stu-id="b6755-105">Result</span></span>

<span data-ttu-id="b6755-106">ICE46 publie un message d’information s’il existe une propriété personnalisée dans une condition, du texte mis en forme et d’autres emplacements qui diffèrent des propriétés définies par le système uniquement dans le cas d’un ou plusieurs caractères.</span><span class="sxs-lookup"><span data-stu-id="b6755-106">ICE46 posts an informational message if there is a custom property in a condition, formatted text, and other location that differs from a system defined properties only in the case of one or more characters.</span></span>

## <a name="example"></a><span data-ttu-id="b6755-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="b6755-107">Example</span></span>

<span data-ttu-id="b6755-108">ICE46 signale les erreurs suivantes pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="b6755-108">ICE46 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="b6755-109">Erreur ICE46</span><span class="sxs-lookup"><span data-stu-id="b6755-109">ICE46 error</span></span>                                                                                                                                            | <span data-ttu-id="b6755-110">Description</span><span class="sxs-lookup"><span data-stu-id="b6755-110">Description</span></span>                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6755-111">La propriété ReinstallMode définie dans la table de propriétés diffère d’une autre propriété définie uniquement par la casse.</span><span class="sxs-lookup"><span data-stu-id="b6755-111">Property ReinstallMode defined in property table differs from another defined property only by case.</span></span>                                                   | <span data-ttu-id="b6755-112">Le nom de la propriété définie par le système **REINSTALLMODE** diffère de la propriété personnalisée par la casse uniquement.</span><span class="sxs-lookup"><span data-stu-id="b6755-112">The system defined property name **REINSTALLMODE** differs from the custom property by case only.</span></span> <span data-ttu-id="b6755-113">Les propriétés respectent la casse, de sorte que la propriété personnalisée n’est pas la même que la propriété système.</span><span class="sxs-lookup"><span data-stu-id="b6755-113">Properties are case sensitive, so custom property is not the same as the system property.</span></span> <span data-ttu-id="b6755-114">Il s’agit d’une cause courante d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="b6755-114">This is a common cause of errors.</span></span> |
| <span data-ttu-id="b6755-115">Propriété « MyProperty » référencée dans la colonne « InstallExecuteSequence ». La condition’de la ligne’InstallFinalize’diffère d’une propriété définie par la casse uniquement.</span><span class="sxs-lookup"><span data-stu-id="b6755-115">Property 'Myproperty' referenced in column 'InstallExecuteSequence'.'Condition' of row 'InstallFinalize' differs from a defined property by case only.</span></span> | <span data-ttu-id="b6755-116">La table de propriétés définit la table MyProperty, mais la propriété référencée est MyProperty.</span><span class="sxs-lookup"><span data-stu-id="b6755-116">The property table defines the table MyProperty, but the referenced property is Myproperty.</span></span> <span data-ttu-id="b6755-117">Les propriétés étant sensibles à la casse, les deux propriétés ne sont pas les mêmes.</span><span class="sxs-lookup"><span data-stu-id="b6755-117">Properties are case sensitive, so the two properties are NOT the same.</span></span> <span data-ttu-id="b6755-118">Il s’agit d’une cause courante d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="b6755-118">This is a common cause of errors.</span></span>                          |



 

[<span data-ttu-id="b6755-119">Table de propriétés</span><span class="sxs-lookup"><span data-stu-id="b6755-119">Property Table</span></span>](property-table.md)



| <span data-ttu-id="b6755-120">Propriété</span><span class="sxs-lookup"><span data-stu-id="b6755-120">Property</span></span>      | <span data-ttu-id="b6755-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6755-121">Value</span></span>   |
|---------------|---------|
| <span data-ttu-id="b6755-122">ReinstallMode</span><span class="sxs-lookup"><span data-stu-id="b6755-122">ReinstallMode</span></span> | <span data-ttu-id="b6755-123">omus</span><span class="sxs-lookup"><span data-stu-id="b6755-123">omus</span></span>    |
| <span data-ttu-id="b6755-124">MyProperty</span><span class="sxs-lookup"><span data-stu-id="b6755-124">MyProperty</span></span>    | <span data-ttu-id="b6755-125">une valeur</span><span class="sxs-lookup"><span data-stu-id="b6755-125">a value</span></span> |



 

<span data-ttu-id="b6755-126">[Table InstallExecuteSequence](installexecutesequence-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="b6755-126">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="b6755-127">Action</span><span class="sxs-lookup"><span data-stu-id="b6755-127">Action</span></span>          | <span data-ttu-id="b6755-128">Condition</span><span class="sxs-lookup"><span data-stu-id="b6755-128">Condition</span></span>  |
|-----------------|------------|
| <span data-ttu-id="b6755-129">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="b6755-129">InstallFinalize</span></span> | <span data-ttu-id="b6755-130">MyProperty</span><span class="sxs-lookup"><span data-stu-id="b6755-130">Myproperty</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b6755-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b6755-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6755-132">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="b6755-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



