---
title: Classes structurelles, abstraites et auxiliaires
description: L’attribut objectClassCategory d’un objet classSchema peut avoir une valeur, comme indiqué dans le tableau suivant, qui indique si la classe est structurelle, abstraite ou auxiliaire.
ms.assetid: 5af740cb-b292-4d80-abe5-3e3d194758f3
ms.tgt_platform: multiple
keywords:
- Classes structurelles, abstraites et auxiliaires AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561bc836794b45b6c028fe8da772b0b38d0936a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028586"
---
# <a name="structural-abstract-and-auxiliary-classes"></a><span data-ttu-id="6941e-104">Classes structurelles, abstraites et auxiliaires</span><span class="sxs-lookup"><span data-stu-id="6941e-104">Structural, Abstract, and Auxiliary Classes</span></span>

<span data-ttu-id="6941e-105">L’attribut **objectClassCategory** d’un objet **classSchema** peut avoir une valeur, comme indiqué dans le tableau suivant, qui indique si la classe est structurelle, abstraite ou auxiliaire.</span><span class="sxs-lookup"><span data-stu-id="6941e-105">The **objectClassCategory** attribute of a **classSchema** object can have a value, as listed in the following table, that indicates whether the class is structural, abstract, or auxiliary.</span></span>



| <span data-ttu-id="6941e-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="6941e-106">Value</span></span> | <span data-ttu-id="6941e-107">Description</span><span class="sxs-lookup"><span data-stu-id="6941e-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6941e-108">1</span><span class="sxs-lookup"><span data-stu-id="6941e-108">1</span></span>     | <span data-ttu-id="6941e-109">Classe structurelle, qui est le seul type de classe qui peut avoir des instances dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="6941e-109">A structural class, which is the only type of class that can have instances in Active Directory Domain Services.</span></span> <span data-ttu-id="6941e-110">Une classe structurelle peut être une sous-classe d’une classe abstraite ou structurelle.</span><span class="sxs-lookup"><span data-stu-id="6941e-110">A structural class can be a subclass of an abstract or structural class.</span></span> <span data-ttu-id="6941e-111">Une classe structurelle peut inclure n’importe quel nombre de classes auxiliaires dans sa définition.</span><span class="sxs-lookup"><span data-stu-id="6941e-111">A structural class can include any number of auxiliary classes in its definition.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="6941e-112">2</span><span class="sxs-lookup"><span data-stu-id="6941e-112">2</span></span>     | <span data-ttu-id="6941e-113">Classe abstraite, qui est un modèle utilisé pour dériver de nouvelles classes abstraites, auxiliaires et structurelles.</span><span class="sxs-lookup"><span data-stu-id="6941e-113">An abstract class, which is a template used to derive new abstract, auxiliary, and structural classes.</span></span> <span data-ttu-id="6941e-114">Une classe abstraite ne peut être qu’une sous-classe d’une classe abstraite.</span><span class="sxs-lookup"><span data-stu-id="6941e-114">An abstract class can only be a subclass of an abstract class.</span></span> <span data-ttu-id="6941e-115">Les classes abstraites ne peuvent pas être instanciées dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="6941e-115">Abstract classes cannot be instantiated in Active Directory Domain Services.</span></span> <span data-ttu-id="6941e-116">Une classe abstraite peut inclure n’importe quel nombre de classes auxiliaires dans sa définition.</span><span class="sxs-lookup"><span data-stu-id="6941e-116">An abstract class can include any number of auxiliary classes in its definition.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="6941e-117">3</span><span class="sxs-lookup"><span data-stu-id="6941e-117">3</span></span>     | <span data-ttu-id="6941e-118">Classe auxiliaire, qui peut être incluse dans la définition d’une classe structurelle, abstraite ou auxiliaire, auquel cas les valeurs **mustContain**, **systemMustContain**, **mayContain** et **systemMayContain** de la classe auxiliaire sont ajoutées à celles de la classe.</span><span class="sxs-lookup"><span data-stu-id="6941e-118">An auxiliary class, which can be included in the definition of a structural, abstract, or auxiliary class, in which case, the **mustContain**, **systemMustContain**, **mayContain**, and **systemMayContain** values of the auxiliary class are added to those of the class.</span></span> <span data-ttu-id="6941e-119">Une classe auxiliaire peut être une sous-classe d’une classe abstraite ou auxiliaire.</span><span class="sxs-lookup"><span data-stu-id="6941e-119">An auxiliary class can be a subclass of an abstract or auxiliary class.</span></span> <span data-ttu-id="6941e-120">Les classes auxiliaires ne peuvent pas être instanciées dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="6941e-120">Auxiliary classes cannot be instantiated in Active Directory Domain Services.</span></span> <span data-ttu-id="6941e-121">Une classe auxiliaire peut inclure n’importe quel nombre de classes auxiliaires dans sa définition.</span><span class="sxs-lookup"><span data-stu-id="6941e-121">An auxiliary class can include any number of auxiliary classes in its definition.</span></span> |



 

<span data-ttu-id="6941e-122">Ne confondez pas le **objectClassCategory** avec une [catégorie d’objet](object-class-and-object-category.md).</span><span class="sxs-lookup"><span data-stu-id="6941e-122">Do not confuse the **objectClassCategory** with an [object category](object-class-and-object-category.md).</span></span>

 

 




