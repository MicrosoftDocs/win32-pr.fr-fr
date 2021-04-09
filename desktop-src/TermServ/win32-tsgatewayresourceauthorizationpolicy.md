---
title: Classe Win32_TSGatewayResourceAuthorizationPolicy
description: Décrit une stratégie d’autorisation d’accès aux ressources Bureau à distance (RD \ 160 ; RAP). Un bureau à distance \ 160 ; RAP est utilisé pour déterminer si un utilisateur est autorisé à se connecter à une ressource spécifiée par le biais de Bureau à distance Gateway (passerelle des services Bureau à distance).
ms.assetid: 284a868d-7856-4a25-ba7b-b4beba8ffffc
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy.Name
- Win32_TSGatewayResourceAuthorizationPolicy.Description
- Win32_TSGatewayResourceAuthorizationPolicy.Enabled
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupType
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupName
- Win32_TSGatewayResourceAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayResourceAuthorizationPolicy.ProtocolNames
- Win32_TSGatewayResourceAuthorizationPolicy.PortNumbers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c262cb1ce3351c89dc5d7edf3b0d106116e83b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032782"
---
# <a name="win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="e9d0e-106">\_Classe TSGatewayResourceAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="e9d0e-106">Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="e9d0e-107">Décrit une stratégie d’autorisation des ressources Bureau à distance (RD RAP).</span><span class="sxs-lookup"><span data-stu-id="e9d0e-107">Describes a Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="e9d0e-108">Une connexion Bureau à distance est utilisée pour décider si un utilisateur est autorisé à se connecter à une ressource spécifiée Bureau à distance via la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-108">An RD RAP is used to decide whether a user is authorized to connect to a specified resource through Remote Desktop Gateway (RD Gateway).</span></span>

## <a name="syntax"></a><span data-ttu-id="e9d0e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9d0e-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceAuthorizationPolicy
{
  string  Name;
  string  Description;
  boolean Enabled;
  string  ResourceGroupType;
  string  ResourceGroupName;
  string  UserGroupNames;
  string  ProtocolNames;
  string  PortNumbers;
};
```

## <a name="members"></a><span data-ttu-id="e9d0e-110">Membres</span><span class="sxs-lookup"><span data-stu-id="e9d0e-110">Members</span></span>

<span data-ttu-id="e9d0e-111">La classe **Win32 \_ TSGatewayResourceAuthorizationPolicy** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e9d0e-111">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these types of members:</span></span>

-   [<span data-ttu-id="e9d0e-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e9d0e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="e9d0e-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e9d0e-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e9d0e-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e9d0e-114">Methods</span></span>

<span data-ttu-id="e9d0e-115">La classe **Win32 \_ TSGatewayResourceAuthorizationPolicy** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-115">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these methods.</span></span>



| <span data-ttu-id="e9d0e-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="e9d0e-116">Method</span></span>                                                                                          | <span data-ttu-id="e9d0e-117">Description</span><span class="sxs-lookup"><span data-stu-id="e9d0e-117">Description</span></span>                                                                                                         |
|:------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9d0e-118">**AddUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-118">**AddUserGroupNames**</span></span>](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | <span data-ttu-id="e9d0e-119">Ajoute les noms de groupes d’utilisateurs spécifiés aux groupes d’utilisateurs existants dans la propriété **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="e9d0e-119">Adds the specified user group names to the existing user groups in the **UserGroupNames** property.</span></span><br/>      |
| [<span data-ttu-id="e9d0e-120">**Créés**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-120">**Create**</span></span>](create-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="e9d0e-121">Crée un RAP.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-121">Creates an RD RAP.</span></span><br/>                                                                                       |
| [<span data-ttu-id="e9d0e-122">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-122">**Delete**</span></span>](delete-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="e9d0e-123">Supprime le RAP (RD) actuel.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-123">Deletes the current RD RAP.</span></span><br/>                                                                              |
| [<span data-ttu-id="e9d0e-124">**RemoveUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-124">**RemoveUserGroupNames**</span></span>](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) | <span data-ttu-id="e9d0e-125">Supprime les noms de groupes d’utilisateurs spécifiés des groupes d’utilisateurs existants dans la propriété **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="e9d0e-125">Removes the specified user group names from the existing user groups in the **UserGroupNames** property.</span></span><br/> |
| [<span data-ttu-id="e9d0e-126">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-126">**SetDescription**</span></span>](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)             | <span data-ttu-id="e9d0e-127">Définit la propriété **Description** de la RD RAP.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-127">Sets the **Description** property for the RD RAP.</span></span><br/>                                                        |
| [<span data-ttu-id="e9d0e-128">**SetEnabled**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-128">**SetEnabled**</span></span>](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)                     | <span data-ttu-id="e9d0e-129">Active ou désactive la RD RAP en définissant la propriété **Enabled** .</span><span class="sxs-lookup"><span data-stu-id="e9d0e-129">Enables or disables the RD RAP by setting the **Enabled** property.</span></span><br/>                                      |
| [<span data-ttu-id="e9d0e-130">**SetName**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-130">**SetName**</span></span>](setname-win32-tsgatewayresourceauthorizationpolicy.md)                           | <span data-ttu-id="e9d0e-131">Définit la propriété de **nom** pour la RD RAP.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-131">Sets the **Name** property for the RD RAP.</span></span><br/>                                                               |
| [<span data-ttu-id="e9d0e-132">**SetPortNumbers**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-132">**SetPortNumbers**</span></span>](setportnumbers-win32-tsgatewayresourceauthorizationpolicy.md)             | <span data-ttu-id="e9d0e-133">Définit la propriété **PortNumbers** pour la RD RAP.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-133">Sets the **PortNumbers** property for the RD RAP.</span></span><br/>                                                        |
| [<span data-ttu-id="e9d0e-134">**SetResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-134">**SetResourceGroup**</span></span>](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)         | <span data-ttu-id="e9d0e-135">Définit les propriétés **ResourceGroupType** et **ResourceGroupName** .</span><span class="sxs-lookup"><span data-stu-id="e9d0e-135">Sets the **ResourceGroupType** and **ResourceGroupName** properties.</span></span><br/>                                     |
| [<span data-ttu-id="e9d0e-136">**SetUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-136">**SetUserGroupNames**</span></span>](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | <span data-ttu-id="e9d0e-137">Définit la propriété **UserGroupNames** pour la RD RAP.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-137">Sets the **UserGroupNames** property for the RD RAP.</span></span><br/>                                                     |
| [<span data-ttu-id="e9d0e-138">**Mise à jour**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-138">**Update**</span></span>](update-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="e9d0e-139">Met à jour le RAP RD actuel.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-139">Updates the current RD RAP.</span></span><br/>                                                                              |



 

### <a name="properties"></a><span data-ttu-id="e9d0e-140">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e9d0e-140">Properties</span></span>

<span data-ttu-id="e9d0e-141">La classe **Win32 \_ TSGatewayResourceAuthorizationPolicy** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-141">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9d0e-142">**Description**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-142">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9d0e-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9d0e-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9d0e-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9d0e-145">Description de la RD RAP.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-145">Description of the RD RAP.</span></span> <span data-ttu-id="e9d0e-146">Cette propriété est modifiée à l’aide de la méthode [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="e9d0e-146">This property is changed with the [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e9d0e-147">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-147">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9d0e-148">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e9d0e-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9d0e-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9d0e-150">Indique si ce RAP est activé.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-150">Indicates whether this RD RAP is enabled.</span></span> <span data-ttu-id="e9d0e-151">Cette propriété est modifiée à l’aide de la méthode [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="e9d0e-151">This property is changed with the [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e9d0e-152">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9d0e-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9d0e-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9d0e-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9d0e-155">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e9d0e-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e9d0e-156">Nom de la RD RAP.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-156">Name of the RD RAP.</span></span> <span data-ttu-id="e9d0e-157">Cette propriété est modifiée à l’aide de la méthode [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="e9d0e-157">This property is changed with the [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e9d0e-158">**PortNumbers**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-158">**PortNumbers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9d0e-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9d0e-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9d0e-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9d0e-161">Liste des numéros de port séparés par des points-virgules autorisés pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-161">List of semicolon-separated port numbers that are allowed for this policy.</span></span> <span data-ttu-id="e9d0e-162">Pour autoriser n’importe quel numéro de port, définissez « \* ».</span><span class="sxs-lookup"><span data-stu-id="e9d0e-162">To allow any port number, set "\*".</span></span>

</dd> <dt>

<span data-ttu-id="e9d0e-163">**ProtocolNames**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-163">**ProtocolNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9d0e-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9d0e-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9d0e-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9d0e-166">Liste des noms de protocole séparés par des points-virgules qui sont activés pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-166">List of semicolon-separated protocol names that are enabled for this policy.</span></span> <span data-ttu-id="e9d0e-167">Les noms doivent correspondre au retour de la méthode [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) de la classe [**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="e9d0e-167">Names must match the return of the [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) method of the [**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e9d0e-168">**ResourceGroupName**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-168">**ResourceGroupName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9d0e-169">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9d0e-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9d0e-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9d0e-171">Nom du groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-171">Resource group name.</span></span> <span data-ttu-id="e9d0e-172">Cette propriété est modifiée à l’aide de la méthode [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="e9d0e-172">This property is changed with the [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e9d0e-173">**ResourceGroupType**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-173">**ResourceGroupType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9d0e-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9d0e-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9d0e-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9d0e-176">Identifie le type du groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-176">Identifies the type of the resource group.</span></span> <span data-ttu-id="e9d0e-177">Cette propriété est modifiée à l’aide de la méthode [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="e9d0e-177">This property is changed with the [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

<dt>

<span data-ttu-id="e9d0e-178">ROUTAGE</span><span class="sxs-lookup"><span data-stu-id="e9d0e-178">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="e9d0e-179">Groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-179">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="e9d0e-180">CG</span><span class="sxs-lookup"><span data-stu-id="e9d0e-180">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="e9d0e-181">Groupe d’ordinateurs, tel qu’il est stocké dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-181">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="e9d0e-182">TOUS les</span><span class="sxs-lookup"><span data-stu-id="e9d0e-182">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="e9d0e-183">Toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-183">All resources.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e9d0e-184">**UserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-184">**UserGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9d0e-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9d0e-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9d0e-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9d0e-187">Liste de noms de groupes d’utilisateurs séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-187">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="e9d0e-188">Si l’utilisateur appartient à l’un de ces groupes d’utilisateurs, l’accès est autorisé.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-188">If the user belongs to any of these user groups, access will be permitted.</span></span> <span data-ttu-id="e9d0e-189">Cette propriété est modifiée à l’aide des méthodes [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)et [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="e9d0e-189">This property is changed with the [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), and [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9d0e-190">Notes</span><span class="sxs-lookup"><span data-stu-id="e9d0e-190">Remarks</span></span>

<span data-ttu-id="e9d0e-191">Pour utiliser cette classe, vous devez être membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-191">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="e9d0e-192">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="e9d0e-192">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e9d0e-193">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-193">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e9d0e-194">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="e9d0e-194">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e9d0e-195">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e9d0e-195">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9d0e-196">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9d0e-196">Requirements</span></span>



| <span data-ttu-id="e9d0e-197">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9d0e-197">Requirement</span></span> | <span data-ttu-id="e9d0e-198">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9d0e-198">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d0e-199">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9d0e-199">Minimum supported client</span></span><br/> | <span data-ttu-id="e9d0e-200">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9d0e-200">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e9d0e-201">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9d0e-201">Minimum supported server</span></span><br/> | <span data-ttu-id="e9d0e-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9d0e-202">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e9d0e-203">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e9d0e-203">Namespace</span></span><br/>                | <span data-ttu-id="e9d0e-204">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="e9d0e-204">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e9d0e-205">MOF</span><span class="sxs-lookup"><span data-stu-id="e9d0e-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9d0e-206"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9d0e-206"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9d0e-207">DLL</span><span class="sxs-lookup"><span data-stu-id="e9d0e-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9d0e-208"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9d0e-208"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e9d0e-209">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9d0e-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9d0e-210">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-210">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="e9d0e-211">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-211">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="e9d0e-212">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-212">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="e9d0e-213">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-213">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="e9d0e-214">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-214">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="e9d0e-215">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="e9d0e-215">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

