---
description: ICE36 valide que chaque icône de la table des icônes figure au moins une fois dans la propriété ARPPRODUCTICON ou dans la classe, ProgId ou Shortcut tables.
ms.assetid: d502c0a9-17e5-467a-8b02-8b254e77b96b
title: ICE36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f24eebc1b591edde418c59b6765d7ee91a00dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034788"
---
# <a name="ice36"></a><span data-ttu-id="4207c-103">ICE36</span><span class="sxs-lookup"><span data-stu-id="4207c-103">ICE36</span></span>

<span data-ttu-id="4207c-104">ICE36 valide que chaque icône de la table des icônes figure au moins une fois dans la propriété [**ARPPRODUCTICON**](arpproducticon.md) ou dans la [classe](class-table.md), [ProgID](progid-table.md)ou [Shortcut](shortcut-table.md) tables.</span><span class="sxs-lookup"><span data-stu-id="4207c-104">ICE36 validates that every icon in the Icon table is listed at least once in the [**ARPPRODUCTICON**](arpproducticon.md) property or the [Class](class-table.md), [ProgId](progid-table.md), or [Shortcut](shortcut-table.md) tables.</span></span>

<span data-ttu-id="4207c-105">Pendant la publication, le programme d’installation installe toutes les icônes listées dans la [table icône](icon-table.md) sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4207c-105">During advertisement, the installer installs all the icons listed in the [Icon table](icon-table.md) on the user's computer.</span></span> <span data-ttu-id="4207c-106">Le fait d’avoir des icônes inutilisées dans la table d’icônes n’empêche pas l’exécution de l’installation, mais elle augmente inutilement la taille du fichier. msi et l’heure et l’espace requis pour publier une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="4207c-106">Having unused icons in the Icon table does not prevent the installation from running, however it does unnecessarily increase the size of the .msi file and the time and space required to advertise a feature.</span></span>

<span data-ttu-id="4207c-107">Si aucune icône n’est référencée dans la propriété ou la table et qu’aucune interface utilisateur n’est fournie pour créer une référence au moment de l’exécution, vous devez supprimer l’icône pour obtenir de meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="4207c-107">If an icon is not referenced in the property or table and there is no UI provided to create a reference at run time, you should remove the icon to achieve better performance.</span></span>

## <a name="result"></a><span data-ttu-id="4207c-108">Résultats</span><span class="sxs-lookup"><span data-stu-id="4207c-108">Result</span></span>

<span data-ttu-id="4207c-109">ICE36 publie un message si une icône de la table d’icônes n’est pas référencée dans la [classe](class-table.md), le [ProgID](progid-table.md)ou les tables de [raccourcis](shortcut-table.md) et si aucune interface utilisateur n’est fournie pour créer une telle référence au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="4207c-109">ICE36 posts a message if there is a icon in the Icon table that is not referenced in the [Class](class-table.md), [ProgId](progid-table.md), or [Shortcut](shortcut-table.md) tables and if there is no UI provided to create such a reference at run time.</span></span>

## <a name="example"></a><span data-ttu-id="4207c-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="4207c-110">Example</span></span>

<span data-ttu-id="4207c-111">ICE36 signale l’erreur suivante pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="4207c-111">ICE36 reports the following error for the example shown.</span></span>

``` syntax
Icon Bloat. Icon Icon4 is not used in the Class, Shortcut, or ProgID table. This adversely affects performance.
```

<span data-ttu-id="4207c-112">[Table d’icônes](icon-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="4207c-112">[Icon Table](icon-table.md) (partial)</span></span>



| <span data-ttu-id="4207c-113">Nom</span><span class="sxs-lookup"><span data-stu-id="4207c-113">Name</span></span>  | <span data-ttu-id="4207c-114">Données</span><span class="sxs-lookup"><span data-stu-id="4207c-114">Data</span></span>     |
|-------|----------|
| <span data-ttu-id="4207c-115">Icon1</span><span class="sxs-lookup"><span data-stu-id="4207c-115">Icon1</span></span> | <span data-ttu-id="4207c-116">Control1</span><span class="sxs-lookup"><span data-stu-id="4207c-116">Control1</span></span> |
| <span data-ttu-id="4207c-117">Icon2</span><span class="sxs-lookup"><span data-stu-id="4207c-117">Icon2</span></span> | <span data-ttu-id="4207c-118">Control2</span><span class="sxs-lookup"><span data-stu-id="4207c-118">Control2</span></span> |
| <span data-ttu-id="4207c-119">Icon3</span><span class="sxs-lookup"><span data-stu-id="4207c-119">Icon3</span></span> | <span data-ttu-id="4207c-120">Control3</span><span class="sxs-lookup"><span data-stu-id="4207c-120">Control3</span></span> |
| <span data-ttu-id="4207c-121">Icon4</span><span class="sxs-lookup"><span data-stu-id="4207c-121">Icon4</span></span> | <span data-ttu-id="4207c-122">Control4</span><span class="sxs-lookup"><span data-stu-id="4207c-122">Control4</span></span> |



 

<span data-ttu-id="4207c-123">[Table ProgID](progid-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="4207c-123">[ProgID Table](progid-table.md) (partial)</span></span>



| <span data-ttu-id="4207c-124">ProgID</span><span class="sxs-lookup"><span data-stu-id="4207c-124">ProgID</span></span>    |
|-----------|
| <span data-ttu-id="4207c-125">Property1</span><span class="sxs-lookup"><span data-stu-id="4207c-125">Property1</span></span> |



 

<span data-ttu-id="4207c-126">[Table de classe](class-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="4207c-126">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="4207c-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="4207c-127">CLSID</span></span>                                  |
|----------------------------------------|
| <span data-ttu-id="4207c-128">{3E469ABA-3644-11d2-8892-00A0C981B015}</span><span class="sxs-lookup"><span data-stu-id="4207c-128">{3E469ABA-3644-11d2-8892-00A0C981B015}</span></span> |



 

<span data-ttu-id="4207c-129">[Table de raccourcis](shortcut-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="4207c-129">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="4207c-130">Raccourci</span><span class="sxs-lookup"><span data-stu-id="4207c-130">Shortcut</span></span>  | <span data-ttu-id="4207c-131">Icône\_</span><span class="sxs-lookup"><span data-stu-id="4207c-131">Icon\_</span></span> |
|-----------|--------|
| <span data-ttu-id="4207c-132">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="4207c-132">Shortcut1</span></span> | <span data-ttu-id="4207c-133">Icon2</span><span class="sxs-lookup"><span data-stu-id="4207c-133">Icon2</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="4207c-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4207c-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4207c-135">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="4207c-135">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



