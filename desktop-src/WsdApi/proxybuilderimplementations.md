---
description: Génère des fonctions pour créer des proxies typés.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: élément proxyBuilderImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2cb64a6ea87b1083871931359a4f7c01ece9b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522136"
---
# <a name="proxybuilderimplementations-element"></a><span data-ttu-id="e16b0-103">élément proxyBuilderImplementations</span><span class="sxs-lookup"><span data-stu-id="e16b0-103">proxyBuilderImplementations element</span></span>

<span data-ttu-id="e16b0-104">Génère des fonctions pour créer des proxies typés.</span><span class="sxs-lookup"><span data-stu-id="e16b0-104">Generates functions to create typed proxies.</span></span>

## <a name="usage"></a><span data-ttu-id="e16b0-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="e16b0-105">Usage</span></span>

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a><span data-ttu-id="e16b0-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="e16b0-106">Attributes</span></span>

<span data-ttu-id="e16b0-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="e16b0-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e16b0-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e16b0-108">Child elements</span></span>



| <span data-ttu-id="e16b0-109">Élément</span><span class="sxs-lookup"><span data-stu-id="e16b0-109">Element</span></span>                                     | <span data-ttu-id="e16b0-110">Description</span><span class="sxs-lookup"><span data-stu-id="e16b0-110">Description</span></span>                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e16b0-111">**Baptisé**</span><span class="sxs-lookup"><span data-stu-id="e16b0-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="e16b0-112">Nom à utiliser pour le type de port dans le code généré.</span><span class="sxs-lookup"><span data-stu-id="e16b0-112">The name to be used for the port type in the generated code.</span></span> <span data-ttu-id="e16b0-113">Par défaut, le nom de code est généré à partir du nom qualifié du type de port.</span><span class="sxs-lookup"><span data-stu-id="e16b0-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="e16b0-114">**portType**</span><span class="sxs-lookup"><span data-stu-id="e16b0-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="e16b0-115">Type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="e16b0-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                             |
| [<span data-ttu-id="e16b0-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="e16b0-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="e16b0-117">Nom de classe à générer à partir de la fonction de générateur de proxy.</span><span class="sxs-lookup"><span data-stu-id="e16b0-117">Class name to generate from the proxy builder function.</span></span><br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="e16b0-118">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e16b0-118">Child element sequence</span></span>

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
)
```

## <a name="parent-elements"></a><span data-ttu-id="e16b0-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e16b0-119">Parent elements</span></span>



| <span data-ttu-id="e16b0-120">Élément</span><span class="sxs-lookup"><span data-stu-id="e16b0-120">Element</span></span>                         | <span data-ttu-id="e16b0-121">Description</span><span class="sxs-lookup"><span data-stu-id="e16b0-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="e16b0-122">**fichier**</span><span class="sxs-lookup"><span data-stu-id="e16b0-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="e16b0-123">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="e16b0-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="e16b0-124">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e16b0-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="e16b0-125">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e16b0-125">Minimum supported system</span></span><br/> | <span data-ttu-id="e16b0-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e16b0-126">Windows Vista</span></span> |
| <span data-ttu-id="e16b0-127">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="e16b0-127">Can be empty</span></span>                        | <span data-ttu-id="e16b0-128">Non</span><span class="sxs-lookup"><span data-stu-id="e16b0-128">No</span></span>            |



 

 




