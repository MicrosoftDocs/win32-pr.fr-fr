---
title: S (API UPnP)
description: Contient les termes relatifs à UPnP qui commencent par la lettre S.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 94be0f7f-8263-40ad-9d48-35540eaa3a3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9386d7946c51bc02e78aa96c36063d22d75d61d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032206"
---
# <a name="s-upnp-apis"></a><span data-ttu-id="7358b-103">S (API UPnP)</span><span class="sxs-lookup"><span data-stu-id="7358b-103">S (UPnP APIs)</span></span>

<span data-ttu-id="7358b-104">Contient les termes relatifs à UPnP qui commencent par la lettre S.</span><span class="sxs-lookup"><span data-stu-id="7358b-104">Contains UPnP-related terms that begin with the letter S.</span></span>

<span data-ttu-id="7358b-105">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) F G [H](h-gly.md) I J K L M [N](n-gly.md) O [P](p-gly.md) Q [R](r-gly.md) S T [U](u-gly.md) V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="7358b-105">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F G [H](h-gly.md) I J K L M [N](n-gly.md) O [P](p-gly.md) Q [R](r-gly.md) S T [U](u-gly.md) V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="7358b-106"><span id="upnp.s_1_gly"></span><span id="UPNP.S_1_GLY"></span>**services**</span><span class="sxs-lookup"><span data-stu-id="7358b-106"><span id="upnp.s_1_gly"></span><span id="UPNP.S_1_GLY"></span>**service**</span></span>
</dt> <dd>

<span data-ttu-id="7358b-107">Un service est une unité fonctionnelle logique.</span><span class="sxs-lookup"><span data-stu-id="7358b-107">A service is a logical functional unit.</span></span> <span data-ttu-id="7358b-108">Les services exposent des actions et modélisent tout ou partie des États d’un appareil physique à l’aide de variables d’État.</span><span class="sxs-lookup"><span data-stu-id="7358b-108">Services expose actions and model some or all of the states of a physical device using state variables.</span></span>

</dd> <dt>

<span data-ttu-id="7358b-109"><span id="upnp.s_2_gly"></span><span id="UPNP.S_2_GLY"></span>**Description du service**</span><span class="sxs-lookup"><span data-stu-id="7358b-109"><span id="upnp.s_2_gly"></span><span id="UPNP.S_2_GLY"></span>**service description**</span></span>
</dt> <dd>

<span data-ttu-id="7358b-110">Une description de service est une liste des actions fournies par un service, ainsi que les variables d’état associées aux actions.</span><span class="sxs-lookup"><span data-stu-id="7358b-110">A service description is a list of the actions a service provides, and the state variables associated with the actions.</span></span>

</dd> <dt>

<span data-ttu-id="7358b-111"><span id="upnp.s_3_gly"></span><span id="UPNP.S_3_GLY"></span>**objet de service**</span><span class="sxs-lookup"><span data-stu-id="7358b-111"><span id="upnp.s_3_gly"></span><span id="UPNP.S_3_GLY"></span>**service object**</span></span>
</dt> <dd>

<span data-ttu-id="7358b-112">Un objet de service est la représentation de l’API du point de contrôle d’un service.</span><span class="sxs-lookup"><span data-stu-id="7358b-112">A service object is the Control Point API representation of a service.</span></span> <span data-ttu-id="7358b-113">Un objet de service implémente l’interface [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) .</span><span class="sxs-lookup"><span data-stu-id="7358b-113">A service object implements the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) interface.</span></span>

</dd> <dt>

<span data-ttu-id="7358b-114"><span id="upnp.s_4_gly"></span><span id="UPNP.S_4_GLY"></span>**type de service**</span><span class="sxs-lookup"><span data-stu-id="7358b-114"><span id="upnp.s_4_gly"></span><span id="UPNP.S_4_GLY"></span>**service type**</span></span>
</dt> <dd>

<span data-ttu-id="7358b-115">Un type de service est un URN qui identifie un service.</span><span class="sxs-lookup"><span data-stu-id="7358b-115">A service type is a URN that identifies a service.</span></span> <span data-ttu-id="7358b-116">Il existe une relation un-à-un entre un modèle de service UPnP et un type de service.</span><span class="sxs-lookup"><span data-stu-id="7358b-116">There is a one-to-one relationship between a UPnP service template and a service type.</span></span> <span data-ttu-id="7358b-117">Plusieurs types de service standard sont définis par les comités de travail du Forum UPnP.</span><span class="sxs-lookup"><span data-stu-id="7358b-117">Several standard service types are defined by the UPnP Forum working committees.</span></span> <span data-ttu-id="7358b-118">Les types de service se présentent sous la forme urn : schemas-UPnP-org : service : serviceType : version.</span><span class="sxs-lookup"><span data-stu-id="7358b-118">The service types are in the form urn:schemas-upnp-org:service:serviceType:version.</span></span> <span data-ttu-id="7358b-119">Par exemple, un type de service de scanneur peut être urn : schemas-UPnP-org : service : scanner : 1.</span><span class="sxs-lookup"><span data-stu-id="7358b-119">For example, a scanner service type could be urn:schemas-upnp-org:service:scanner:1.</span></span>

<span data-ttu-id="7358b-120">Les fournisseurs UPnP peuvent spécifier des services supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="7358b-120">UPnP vendors may specify additional services.</span></span> <span data-ttu-id="7358b-121">Ces services sont dénotés par urn : Domain-Name : service : serviceType : version où Domain-Name est un nom de domaine qui est enregistré auprès du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7358b-121">Such services are denoted by urn:domain-name:service:serviceType:version where domain-name is a domain name that is registered to the vendor.</span></span>

</dd> <dt>

<span data-ttu-id="7358b-122"><span id="upnp.s_5_gly"></span><span id="UPNP.S_5_GLY"></span>**variable d’État**</span><span class="sxs-lookup"><span data-stu-id="7358b-122"><span id="upnp.s_5_gly"></span><span id="UPNP.S_5_GLY"></span>**state variable**</span></span>
</dt> <dd>

<span data-ttu-id="7358b-123">Une variable d’État est un élément de données qui décrit une partie de l’état d’un service.</span><span class="sxs-lookup"><span data-stu-id="7358b-123">A state variable is a piece of data that describes some part of a service's state.</span></span>

</dd> </dl>

 

 




