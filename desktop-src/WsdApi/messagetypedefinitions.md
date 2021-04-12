---
description: Génère des constantes C pour les tables de schéma XML pour les types de messages.
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: élément messageTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f86043cc28b527778c91772ad731d3a271921f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202265"
---
# <a name="messagetypedefinitions-element"></a><span data-ttu-id="b77d1-103">élément messageTypeDefinitions</span><span class="sxs-lookup"><span data-stu-id="b77d1-103">messageTypeDefinitions element</span></span>

<span data-ttu-id="b77d1-104">Génère des constantes C pour les tables de schéma XML pour les types de messages.</span><span class="sxs-lookup"><span data-stu-id="b77d1-104">Generates C constants for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="b77d1-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="b77d1-105">Usage</span></span>

``` syntax
<messageTypeDefinitions>
  child elements
</messageTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="b77d1-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="b77d1-106">Attributes</span></span>

<span data-ttu-id="b77d1-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="b77d1-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b77d1-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b77d1-108">Child elements</span></span>



| <span data-ttu-id="b77d1-109">Élément</span><span class="sxs-lookup"><span data-stu-id="b77d1-109">Element</span></span>                                   | <span data-ttu-id="b77d1-110">Description</span><span class="sxs-lookup"><span data-stu-id="b77d1-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="b77d1-111">**opération**</span><span class="sxs-lookup"><span data-stu-id="b77d1-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="b77d1-112">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="b77d1-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="b77d1-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="b77d1-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="b77d1-114">Spécifie le type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="b77d1-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="b77d1-115">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b77d1-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="b77d1-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b77d1-116">Parent elements</span></span>



| <span data-ttu-id="b77d1-117">Élément</span><span class="sxs-lookup"><span data-stu-id="b77d1-117">Element</span></span>                         | <span data-ttu-id="b77d1-118">Description</span><span class="sxs-lookup"><span data-stu-id="b77d1-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="b77d1-119">**fichier**</span><span class="sxs-lookup"><span data-stu-id="b77d1-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="b77d1-120">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="b77d1-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b77d1-121">Notes</span><span class="sxs-lookup"><span data-stu-id="b77d1-121">Remarks</span></span>

<span data-ttu-id="b77d1-122">Cet élément est généralement utilisé dans les fichiers sources C pour fournir les tables de schéma déclarées par [**messageTypeDeclarations**](messagetypedeclarations.md).</span><span class="sxs-lookup"><span data-stu-id="b77d1-122">This element is generally used in C source files to provide the schema tables declared by [**messageTypeDeclarations**](messagetypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="b77d1-123">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b77d1-123">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="b77d1-124">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b77d1-124">Minimum supported system</span></span><br/> | <span data-ttu-id="b77d1-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b77d1-125">Windows Vista</span></span> |
| <span data-ttu-id="b77d1-126">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="b77d1-126">Can be empty</span></span>                        | <span data-ttu-id="b77d1-127">Oui</span><span class="sxs-lookup"><span data-stu-id="b77d1-127">Yes</span></span>           |



 

 




