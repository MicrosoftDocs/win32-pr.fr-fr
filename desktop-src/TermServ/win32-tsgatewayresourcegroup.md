---
title: Classe Win32_TSGatewayResourceGroup
description: Décrit un groupe de ressources, qui mappe un ensemble de ressources (noms d’ordinateur) à une entité unique.
ms.assetid: 5715a2ea-9bbc-4704-835e-ba6d93a72368
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceGroup de la classe Services Bureau à distance
- Win32_TSGatewayResourceGroup de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup.Name
- Win32_TSGatewayResourceGroup.Description
- Win32_TSGatewayResourceGroup.AssociatedRAPs
- Win32_TSGatewayResourceGroup.Resources
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffeda42abafd24526360f5e549f004cae0c3140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511943"
---
# <a name="win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="77442-105">\_Classe TSGatewayResourceGroup Win32</span><span class="sxs-lookup"><span data-stu-id="77442-105">Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="77442-106">Décrit un groupe de ressources, qui mappe un ensemble de ressources (noms d’ordinateur) à une entité unique.</span><span class="sxs-lookup"><span data-stu-id="77442-106">Describes a resource group, which maps a set of resources (computer names) to a single entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="77442-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77442-107">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceGroup
{
  string Name;
  string Description;
  string AssociatedRAPs;
  string Resources;
};
```

## <a name="members"></a><span data-ttu-id="77442-108">Membres</span><span class="sxs-lookup"><span data-stu-id="77442-108">Members</span></span>

<span data-ttu-id="77442-109">La classe **Win32 \_ TSGatewayResourceGroup** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="77442-109">The **Win32\_TSGatewayResourceGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="77442-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="77442-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="77442-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="77442-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="77442-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="77442-112">Methods</span></span>

<span data-ttu-id="77442-113">La classe **Win32 \_ TSGatewayResourceGroup** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="77442-113">The **Win32\_TSGatewayResourceGroup** class has these methods.</span></span>



| <span data-ttu-id="77442-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="77442-114">Method</span></span>                                                                  | <span data-ttu-id="77442-115">Description</span><span class="sxs-lookup"><span data-stu-id="77442-115">Description</span></span>                                                                           |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="77442-116">**AddResources**</span><span class="sxs-lookup"><span data-stu-id="77442-116">**AddResources**</span></span>](addresources-win32-tsgatewayresourcegroup.md)       | <span data-ttu-id="77442-117">Ajoute des ressources à la propriété des **ressources** pour ce groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="77442-117">Adds resources to the **Resources** property for this resource group.</span></span><br/>      |
| [<span data-ttu-id="77442-118">**Créés**</span><span class="sxs-lookup"><span data-stu-id="77442-118">**Create**</span></span>](create-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="77442-119">Crée un groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="77442-119">Creates a resource group.</span></span><br/>                                                  |
| [<span data-ttu-id="77442-120">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="77442-120">**Delete**</span></span>](delete-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="77442-121">Supprime ce groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="77442-121">Deletes this resource group.</span></span><br/>                                               |
| [<span data-ttu-id="77442-122">**RemoveResources**</span><span class="sxs-lookup"><span data-stu-id="77442-122">**RemoveResources**</span></span>](removeresources-win32-tsgatewayresourcegroup.md) | <span data-ttu-id="77442-123">Supprime les ressources de la propriété des **ressources** pour ce groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="77442-123">Deletes resources from the **Resources** property for this resource group.</span></span><br/> |
| [<span data-ttu-id="77442-124">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="77442-124">**SetDescription**</span></span>](setdescription-win32-tsgatewayresourcegroup.md)   | <span data-ttu-id="77442-125">Définit la propriété **Description** pour ce groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="77442-125">Sets the **Description** property for this resource group.</span></span><br/>                 |
| [<span data-ttu-id="77442-126">**SetName**</span><span class="sxs-lookup"><span data-stu-id="77442-126">**SetName**</span></span>](setname-win32-tsgatewayresourcegroup.md)                 | <span data-ttu-id="77442-127">Définit la propriété de **nom** pour ce groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="77442-127">Sets the **Name** property for this resource group.</span></span><br/>                        |
| [<span data-ttu-id="77442-128">**SetResources**</span><span class="sxs-lookup"><span data-stu-id="77442-128">**SetResources**</span></span>](setresources-win32-tsgatewayresourcegroup.md)       | <span data-ttu-id="77442-129">Définit la propriété des **ressources** pour ce groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="77442-129">Sets the **Resources** property for this resource group.</span></span><br/>                   |
| [<span data-ttu-id="77442-130">**Mise à jour**</span><span class="sxs-lookup"><span data-stu-id="77442-130">**Update**</span></span>](update-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="77442-131">Met à jour ce groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="77442-131">Updates this resource group.</span></span><br/>                                               |



 

### <a name="properties"></a><span data-ttu-id="77442-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="77442-132">Properties</span></span>

<span data-ttu-id="77442-133">La classe **Win32 \_ TSGatewayResourceGroup** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="77442-133">The **Win32\_TSGatewayResourceGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="77442-134">**AssociatedRAPs**</span><span class="sxs-lookup"><span data-stu-id="77442-134">**AssociatedRAPs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77442-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="77442-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77442-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="77442-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77442-137">Liste délimitée par des points-virgules de Services Bureau à distance les stratégies d’autorisation des ressources (RD stratégies) associées à ce groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="77442-137">Semicolon-separated list of Remote Desktop Services resource authorization policies (RD RAPs) that are associated with this resource group.</span></span>

</dd> <dt>

<span data-ttu-id="77442-138">**Description**</span><span class="sxs-lookup"><span data-stu-id="77442-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77442-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="77442-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77442-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="77442-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77442-141">Description du groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="77442-141">Description of the resource group.</span></span> <span data-ttu-id="77442-142">Cette propriété peut être modifiée à l’aide de la méthode [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="77442-142">This property can be changed with the [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="77442-143">**Nom**</span><span class="sxs-lookup"><span data-stu-id="77442-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77442-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="77442-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77442-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="77442-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77442-146">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="77442-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="77442-147">Nom du groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="77442-147">Name of the resource group.</span></span> <span data-ttu-id="77442-148">Cette propriété peut être modifiée à l’aide de la méthode [**SetName**](setname-win32-tsgatewayresourcegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="77442-148">This property can be changed with the [**SetName**](setname-win32-tsgatewayresourcegroup.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="77442-149">**Ressources**</span><span class="sxs-lookup"><span data-stu-id="77442-149">**Resources**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77442-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="77442-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77442-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="77442-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77442-152">Liste de ressources séparées par des points-virgules dans ce groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="77442-152">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="77442-153">« \* » Signifie toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="77442-153">An "\*" means all resources.</span></span> <span data-ttu-id="77442-154">Cette propriété peut être modifiée avec les méthodes [**SetResources**](setresources-win32-tsgatewayresourcegroup.md), [**AddResources**](addresources-win32-tsgatewayresourcegroup.md), [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md)et [**Update**](update-win32-tsgatewayresourcegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="77442-154">This property can be changed with the [**SetResources**](setresources-win32-tsgatewayresourcegroup.md), [**AddResources**](addresources-win32-tsgatewayresourcegroup.md), [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md), and [**Update**](update-win32-tsgatewayresourcegroup.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77442-155">Notes</span><span class="sxs-lookup"><span data-stu-id="77442-155">Remarks</span></span>

<span data-ttu-id="77442-156">Pour utiliser cette classe, vous devez être membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="77442-156">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="77442-157">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="77442-157">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="77442-158">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="77442-158">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="77442-159">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="77442-159">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="77442-160">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="77442-160">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="77442-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77442-161">Requirements</span></span>



| <span data-ttu-id="77442-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77442-162">Requirement</span></span> | <span data-ttu-id="77442-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="77442-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="77442-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77442-164">Minimum supported client</span></span><br/> | <span data-ttu-id="77442-165">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="77442-165">None supported</span></span><br/>                                                                |
| <span data-ttu-id="77442-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77442-166">Minimum supported server</span></span><br/> | <span data-ttu-id="77442-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77442-167">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="77442-168">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="77442-168">Namespace</span></span><br/>                | <span data-ttu-id="77442-169">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="77442-169">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="77442-170">MOF</span><span class="sxs-lookup"><span data-stu-id="77442-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77442-171"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77442-171"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="77442-172">DLL</span><span class="sxs-lookup"><span data-stu-id="77442-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77442-173"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77442-173"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="77442-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77442-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77442-175">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="77442-175">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="77442-176">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="77442-176">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="77442-177">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="77442-177">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="77442-178">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="77442-178">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="77442-179">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="77442-179">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="77442-180">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="77442-180">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

