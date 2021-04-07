---
description: Définit un service à héberger dans une fonction de générateur d’hôte.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: élément service hébergé
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfcf2f4c67cadf90279221fd5bdfd518e285e844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863990"
---
# <a name="hostedservice-element"></a><span data-ttu-id="f26f0-103">élément service hébergé</span><span class="sxs-lookup"><span data-stu-id="f26f0-103">hostedService element</span></span>

<span data-ttu-id="f26f0-104">Définit un service à héberger dans une fonction de générateur d’hôte.</span><span class="sxs-lookup"><span data-stu-id="f26f0-104">Defines a service to be hosted in a host builder function.</span></span>

## <a name="usage"></a><span data-ttu-id="f26f0-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="f26f0-105">Usage</span></span>

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a><span data-ttu-id="f26f0-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="f26f0-106">Attributes</span></span>

<span data-ttu-id="f26f0-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="f26f0-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f26f0-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f26f0-108">Child elements</span></span>



| <span data-ttu-id="f26f0-109">Élément</span><span class="sxs-lookup"><span data-stu-id="f26f0-109">Element</span></span>                                     | <span data-ttu-id="f26f0-110">Description</span><span class="sxs-lookup"><span data-stu-id="f26f0-110">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f26f0-111">**Baptisé**</span><span class="sxs-lookup"><span data-stu-id="f26f0-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="f26f0-112">Spécifie le nom à utiliser pour le type de port dans le code généré.</span><span class="sxs-lookup"><span data-stu-id="f26f0-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="f26f0-113">Par défaut, le nom de code est généré à partir du nom qualifié du type de port.</span><span class="sxs-lookup"><span data-stu-id="f26f0-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="f26f0-114">**portType**</span><span class="sxs-lookup"><span data-stu-id="f26f0-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="f26f0-115">Type de port pour lequel le code doit être généré.</span><span class="sxs-lookup"><span data-stu-id="f26f0-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                                       |
| [<span data-ttu-id="f26f0-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="f26f0-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="f26f0-117">Nom de la classe à générer à partir de la fonction de générateur.</span><span class="sxs-lookup"><span data-stu-id="f26f0-117">Class name to generate from builder function.</span></span><br/> <br/>                                                                                                      |
| [<span data-ttu-id="f26f0-118">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="f26f0-118">**ServiceID**</span></span>](serviceid.md)<br/>   | <span data-ttu-id="f26f0-119">URI qui représente l’identificateur de service.</span><span class="sxs-lookup"><span data-stu-id="f26f0-119">A URI that represents the service identifier.</span></span><br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="f26f0-120">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f26f0-120">Child element sequence</span></span>

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a><span data-ttu-id="f26f0-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f26f0-121">Parent elements</span></span>



| <span data-ttu-id="f26f0-122">Élément</span><span class="sxs-lookup"><span data-stu-id="f26f0-122">Element</span></span>                         | <span data-ttu-id="f26f0-123">Description</span><span class="sxs-lookup"><span data-stu-id="f26f0-123">Description</span></span>                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="f26f0-124">**fichier**</span><span class="sxs-lookup"><span data-stu-id="f26f0-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="f26f0-125">Spécification du fichier de sortie pour le générateur de code.</span><span class="sxs-lookup"><span data-stu-id="f26f0-125">The output file specification for the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="f26f0-126">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="f26f0-126">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="f26f0-127">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f26f0-127">Minimum supported system</span></span><br/> | <span data-ttu-id="f26f0-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f26f0-128">Windows Vista</span></span> |
| <span data-ttu-id="f26f0-129">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="f26f0-129">Can be empty</span></span>                        | <span data-ttu-id="f26f0-130">Non</span><span class="sxs-lookup"><span data-stu-id="f26f0-130">No</span></span>            |



 

 




