---
description: Définit le préfixe à utiliser dans le code généré pour les noms de macros dans l’espace de noms.
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: élément macroPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76c88dc48505e3344db1467463a9a99639edd881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517780"
---
# <a name="macroprefix-element"></a><span data-ttu-id="4aa0d-103">élément macroPrefix</span><span class="sxs-lookup"><span data-stu-id="4aa0d-103">macroPrefix element</span></span>

<span data-ttu-id="4aa0d-104">Définit le préfixe à utiliser dans le code généré pour les noms de macros dans l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="4aa0d-104">Defines the prefix to be used in the generated code for names of macros in the namespace.</span></span>

## <a name="usage"></a><span data-ttu-id="4aa0d-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="4aa0d-105">Usage</span></span>

``` syntax
<macroPrefix/>
```

## <a name="attributes"></a><span data-ttu-id="4aa0d-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="4aa0d-106">Attributes</span></span>

<span data-ttu-id="4aa0d-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="4aa0d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4aa0d-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4aa0d-108">Child elements</span></span>

<span data-ttu-id="4aa0d-109">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="4aa0d-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="4aa0d-110">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4aa0d-110">Parent elements</span></span>



| <span data-ttu-id="4aa0d-111">Élément</span><span class="sxs-lookup"><span data-stu-id="4aa0d-111">Element</span></span>                                   | <span data-ttu-id="4aa0d-112">Description</span><span class="sxs-lookup"><span data-stu-id="4aa0d-112">Description</span></span>                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="4aa0d-113">**Joint**</span><span class="sxs-lookup"><span data-stu-id="4aa0d-113">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="4aa0d-114">Espace de noms à utiliser pour la génération de code.</span><span class="sxs-lookup"><span data-stu-id="4aa0d-114">A namespace to be used for code generation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4aa0d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4aa0d-115">Remarks</span></span>

<span data-ttu-id="4aa0d-116">Cet élément remplace le préfixe d’URI par défaut utilisé pour les macros générées.</span><span class="sxs-lookup"><span data-stu-id="4aa0d-116">This element overrides the default URI prefix used for generated macros.</span></span> <span data-ttu-id="4aa0d-117">Par exemple, si le préfixe de macro est « AV \_ » et que le nom est « tuner », la macro générée pour le nom qualifié sera « \_ tuner AV ».</span><span class="sxs-lookup"><span data-stu-id="4aa0d-117">For example, if the macro prefix is "AV\_" and the name is "Tuner", the macro generated for the qualified name will be "AV\_Tuner".</span></span>

<span data-ttu-id="4aa0d-118">Par défaut, le code généré crée un préfixe de macro préféré à partir de l’URI.</span><span class="sxs-lookup"><span data-stu-id="4aa0d-118">By default, the code generated creates a preferred macro prefix from the URI.</span></span>

## <a name="element-information"></a><span data-ttu-id="4aa0d-119">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4aa0d-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="4aa0d-120">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4aa0d-120">Minimum supported system</span></span><br/> | <span data-ttu-id="4aa0d-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4aa0d-121">Windows Vista</span></span> |
| <span data-ttu-id="4aa0d-122">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="4aa0d-122">Can be empty</span></span>                        | <span data-ttu-id="4aa0d-123">Oui</span><span class="sxs-lookup"><span data-stu-id="4aa0d-123">Yes</span></span>           |



 

 




