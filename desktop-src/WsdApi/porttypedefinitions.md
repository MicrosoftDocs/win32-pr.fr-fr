---
description: Génère des constantes C pour les types de ports.
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: élément portTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff073eb7b0f9cbc4b0b6df87c8f9fc84d4f62882
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996546"
---
# <a name="porttypedefinitions-element"></a><span data-ttu-id="cf255-103">élément portTypeDefinitions</span><span class="sxs-lookup"><span data-stu-id="cf255-103">portTypeDefinitions element</span></span>

<span data-ttu-id="cf255-104">Génère des constantes C pour les types de ports.</span><span class="sxs-lookup"><span data-stu-id="cf255-104">Generates C constants for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="cf255-105">Usage</span><span class="sxs-lookup"><span data-stu-id="cf255-105">Usage</span></span>

``` syntax
<portTypeDefinitions>
  child elements
</portTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="cf255-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="cf255-106">Attributes</span></span>

<span data-ttu-id="cf255-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="cf255-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="cf255-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cf255-108">Child elements</span></span>



| <span data-ttu-id="cf255-109">Élément</span><span class="sxs-lookup"><span data-stu-id="cf255-109">Element</span></span>                                                   | <span data-ttu-id="cf255-110">Description</span><span class="sxs-lookup"><span data-stu-id="cf255-110">Description</span></span>                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf255-111">**Baptisé**</span><span class="sxs-lookup"><span data-stu-id="cf255-111">**codeName**</span></span>](codename.md)<br/>                   | <span data-ttu-id="cf255-112">Spécifie le nom à utiliser pour le type de port dans le code généré.</span><span class="sxs-lookup"><span data-stu-id="cf255-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="cf255-113">Par défaut, le nom de code est généré à partir du nom qualifié du type de port.</span><span class="sxs-lookup"><span data-stu-id="cf255-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/>         |
| [<span data-ttu-id="cf255-114">**eventStubFunction**</span><span class="sxs-lookup"><span data-stu-id="cf255-114">**eventStubFunction**</span></span>](eventstubfunction.md)<br/> | <span data-ttu-id="cf255-115">Spécifie si les références de fonction stub doivent être incluses dans les structures d’opération dans les définitions de type de port pour les opérations de notification.</span><span class="sxs-lookup"><span data-stu-id="cf255-115">Specifies whether stub function references should be included in the operation structures in the port type definitions for notification operations.</span></span><br/> <br/>        |
| [<span data-ttu-id="cf255-116">**opération**</span><span class="sxs-lookup"><span data-stu-id="cf255-116">**operation**</span></span>](operation.md)<br/>                 | <span data-ttu-id="cf255-117">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="cf255-117">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                                  |
| [<span data-ttu-id="cf255-118">**portType**</span><span class="sxs-lookup"><span data-stu-id="cf255-118">**portType**</span></span>](porttype.md)<br/>                   | <span data-ttu-id="cf255-119">Spécifie le type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="cf255-119">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                                 |
| [<span data-ttu-id="cf255-120">**stubFunction**</span><span class="sxs-lookup"><span data-stu-id="cf255-120">**stubFunction**</span></span>](stubfunction.md)<br/>           | <span data-ttu-id="cf255-121">Spécifie si les références de fonction stub doivent être incluses dans les structures d’opération dans les définitions de type de port pour les opérations unidirectionnelles et bidirectionnelles.</span><span class="sxs-lookup"><span data-stu-id="cf255-121">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="cf255-122">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cf255-122">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  stubFunction?, 
  eventStubFunction?, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="cf255-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="cf255-123">Parent elements</span></span>



| <span data-ttu-id="cf255-124">Élément</span><span class="sxs-lookup"><span data-stu-id="cf255-124">Element</span></span>                         | <span data-ttu-id="cf255-125">Description</span><span class="sxs-lookup"><span data-stu-id="cf255-125">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="cf255-126">**txt**</span><span class="sxs-lookup"><span data-stu-id="cf255-126">**file**</span></span>](file.md)<br/> | <span data-ttu-id="cf255-127">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="cf255-127">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="cf255-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="cf255-128">Remarks</span></span>

<span data-ttu-id="cf255-129">Cet élément est généralement utilisé dans les fichiers sources C pour fournir les constantes de type de port déclarées par [**portTypeDeclarations**](porttypedeclarations.md).</span><span class="sxs-lookup"><span data-stu-id="cf255-129">This element is generally used in C source files to provide the port type constants declared by [**portTypeDeclarations**](porttypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="cf255-130">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="cf255-130">Element information</span></span>



| <span data-ttu-id="cf255-131">Étiquette</span><span class="sxs-lookup"><span data-stu-id="cf255-131">Label</span></span> | <span data-ttu-id="cf255-132">Value</span><span class="sxs-lookup"><span data-stu-id="cf255-132">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="cf255-133">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf255-133">Minimum supported system</span></span><br/> | <span data-ttu-id="cf255-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf255-134">Windows Vista</span></span> |
| <span data-ttu-id="cf255-135">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="cf255-135">Can be empty</span></span>                        | <span data-ttu-id="cf255-136">Oui</span><span class="sxs-lookup"><span data-stu-id="cf255-136">Yes</span></span>           |



 

 




