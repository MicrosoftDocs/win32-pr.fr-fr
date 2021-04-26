---
description: Génère des déclarations de constante C pour les types de port.
ms.assetid: 05a06206-3cc4-428d-b9f2-b7945e63922c
title: élément portTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e19780d4a48c95cd47872b0428b368e6b7e99887
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996556"
---
# <a name="porttypedeclarations-element"></a><span data-ttu-id="74763-103">élément portTypeDeclarations</span><span class="sxs-lookup"><span data-stu-id="74763-103">portTypeDeclarations element</span></span>

<span data-ttu-id="74763-104">Génère des déclarations de constante C pour les types de port.</span><span class="sxs-lookup"><span data-stu-id="74763-104">Generates C constant declarations for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="74763-105">Usage</span><span class="sxs-lookup"><span data-stu-id="74763-105">Usage</span></span>

``` syntax
<portTypeDeclarations>
  child elements
</portTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="74763-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="74763-106">Attributes</span></span>

<span data-ttu-id="74763-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="74763-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="74763-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="74763-108">Child elements</span></span>



| <span data-ttu-id="74763-109">Élément</span><span class="sxs-lookup"><span data-stu-id="74763-109">Element</span></span>                                   | <span data-ttu-id="74763-110">Description</span><span class="sxs-lookup"><span data-stu-id="74763-110">Description</span></span>                                                                                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74763-111">**Baptisé**</span><span class="sxs-lookup"><span data-stu-id="74763-111">**codeName**</span></span>](codename.md)<br/>   | <span data-ttu-id="74763-112">Spécifie le nom à utiliser pour le type de port dans le code généré.</span><span class="sxs-lookup"><span data-stu-id="74763-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="74763-113">Par défaut, le nom de code est généré à partir du nom qualifié du type de port.</span><span class="sxs-lookup"><span data-stu-id="74763-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="74763-114">**opération**</span><span class="sxs-lookup"><span data-stu-id="74763-114">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="74763-115">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="74763-115">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                          |
| [<span data-ttu-id="74763-116">**portType**</span><span class="sxs-lookup"><span data-stu-id="74763-116">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="74763-117">Spécifie le type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="74763-117">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                         |



### <a name="child-element-sequence"></a><span data-ttu-id="74763-118">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="74763-118">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="74763-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="74763-119">Parent elements</span></span>



| <span data-ttu-id="74763-120">Élément</span><span class="sxs-lookup"><span data-stu-id="74763-120">Element</span></span>                         | <span data-ttu-id="74763-121">Description</span><span class="sxs-lookup"><span data-stu-id="74763-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="74763-122">**txt**</span><span class="sxs-lookup"><span data-stu-id="74763-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="74763-123">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="74763-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="74763-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="74763-124">Remarks</span></span>

<span data-ttu-id="74763-125">Les déclarations de type de port sont référencées par l’application et une grande partie du code généré.</span><span class="sxs-lookup"><span data-stu-id="74763-125">Port type declarations are referenced by the application and much of the generated code.</span></span> <span data-ttu-id="74763-126">Cet élément est utilisé pour générer des fichiers include.</span><span class="sxs-lookup"><span data-stu-id="74763-126">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="74763-127">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="74763-127">Element information</span></span>



| <span data-ttu-id="74763-128">Étiquette</span><span class="sxs-lookup"><span data-stu-id="74763-128">Label</span></span> | <span data-ttu-id="74763-129">Value</span><span class="sxs-lookup"><span data-stu-id="74763-129">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="74763-130">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74763-130">Minimum supported system</span></span><br/> | <span data-ttu-id="74763-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74763-131">Windows Vista</span></span> |
| <span data-ttu-id="74763-132">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="74763-132">Can be empty</span></span>                        | <span data-ttu-id="74763-133">Oui</span><span class="sxs-lookup"><span data-stu-id="74763-133">Yes</span></span>           |



 

 




