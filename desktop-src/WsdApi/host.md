---
description: Définit les éléments ServiceID et types pour l’hôte de service.
ms.assetid: 95066c04-5bdc-4c97-98b8-1da9928d9395
title: élément hôte
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec073a89cf1911ab363d757d36cd264c85c8a5c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863993"
---
# <a name="host-element"></a><span data-ttu-id="5d911-103">élément hôte</span><span class="sxs-lookup"><span data-stu-id="5d911-103">host element</span></span>

<span data-ttu-id="5d911-104">Définit les éléments [**ServiceId**](serviceid.md) et [**types**](types.md) pour l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="5d911-104">Defines the [**ServiceID**](serviceid.md) and [**Types**](types.md) elements for the service host.</span></span>

## <a name="usage"></a><span data-ttu-id="5d911-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="5d911-105">Usage</span></span>

``` syntax
<host>
  child elements
</host>
```

## <a name="attributes"></a><span data-ttu-id="5d911-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="5d911-106">Attributes</span></span>

<span data-ttu-id="5d911-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="5d911-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5d911-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5d911-108">Child elements</span></span>



| <span data-ttu-id="5d911-109">Élément</span><span class="sxs-lookup"><span data-stu-id="5d911-109">Element</span></span>                                   | <span data-ttu-id="5d911-110">Description</span><span class="sxs-lookup"><span data-stu-id="5d911-110">Description</span></span>                                                                 |
|-------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="5d911-111">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="5d911-111">**ServiceID**</span></span>](serviceid.md)<br/> | <span data-ttu-id="5d911-112">Définit l’identificateur de service pour l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="5d911-112">Defines the service identifier for the service host.</span></span><br/> <br/> |
| [<span data-ttu-id="5d911-113">**Types**</span><span class="sxs-lookup"><span data-stu-id="5d911-113">**Types**</span></span>](types.md)<br/>         | <span data-ttu-id="5d911-114">Définit une liste de noms qualifiés XSD.</span><span class="sxs-lookup"><span data-stu-id="5d911-114">Defines a list of XSD qualified names.</span></span><br/> <br/>               |



### <a name="child-element-sequence"></a><span data-ttu-id="5d911-115">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5d911-115">Child element sequence</span></span>

``` syntax
(
  ServiceID, 
  Types
)
```

## <a name="parent-elements"></a><span data-ttu-id="5d911-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5d911-116">Parent elements</span></span>



| <span data-ttu-id="5d911-117">Élément</span><span class="sxs-lookup"><span data-stu-id="5d911-117">Element</span></span>                                         | <span data-ttu-id="5d911-118">Description</span><span class="sxs-lookup"><span data-stu-id="5d911-118">Description</span></span>                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="5d911-119">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="5d911-119">**hostMetadata**</span></span>](hostmetadata.md)<br/> | <span data-ttu-id="5d911-120">Métadonnées d’hébergement pour l’appareil à implémenter.</span><span class="sxs-lookup"><span data-stu-id="5d911-120">The hosting metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="5d911-121">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="5d911-121">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="5d911-122">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d911-122">Minimum supported system</span></span><br/> | <span data-ttu-id="5d911-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d911-123">Windows Vista</span></span> |
| <span data-ttu-id="5d911-124">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="5d911-124">Can be empty</span></span>                        | <span data-ttu-id="5d911-125">Non</span><span class="sxs-lookup"><span data-stu-id="5d911-125">No</span></span>            |



 

 




