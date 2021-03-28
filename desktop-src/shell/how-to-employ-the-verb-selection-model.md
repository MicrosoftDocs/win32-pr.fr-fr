---
description: Les valeurs de Registre doivent être définies pour que les verbes gèrent les situations où un utilisateur peut sélectionner un seul élément, plusieurs éléments ou une sélection d’un élément. Un verbe requiert des valeurs de Registre distinctes pour chacune des trois situations prises en charge par le verbe.
ms.assetid: B6D4C879-3E52-4010-9B2E-3BCD81BB6C93
title: Comment utiliser le modèle de sélection de verbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724cd1c15b18657e27f9cfc53e9362685c6e2e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973159"
---
# <a name="how-to-employ-the-verb-selection-model"></a><span data-ttu-id="2978e-104">Comment utiliser le modèle de sélection de verbe</span><span class="sxs-lookup"><span data-stu-id="2978e-104">How to Employ the Verb Selection Model</span></span>

<span data-ttu-id="2978e-105">Les valeurs de Registre doivent être définies pour que les verbes gèrent les situations où un utilisateur peut sélectionner un seul élément, plusieurs éléments ou une sélection d’un élément.</span><span class="sxs-lookup"><span data-stu-id="2978e-105">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="2978e-106">Un verbe requiert des valeurs de Registre distinctes pour chacune des trois situations prises en charge par le verbe.</span><span class="sxs-lookup"><span data-stu-id="2978e-106">A verb requires separate registry values for each of these three situations that the verb supports.</span></span>

## <a name="instructions"></a><span data-ttu-id="2978e-107">Instructions</span><span class="sxs-lookup"><span data-stu-id="2978e-107">Instructions</span></span>


<span data-ttu-id="2978e-108">Spécifiez la valeur MultiSelectModel pour tous les verbes.</span><span class="sxs-lookup"><span data-stu-id="2978e-108">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="2978e-109">Si la valeur MultiSelectModel n’est pas spécifiée, elle est déduite du type d’implémentation de verbe que vous avez choisi.</span><span class="sxs-lookup"><span data-stu-id="2978e-109">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="2978e-110">Pour les méthodes basées sur COM (par exemple, DropTarget et ExecuteCommand), le **lecteur** est supposé, et pour les autres méthodes, le **document** est supposé.</span><span class="sxs-lookup"><span data-stu-id="2978e-110">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>

<span data-ttu-id="2978e-111">Les valeurs possibles pour le modèle de sélection de verbe sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2978e-111">The possible values for the verb selection model are as follows:</span></span>

1.  <span data-ttu-id="2978e-112">Spécifiez **Single** pour les verbes qui prennent en charge une seule sélection.</span><span class="sxs-lookup"><span data-stu-id="2978e-112">Specify **Single** for verbs that support only a single selection.</span></span>
2.  <span data-ttu-id="2978e-113">Spécifiez **Player** pour les verbes qui prennent en charge un nombre quelconque d’éléments.</span><span class="sxs-lookup"><span data-stu-id="2978e-113">Specify **Player** for verbs that support any number of items.</span></span>
3.  <span data-ttu-id="2978e-114">Spécifiez **document** pour les verbes qui créent une fenêtre de niveau supérieur pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="2978e-114">Specify **Document** for verbs that create a top-level window for each item.</span></span> <span data-ttu-id="2978e-115">Cela limite le nombre d’éléments qui sont activés et aide à éviter de manquer de ressources système si l’utilisateur ouvre un trop grand nombre de fenêtres.</span><span class="sxs-lookup"><span data-stu-id="2978e-115">Doing so limits the number of items that are activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

## <a name="remarks"></a><span data-ttu-id="2978e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="2978e-116">Remarks</span></span>

<span data-ttu-id="2978e-117">Lorsque le nombre d’éléments sélectionnés ne correspond pas au modèle de sélection de verbe ou est supérieur aux limites par défaut indiquées dans le tableau suivant, le verbe ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="2978e-117">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="2978e-118">Type d’implémentation de verbe</span><span class="sxs-lookup"><span data-stu-id="2978e-118">Type of verb implementation</span></span> | <span data-ttu-id="2978e-119">Document</span><span class="sxs-lookup"><span data-stu-id="2978e-119">Document</span></span> | <span data-ttu-id="2978e-120">Lecteur</span><span class="sxs-lookup"><span data-stu-id="2978e-120">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="2978e-121">Hérité</span><span class="sxs-lookup"><span data-stu-id="2978e-121">Legacy</span></span>                      | <span data-ttu-id="2978e-122">15 éléments</span><span class="sxs-lookup"><span data-stu-id="2978e-122">15 items</span></span> | <span data-ttu-id="2978e-123">100 éléments</span><span class="sxs-lookup"><span data-stu-id="2978e-123">100 items</span></span> |
| <span data-ttu-id="2978e-124">COM</span><span class="sxs-lookup"><span data-stu-id="2978e-124">COM</span></span>                         | <span data-ttu-id="2978e-125">15 éléments</span><span class="sxs-lookup"><span data-stu-id="2978e-125">15 items</span></span> | <span data-ttu-id="2978e-126">Aucune limite</span><span class="sxs-lookup"><span data-stu-id="2978e-126">No limit</span></span>  |



 

<span data-ttu-id="2978e-127">Voici des exemples d’entrées de Registre qui utilisent la valeur MultiSelectModel.</span><span class="sxs-lookup"><span data-stu-id="2978e-127">The following are example registry entries that use the MultiSelectModel value.</span></span>

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

 

 



