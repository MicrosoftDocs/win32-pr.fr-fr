---
description: Spécifie un fichier XSD à traiter pour les informations de contrat.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: élément xsd
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9628a078129446f51729c92c447f8da5736dab88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865337"
---
# <a name="xsd-element"></a><span data-ttu-id="31826-103">élément xsd</span><span class="sxs-lookup"><span data-stu-id="31826-103">xsd element</span></span>

<span data-ttu-id="31826-104">Spécifie un fichier XSD à traiter pour les informations de contrat.</span><span class="sxs-lookup"><span data-stu-id="31826-104">Specifies an XSD file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="31826-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="31826-105">Usage</span></span>

``` syntax
<xsd
  path = "pathname string">
  child elements
</xsd>
```

## <a name="attributes"></a><span data-ttu-id="31826-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="31826-106">Attributes</span></span>



| <span data-ttu-id="31826-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="31826-107">Attribute</span></span>           | <span data-ttu-id="31826-108">Type</span><span class="sxs-lookup"><span data-stu-id="31826-108">Type</span></span>                       | <span data-ttu-id="31826-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="31826-109">Required</span></span>       | <span data-ttu-id="31826-110">Description</span><span class="sxs-lookup"><span data-stu-id="31826-110">Description</span></span>                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="31826-111">**path**</span><span class="sxs-lookup"><span data-stu-id="31826-111">**path**</span></span><br/> | <span data-ttu-id="31826-112">chaîne du chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="31826-112">pathname string</span></span><br/> | <span data-ttu-id="31826-113">Oui</span><span class="sxs-lookup"><span data-stu-id="31826-113">Yes</span></span><br/> | <span data-ttu-id="31826-114">Fichier et chemin d’accès du fichier d’entrée XSD.</span><span class="sxs-lookup"><span data-stu-id="31826-114">File and path of the XSD input file.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="31826-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="31826-115">Child elements</span></span>



| <span data-ttu-id="31826-116">Élément</span><span class="sxs-lookup"><span data-stu-id="31826-116">Element</span></span>                               | <span data-ttu-id="31826-117">Description</span><span class="sxs-lookup"><span data-stu-id="31826-117">Description</span></span>                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="31826-118">**typeUri**</span><span class="sxs-lookup"><span data-stu-id="31826-118">**typeUri**</span></span>](typeuri.md)<br/> | <span data-ttu-id="31826-119">Spécifie un type à inclure à partir d’un fichier XSD.</span><span class="sxs-lookup"><span data-stu-id="31826-119">Specifies a type to include from an XSD file.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="31826-120">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="31826-120">Child element sequence</span></span>

``` syntax
typeUri*
```

## <a name="parent-elements"></a><span data-ttu-id="31826-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="31826-121">Parent elements</span></span>



| <span data-ttu-id="31826-122">Élément</span><span class="sxs-lookup"><span data-stu-id="31826-122">Element</span></span>                                     | <span data-ttu-id="31826-123">Description</span><span class="sxs-lookup"><span data-stu-id="31826-123">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="31826-124">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="31826-124">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="31826-125">Élément racine d’un fichier de script XML du générateur de code WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="31826-125">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="31826-126">Notes</span><span class="sxs-lookup"><span data-stu-id="31826-126">Remarks</span></span>

<span data-ttu-id="31826-127">La chaîne de nom de fichier doit également inclure des informations de chemin d’accès complètes.</span><span class="sxs-lookup"><span data-stu-id="31826-127">The filename string should include complete path information as well.</span></span>

## <a name="element-information"></a><span data-ttu-id="31826-128">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="31826-128">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="31826-129">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31826-129">Minimum supported system</span></span><br/> | <span data-ttu-id="31826-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31826-130">Windows Vista</span></span> |
| <span data-ttu-id="31826-131">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="31826-131">Can be empty</span></span>                        | <span data-ttu-id="31826-132">Oui</span><span class="sxs-lookup"><span data-stu-id="31826-132">Yes</span></span>           |



 

 




