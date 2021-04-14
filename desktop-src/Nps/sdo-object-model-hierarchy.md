---
title: Hiérarchie du modèle objet
description: Les objets dans le modèle objet SDO sont organisés dans une hiérarchie. Cela signifie que les objets dans SDO fournissent un accès à d’autres objets dans SDO.
ms.assetid: 22159f61-2b35-4a0d-9b8b-8cb0a8192afb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2484b4d7402f8a5b43a590651f36d4d1707bca2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382236"
---
# <a name="object-model-hierarchy"></a><span data-ttu-id="0a669-104">Hiérarchie du modèle objet</span><span class="sxs-lookup"><span data-stu-id="0a669-104">Object Model Hierarchy</span></span>

<span data-ttu-id="0a669-105">Les objets dans le modèle objet SDO sont organisés dans une hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="0a669-105">The objects in the SDO object model are arranged in a hierarchy.</span></span> <span data-ttu-id="0a669-106">Cela signifie que les objets dans SDO fournissent un accès à d’autres objets dans SDO.</span><span class="sxs-lookup"><span data-stu-id="0a669-106">This means objects in SDO provide access to other objects in SDO.</span></span>

<span data-ttu-id="0a669-107">Les objets permettent d’accéder à d’autres objets de deux manières.</span><span class="sxs-lookup"><span data-stu-id="0a669-107">Objects provide access to other objects in two ways.</span></span> <span data-ttu-id="0a669-108">L’une des manières est que l’objet expose une interface qui fournit des méthodes pour récupérer d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="0a669-108">One way is for the object to expose an interface that provides methods to retrieve other objects.</span></span> <span data-ttu-id="0a669-109">L’objet machine est un exemple de cette approche.</span><span class="sxs-lookup"><span data-stu-id="0a669-109">An example of this approach is the Machine object.</span></span> <span data-ttu-id="0a669-110">L’objet ordinateur expose l’interface [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) .</span><span class="sxs-lookup"><span data-stu-id="0a669-110">The Machine object exposes the [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) interface.</span></span> <span data-ttu-id="0a669-111">La méthode [**ISdoMachine :: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) récupère un objet de service.</span><span class="sxs-lookup"><span data-stu-id="0a669-111">The [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) method retrieves a Service object.</span></span> <span data-ttu-id="0a669-112">La méthode [**ISdoMachine :: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) récupère un objet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0a669-112">The [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) method retrieves a User Object.</span></span>

![objet ordinateur exposant l’interface isdomachine](images/sdo01.png)

<span data-ttu-id="0a669-114">Pour plus d’informations, consultez la page [obtention d’SDOs de service et d’utilisateur](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos).</span><span class="sxs-lookup"><span data-stu-id="0a669-114">For more information, see [Obtaining Service and User SDOs](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos).</span></span>

<span data-ttu-id="0a669-115">La deuxième façon dont les objets fournissent l’accès aux autres objets est qu’une collection d’objets est représentée comme une propriété de l’objet qui le contient.</span><span class="sxs-lookup"><span data-stu-id="0a669-115">The second way that objects provide access to other objects is that an object collection is represented as a property of the object that contains it.</span></span> <span data-ttu-id="0a669-116">Pour récupérer une collection d’objets, appelez [**ISdo :: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) sur la propriété d’un objet qui représente la collection.</span><span class="sxs-lookup"><span data-stu-id="0a669-116">To retrieve an object collection, call [**ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) on the property of an object that represents the collection.</span></span> <span data-ttu-id="0a669-117">Par exemple, pour récupérer la collection de stratégies, appelez **ISdo :: GetProperty** sur l’interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) exposée par l’objet NPS.</span><span class="sxs-lookup"><span data-stu-id="0a669-117">For example, to retrieve the Policies collection, call **ISdo::GetProperty** on the [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface exposed by the NPS object.</span></span>

> [!Note]  
> <span data-ttu-id="0a669-118">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="0a669-118">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

![récupération de la collection de stratégies](images/sdo02.png)

<span data-ttu-id="0a669-120">Pour obtenir un exemple de code qui récupère la collection de stratégies, consultez [récupération d’une collection](/windows/desktop/Nps/sdo-retrieving-a-collection).</span><span class="sxs-lookup"><span data-stu-id="0a669-120">For sample code that retrieves the Policies collection, see [Retrieving a Collection](/windows/desktop/Nps/sdo-retrieving-a-collection).</span></span>

<span data-ttu-id="0a669-121">L' [**objet de données du serveur NPS**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) possède les propriétés suivantes qui représentent des collections :</span><span class="sxs-lookup"><span data-stu-id="0a669-121">The [**NPS Server Data Object**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) has the following properties that represent collections:</span></span>

<dl> <dt>

<span data-ttu-id="0a669-122"><span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Auprès</span><span class="sxs-lookup"><span data-stu-id="0a669-122"><span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Auditors</span></span>
</dt> <dd>

<span data-ttu-id="0a669-123">Le seul auditeur de la collection d’auditeurs est le [**Journal des événements NT**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).</span><span class="sxs-lookup"><span data-stu-id="0a669-123">The only auditor in the Auditors collection is the [**NT Event Log**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).</span></span>

</dd> <dt>

<span data-ttu-id="0a669-124"><span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Directives</span><span class="sxs-lookup"><span data-stu-id="0a669-124"><span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Policies</span></span>
</dt> <dd>

<span data-ttu-id="0a669-125">Chaque [**objet de stratégie**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) a une propriété qui représente une collection de conditions.</span><span class="sxs-lookup"><span data-stu-id="0a669-125">Each [**policy object**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) has a property that represents a collection of conditions.</span></span>

</dd> <dt>

<span data-ttu-id="0a669-126"><span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Profils</span><span class="sxs-lookup"><span data-stu-id="0a669-126"><span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Profiles</span></span>
</dt> <dd>

<span data-ttu-id="0a669-127">Chaque [**objet de profil**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) dans les collections de profils a une propriété qui représente une collection d’attributs.</span><span class="sxs-lookup"><span data-stu-id="0a669-127">Each [**profile object**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) in the Profiles collections has a property that represents an attributes collection.</span></span> <span data-ttu-id="0a669-128">Consultez [attributs pris en charge par SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes) pour obtenir la liste des attributs pris en charge par SDO.</span><span class="sxs-lookup"><span data-stu-id="0a669-128">See [SDO Supported Attributes](/windows/desktop/Nps/sdo-sdo-supported-attributes) for a list of the attributes supported by SDO.</span></span>

</dd> <dt>

<span data-ttu-id="0a669-129"><span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Relatifs</span><span class="sxs-lookup"><span data-stu-id="0a669-129"><span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Protocols</span></span>
</dt> <dd>

<span data-ttu-id="0a669-130">La collection Protocols contient l’objet de protocole RADIUS, qui contient une collection de clients qui représente des clients RADIUS.</span><span class="sxs-lookup"><span data-stu-id="0a669-130">The protocols collection contains the RADIUS protocol object, which contains a clients collection that represents RADIUS clients.</span></span> <span data-ttu-id="0a669-131">Consultez [Ajout d’un client](/windows/desktop/Nps/sdo-adding-a-client) pour obtenir un exemple de code qui montre comment récupérer la collection de clients.</span><span class="sxs-lookup"><span data-stu-id="0a669-131">See [Adding a Client](/windows/desktop/Nps/sdo-adding-a-client) for sample code that shows how to retrieve the client collection.</span></span>

</dd> <dt>

<span data-ttu-id="0a669-132"><span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Stratégies de proxy</span><span class="sxs-lookup"><span data-stu-id="0a669-132"><span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Proxy Policies</span></span>
</dt> <dd>

<span data-ttu-id="0a669-133">Cette collection contient les stratégies d’accès réseau utilisées pour le traitement des demandes de connexion.</span><span class="sxs-lookup"><span data-stu-id="0a669-133">This collection contains Network Access Policies used for connection request processing.</span></span>

</dd> <dt>

<span data-ttu-id="0a669-134"><span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Profils de proxy</span><span class="sxs-lookup"><span data-stu-id="0a669-134"><span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Proxy Profiles</span></span>
</dt> <dd>

<span data-ttu-id="0a669-135">Cette collection contient les profils utilisés pour le traitement des demandes de connexion.</span><span class="sxs-lookup"><span data-stu-id="0a669-135">This collection contains profiles used for connection request processing.</span></span>

</dd> <dt>

<span data-ttu-id="0a669-136"><span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>Groupes de serveurs RADIUS</span><span class="sxs-lookup"><span data-stu-id="0a669-136"><span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>RADIUS Server Groups</span></span>
</dt> <dd>

<span data-ttu-id="0a669-137">Chaque [**groupe de serveurs RADIUS**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) de la collection de groupes de serveurs RADIUS a une propriété qui représente la collection de serveurs dans ce groupe de serveurs.</span><span class="sxs-lookup"><span data-stu-id="0a669-137">Each [**RADIUS server group**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) in the RADIUS Server Groups collection has a property that represents the collection of servers in that server group.</span></span>

</dd> <dt>

<span data-ttu-id="0a669-138"><span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Gestionnaires de demandes</span><span class="sxs-lookup"><span data-stu-id="0a669-138"><span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Request Handlers</span></span>
</dt> <dd>

<span data-ttu-id="0a669-139">Cette collection contient la collection « Microsoft Realms évaluateur ».</span><span class="sxs-lookup"><span data-stu-id="0a669-139">This collection contains the "Microsoft Realms Evaluator" collection.</span></span> <span data-ttu-id="0a669-140">Les paramètres « authentification SAM Microsoft NT » et « Microsoft Accounting » sont également disponibles dans ce regroupement.</span><span class="sxs-lookup"><span data-stu-id="0a669-140">The "Microsoft NT SAM Authentication" and "Microsoft Accounting" settings are also available in this collection.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="0a669-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0a669-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a669-142">Objets et propriétés SDO</span><span class="sxs-lookup"><span data-stu-id="0a669-142">SDO Objects and Properties</span></span>](/windows/desktop/Nps/sdo-objects-and-properties)
</dt> <dt>

[<span data-ttu-id="0a669-143">Attributs pris en charge par SDO</span><span class="sxs-lookup"><span data-stu-id="0a669-143">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 