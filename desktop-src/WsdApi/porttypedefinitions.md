---
description: Génère des constantes C pour les types de ports.
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: élément portTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60f55408df938ed95af14c69b2676473ac1bda71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203001"
---
# <a name="porttypedefinitions-element"></a><span data-ttu-id="10581-103">élément portTypeDefinitions</span><span class="sxs-lookup"><span data-stu-id="10581-103">portTypeDefinitions element</span></span>

<span data-ttu-id="10581-104">Génère des constantes C pour les types de ports.</span><span class="sxs-lookup"><span data-stu-id="10581-104">Generates C constants for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="10581-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="10581-105">Usage</span></span>

``` syntax
<portTypeDefinitions>
  child elements
</portTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="10581-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="10581-106">Attributes</span></span>

<span data-ttu-id="10581-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="10581-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="10581-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="10581-108">Child elements</span></span>



| <span data-ttu-id="10581-109">Élément</span><span class="sxs-lookup"><span data-stu-id="10581-109">Element</span></span>                                                   | <span data-ttu-id="10581-110">Description</span><span class="sxs-lookup"><span data-stu-id="10581-110">Description</span></span>                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10581-111">**Baptisé**</span><span class="sxs-lookup"><span data-stu-id="10581-111">**codeName**</span></span>](codename.md)<br/>                   | <span data-ttu-id="10581-112">Spécifie le nom à utiliser pour le type de port dans le code généré.</span><span class="sxs-lookup"><span data-stu-id="10581-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="10581-113">Par défaut, le nom de code est généré à partir du nom qualifié du type de port.</span><span class="sxs-lookup"><span data-stu-id="10581-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/>         |
| [<span data-ttu-id="10581-114">**eventStubFunction**</span><span class="sxs-lookup"><span data-stu-id="10581-114">**eventStubFunction**</span></span>](eventstubfunction.md)<br/> | <span data-ttu-id="10581-115">Spécifie si les références de fonction stub doivent être incluses dans les structures d’opération dans les définitions de type de port pour les opérations de notification.</span><span class="sxs-lookup"><span data-stu-id="10581-115">Specifies whether stub function references should be included in the operation structures in the port type definitions for notification operations.</span></span><br/> <br/>        |
| [<span data-ttu-id="10581-116">**opération**</span><span class="sxs-lookup"><span data-stu-id="10581-116">**operation**</span></span>](operation.md)<br/>                 | <span data-ttu-id="10581-117">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="10581-117">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                                  |
| [<span data-ttu-id="10581-118">**portType**</span><span class="sxs-lookup"><span data-stu-id="10581-118">**portType**</span></span>](porttype.md)<br/>                   | <span data-ttu-id="10581-119">Spécifie le type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="10581-119">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                                 |
| [<span data-ttu-id="10581-120">**stubFunction**</span><span class="sxs-lookup"><span data-stu-id="10581-120">**stubFunction**</span></span>](stubfunction.md)<br/>           | <span data-ttu-id="10581-121">Spécifie si les références de fonction stub doivent être incluses dans les structures d’opération dans les définitions de type de port pour les opérations unidirectionnelles et bidirectionnelles.</span><span class="sxs-lookup"><span data-stu-id="10581-121">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="10581-122">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="10581-122">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  stubFunction?, 
  eventStubFunction?, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="10581-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="10581-123">Parent elements</span></span>



| <span data-ttu-id="10581-124">Élément</span><span class="sxs-lookup"><span data-stu-id="10581-124">Element</span></span>                         | <span data-ttu-id="10581-125">Description</span><span class="sxs-lookup"><span data-stu-id="10581-125">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="10581-126">**fichier**</span><span class="sxs-lookup"><span data-stu-id="10581-126">**file**</span></span>](file.md)<br/> | <span data-ttu-id="10581-127">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="10581-127">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="10581-128">Notes</span><span class="sxs-lookup"><span data-stu-id="10581-128">Remarks</span></span>

<span data-ttu-id="10581-129">Cet élément est généralement utilisé dans les fichiers sources C pour fournir les constantes de type de port déclarées par [**portTypeDeclarations**](porttypedeclarations.md).</span><span class="sxs-lookup"><span data-stu-id="10581-129">This element is generally used in C source files to provide the port type constants declared by [**portTypeDeclarations**](porttypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="10581-130">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="10581-130">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="10581-131">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10581-131">Minimum supported system</span></span><br/> | <span data-ttu-id="10581-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10581-132">Windows Vista</span></span> |
| <span data-ttu-id="10581-133">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="10581-133">Can be empty</span></span>                        | <span data-ttu-id="10581-134">Oui</span><span class="sxs-lookup"><span data-stu-id="10581-134">Yes</span></span>           |



 

 




