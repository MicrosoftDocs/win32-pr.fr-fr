---
description: ICE21 valide que chaque composant de la table de composants appartient à une fonctionnalité. Elle utilise la table FeatureComponents pour vérifier ce mappage.
ms.assetid: 68983d6a-b807-4730-a645-378001e558ec
title: ICE21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c457d026b3dc57a718eabea704254a3448a3de26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538908"
---
# <a name="ice21"></a><span data-ttu-id="18347-104">ICE21</span><span class="sxs-lookup"><span data-stu-id="18347-104">ICE21</span></span>

<span data-ttu-id="18347-105">ICE21 valide que chaque composant de la [table de composants](component-table.md) appartient à une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="18347-105">ICE21 validates that every component in the [Component table](component-table.md) belongs to a feature.</span></span> <span data-ttu-id="18347-106">Elle utilise la [table FeatureComponents](featurecomponents-table.md) pour vérifier ce mappage.</span><span class="sxs-lookup"><span data-stu-id="18347-106">It uses the [FeatureComponents table](featurecomponents-table.md) to check for this mapping.</span></span>

## <a name="result"></a><span data-ttu-id="18347-107">Résultats</span><span class="sxs-lookup"><span data-stu-id="18347-107">Result</span></span>

<span data-ttu-id="18347-108">ICE21 publie un message d’erreur si le package d’installation contient un composant qui n’appartient pas à une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="18347-108">ICE21 posts an error message if the installation package contains a component that does not belong to a feature.</span></span>

## <a name="example"></a><span data-ttu-id="18347-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="18347-109">Example</span></span>

<span data-ttu-id="18347-110">Dans l’exemple suivant, ICE21 publie un message d’erreur indiquant que le composant COMP1 n’est mappé à aucune fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="18347-110">For the following example, ICE21 posts an error message stating that the component Comp1 does not map to any feature.</span></span>

<span data-ttu-id="18347-111">[Table des composants](component-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="18347-111">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="18347-112">Composant</span><span class="sxs-lookup"><span data-stu-id="18347-112">Component</span></span> |
|-----------|
| <span data-ttu-id="18347-113">COMP1</span><span class="sxs-lookup"><span data-stu-id="18347-113">Comp1</span></span>     |
| <span data-ttu-id="18347-114">COMP2</span><span class="sxs-lookup"><span data-stu-id="18347-114">Comp2</span></span>     |



 

<span data-ttu-id="18347-115">[Table FeatureComponents](featurecomponents-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="18347-115">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="18347-116">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="18347-116">Feature</span></span>  | <span data-ttu-id="18347-117">Composant</span><span class="sxs-lookup"><span data-stu-id="18347-117">Component</span></span> |
|----------|-----------|
| <span data-ttu-id="18347-118">Feature1</span><span class="sxs-lookup"><span data-stu-id="18347-118">Feature1</span></span> | <span data-ttu-id="18347-119">COMP2</span><span class="sxs-lookup"><span data-stu-id="18347-119">Comp2</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="18347-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="18347-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18347-121">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="18347-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



