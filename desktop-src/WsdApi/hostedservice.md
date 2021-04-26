---
description: Définit un service à héberger dans une fonction de générateur d’hôte.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: élément service hébergé
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96c9f6e010989f4844d93299bb34f1ab8893236
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994786"
---
# <a name="hostedservice-element"></a><span data-ttu-id="0f8b1-103">élément service hébergé</span><span class="sxs-lookup"><span data-stu-id="0f8b1-103">hostedService element</span></span>

<span data-ttu-id="0f8b1-104">Définit un service à héberger dans une fonction de générateur d’hôte.</span><span class="sxs-lookup"><span data-stu-id="0f8b1-104">Defines a service to be hosted in a host builder function.</span></span>

## <a name="usage"></a><span data-ttu-id="0f8b1-105">Usage</span><span class="sxs-lookup"><span data-stu-id="0f8b1-105">Usage</span></span>

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a><span data-ttu-id="0f8b1-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="0f8b1-106">Attributes</span></span>

<span data-ttu-id="0f8b1-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="0f8b1-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0f8b1-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0f8b1-108">Child elements</span></span>



| <span data-ttu-id="0f8b1-109">Élément</span><span class="sxs-lookup"><span data-stu-id="0f8b1-109">Element</span></span>                                     | <span data-ttu-id="0f8b1-110">Description</span><span class="sxs-lookup"><span data-stu-id="0f8b1-110">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f8b1-111">**Baptisé**</span><span class="sxs-lookup"><span data-stu-id="0f8b1-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="0f8b1-112">Spécifie le nom à utiliser pour le type de port dans le code généré.</span><span class="sxs-lookup"><span data-stu-id="0f8b1-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="0f8b1-113">Par défaut, le nom de code est généré à partir du nom qualifié du type de port.</span><span class="sxs-lookup"><span data-stu-id="0f8b1-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="0f8b1-114">**portType**</span><span class="sxs-lookup"><span data-stu-id="0f8b1-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="0f8b1-115">Type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="0f8b1-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                                       |
| [<span data-ttu-id="0f8b1-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="0f8b1-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="0f8b1-117">Nom de la classe à générer à partir de la fonction de générateur.</span><span class="sxs-lookup"><span data-stu-id="0f8b1-117">Class name to generate from builder function.</span></span><br/> <br/>                                                                                                      |
| [<span data-ttu-id="0f8b1-118">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="0f8b1-118">**ServiceID**</span></span>](serviceid.md)<br/>   | <span data-ttu-id="0f8b1-119">URI qui représente l’identificateur de service.</span><span class="sxs-lookup"><span data-stu-id="0f8b1-119">A URI that represents the service identifier.</span></span><br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="0f8b1-120">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0f8b1-120">Child element sequence</span></span>

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a><span data-ttu-id="0f8b1-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0f8b1-121">Parent elements</span></span>



| <span data-ttu-id="0f8b1-122">Élément</span><span class="sxs-lookup"><span data-stu-id="0f8b1-122">Element</span></span>                         | <span data-ttu-id="0f8b1-123">Description</span><span class="sxs-lookup"><span data-stu-id="0f8b1-123">Description</span></span>                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="0f8b1-124">**txt**</span><span class="sxs-lookup"><span data-stu-id="0f8b1-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="0f8b1-125">Spécification du fichier de sortie pour le générateur de code.</span><span class="sxs-lookup"><span data-stu-id="0f8b1-125">The output file specification for the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="0f8b1-126">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0f8b1-126">Element information</span></span>



| <span data-ttu-id="0f8b1-127">Étiquette</span><span class="sxs-lookup"><span data-stu-id="0f8b1-127">Label</span></span> | <span data-ttu-id="0f8b1-128">Value</span><span class="sxs-lookup"><span data-stu-id="0f8b1-128">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="0f8b1-129">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f8b1-129">Minimum supported system</span></span><br/> | <span data-ttu-id="0f8b1-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f8b1-130">Windows Vista</span></span> |
| <span data-ttu-id="0f8b1-131">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="0f8b1-131">Can be empty</span></span>                        | <span data-ttu-id="0f8b1-132">Non</span><span class="sxs-lookup"><span data-stu-id="0f8b1-132">No</span></span>            |



 

 




