---
description: 'Spécifie l’emplacement de téléchargement pour une directive wsdl : import qui ne spécifie pas explicitement d’emplacement.'
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: élément importHint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c874879ee0a608c100f32a0520a85efe76080cc2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998756"
---
# <a name="importhint-element"></a><span data-ttu-id="3b15d-103">élément importHint</span><span class="sxs-lookup"><span data-stu-id="3b15d-103">importHint element</span></span>

<span data-ttu-id="3b15d-104">Spécifie l’emplacement de téléchargement pour une \<wsdl:import> directive qui ne spécifie pas explicitement d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="3b15d-104">Specifies the download location for a \<wsdl:import> directive that does not explicitly specify a location.</span></span>

## <a name="usage"></a><span data-ttu-id="3b15d-105">Usage</span><span class="sxs-lookup"><span data-stu-id="3b15d-105">Usage</span></span>

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a><span data-ttu-id="3b15d-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="3b15d-106">Attributes</span></span>

<span data-ttu-id="3b15d-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="3b15d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3b15d-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3b15d-108">Child elements</span></span>



| <span data-ttu-id="3b15d-109">Élément</span><span class="sxs-lookup"><span data-stu-id="3b15d-109">Element</span></span>                                   | <span data-ttu-id="3b15d-110">Description</span><span class="sxs-lookup"><span data-stu-id="3b15d-110">Description</span></span>                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b15d-111">**location**</span><span class="sxs-lookup"><span data-stu-id="3b15d-111">**location**</span></span>](location.md)<br/>   | <span data-ttu-id="3b15d-112">Emplacement du fichier à importer.</span><span class="sxs-lookup"><span data-stu-id="3b15d-112">The location of the file to import.</span></span> <span data-ttu-id="3b15d-113">L’emplacement peut être un chemin d’accès relatif, un chemin d’accès absolu ou une URL HTTP.</span><span class="sxs-lookup"><span data-stu-id="3b15d-113">The location may be a relative path, an absolute path, or an HTTP URL.</span></span><br/> <br/> |
| [<span data-ttu-id="3b15d-114">**Joint**</span><span class="sxs-lookup"><span data-stu-id="3b15d-114">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="3b15d-115">Espace de noms à importer.</span><span class="sxs-lookup"><span data-stu-id="3b15d-115">The namespace to import.</span></span> <span data-ttu-id="3b15d-116">Cela doit correspondre à l’espace de noms spécifié dans l' \<wsdl:import> élément.</span><span class="sxs-lookup"><span data-stu-id="3b15d-116">This should match the namespace specified in the \<wsdl:import> element.</span></span><br/> <br/>     |



### <a name="child-element-sequence"></a><span data-ttu-id="3b15d-117">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3b15d-117">Child element sequence</span></span>

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a><span data-ttu-id="3b15d-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3b15d-118">Parent elements</span></span>



| <span data-ttu-id="3b15d-119">Élément</span><span class="sxs-lookup"><span data-stu-id="3b15d-119">Element</span></span>                         | <span data-ttu-id="3b15d-120">Description</span><span class="sxs-lookup"><span data-stu-id="3b15d-120">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="3b15d-121">**WSDL**</span><span class="sxs-lookup"><span data-stu-id="3b15d-121">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="3b15d-122">Spécifie un fichier WSDL à traiter pour les informations de contrat.</span><span class="sxs-lookup"><span data-stu-id="3b15d-122">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="3b15d-123">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="3b15d-123">Element information</span></span>



| <span data-ttu-id="3b15d-124">Étiquette</span><span class="sxs-lookup"><span data-stu-id="3b15d-124">Label</span></span> | <span data-ttu-id="3b15d-125">Value</span><span class="sxs-lookup"><span data-stu-id="3b15d-125">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="3b15d-126">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b15d-126">Minimum supported system</span></span><br/> | <span data-ttu-id="3b15d-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b15d-127">Windows Vista</span></span> |
| <span data-ttu-id="3b15d-128">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="3b15d-128">Can be empty</span></span>                        | <span data-ttu-id="3b15d-129">Non</span><span class="sxs-lookup"><span data-stu-id="3b15d-129">No</span></span>            |



 

 




