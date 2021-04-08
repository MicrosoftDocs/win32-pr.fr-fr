---
title: Classe Win32_TSGatewayLoadBalancer
description: Décrit un ensemble de serveurs d’équilibrage de charge de passerelle Bureau à Bureau à distance. Ils sont utilisés pour équilibrer la charge des connexions de passerelle Bureau à distance sur plusieurs serveurs.
ms.assetid: aa7e7b77-7233-4c6a-8f41-cc332fa509d5
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayLoadBalancer de la classe Services Bureau à distance
- Win32_TSGatewayLoadBalancer de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer.Servers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4956ed4dc9536ff6f7e3263071a2a477cb0f515
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741252"
---
# <a name="win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="42ea5-106">\_Classe TSGatewayLoadBalancer Win32</span><span class="sxs-lookup"><span data-stu-id="42ea5-106">Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="42ea5-107">Décrit un ensemble de serveurs d’équilibrage de charge de passerelle Bureau à Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="42ea5-107">Describes a set of Remote Desktop Gateway (RD Gateway) load-balancing servers.</span></span> <span data-ttu-id="42ea5-108">Ils sont utilisés pour équilibrer la charge des connexions de passerelle Bureau à distance sur plusieurs serveurs.</span><span class="sxs-lookup"><span data-stu-id="42ea5-108">These are used to load balance RD Gateway connections across multiple servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="42ea5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42ea5-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayLoadBalancer
{
  string Servers;
};
```

## <a name="members"></a><span data-ttu-id="42ea5-110">Membres</span><span class="sxs-lookup"><span data-stu-id="42ea5-110">Members</span></span>

<span data-ttu-id="42ea5-111">La classe **Win32 \_ TSGatewayLoadBalancer** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="42ea5-111">The **Win32\_TSGatewayLoadBalancer** class has these types of members:</span></span>

-   [<span data-ttu-id="42ea5-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="42ea5-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="42ea5-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="42ea5-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="42ea5-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="42ea5-114">Methods</span></span>

<span data-ttu-id="42ea5-115">La classe **Win32 \_ TSGatewayLoadBalancer** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="42ea5-115">The **Win32\_TSGatewayLoadBalancer** class has these methods.</span></span>



| <span data-ttu-id="42ea5-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="42ea5-116">Method</span></span>                                                                             | <span data-ttu-id="42ea5-117">Description</span><span class="sxs-lookup"><span data-stu-id="42ea5-117">Description</span></span>                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42ea5-118">**AddServers**</span><span class="sxs-lookup"><span data-stu-id="42ea5-118">**AddServers**</span></span>](addservers-win32-tsgatewayloadbalancer.md)                       | <span data-ttu-id="42ea5-119">Ajoute des serveurs à la propriété **serveurs** .</span><span class="sxs-lookup"><span data-stu-id="42ea5-119">Adds servers to the **Servers** property.</span></span><br/>                                                             |
| [<span data-ttu-id="42ea5-120">**DeleteAllServers**</span><span class="sxs-lookup"><span data-stu-id="42ea5-120">**DeleteAllServers**</span></span>](deleteallservers-win32-tsgatewayloadbalancer.md)           | <span data-ttu-id="42ea5-121">Supprime tous les serveurs d’équilibrage de charge de la passerelle Bureau à distance qui participent à la batterie d’équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="42ea5-121">Deletes all RD Gateway load-balancing servers participating in the load-balancing farm.</span></span><br/>               |
| [<span data-ttu-id="42ea5-122">**DeleteServers**</span><span class="sxs-lookup"><span data-stu-id="42ea5-122">**DeleteServers**</span></span>](deleteservers-win32-tsgatewayloadbalancer.md)                 | <span data-ttu-id="42ea5-123">Supprime les serveurs de la propriété **serveurs** .</span><span class="sxs-lookup"><span data-stu-id="42ea5-123">Deletes servers from the **Servers** property.</span></span><br/>                                                        |
| [<span data-ttu-id="42ea5-124">**IsLoadBalancingServer**</span><span class="sxs-lookup"><span data-stu-id="42ea5-124">**IsLoadBalancingServer**</span></span>](win32-tsgatewayloadbalancer-isloadbalancingserver.md) | <span data-ttu-id="42ea5-125">Détermine si le serveur peut effectuer l’équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="42ea5-125">Determines whether the server can perform load balancing.</span></span><br/>                                             |
| [<span data-ttu-id="42ea5-126">**SetServers**</span><span class="sxs-lookup"><span data-stu-id="42ea5-126">**SetServers**</span></span>](setservers-win32-tsgatewayloadbalancer.md)                       | <span data-ttu-id="42ea5-127">Définit la propriété **serveurs** avec la liste séparée par des points-virgules des serveurs d’équilibrage de charge de la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="42ea5-127">Sets the **Servers** property with the semicolon-separated list of RD Gateway load-balancing servers.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="42ea5-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="42ea5-128">Properties</span></span>

<span data-ttu-id="42ea5-129">La classe **Win32 \_ TSGatewayLoadBalancer** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="42ea5-129">The **Win32\_TSGatewayLoadBalancer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42ea5-130">**Serveurs**</span><span class="sxs-lookup"><span data-stu-id="42ea5-130">**Servers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ea5-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="42ea5-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42ea5-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="42ea5-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42ea5-133">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="42ea5-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="42ea5-134">Liste séparée par des points-virgules des serveurs d’équilibrage de charge de la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="42ea5-134">Semicolon-separated list of RD Gateway load-balancing servers.</span></span> <span data-ttu-id="42ea5-135">Cette propriété peut être modifiée à l’aide des méthodes [**SetServers**](setservers-win32-tsgatewayloadbalancer.md), [**AddServers**](addservers-win32-tsgatewayloadbalancer.md), [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md)et [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md) .</span><span class="sxs-lookup"><span data-stu-id="42ea5-135">This property can be changed with the [**SetServers**](setservers-win32-tsgatewayloadbalancer.md), [**AddServers**](addservers-win32-tsgatewayloadbalancer.md), [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md), and [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42ea5-136">Notes</span><span class="sxs-lookup"><span data-stu-id="42ea5-136">Remarks</span></span>

<span data-ttu-id="42ea5-137">Pour utiliser cette classe, vous devez être membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="42ea5-137">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="42ea5-138">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="42ea5-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="42ea5-139">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="42ea5-139">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="42ea5-140">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="42ea5-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="42ea5-141">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="42ea5-141">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="42ea5-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42ea5-142">Requirements</span></span>



| <span data-ttu-id="42ea5-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42ea5-143">Requirement</span></span> | <span data-ttu-id="42ea5-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="42ea5-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="42ea5-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42ea5-145">Minimum supported client</span></span><br/> | <span data-ttu-id="42ea5-146">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="42ea5-146">None supported</span></span><br/>                                                                |
| <span data-ttu-id="42ea5-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42ea5-147">Minimum supported server</span></span><br/> | <span data-ttu-id="42ea5-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42ea5-148">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="42ea5-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="42ea5-149">Namespace</span></span><br/>                | <span data-ttu-id="42ea5-150">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="42ea5-150">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="42ea5-151">MOF</span><span class="sxs-lookup"><span data-stu-id="42ea5-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42ea5-152"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42ea5-152"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="42ea5-153">DLL</span><span class="sxs-lookup"><span data-stu-id="42ea5-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42ea5-154"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42ea5-154"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="42ea5-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42ea5-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42ea5-156">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="42ea5-156">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="42ea5-157">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="42ea5-157">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="42ea5-158">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="42ea5-158">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="42ea5-159">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="42ea5-159">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="42ea5-160">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="42ea5-160">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="42ea5-161">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="42ea5-161">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

