---
description: ICE67 vérifie que la cible d’un raccourci non publié appartient au même composant que le raccourci lui-même, ou que les attributs du composant cible garantissent qu’il ne modifie pas les emplacements d’installation.
ms.assetid: 3fc462e7-4c11-4167-a157-6c1e0791901d
title: ICE67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca140a2d7eace9b693e82763f6bf5824346b51e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952732"
---
# <a name="ice67"></a><span data-ttu-id="75353-103">ICE67</span><span class="sxs-lookup"><span data-stu-id="75353-103">ICE67</span></span>

<span data-ttu-id="75353-104">ICE67 vérifie que la cible d’un raccourci non publié appartient au même composant que le raccourci lui-même, ou que les attributs du composant cible garantissent qu’il ne modifie pas les emplacements d’installation.</span><span class="sxs-lookup"><span data-stu-id="75353-104">ICE67 checks that the target of a non-advertised shortcut belongs to the same component as the shortcut itself, or that the attributes of the target component ensure that it does not change installation locations.</span></span>

<span data-ttu-id="75353-105">Si vous ne corrigez pas un avertissement ou une erreur signalée par ICE67, le raccourci risque d’être non valide si le composant cible change d’État et que le composant source ne le fait pas.</span><span class="sxs-lookup"><span data-stu-id="75353-105">Failure to fix a warning or error reported by ICE67 can cause the shortcut to be invalid if the target component changes state and the source component does not.</span></span> <span data-ttu-id="75353-106">Par exemple, lorsque le composant du fichier cible est configuré pour s’exécuter à partir de la source, une réinstallation qui modifie le composant en local entraîne le non réinstallation du composant contenant le raccourci.</span><span class="sxs-lookup"><span data-stu-id="75353-106">For example, when the target file's component is set to run from source, a reinstallation that changes the component to local results in the component containing the shortcut not being reinstalled.</span></span> <span data-ttu-id="75353-107">Par conséquent, le raccourci pointe vers un emplacement non valide.</span><span class="sxs-lookup"><span data-stu-id="75353-107">Thus the shortcut points to an invalid location.</span></span>

<span data-ttu-id="75353-108">Notez que dans certains cas, l’utilisation d’un autre composant pour le raccourci est inévitable.</span><span class="sxs-lookup"><span data-stu-id="75353-108">Note that in some cases, using a different component for the shortcut is unavoidable.</span></span> <span data-ttu-id="75353-109">Par exemple, si le raccourci est créé dans le profil utilisateur et que le fichier est installé dans un répertoire qui n’est pas du profil, vous risquez de ne pas pouvoir utiliser le même composant pour les deux éléments de données.</span><span class="sxs-lookup"><span data-stu-id="75353-109">For example, if the shortcut is created in the user profile and the file is installed to a non-profile directory, you may not be able to use the same component for both pieces of data.</span></span> <span data-ttu-id="75353-110">(Cela entraîne des défaillances dans les scénarios multi-utilisateur, tels que ceux décrits dans [ICE57](ice57.md)).</span><span class="sxs-lookup"><span data-stu-id="75353-110">(This results in failures in multi-user scenarios – such as those described in [ICE57](ice57.md)).</span></span> <span data-ttu-id="75353-111">Dans ce cas, vous serez peut-être en mesure d’utiliser des raccourcis publiés pour obtenir le comportement souhaité, ou vous pouvez simplement vous assurer que le composant cible ne peut pas passer d’une exécution à une source à une source locale.</span><span class="sxs-lookup"><span data-stu-id="75353-111">In this case, you may be able to use advertised shortcuts to achieve the behavior you want, or you can simply ensure that the target component cannot change from run-from-source to local.</span></span>

## <a name="result"></a><span data-ttu-id="75353-112">Résultats</span><span class="sxs-lookup"><span data-stu-id="75353-112">Result</span></span>

<span data-ttu-id="75353-113">ICE67 retourne une erreur ou un avertissement si la cible d’un raccourci non publié n’appartient pas au même composant que le raccourci lui-même, ou si les attributs du composant cible ne garantissent pas que les emplacements d’installation ne changeront pas.</span><span class="sxs-lookup"><span data-stu-id="75353-113">ICE67 returns an error or a warning if the target of a non-advertised shortcut does not belong to the same component as the shortcut itself, or if the attributes of the target component do not ensure that the installation locations will not change.</span></span>

## <a name="example"></a><span data-ttu-id="75353-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="75353-114">Example</span></span>

<span data-ttu-id="75353-115">ICE67 signale les erreurs et avertissements suivants pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="75353-115">ICE67 reports the following warning and errors for the example shown.</span></span>

``` syntax
The shortcut 'Shortcut1' is a non-advertised shortcut with a file target. The shortcut and target are installed by different components, and the target component can run locally or from source.
```

<span data-ttu-id="75353-116">Shortcut1 est installé par COMPONENT2, mais son fichier cible, fichier1, est installé par Composant1.</span><span class="sxs-lookup"><span data-stu-id="75353-116">Shortcut1 is installed by Component2, but its target file, File1, is installed by component1.</span></span> <span data-ttu-id="75353-117">Le composant cible est marqué comme étant facultatif (ce qui signifie qu’il peut être local ou d’exécution à partir de la source).</span><span class="sxs-lookup"><span data-stu-id="75353-117">The target component is marked optional (meaning that it can be local or run-from-source).</span></span> <span data-ttu-id="75353-118">Une situation susceptible de provoquer un problème est si Composant1 passe de l’exécution à partir de la source à la valeur locale.</span><span class="sxs-lookup"><span data-stu-id="75353-118">One possible situation that would cause a problem is if Component1 changes from run-from-source to local.</span></span> <span data-ttu-id="75353-119">Shortcut1 ne peut alors pas pointer vers un emplacement non valide.</span><span class="sxs-lookup"><span data-stu-id="75353-119">This would cause Shortcut1 to point to an invalid location.</span></span>

<span data-ttu-id="75353-120">Pour résoudre cet avertissement, installez le raccourci dans le cadre de Composant1 ou marquez Composant1 comme LocalOnly ou SourceOnly.</span><span class="sxs-lookup"><span data-stu-id="75353-120">To fix this warning, Install the shortcut as part of Component1, or mark Component1 as LocalOnly or SourceOnly.</span></span>

<span data-ttu-id="75353-121">[Table de fichiers](file-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="75353-121">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="75353-122">Fichier</span><span class="sxs-lookup"><span data-stu-id="75353-122">File</span></span>  | <span data-ttu-id="75353-123">-\_</span><span class="sxs-lookup"><span data-stu-id="75353-123">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="75353-124">Fichier1</span><span class="sxs-lookup"><span data-stu-id="75353-124">File1</span></span> | <span data-ttu-id="75353-125">Composant1</span><span class="sxs-lookup"><span data-stu-id="75353-125">Component1</span></span>  |



 

<span data-ttu-id="75353-126">[Table de raccourcis](shortcut-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="75353-126">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="75353-127">Raccourci</span><span class="sxs-lookup"><span data-stu-id="75353-127">Shortcut</span></span>  | <span data-ttu-id="75353-128">-\_</span><span class="sxs-lookup"><span data-stu-id="75353-128">Component\_</span></span> | <span data-ttu-id="75353-129">Cible</span><span class="sxs-lookup"><span data-stu-id="75353-129">Target</span></span>      |
|-----------|-------------|-------------|
| <span data-ttu-id="75353-130">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="75353-130">Shortcut1</span></span> | <span data-ttu-id="75353-131">Component2</span><span class="sxs-lookup"><span data-stu-id="75353-131">Component2</span></span>  | <span data-ttu-id="75353-132">\[\#File1\]</span><span class="sxs-lookup"><span data-stu-id="75353-132">\[\#File1\]</span></span> |



 

<span data-ttu-id="75353-133">[Table des composants](component-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="75353-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="75353-134">Composant</span><span class="sxs-lookup"><span data-stu-id="75353-134">Component</span></span>  | <span data-ttu-id="75353-135">Attributs</span><span class="sxs-lookup"><span data-stu-id="75353-135">Attributes</span></span> |
|------------|------------|
| <span data-ttu-id="75353-136">Composant1</span><span class="sxs-lookup"><span data-stu-id="75353-136">Component1</span></span> | <span data-ttu-id="75353-137">2</span><span class="sxs-lookup"><span data-stu-id="75353-137">2</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="75353-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75353-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75353-139">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="75353-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



