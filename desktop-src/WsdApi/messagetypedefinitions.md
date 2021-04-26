---
description: Génère des constantes C pour les tables de schéma XML pour les types de messages.
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: élément messageTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f1b6563254a93122960b4a990fe0bd18ab1453
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998706"
---
# <a name="messagetypedefinitions-element"></a><span data-ttu-id="b78fa-103">élément messageTypeDefinitions</span><span class="sxs-lookup"><span data-stu-id="b78fa-103">messageTypeDefinitions element</span></span>

<span data-ttu-id="b78fa-104">Génère des constantes C pour les tables de schéma XML pour les types de messages.</span><span class="sxs-lookup"><span data-stu-id="b78fa-104">Generates C constants for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="b78fa-105">Usage</span><span class="sxs-lookup"><span data-stu-id="b78fa-105">Usage</span></span>

``` syntax
<messageTypeDefinitions>
  child elements
</messageTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="b78fa-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="b78fa-106">Attributes</span></span>

<span data-ttu-id="b78fa-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="b78fa-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b78fa-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b78fa-108">Child elements</span></span>



| <span data-ttu-id="b78fa-109">Élément</span><span class="sxs-lookup"><span data-stu-id="b78fa-109">Element</span></span>                                   | <span data-ttu-id="b78fa-110">Description</span><span class="sxs-lookup"><span data-stu-id="b78fa-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="b78fa-111">**opération**</span><span class="sxs-lookup"><span data-stu-id="b78fa-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="b78fa-112">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="b78fa-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="b78fa-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="b78fa-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="b78fa-114">Spécifie le type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="b78fa-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="b78fa-115">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b78fa-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="b78fa-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b78fa-116">Parent elements</span></span>



| <span data-ttu-id="b78fa-117">Élément</span><span class="sxs-lookup"><span data-stu-id="b78fa-117">Element</span></span>                         | <span data-ttu-id="b78fa-118">Description</span><span class="sxs-lookup"><span data-stu-id="b78fa-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="b78fa-119">**txt**</span><span class="sxs-lookup"><span data-stu-id="b78fa-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="b78fa-120">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="b78fa-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b78fa-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="b78fa-121">Remarks</span></span>

<span data-ttu-id="b78fa-122">Cet élément est généralement utilisé dans les fichiers sources C pour fournir les tables de schéma déclarées par [**messageTypeDeclarations**](messagetypedeclarations.md).</span><span class="sxs-lookup"><span data-stu-id="b78fa-122">This element is generally used in C source files to provide the schema tables declared by [**messageTypeDeclarations**](messagetypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="b78fa-123">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b78fa-123">Element information</span></span>



| <span data-ttu-id="b78fa-124">Étiquette</span><span class="sxs-lookup"><span data-stu-id="b78fa-124">Label</span></span> | <span data-ttu-id="b78fa-125">Value</span><span class="sxs-lookup"><span data-stu-id="b78fa-125">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="b78fa-126">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b78fa-126">Minimum supported system</span></span><br/> | <span data-ttu-id="b78fa-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b78fa-127">Windows Vista</span></span> |
| <span data-ttu-id="b78fa-128">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="b78fa-128">Can be empty</span></span>                        | <span data-ttu-id="b78fa-129">Oui</span><span class="sxs-lookup"><span data-stu-id="b78fa-129">Yes</span></span>           |



 

 




