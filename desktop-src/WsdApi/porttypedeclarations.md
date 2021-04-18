---
description: Génère des déclarations de constante C pour les types de port.
ms.assetid: 05a06206-3cc4-428d-b9f2-b7945e63922c
title: élément portTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c4e202f1451d93b519bd59ea51f591c37a92957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533826"
---
# <a name="porttypedeclarations-element"></a><span data-ttu-id="b4f49-103">élément portTypeDeclarations</span><span class="sxs-lookup"><span data-stu-id="b4f49-103">portTypeDeclarations element</span></span>

<span data-ttu-id="b4f49-104">Génère des déclarations de constante C pour les types de port.</span><span class="sxs-lookup"><span data-stu-id="b4f49-104">Generates C constant declarations for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="b4f49-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="b4f49-105">Usage</span></span>

``` syntax
<portTypeDeclarations>
  child elements
</portTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="b4f49-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="b4f49-106">Attributes</span></span>

<span data-ttu-id="b4f49-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="b4f49-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b4f49-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b4f49-108">Child elements</span></span>



| <span data-ttu-id="b4f49-109">Élément</span><span class="sxs-lookup"><span data-stu-id="b4f49-109">Element</span></span>                                   | <span data-ttu-id="b4f49-110">Description</span><span class="sxs-lookup"><span data-stu-id="b4f49-110">Description</span></span>                                                                                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4f49-111">**Baptisé**</span><span class="sxs-lookup"><span data-stu-id="b4f49-111">**codeName**</span></span>](codename.md)<br/>   | <span data-ttu-id="b4f49-112">Spécifie le nom à utiliser pour le type de port dans le code généré.</span><span class="sxs-lookup"><span data-stu-id="b4f49-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="b4f49-113">Par défaut, le nom de code est généré à partir du nom qualifié du type de port.</span><span class="sxs-lookup"><span data-stu-id="b4f49-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="b4f49-114">**opération**</span><span class="sxs-lookup"><span data-stu-id="b4f49-114">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="b4f49-115">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="b4f49-115">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                          |
| [<span data-ttu-id="b4f49-116">**portType**</span><span class="sxs-lookup"><span data-stu-id="b4f49-116">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="b4f49-117">Spécifie le type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="b4f49-117">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                         |



### <a name="child-element-sequence"></a><span data-ttu-id="b4f49-118">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b4f49-118">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="b4f49-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b4f49-119">Parent elements</span></span>



| <span data-ttu-id="b4f49-120">Élément</span><span class="sxs-lookup"><span data-stu-id="b4f49-120">Element</span></span>                         | <span data-ttu-id="b4f49-121">Description</span><span class="sxs-lookup"><span data-stu-id="b4f49-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="b4f49-122">**fichier**</span><span class="sxs-lookup"><span data-stu-id="b4f49-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="b4f49-123">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="b4f49-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b4f49-124">Notes</span><span class="sxs-lookup"><span data-stu-id="b4f49-124">Remarks</span></span>

<span data-ttu-id="b4f49-125">Les déclarations de type de port sont référencées par l’application et une grande partie du code généré.</span><span class="sxs-lookup"><span data-stu-id="b4f49-125">Port type declarations are referenced by the application and much of the generated code.</span></span> <span data-ttu-id="b4f49-126">Cet élément est utilisé pour générer des fichiers include.</span><span class="sxs-lookup"><span data-stu-id="b4f49-126">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="b4f49-127">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="b4f49-127">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="b4f49-128">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4f49-128">Minimum supported system</span></span><br/> | <span data-ttu-id="b4f49-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4f49-129">Windows Vista</span></span> |
| <span data-ttu-id="b4f49-130">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="b4f49-130">Can be empty</span></span>                        | <span data-ttu-id="b4f49-131">Oui</span><span class="sxs-lookup"><span data-stu-id="b4f49-131">Yes</span></span>           |



 

 




