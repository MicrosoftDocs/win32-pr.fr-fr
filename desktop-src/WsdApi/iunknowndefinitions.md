---
description: Génère des implémentations pour les fonctions QueryInterface, AddRef et Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Élément IUnknownDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ca92338e3dc97a12e04228510fc17eb2ef2483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524991"
---
# <a name="iunknowndefinitions-element"></a><span data-ttu-id="4287e-103">Élément IUnknownDefinitions</span><span class="sxs-lookup"><span data-stu-id="4287e-103">IUnknownDefinitions element</span></span>

<span data-ttu-id="4287e-104">Génère des implémentations pour les fonctions QueryInterface, AddRef et Release.</span><span class="sxs-lookup"><span data-stu-id="4287e-104">Generates implementations for the QueryInterface, AddRef and Release functions.</span></span>

## <a name="usage"></a><span data-ttu-id="4287e-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="4287e-105">Usage</span></span>

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="4287e-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="4287e-106">Attributes</span></span>



| <span data-ttu-id="4287e-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="4287e-107">Attribute</span></span>                  | <span data-ttu-id="4287e-108">Type</span><span class="sxs-lookup"><span data-stu-id="4287e-108">Type</span></span>                         | <span data-ttu-id="4287e-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4287e-109">Required</span></span>       | <span data-ttu-id="4287e-110">Description</span><span class="sxs-lookup"><span data-stu-id="4287e-110">Description</span></span>                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| <span data-ttu-id="4287e-111">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="4287e-111">**proxyClass**</span></span><br/>  | <span data-ttu-id="4287e-112">chaîne de caractères \_</span><span class="sxs-lookup"><span data-stu-id="4287e-112">character\_string</span></span><br/> | <span data-ttu-id="4287e-113">Oui</span><span class="sxs-lookup"><span data-stu-id="4287e-113">Yes</span></span><br/> | <span data-ttu-id="4287e-114">Nom de la classe d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="4287e-114">The name of the implementing class.</span></span><br/> <br/> |
| <span data-ttu-id="4287e-115">**refCountVar**</span><span class="sxs-lookup"><span data-stu-id="4287e-115">**refCountVar**</span></span><br/> | <span data-ttu-id="4287e-116">chaîne de caractères \_</span><span class="sxs-lookup"><span data-stu-id="4287e-116">character\_string</span></span><br/> | <span data-ttu-id="4287e-117">Oui</span><span class="sxs-lookup"><span data-stu-id="4287e-117">Yes</span></span><br/> | <span data-ttu-id="4287e-118">Nom de la variable du décompte de références.</span><span class="sxs-lookup"><span data-stu-id="4287e-118">The reference count variable name.</span></span><br/> <br/>  |



## <a name="child-elements"></a><span data-ttu-id="4287e-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4287e-119">Child elements</span></span>



| <span data-ttu-id="4287e-120">Élément</span><span class="sxs-lookup"><span data-stu-id="4287e-120">Element</span></span>                                   | <span data-ttu-id="4287e-121">Description</span><span class="sxs-lookup"><span data-stu-id="4287e-121">Description</span></span>                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="4287e-122">**interface**</span><span class="sxs-lookup"><span data-stu-id="4287e-122">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="4287e-123">Nom de l’interface à retourner par QueryInterface.</span><span class="sxs-lookup"><span data-stu-id="4287e-123">The name of the interface to be returned by QueryInterface.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="4287e-124">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4287e-124">Child element sequence</span></span>

``` syntax
interface
```

## <a name="parent-elements"></a><span data-ttu-id="4287e-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4287e-125">Parent elements</span></span>



| <span data-ttu-id="4287e-126">Élément</span><span class="sxs-lookup"><span data-stu-id="4287e-126">Element</span></span>                         | <span data-ttu-id="4287e-127">Description</span><span class="sxs-lookup"><span data-stu-id="4287e-127">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="4287e-128">**fichier**</span><span class="sxs-lookup"><span data-stu-id="4287e-128">**file**</span></span>](file.md)<br/> | <span data-ttu-id="4287e-129">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="4287e-129">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="4287e-130">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4287e-130">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="4287e-131">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4287e-131">Minimum supported system</span></span><br/> | <span data-ttu-id="4287e-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4287e-132">Windows Vista</span></span> |
| <span data-ttu-id="4287e-133">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="4287e-133">Can be empty</span></span>                        | <span data-ttu-id="4287e-134">Non</span><span class="sxs-lookup"><span data-stu-id="4287e-134">No</span></span>            |



 

 




