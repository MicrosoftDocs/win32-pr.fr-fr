---
description: Génère des déclarations de constante C pour les tables de schéma XML pour les types de messages.
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: élément messageTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 700511d3c0a83badcb15b0e07491a14ade53f454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952681"
---
# <a name="messagetypedeclarations-element"></a><span data-ttu-id="188dc-103">élément messageTypeDeclarations</span><span class="sxs-lookup"><span data-stu-id="188dc-103">messageTypeDeclarations element</span></span>

<span data-ttu-id="188dc-104">Génère des déclarations de constante C pour les tables de schéma XML pour les types de messages.</span><span class="sxs-lookup"><span data-stu-id="188dc-104">Generates C constant declarations for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="188dc-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="188dc-105">Usage</span></span>

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="188dc-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="188dc-106">Attributes</span></span>

<span data-ttu-id="188dc-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="188dc-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="188dc-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="188dc-108">Child elements</span></span>



| <span data-ttu-id="188dc-109">Élément</span><span class="sxs-lookup"><span data-stu-id="188dc-109">Element</span></span>                                   | <span data-ttu-id="188dc-110">Description</span><span class="sxs-lookup"><span data-stu-id="188dc-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="188dc-111">**opération**</span><span class="sxs-lookup"><span data-stu-id="188dc-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="188dc-112">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="188dc-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="188dc-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="188dc-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="188dc-114">Spécifie le type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="188dc-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="188dc-115">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="188dc-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="188dc-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="188dc-116">Parent elements</span></span>



| <span data-ttu-id="188dc-117">Élément</span><span class="sxs-lookup"><span data-stu-id="188dc-117">Element</span></span>                         | <span data-ttu-id="188dc-118">Description</span><span class="sxs-lookup"><span data-stu-id="188dc-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="188dc-119">**fichier**</span><span class="sxs-lookup"><span data-stu-id="188dc-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="188dc-120">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="188dc-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="188dc-121">Notes</span><span class="sxs-lookup"><span data-stu-id="188dc-121">Remarks</span></span>

<span data-ttu-id="188dc-122">Les tables de schéma sont référencées par des définitions de type de port.</span><span class="sxs-lookup"><span data-stu-id="188dc-122">Schema tables are referenced by port type definitions.</span></span> <span data-ttu-id="188dc-123">Cet élément est donc généralement utilisé juste avant les éléments [**portTypeDefinitions**](porttypedefinitions.md) .</span><span class="sxs-lookup"><span data-stu-id="188dc-123">This element is therefore generally used just prior to [**portTypeDefinitions**](porttypedefinitions.md) elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="188dc-124">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="188dc-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="188dc-125">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="188dc-125">Minimum supported system</span></span><br/> | <span data-ttu-id="188dc-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="188dc-126">Windows Vista</span></span> |
| <span data-ttu-id="188dc-127">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="188dc-127">Can be empty</span></span>                        | <span data-ttu-id="188dc-128">Oui</span><span class="sxs-lookup"><span data-stu-id="188dc-128">Yes</span></span>           |



 

 




