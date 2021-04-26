---
description: Génère des déclarations de constante C pour les tables de schéma XML pour les types de messages.
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: élément messageTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696cd6d30e6a791f68c152e0d0c5d0b1a7300769
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998726"
---
# <a name="messagetypedeclarations-element"></a><span data-ttu-id="0f4dd-103">élément messageTypeDeclarations</span><span class="sxs-lookup"><span data-stu-id="0f4dd-103">messageTypeDeclarations element</span></span>

<span data-ttu-id="0f4dd-104">Génère des déclarations de constante C pour les tables de schéma XML pour les types de messages.</span><span class="sxs-lookup"><span data-stu-id="0f4dd-104">Generates C constant declarations for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="0f4dd-105">Usage</span><span class="sxs-lookup"><span data-stu-id="0f4dd-105">Usage</span></span>

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="0f4dd-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="0f4dd-106">Attributes</span></span>

<span data-ttu-id="0f4dd-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="0f4dd-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0f4dd-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0f4dd-108">Child elements</span></span>



| <span data-ttu-id="0f4dd-109">Élément</span><span class="sxs-lookup"><span data-stu-id="0f4dd-109">Element</span></span>                                   | <span data-ttu-id="0f4dd-110">Description</span><span class="sxs-lookup"><span data-stu-id="0f4dd-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="0f4dd-111">**opération**</span><span class="sxs-lookup"><span data-stu-id="0f4dd-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="0f4dd-112">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="0f4dd-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="0f4dd-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="0f4dd-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="0f4dd-114">Spécifie le type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="0f4dd-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="0f4dd-115">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0f4dd-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="0f4dd-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0f4dd-116">Parent elements</span></span>



| <span data-ttu-id="0f4dd-117">Élément</span><span class="sxs-lookup"><span data-stu-id="0f4dd-117">Element</span></span>                         | <span data-ttu-id="0f4dd-118">Description</span><span class="sxs-lookup"><span data-stu-id="0f4dd-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="0f4dd-119">**txt**</span><span class="sxs-lookup"><span data-stu-id="0f4dd-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="0f4dd-120">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="0f4dd-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0f4dd-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="0f4dd-121">Remarks</span></span>

<span data-ttu-id="0f4dd-122">Les tables de schéma sont référencées par des définitions de type de port.</span><span class="sxs-lookup"><span data-stu-id="0f4dd-122">Schema tables are referenced by port type definitions.</span></span> <span data-ttu-id="0f4dd-123">Cet élément est donc généralement utilisé juste avant les éléments [**portTypeDefinitions**](porttypedefinitions.md) .</span><span class="sxs-lookup"><span data-stu-id="0f4dd-123">This element is therefore generally used just prior to [**portTypeDefinitions**](porttypedefinitions.md) elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="0f4dd-124">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0f4dd-124">Element information</span></span>



| <span data-ttu-id="0f4dd-125">Étiquette</span><span class="sxs-lookup"><span data-stu-id="0f4dd-125">Label</span></span> | <span data-ttu-id="0f4dd-126">Value</span><span class="sxs-lookup"><span data-stu-id="0f4dd-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="0f4dd-127">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f4dd-127">Minimum supported system</span></span><br/> | <span data-ttu-id="0f4dd-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f4dd-128">Windows Vista</span></span> |
| <span data-ttu-id="0f4dd-129">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="0f4dd-129">Can be empty</span></span>                        | <span data-ttu-id="0f4dd-130">Oui</span><span class="sxs-lookup"><span data-stu-id="0f4dd-130">Yes</span></span>           |



 

 




