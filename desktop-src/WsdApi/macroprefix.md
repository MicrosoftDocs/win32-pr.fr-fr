---
description: Définit le préfixe à utiliser dans le code généré pour les noms de macros dans l’espace de noms.
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: élément macroPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9590092d78ea4700715a868bb7e50f15833011
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998746"
---
# <a name="macroprefix-element"></a><span data-ttu-id="2da99-103">élément macroPrefix</span><span class="sxs-lookup"><span data-stu-id="2da99-103">macroPrefix element</span></span>

<span data-ttu-id="2da99-104">Définit le préfixe à utiliser dans le code généré pour les noms de macros dans l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="2da99-104">Defines the prefix to be used in the generated code for names of macros in the namespace.</span></span>

## <a name="usage"></a><span data-ttu-id="2da99-105">Usage</span><span class="sxs-lookup"><span data-stu-id="2da99-105">Usage</span></span>

``` syntax
<macroPrefix/>
```

## <a name="attributes"></a><span data-ttu-id="2da99-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="2da99-106">Attributes</span></span>

<span data-ttu-id="2da99-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="2da99-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2da99-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2da99-108">Child elements</span></span>

<span data-ttu-id="2da99-109">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="2da99-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="2da99-110">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2da99-110">Parent elements</span></span>



| <span data-ttu-id="2da99-111">Élément</span><span class="sxs-lookup"><span data-stu-id="2da99-111">Element</span></span>                                   | <span data-ttu-id="2da99-112">Description</span><span class="sxs-lookup"><span data-stu-id="2da99-112">Description</span></span>                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="2da99-113">**Joint**</span><span class="sxs-lookup"><span data-stu-id="2da99-113">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="2da99-114">Espace de noms à utiliser pour la génération de code.</span><span class="sxs-lookup"><span data-stu-id="2da99-114">A namespace to be used for code generation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="2da99-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="2da99-115">Remarks</span></span>

<span data-ttu-id="2da99-116">Cet élément remplace le préfixe d’URI par défaut utilisé pour les macros générées.</span><span class="sxs-lookup"><span data-stu-id="2da99-116">This element overrides the default URI prefix used for generated macros.</span></span> <span data-ttu-id="2da99-117">Par exemple, si le préfixe de macro est « AV \_ » et que le nom est « tuner », la macro générée pour le nom qualifié sera « \_ tuner AV ».</span><span class="sxs-lookup"><span data-stu-id="2da99-117">For example, if the macro prefix is "AV\_" and the name is "Tuner", the macro generated for the qualified name will be "AV\_Tuner".</span></span>

<span data-ttu-id="2da99-118">Par défaut, le code généré crée un préfixe de macro préféré à partir de l’URI.</span><span class="sxs-lookup"><span data-stu-id="2da99-118">By default, the code generated creates a preferred macro prefix from the URI.</span></span>

## <a name="element-information"></a><span data-ttu-id="2da99-119">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="2da99-119">Element information</span></span>



| <span data-ttu-id="2da99-120">Étiquette</span><span class="sxs-lookup"><span data-stu-id="2da99-120">Label</span></span> | <span data-ttu-id="2da99-121">Value</span><span class="sxs-lookup"><span data-stu-id="2da99-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="2da99-122">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2da99-122">Minimum supported system</span></span><br/> | <span data-ttu-id="2da99-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2da99-123">Windows Vista</span></span> |
| <span data-ttu-id="2da99-124">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="2da99-124">Can be empty</span></span>                        | <span data-ttu-id="2da99-125">Oui</span><span class="sxs-lookup"><span data-stu-id="2da99-125">Yes</span></span>           |



 

 




