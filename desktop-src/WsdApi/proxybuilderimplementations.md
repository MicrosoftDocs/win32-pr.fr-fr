---
description: Génère des fonctions pour créer des proxies typés.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: élément proxyBuilderImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ad22348b33c60689adf60c029e3a08c2f4d417c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996466"
---
# <a name="proxybuilderimplementations-element"></a><span data-ttu-id="eae8a-103">élément proxyBuilderImplementations</span><span class="sxs-lookup"><span data-stu-id="eae8a-103">proxyBuilderImplementations element</span></span>

<span data-ttu-id="eae8a-104">Génère des fonctions pour créer des proxies typés.</span><span class="sxs-lookup"><span data-stu-id="eae8a-104">Generates functions to create typed proxies.</span></span>

## <a name="usage"></a><span data-ttu-id="eae8a-105">Usage</span><span class="sxs-lookup"><span data-stu-id="eae8a-105">Usage</span></span>

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a><span data-ttu-id="eae8a-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="eae8a-106">Attributes</span></span>

<span data-ttu-id="eae8a-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="eae8a-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="eae8a-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="eae8a-108">Child elements</span></span>



| <span data-ttu-id="eae8a-109">Élément</span><span class="sxs-lookup"><span data-stu-id="eae8a-109">Element</span></span>                                     | <span data-ttu-id="eae8a-110">Description</span><span class="sxs-lookup"><span data-stu-id="eae8a-110">Description</span></span>                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eae8a-111">**Baptisé**</span><span class="sxs-lookup"><span data-stu-id="eae8a-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="eae8a-112">Nom à utiliser pour le type de port dans le code généré.</span><span class="sxs-lookup"><span data-stu-id="eae8a-112">The name to be used for the port type in the generated code.</span></span> <span data-ttu-id="eae8a-113">Par défaut, le nom de code est généré à partir du nom qualifié du type de port.</span><span class="sxs-lookup"><span data-stu-id="eae8a-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="eae8a-114">**portType**</span><span class="sxs-lookup"><span data-stu-id="eae8a-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="eae8a-115">Type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="eae8a-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                             |
| [<span data-ttu-id="eae8a-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="eae8a-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="eae8a-117">Nom de classe à générer à partir de la fonction de générateur de proxy.</span><span class="sxs-lookup"><span data-stu-id="eae8a-117">Class name to generate from the proxy builder function.</span></span><br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="eae8a-118">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="eae8a-118">Child element sequence</span></span>

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
)
```

## <a name="parent-elements"></a><span data-ttu-id="eae8a-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="eae8a-119">Parent elements</span></span>



| <span data-ttu-id="eae8a-120">Élément</span><span class="sxs-lookup"><span data-stu-id="eae8a-120">Element</span></span>                         | <span data-ttu-id="eae8a-121">Description</span><span class="sxs-lookup"><span data-stu-id="eae8a-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="eae8a-122">**txt**</span><span class="sxs-lookup"><span data-stu-id="eae8a-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="eae8a-123">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="eae8a-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="eae8a-124">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="eae8a-124">Element information</span></span>



| <span data-ttu-id="eae8a-125">Étiquette</span><span class="sxs-lookup"><span data-stu-id="eae8a-125">Label</span></span> | <span data-ttu-id="eae8a-126">Value</span><span class="sxs-lookup"><span data-stu-id="eae8a-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="eae8a-127">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eae8a-127">Minimum supported system</span></span><br/> | <span data-ttu-id="eae8a-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eae8a-128">Windows Vista</span></span> |
| <span data-ttu-id="eae8a-129">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="eae8a-129">Can be empty</span></span>                        | <span data-ttu-id="eae8a-130">Non</span><span class="sxs-lookup"><span data-stu-id="eae8a-130">No</span></span>            |



 

 




