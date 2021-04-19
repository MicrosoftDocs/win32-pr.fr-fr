---
description: 'Spécifie l’emplacement de téléchargement pour une directive wsdl : import qui ne spécifie pas explicitement d’emplacement.'
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: élément importHint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29fcd65f9af02b8077ba828081ac9ed767d64e3
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380653"
---
# <a name="importhint-element"></a><span data-ttu-id="34856-103">élément importHint</span><span class="sxs-lookup"><span data-stu-id="34856-103">importHint element</span></span>

<span data-ttu-id="34856-104">Spécifie l’emplacement de téléchargement pour une \<wsdl:import> directive qui ne spécifie pas explicitement d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="34856-104">Specifies the download location for a \<wsdl:import> directive that does not explicitly specify a location.</span></span>

## <a name="usage"></a><span data-ttu-id="34856-105">Usage</span><span class="sxs-lookup"><span data-stu-id="34856-105">Usage</span></span>

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a><span data-ttu-id="34856-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="34856-106">Attributes</span></span>

<span data-ttu-id="34856-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="34856-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="34856-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="34856-108">Child elements</span></span>



| <span data-ttu-id="34856-109">Élément</span><span class="sxs-lookup"><span data-stu-id="34856-109">Element</span></span>                                   | <span data-ttu-id="34856-110">Description</span><span class="sxs-lookup"><span data-stu-id="34856-110">Description</span></span>                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34856-111">**location**</span><span class="sxs-lookup"><span data-stu-id="34856-111">**location**</span></span>](location.md)<br/>   | <span data-ttu-id="34856-112">Emplacement du fichier à importer.</span><span class="sxs-lookup"><span data-stu-id="34856-112">The location of the file to import.</span></span> <span data-ttu-id="34856-113">L’emplacement peut être un chemin d’accès relatif, un chemin d’accès absolu ou une URL HTTP.</span><span class="sxs-lookup"><span data-stu-id="34856-113">The location may be a relative path, an absolute path, or an HTTP URL.</span></span><br/> <br/> |
| [<span data-ttu-id="34856-114">**Joint**</span><span class="sxs-lookup"><span data-stu-id="34856-114">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="34856-115">Espace de noms à importer.</span><span class="sxs-lookup"><span data-stu-id="34856-115">The namespace to import.</span></span> <span data-ttu-id="34856-116">Cela doit correspondre à l’espace de noms spécifié dans l' \<wsdl:import> élément.</span><span class="sxs-lookup"><span data-stu-id="34856-116">This should match the namespace specified in the \<wsdl:import> element.</span></span><br/> <br/>     |



### <a name="child-element-sequence"></a><span data-ttu-id="34856-117">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="34856-117">Child element sequence</span></span>

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a><span data-ttu-id="34856-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="34856-118">Parent elements</span></span>



| <span data-ttu-id="34856-119">Élément</span><span class="sxs-lookup"><span data-stu-id="34856-119">Element</span></span>                         | <span data-ttu-id="34856-120">Description</span><span class="sxs-lookup"><span data-stu-id="34856-120">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="34856-121">**WSDL**</span><span class="sxs-lookup"><span data-stu-id="34856-121">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="34856-122">Spécifie un fichier WSDL à traiter pour les informations de contrat.</span><span class="sxs-lookup"><span data-stu-id="34856-122">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="34856-123">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="34856-123">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="34856-124">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34856-124">Minimum supported system</span></span><br/> | <span data-ttu-id="34856-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34856-125">Windows Vista</span></span> |
| <span data-ttu-id="34856-126">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="34856-126">Can be empty</span></span>                        | <span data-ttu-id="34856-127">Non</span><span class="sxs-lookup"><span data-stu-id="34856-127">No</span></span>            |



 

 




