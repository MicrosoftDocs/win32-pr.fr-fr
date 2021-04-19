---
description: URI qui représente l’identificateur de service.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: Élément ServiceID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305e97250b0b33d276dced4b5d454aec9298387c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539728"
---
# <a name="serviceid-element"></a><span data-ttu-id="932f8-103">Élément ServiceID</span><span class="sxs-lookup"><span data-stu-id="932f8-103">ServiceID element</span></span>

<span data-ttu-id="932f8-104">URI qui représente l’identificateur de service.</span><span class="sxs-lookup"><span data-stu-id="932f8-104">A URI that represents the service identifier.</span></span>

## <a name="usage"></a><span data-ttu-id="932f8-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="932f8-105">Usage</span></span>

``` syntax
<ServiceID/>
```

## <a name="attributes"></a><span data-ttu-id="932f8-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="932f8-106">Attributes</span></span>

<span data-ttu-id="932f8-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="932f8-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="932f8-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="932f8-108">Child elements</span></span>

<span data-ttu-id="932f8-109">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="932f8-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="932f8-110">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="932f8-110">Parent elements</span></span>



| <span data-ttu-id="932f8-111">Élément</span><span class="sxs-lookup"><span data-stu-id="932f8-111">Element</span></span>                             | <span data-ttu-id="932f8-112">Description</span><span class="sxs-lookup"><span data-stu-id="932f8-112">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="932f8-113">**HBA**</span><span class="sxs-lookup"><span data-stu-id="932f8-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="932f8-114">Définit les éléments **ServiceId** et [**types**](types.md) pour l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="932f8-114">Defines the **ServiceID** and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="932f8-115">S’il n’est pas fourni explicitement, WSDAPI ne fournit pas de données par défaut en réponse aux demandes de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="932f8-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                     |
| [<span data-ttu-id="932f8-116">**Hébergement**</span><span class="sxs-lookup"><span data-stu-id="932f8-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="932f8-117">Définit les éléments **ServiceId** et [**types**](types.md) pour les services fournis par cet hôte de service.</span><span class="sxs-lookup"><span data-stu-id="932f8-117">Defines the **ServiceID** and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="932f8-118">Chaque service fourni par cet hôte de service doit disposer de ses propres informations d’élément [**hébergé**](hosted.md) pour s’assurer que le service est correctement publié dans les réponses aux demandes de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="932f8-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="932f8-119">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="932f8-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="932f8-120">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="932f8-120">Minimum supported system</span></span><br/> | <span data-ttu-id="932f8-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="932f8-121">Windows Vista</span></span> |
| <span data-ttu-id="932f8-122">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="932f8-122">Can be empty</span></span>                        | <span data-ttu-id="932f8-123">Oui</span><span class="sxs-lookup"><span data-stu-id="932f8-123">Yes</span></span>           |



 

 




