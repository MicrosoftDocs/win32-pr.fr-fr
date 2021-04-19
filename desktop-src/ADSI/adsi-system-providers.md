---
title: Fournisseurs de services ADSI
description: Cette rubrique donne une vue d’ensemble des fournisseurs de services ADSI fournis sur le serveur.
ms.assetid: 419d7953-a879-4d6c-be74-173d76c3f932
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, fournisseurs de services
- Fournisseurs de services ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44ba4ebc63338bfb38d2b9d5da1f46e51b31aa8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106513740"
---
# <a name="adsi-service-providers"></a><span data-ttu-id="9e79b-105">Fournisseurs de services ADSI</span><span class="sxs-lookup"><span data-stu-id="9e79b-105">ADSI Service Providers</span></span>

<span data-ttu-id="9e79b-106">ADSI comprend les fournisseurs de services listés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9e79b-106">ADSI includes the service providers listed in the following table.</span></span>



| <span data-ttu-id="9e79b-107">Fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="9e79b-107">Service provider</span></span> | <span data-ttu-id="9e79b-108">Description</span><span class="sxs-lookup"><span data-stu-id="9e79b-108">Description</span></span>                                                                                | <span data-ttu-id="9e79b-109">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="9e79b-109">For more information</span></span>                                      |
|------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9e79b-110">LDAP</span><span class="sxs-lookup"><span data-stu-id="9e79b-110">LDAP</span></span><br/>  | <span data-ttu-id="9e79b-111">Implémentation de l’espace de noms compatible avec le protocole Lightweight Directory Access.</span><span class="sxs-lookup"><span data-stu-id="9e79b-111">Namespace implementation compatible with Lightweight Directory Access Protocol.</span></span><br/> | [<span data-ttu-id="9e79b-112">Fournisseur LDAP ADSI</span><span class="sxs-lookup"><span data-stu-id="9e79b-112">ADSI LDAP Provider</span></span>](adsi-ldap-provider.md)<br/>   |
| <span data-ttu-id="9e79b-113">WinNT</span><span class="sxs-lookup"><span data-stu-id="9e79b-113">WinNT</span></span><br/> | <span data-ttu-id="9e79b-114">Implémentation de l’espace de noms compatible avec Windows.</span><span class="sxs-lookup"><span data-stu-id="9e79b-114">Namespace implementation compatible with Windows.</span></span><br/>                               | [<span data-ttu-id="9e79b-115">Fournisseur WinNT ADSI</span><span class="sxs-lookup"><span data-stu-id="9e79b-115">ADSI WinNT Provider</span></span>](adsi-winnt-provider.md)<br/> |



 

<span data-ttu-id="9e79b-116">D’autres fournisseurs de services sont inclus dans le cadre de produits autres qu’ADSI.</span><span class="sxs-lookup"><span data-stu-id="9e79b-116">Other service providers are included as part of products other than ADSI.</span></span> <span data-ttu-id="9e79b-117">Les fournisseurs de services ADSI implémentés par Microsoft sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="9e79b-117">The following are the ADSI service providers implemented by Microsoft.</span></span>



| <span data-ttu-id="9e79b-118">Fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="9e79b-118">Service provider</span></span> | <span data-ttu-id="9e79b-119">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="9e79b-119">For more information</span></span>                                                                        |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e79b-120">IIS</span><span class="sxs-lookup"><span data-stu-id="9e79b-120">IIS</span></span><br/>   | <span data-ttu-id="9e79b-121">[Architecture du fournisseur ADSI IIS](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="9e79b-121">[IIS ADSI Provider Architecture](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))</span></span><br/> |



 

<span data-ttu-id="9e79b-122">Les méthodes et méthodes de propriété exposées par les interfaces ADSI ne sont pas prises en charge par chaque fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="9e79b-122">The methods and property methods exposed by ADSI interfaces are not supported by every service provider.</span></span> <span data-ttu-id="9e79b-123">Étant donné que les différents services d’annuaire varient selon les types d’objets et de propriétés stockés, utilisent des protocoles différents et l’authentification, ADSI est conçu pour fonctionner de manière transparente avec les fournisseurs de services pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9e79b-123">Because different directory services vary in the types of objects and properties stored, use different protocols, and authentication, ADSI is designed to work seamlessly with supported service providers.</span></span> <span data-ttu-id="9e79b-124">Par conséquent, il existe des interfaces, des méthodes et des méthodes de propriété qui fonctionnent avec un fournisseur de services, tel que LDAP, qui peut ne pas fonctionner sur un autre, tel que Winnt.</span><span class="sxs-lookup"><span data-stu-id="9e79b-124">Thus, there are interfaces, methods, and property methods that work with one service provider, such as LDAP, that may not work on another, such as WinNT.</span></span>

<span data-ttu-id="9e79b-125">Cette section contient des informations spécifiques au fournisseur, telles que le format ADsPath, une liste des objets ADSI utilisés pour ce fournisseur de services, ainsi que des informations sur le type de données et la syntaxe pour les fournisseurs de services inclus avec ADSI.</span><span class="sxs-lookup"><span data-stu-id="9e79b-125">This section contains provider-specific information, such as the ADsPath format, a listing of ADSI objects used for that service provider, and data type and syntax information for the service providers included with ADSI.</span></span> <span data-ttu-id="9e79b-126">Il existe également une description résumée des interfaces ADSI prises en charge par chaque fournisseur inclus dans ADSI.</span><span class="sxs-lookup"><span data-stu-id="9e79b-126">There is also a summary description of ADSI interfaces supported by each provider included with ADSI.</span></span>

<span data-ttu-id="9e79b-127">Dans ADSI, différents fournisseurs sont associés à différentes dll.</span><span class="sxs-lookup"><span data-stu-id="9e79b-127">In ADSI, different providers are associated with different DLLs.</span></span> <span data-ttu-id="9e79b-128">Le fournisseur LDAP est associé à Adsldp.dll, Adsldpc.dll et Adsmsext.dll.</span><span class="sxs-lookup"><span data-stu-id="9e79b-128">The LDAP provider is associated with Adsldp.dll, Adsldpc.dll, and Adsmsext.dll.</span></span> <span data-ttu-id="9e79b-129">Le fournisseur Winnt est associé à Adsnt.dll.</span><span class="sxs-lookup"><span data-stu-id="9e79b-129">The WinNT provider is associated with Adsnt.dll.</span></span> <span data-ttu-id="9e79b-130">Le fournisseur de routeur est associé à Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="9e79b-130">The ROUTER provider is associated with Activeds.dll.</span></span>

> [!Note]  
> <span data-ttu-id="9e79b-131">Ne partez pas du principe que les fournisseurs ADSI par défaut sont thread-safe.</span><span class="sxs-lookup"><span data-stu-id="9e79b-131">Do not assume that default ADSI providers are thread-safe.</span></span> <span data-ttu-id="9e79b-132">Les développeurs d’applications multithread doivent coordonner l’accès entre les threads par le biais de l’utilisation appropriée d’objets de synchronisation tels que les sémaphores, les mutex, les sections critiques, etc.</span><span class="sxs-lookup"><span data-stu-id="9e79b-132">Multithreaded application developers should coordinate access between threads through the proper use of synchronization objects such as semaphores, mutexes, critical sections, and so on.</span></span>

 

<span data-ttu-id="9e79b-133">Pour plus d’informations sur les fournisseurs de services [](adsi-router.md) ADSI, consultez [prise en charge du routeur ADSI et du fournisseur d’interfaces ADSI](provider-support-of-adsi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="9e79b-133">For more information about ADSI service providers, see [ADSI Router](adsi-router.md) and [Provider Support of ADSI interfaces](provider-support-of-adsi-interfaces.md).</span></span>

 

