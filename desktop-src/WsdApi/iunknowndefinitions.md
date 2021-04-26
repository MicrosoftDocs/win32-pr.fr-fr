---
description: Génère des implémentations pour les fonctions QueryInterface, AddRef et Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Élément IUnknownDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb3a4f76145e585411e64c10ea7af922db931846
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995146"
---
# <a name="iunknowndefinitions-element"></a><span data-ttu-id="79c4b-103">Élément IUnknownDefinitions</span><span class="sxs-lookup"><span data-stu-id="79c4b-103">IUnknownDefinitions element</span></span>

<span data-ttu-id="79c4b-104">Génère des implémentations pour les fonctions QueryInterface, AddRef et Release.</span><span class="sxs-lookup"><span data-stu-id="79c4b-104">Generates implementations for the QueryInterface, AddRef and Release functions.</span></span>

## <a name="usage"></a><span data-ttu-id="79c4b-105">Usage</span><span class="sxs-lookup"><span data-stu-id="79c4b-105">Usage</span></span>

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="79c4b-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="79c4b-106">Attributes</span></span>



| <span data-ttu-id="79c4b-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="79c4b-107">Attribute</span></span>                  | <span data-ttu-id="79c4b-108">Type</span><span class="sxs-lookup"><span data-stu-id="79c4b-108">Type</span></span>                         | <span data-ttu-id="79c4b-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="79c4b-109">Required</span></span>       | <span data-ttu-id="79c4b-110">Description</span><span class="sxs-lookup"><span data-stu-id="79c4b-110">Description</span></span>                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| <span data-ttu-id="79c4b-111">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="79c4b-111">**proxyClass**</span></span><br/>  | <span data-ttu-id="79c4b-112">chaîne de caractères \_</span><span class="sxs-lookup"><span data-stu-id="79c4b-112">character\_string</span></span><br/> | <span data-ttu-id="79c4b-113">Oui</span><span class="sxs-lookup"><span data-stu-id="79c4b-113">Yes</span></span><br/> | <span data-ttu-id="79c4b-114">Nom de la classe d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="79c4b-114">The name of the implementing class.</span></span><br/> <br/> |
| <span data-ttu-id="79c4b-115">**refCountVar**</span><span class="sxs-lookup"><span data-stu-id="79c4b-115">**refCountVar**</span></span><br/> | <span data-ttu-id="79c4b-116">chaîne de caractères \_</span><span class="sxs-lookup"><span data-stu-id="79c4b-116">character\_string</span></span><br/> | <span data-ttu-id="79c4b-117">Oui</span><span class="sxs-lookup"><span data-stu-id="79c4b-117">Yes</span></span><br/> | <span data-ttu-id="79c4b-118">Nom de la variable du décompte de références.</span><span class="sxs-lookup"><span data-stu-id="79c4b-118">The reference count variable name.</span></span><br/> <br/>  |



## <a name="child-elements"></a><span data-ttu-id="79c4b-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="79c4b-119">Child elements</span></span>



| <span data-ttu-id="79c4b-120">Élément</span><span class="sxs-lookup"><span data-stu-id="79c4b-120">Element</span></span>                                   | <span data-ttu-id="79c4b-121">Description</span><span class="sxs-lookup"><span data-stu-id="79c4b-121">Description</span></span>                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="79c4b-122">**interface**</span><span class="sxs-lookup"><span data-stu-id="79c4b-122">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="79c4b-123">Nom de l’interface à retourner par QueryInterface.</span><span class="sxs-lookup"><span data-stu-id="79c4b-123">The name of the interface to be returned by QueryInterface.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="79c4b-124">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="79c4b-124">Child element sequence</span></span>

``` syntax
interface
```

## <a name="parent-elements"></a><span data-ttu-id="79c4b-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="79c4b-125">Parent elements</span></span>



| <span data-ttu-id="79c4b-126">Élément</span><span class="sxs-lookup"><span data-stu-id="79c4b-126">Element</span></span>                         | <span data-ttu-id="79c4b-127">Description</span><span class="sxs-lookup"><span data-stu-id="79c4b-127">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="79c4b-128">**txt**</span><span class="sxs-lookup"><span data-stu-id="79c4b-128">**file**</span></span>](file.md)<br/> | <span data-ttu-id="79c4b-129">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="79c4b-129">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="79c4b-130">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="79c4b-130">Element information</span></span>



| <span data-ttu-id="79c4b-131">Étiquette</span><span class="sxs-lookup"><span data-stu-id="79c4b-131">Label</span></span> | <span data-ttu-id="79c4b-132">Value</span><span class="sxs-lookup"><span data-stu-id="79c4b-132">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="79c4b-133">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79c4b-133">Minimum supported system</span></span><br/> | <span data-ttu-id="79c4b-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79c4b-134">Windows Vista</span></span> |
| <span data-ttu-id="79c4b-135">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="79c4b-135">Can be empty</span></span>                        | <span data-ttu-id="79c4b-136">Non</span><span class="sxs-lookup"><span data-stu-id="79c4b-136">No</span></span>            |



 

 




