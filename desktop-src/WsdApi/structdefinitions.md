---
description: Génère des définitions de structure C pour les types connus.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: élément structDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33ca9ac9ce3f9e868646c0bfff260238c30e572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536169"
---
# <a name="structdefinitions-element"></a><span data-ttu-id="00b75-103">élément structDefinitions</span><span class="sxs-lookup"><span data-stu-id="00b75-103">structDefinitions element</span></span>

<span data-ttu-id="00b75-104">Génère des définitions de structure C pour les types connus.</span><span class="sxs-lookup"><span data-stu-id="00b75-104">Generates C structure definitions for known types.</span></span>

## <a name="usage"></a><span data-ttu-id="00b75-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="00b75-105">Usage</span></span>

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a><span data-ttu-id="00b75-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="00b75-106">Attributes</span></span>

<span data-ttu-id="00b75-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="00b75-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="00b75-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="00b75-108">Child elements</span></span>

<span data-ttu-id="00b75-109">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="00b75-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="00b75-110">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="00b75-110">Parent elements</span></span>



| <span data-ttu-id="00b75-111">Élément</span><span class="sxs-lookup"><span data-stu-id="00b75-111">Element</span></span>                         | <span data-ttu-id="00b75-112">Description</span><span class="sxs-lookup"><span data-stu-id="00b75-112">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="00b75-113">**fichier**</span><span class="sxs-lookup"><span data-stu-id="00b75-113">**file**</span></span>](file.md)<br/> | <span data-ttu-id="00b75-114">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="00b75-114">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="00b75-115">Notes</span><span class="sxs-lookup"><span data-stu-id="00b75-115">Remarks</span></span>

<span data-ttu-id="00b75-116">Les structures des types connus sont référencées par une grande partie du code généré et par le code de l’application.</span><span class="sxs-lookup"><span data-stu-id="00b75-116">Structures for known types are referenced by much of the generated code and by application code.</span></span> <span data-ttu-id="00b75-117">Cet élément est utilisé pour générer des fichiers include.</span><span class="sxs-lookup"><span data-stu-id="00b75-117">This element is used to generate include files.</span></span> <span data-ttu-id="00b75-118">Cet élément doit se produire après un élément [**structDeclarations**](structdeclarations.md) afin que les références entre les structures soient gérées correctement.</span><span class="sxs-lookup"><span data-stu-id="00b75-118">This element should occur after a [**structDeclarations**](structdeclarations.md) element so that references between structures are handled properly.</span></span>

## <a name="element-information"></a><span data-ttu-id="00b75-119">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="00b75-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="00b75-120">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00b75-120">Minimum supported system</span></span><br/> | <span data-ttu-id="00b75-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00b75-121">Windows Vista</span></span> |
| <span data-ttu-id="00b75-122">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="00b75-122">Can be empty</span></span>                        | <span data-ttu-id="00b75-123">Oui</span><span class="sxs-lookup"><span data-stu-id="00b75-123">Yes</span></span>           |



 

 




