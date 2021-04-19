---
description: Génère des définitions de structure C pour les types de messages.
ms.assetid: 68459b22-0f35-444a-969e-29695e735774
title: élément messageStructureDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8840e4493cb97d33cb0dac8ce1ace97cc1789e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106530852"
---
# <a name="messagestructuredefinitions-element"></a><span data-ttu-id="012b5-103">élément messageStructureDefinitions</span><span class="sxs-lookup"><span data-stu-id="012b5-103">messageStructureDefinitions element</span></span>

<span data-ttu-id="012b5-104">Génère des définitions de structure C pour les types de messages.</span><span class="sxs-lookup"><span data-stu-id="012b5-104">Generates C structure definitions for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="012b5-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="012b5-105">Usage</span></span>

``` syntax
<messageStructureDefinitions>
  child elements
</messageStructureDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="012b5-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="012b5-106">Attributes</span></span>

<span data-ttu-id="012b5-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="012b5-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="012b5-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="012b5-108">Child elements</span></span>



| <span data-ttu-id="012b5-109">Élément</span><span class="sxs-lookup"><span data-stu-id="012b5-109">Element</span></span>                                   | <span data-ttu-id="012b5-110">Description</span><span class="sxs-lookup"><span data-stu-id="012b5-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="012b5-111">**opération**</span><span class="sxs-lookup"><span data-stu-id="012b5-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="012b5-112">Spécifie une opération pour laquelle du code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="012b5-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="012b5-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="012b5-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="012b5-114">Spécifie le type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="012b5-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="012b5-115">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="012b5-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="012b5-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="012b5-116">Parent elements</span></span>



| <span data-ttu-id="012b5-117">Élément</span><span class="sxs-lookup"><span data-stu-id="012b5-117">Element</span></span>                         | <span data-ttu-id="012b5-118">Description</span><span class="sxs-lookup"><span data-stu-id="012b5-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="012b5-119">**fichier**</span><span class="sxs-lookup"><span data-stu-id="012b5-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="012b5-120">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="012b5-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="012b5-121">Notes</span><span class="sxs-lookup"><span data-stu-id="012b5-121">Remarks</span></span>

<span data-ttu-id="012b5-122">Les structures de message sont référencées par le code stub et le proxy générés.</span><span class="sxs-lookup"><span data-stu-id="012b5-122">Message structures are referenced by generated proxy and stub code.</span></span> <span data-ttu-id="012b5-123">Cet élément est utilisé pour générer des fichiers include.</span><span class="sxs-lookup"><span data-stu-id="012b5-123">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="012b5-124">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="012b5-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="012b5-125">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="012b5-125">Minimum supported system</span></span><br/> | <span data-ttu-id="012b5-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="012b5-126">Windows Vista</span></span> |
| <span data-ttu-id="012b5-127">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="012b5-127">Can be empty</span></span>                        | <span data-ttu-id="012b5-128">Oui</span><span class="sxs-lookup"><span data-stu-id="012b5-128">Yes</span></span>           |



 

 




