---
description: ICE02 valide le fait que certaines références entre le composant, le fichier et les tables du Registre sont réciproques. Ces références doivent être réciproques pour permettre au programme d’installation de déterminer correctement l’état d’installation des composants.
ms.assetid: 864404f1-439d-49a2-973d-4e6e1618863e
title: ICE02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975203825d079d5eeb1ec5e4183767dd68625bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750133"
---
# <a name="ice02"></a><span data-ttu-id="7fe0e-104">ICE02</span><span class="sxs-lookup"><span data-stu-id="7fe0e-104">ICE02</span></span>

<span data-ttu-id="7fe0e-105">ICE02 valide le fait que certaines références entre le [composant](component-table.md), le [fichier](file-table.md)et les tables [du Registre](registry-table.md) sont réciproques.</span><span class="sxs-lookup"><span data-stu-id="7fe0e-105">ICE02 validates that certain references between the [Component](component-table.md), [File](file-table.md), and [Registry](registry-table.md) tables are reciprocal.</span></span> <span data-ttu-id="7fe0e-106">Ces références doivent être réciproques pour permettre au programme d’installation de déterminer correctement l’état d’installation des composants.</span><span class="sxs-lookup"><span data-stu-id="7fe0e-106">These references must to be reciprocal for the installer to correctly determine the installation state of components.</span></span>

<span data-ttu-id="7fe0e-107">Le programme d’installation utilise la colonne keyPath de la table Component pour détecter la présence du composant figurant dans la colonne Component.</span><span class="sxs-lookup"><span data-stu-id="7fe0e-107">The installer uses the KeyPath column of the Component table to detect the presence of the component listed in the Component column.</span></span> <span data-ttu-id="7fe0e-108">La colonne keyPath contient une clé dans le registre ou les tables de fichiers.</span><span class="sxs-lookup"><span data-stu-id="7fe0e-108">The KeyPath column contains a key into the Registry or File tables.</span></span> <span data-ttu-id="7fe0e-109">Ces deux tables ont une colonne de composant \_ qui contient une clé dans la table des composants pointant vers le composant qui contrôle l’entrée ou le fichier de registre.</span><span class="sxs-lookup"><span data-stu-id="7fe0e-109">Both of these tables have a Component\_ column that contains a key back into the Component table pointing to the component that controls the registry entry or file.</span></span> <span data-ttu-id="7fe0e-110">Ces références doivent être réciproques.</span><span class="sxs-lookup"><span data-stu-id="7fe0e-110">These references must be reciprocal.</span></span>

## <a name="result"></a><span data-ttu-id="7fe0e-111">Résultats</span><span class="sxs-lookup"><span data-stu-id="7fe0e-111">Result</span></span>

<span data-ttu-id="7fe0e-112">ICE02 publie un message d’erreur s’il trouve une référence qui doit être réciproque et ne l’est pas.</span><span class="sxs-lookup"><span data-stu-id="7fe0e-112">ICE02 posts an error message if it finds a reference that should be reciprocal and is not.</span></span>

## <a name="example"></a><span data-ttu-id="7fe0e-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="7fe0e-113">Example</span></span>

<span data-ttu-id="7fe0e-114">ICE02 publie le message d’erreur suivant pour un fichier. msi contenant les entrées de base de données affichées.</span><span class="sxs-lookup"><span data-stu-id="7fe0e-114">ICE02 would post the following error message for a .msi file containing the database entries shown.</span></span>

``` syntax
File: 'Red_File' cannot be the key file for Component: 'Blue'. The file belongs to Component: 'Red'
```

<span data-ttu-id="7fe0e-115">[Table des composants](component-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="7fe0e-115">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="7fe0e-116">Composant</span><span class="sxs-lookup"><span data-stu-id="7fe0e-116">Component</span></span> | <span data-ttu-id="7fe0e-117">KeyPath</span><span class="sxs-lookup"><span data-stu-id="7fe0e-117">KeyPath</span></span>   |
|-----------|-----------|
| <span data-ttu-id="7fe0e-118">Rouge</span><span class="sxs-lookup"><span data-stu-id="7fe0e-118">Red</span></span>       | <span data-ttu-id="7fe0e-119">\_Fichier rouge</span><span class="sxs-lookup"><span data-stu-id="7fe0e-119">Red\_File</span></span> |
| <span data-ttu-id="7fe0e-120">Bleu</span><span class="sxs-lookup"><span data-stu-id="7fe0e-120">Blue</span></span>      | <span data-ttu-id="7fe0e-121">\_Fichier rouge</span><span class="sxs-lookup"><span data-stu-id="7fe0e-121">Red\_File</span></span> |



 

<span data-ttu-id="7fe0e-122">[Table de fichiers](file-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="7fe0e-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="7fe0e-123">Colonne de fichier</span><span class="sxs-lookup"><span data-stu-id="7fe0e-123">File Column</span></span> | <span data-ttu-id="7fe0e-124">-\_</span><span class="sxs-lookup"><span data-stu-id="7fe0e-124">Component\_</span></span> |
|-------------|-------------|
| <span data-ttu-id="7fe0e-125">\_Fichier rouge</span><span class="sxs-lookup"><span data-stu-id="7fe0e-125">Red\_File</span></span>   | <span data-ttu-id="7fe0e-126">Rouge</span><span class="sxs-lookup"><span data-stu-id="7fe0e-126">Red</span></span>         |
| <span data-ttu-id="7fe0e-127">\_Fichier Blue</span><span class="sxs-lookup"><span data-stu-id="7fe0e-127">Blue\_File</span></span>  | <span data-ttu-id="7fe0e-128">Bleu</span><span class="sxs-lookup"><span data-stu-id="7fe0e-128">Blue</span></span>        |



 

<span data-ttu-id="7fe0e-129">Le composant Blue fait référence \_ à un fichier rouge, mais le fichier rouge \_ n’est pas contrôlé par le composant Blue et ne peut donc pas être le fichier keyPath.</span><span class="sxs-lookup"><span data-stu-id="7fe0e-129">Component Blue references Red\_File, but Red\_File is not controlled by Component Blue and therefore cannot be the KeyPath file.</span></span> <span data-ttu-id="7fe0e-130">Si le programme d’installation a été appelé pour avoir l’état d’installation bleu, il ne vérifierait pas correctement si le \_ fichier rouge a été installé.</span><span class="sxs-lookup"><span data-stu-id="7fe0e-130">If the installer were called to get the installation state of Blue it would incorrectly check whether Red\_File was installed.</span></span> <span data-ttu-id="7fe0e-131">La modification du champ keyPath pour Blue dans la table Component en \_ fichier Blue corrige l’erreur.</span><span class="sxs-lookup"><span data-stu-id="7fe0e-131">Changing the KeyPath field for Blue in the Component Table to Blue\_File fixes the error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fe0e-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7fe0e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fe0e-133">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="7fe0e-133">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



