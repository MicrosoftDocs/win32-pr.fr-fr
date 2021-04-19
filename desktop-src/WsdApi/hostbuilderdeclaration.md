---
description: Génère une déclaration pour une fonction qui crée un hôte typé.
ms.assetid: 3c08e913-b47e-4ca7-b8bc-7b036e57db01
title: élément hostBuilderDeclaration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16576050efc76264f42dff6a19549f69933185b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522173"
---
# <a name="hostbuilderdeclaration-element"></a><span data-ttu-id="c0329-103">élément hostBuilderDeclaration</span><span class="sxs-lookup"><span data-stu-id="c0329-103">hostBuilderDeclaration element</span></span>

<span data-ttu-id="c0329-104">Génère une déclaration pour une fonction qui crée un hôte typé.</span><span class="sxs-lookup"><span data-stu-id="c0329-104">Generates a declaration for a function that creates a typed host.</span></span>

## <a name="usage"></a><span data-ttu-id="c0329-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="c0329-105">Usage</span></span>

``` syntax
<hostBuilderDeclaration>
  child elements
</hostBuilderDeclaration>
```

## <a name="attributes"></a><span data-ttu-id="c0329-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="c0329-106">Attributes</span></span>

<span data-ttu-id="c0329-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="c0329-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c0329-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c0329-108">Child elements</span></span>



| <span data-ttu-id="c0329-109">Élément</span><span class="sxs-lookup"><span data-stu-id="c0329-109">Element</span></span>                                   | <span data-ttu-id="c0329-110">Description</span><span class="sxs-lookup"><span data-stu-id="c0329-110">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0329-111">**interface**</span><span class="sxs-lookup"><span data-stu-id="c0329-111">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="c0329-112">Nom de l’interface de service à inclure pour l’hôte.</span><span class="sxs-lookup"><span data-stu-id="c0329-112">The name of service interface to be included for host.</span></span> <span data-ttu-id="c0329-113">La valeur de cet élément doit correspondre à la valeur de l’élément enfant de l' [**interface**](interface.md) de [**service hébergé**](hostedservice.md).</span><span class="sxs-lookup"><span data-stu-id="c0329-113">The value of this element must match the value of the [**interface**](interface.md) child element of [**hostedService**](hostedservice.md).</span></span> <br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="c0329-114">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c0329-114">Child element sequence</span></span>

``` syntax
interface+
```

## <a name="parent-elements"></a><span data-ttu-id="c0329-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c0329-115">Parent elements</span></span>



| <span data-ttu-id="c0329-116">Élément</span><span class="sxs-lookup"><span data-stu-id="c0329-116">Element</span></span>                         | <span data-ttu-id="c0329-117">Description</span><span class="sxs-lookup"><span data-stu-id="c0329-117">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="c0329-118">**fichier**</span><span class="sxs-lookup"><span data-stu-id="c0329-118">**file**</span></span>](file.md)<br/> | <span data-ttu-id="c0329-119">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="c0329-119">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="c0329-120">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c0329-120">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="c0329-121">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0329-121">Minimum supported system</span></span><br/> | <span data-ttu-id="c0329-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0329-122">Windows Vista</span></span> |
| <span data-ttu-id="c0329-123">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="c0329-123">Can be empty</span></span>                        | <span data-ttu-id="c0329-124">Non</span><span class="sxs-lookup"><span data-stu-id="c0329-124">No</span></span>            |



 

 




