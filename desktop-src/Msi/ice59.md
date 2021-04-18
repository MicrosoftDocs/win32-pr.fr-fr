---
description: ICE59 vérifie que les raccourcis publiés appartiennent à des composants installés par la fonctionnalité cible du raccourci.
ms.assetid: 9cd19137-792d-4fde-92d2-7d96942448d6
title: ICE59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5631b723a158bb371fff3211654a70d694b6cb5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519866"
---
# <a name="ice59"></a><span data-ttu-id="f83da-103">ICE59</span><span class="sxs-lookup"><span data-stu-id="f83da-103">ICE59</span></span>

<span data-ttu-id="f83da-104">ICE59 vérifie que les raccourcis publiés appartiennent à des composants installés par la fonctionnalité cible du raccourci.</span><span class="sxs-lookup"><span data-stu-id="f83da-104">ICE59 checks that advertised shortcuts belong to components that are installed by the target feature of the shortcut.</span></span>

<span data-ttu-id="f83da-105">Les erreurs signalées par ICE59 entraînent généralement le comportement suivant :</span><span class="sxs-lookup"><span data-stu-id="f83da-105">Errors reported by ICE59 generally lead to the following behavior:</span></span>

1.  <span data-ttu-id="f83da-106">Le raccourci publié lance le Windows Installer pour installer la fonctionnalité indiquée dans la colonne cible.</span><span class="sxs-lookup"><span data-stu-id="f83da-106">The advertised shortcut will launch the Windows Installer to install the feature listed in the Target column.</span></span>
2.  <span data-ttu-id="f83da-107">Toutefois, étant donné que la [table FeatureComponents](featurecomponents-table.md) ne mappe pas la fonctionnalité cible au composant contenant le raccourci, le fichier keyfile du composant (qui est activé par le raccourci) n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="f83da-107">But because the [FeatureComponents table](featurecomponents-table.md) does not map the target feature to the component containing the shortcut, the keyfile of the component (which is activated by the shortcut) is not installed.</span></span>
3.  <span data-ttu-id="f83da-108">Par conséquent, le raccourci est rompu et n’a rien à faire.</span><span class="sxs-lookup"><span data-stu-id="f83da-108">Therefore the shortcut is broken and will not do anything.</span></span>

## <a name="result"></a><span data-ttu-id="f83da-109">Résultats</span><span class="sxs-lookup"><span data-stu-id="f83da-109">Result</span></span>

<span data-ttu-id="f83da-110">ICE59 publie une erreur si un raccourci publié n’appartient pas aux composants installés par la fonctionnalité cible du raccourci.</span><span class="sxs-lookup"><span data-stu-id="f83da-110">ICE59 posts an error if an advertised shortcut does not belong to the components that are installed by the target feature of the shortcut.</span></span>

## <a name="example"></a><span data-ttu-id="f83da-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="f83da-111">Example</span></span>

<span data-ttu-id="f83da-112">ICE59 signale l’erreur suivante pour l’exemple ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="f83da-112">ICE59 reports the following error for the example shown:</span></span>

``` syntax
The shortcut ShortcutB activates component ComponentB and advertises feature FeatureA, but there is no mapping between FeatureA and ComponentB in the FeatureComponents table.
```

<span data-ttu-id="f83da-113">Dans ce cas, ShortcutB publie Feature et, lorsqu’il est activé, démarre le fichier de clé de ComponentB.</span><span class="sxs-lookup"><span data-stu-id="f83da-113">In this case, ShortcutB advertises FeatureA, and when activated, starts the key file of ComponentB.</span></span> <span data-ttu-id="f83da-114">Pourtant, ComponentB n’est jamais installé par Feature. par conséquent, même après la fin de la phase d’installation à la demande, la cible du raccourci n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="f83da-114">Yet ComponentB is never installed by FeatureA, so even after the installation-on-demand phase completes, the target of the shortcut does not exist.</span></span>

<span data-ttu-id="f83da-115">Pour corriger cette erreur, ajoutez une ligne à la [table FeatureComponents](featurecomponents-table.md) qui associe Feature et ComponentB.</span><span class="sxs-lookup"><span data-stu-id="f83da-115">To fix this error, add a row to the [FeatureComponents table](featurecomponents-table.md) that associates FeatureA and ComponentB.</span></span>

<span data-ttu-id="f83da-116">[Table de raccourcis](shortcut-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="f83da-116">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="f83da-117">Raccourci</span><span class="sxs-lookup"><span data-stu-id="f83da-117">Shortcut</span></span>  | <span data-ttu-id="f83da-118">Cible</span><span class="sxs-lookup"><span data-stu-id="f83da-118">Target</span></span>   | <span data-ttu-id="f83da-119">-\_</span><span class="sxs-lookup"><span data-stu-id="f83da-119">Component\_</span></span> |
|-----------|----------|-------------|
| <span data-ttu-id="f83da-120">ShortcutB</span><span class="sxs-lookup"><span data-stu-id="f83da-120">ShortcutB</span></span> | <span data-ttu-id="f83da-121">FeatureA</span><span class="sxs-lookup"><span data-stu-id="f83da-121">FeatureA</span></span> | <span data-ttu-id="f83da-122">ComponentB</span><span class="sxs-lookup"><span data-stu-id="f83da-122">ComponentB</span></span>  |



 

[<span data-ttu-id="f83da-123">Table FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="f83da-123">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="f83da-124">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="f83da-124">Feature\_</span></span> | <span data-ttu-id="f83da-125">-\_</span><span class="sxs-lookup"><span data-stu-id="f83da-125">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="f83da-126">FeatureA</span><span class="sxs-lookup"><span data-stu-id="f83da-126">FeatureA</span></span>  | <span data-ttu-id="f83da-127">Composant</span><span class="sxs-lookup"><span data-stu-id="f83da-127">ComponentA</span></span>  |



 

<span data-ttu-id="f83da-128">[Table des fonctionnalités](feature-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="f83da-128">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="f83da-129">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="f83da-129">Feature</span></span>  | <span data-ttu-id="f83da-130">Level</span><span class="sxs-lookup"><span data-stu-id="f83da-130">Level</span></span> |
|----------|-------|
| <span data-ttu-id="f83da-131">FeatureA</span><span class="sxs-lookup"><span data-stu-id="f83da-131">FeatureA</span></span> | <span data-ttu-id="f83da-132">10</span><span class="sxs-lookup"><span data-stu-id="f83da-132">10</span></span>    |



 

<span data-ttu-id="f83da-133">[Table des composants](component-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="f83da-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="f83da-134">Composant</span><span class="sxs-lookup"><span data-stu-id="f83da-134">Component</span></span>  | <span data-ttu-id="f83da-135">KeyPath</span><span class="sxs-lookup"><span data-stu-id="f83da-135">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="f83da-136">Composant</span><span class="sxs-lookup"><span data-stu-id="f83da-136">ComponentA</span></span> | <span data-ttu-id="f83da-137">Filea</span><span class="sxs-lookup"><span data-stu-id="f83da-137">FileA</span></span>   |
| <span data-ttu-id="f83da-138">ComponentB</span><span class="sxs-lookup"><span data-stu-id="f83da-138">ComponentB</span></span> | <span data-ttu-id="f83da-139">FileB</span><span class="sxs-lookup"><span data-stu-id="f83da-139">FileB</span></span>   |



 

<span data-ttu-id="f83da-140">[Table de fichiers](file-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="f83da-140">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="f83da-141">Fichier</span><span class="sxs-lookup"><span data-stu-id="f83da-141">File</span></span>  | <span data-ttu-id="f83da-142">-\_</span><span class="sxs-lookup"><span data-stu-id="f83da-142">Component\_</span></span> | <span data-ttu-id="f83da-143">Séquence</span><span class="sxs-lookup"><span data-stu-id="f83da-143">Sequence</span></span> |
|-------|-------------|----------|
| <span data-ttu-id="f83da-144">Filea</span><span class="sxs-lookup"><span data-stu-id="f83da-144">FileA</span></span> | <span data-ttu-id="f83da-145">Composant</span><span class="sxs-lookup"><span data-stu-id="f83da-145">ComponentA</span></span>  | <span data-ttu-id="f83da-146">1</span><span class="sxs-lookup"><span data-stu-id="f83da-146">1</span></span>        |
| <span data-ttu-id="f83da-147">FileB</span><span class="sxs-lookup"><span data-stu-id="f83da-147">FileB</span></span> | <span data-ttu-id="f83da-148">ComponentB</span><span class="sxs-lookup"><span data-stu-id="f83da-148">ComponentB</span></span>  | <span data-ttu-id="f83da-149">2</span><span class="sxs-lookup"><span data-stu-id="f83da-149">2</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f83da-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f83da-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f83da-151">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="f83da-151">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



