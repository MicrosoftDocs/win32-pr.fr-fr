---
title: Méthode Update de la classe Win32_TSGatewayResourceAuthorizationPolicy
description: Met à jour la stratégie d’autorisation des ressources Bureau à distance actuelle (RD \ 160 ; RAP).
ms.assetid: af997bb8-6027-4f37-80fb-e89622840a2b
ms.tgt_platform: multiple
keywords:
- Mettre à jour la méthode Services Bureau à distance
- Mise à jour de la méthode Services Bureau à distance, classe Win32_TSGatewayResourceAuthorizationPolicy
- Services Bureau à distance de la classe Win32_TSGatewayResourceAuthorizationPolicy, méthode Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904d5fa092cddfbfda1c94f1810a6f6da1a9a8a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104281"
---
# <a name="update-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="01f23-106">Méthode Update de la \_ classe TSGatewayResourceAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="01f23-106">Update method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="01f23-107">Met à jour la stratégie d’autorisation d’accès aux ressources Bureau à distance en cours (RD RAP).</span><span class="sxs-lookup"><span data-stu-id="01f23-107">Updates the current Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="01f23-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01f23-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupName,
  [in] string  ResourceGroupType,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a><span data-ttu-id="01f23-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01f23-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01f23-110">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="01f23-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01f23-111">Nom de la RD RAP.</span><span class="sxs-lookup"><span data-stu-id="01f23-111">Name of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="01f23-112">*Description* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="01f23-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01f23-113">Description de la RD RAP.</span><span class="sxs-lookup"><span data-stu-id="01f23-113">Description of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="01f23-114">*Activé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="01f23-114">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01f23-115">Indique si le RAP des services Bureau à distance doit être activé.</span><span class="sxs-lookup"><span data-stu-id="01f23-115">Indicates whether the RD RAP should be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="01f23-116">*ResourceGroupName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="01f23-116">*ResourceGroupName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01f23-117">Nom du groupe de ressources associé à ce RAP.</span><span class="sxs-lookup"><span data-stu-id="01f23-117">Resource group name associated with this RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="01f23-118">*ResourceGroupType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="01f23-118">*ResourceGroupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01f23-119">Type de groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="01f23-119">Resource group type.</span></span>

<dt>

<span data-ttu-id="01f23-120">ROUTAGE</span><span class="sxs-lookup"><span data-stu-id="01f23-120">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="01f23-121">Groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="01f23-121">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="01f23-122">CG</span><span class="sxs-lookup"><span data-stu-id="01f23-122">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="01f23-123">Groupe d’ordinateurs, tel qu’il est stocké dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="01f23-123">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="01f23-124">TOUS les</span><span class="sxs-lookup"><span data-stu-id="01f23-124">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="01f23-125">Toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="01f23-125">All resources.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="01f23-126">*UserGroupNames* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="01f23-126">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01f23-127">Liste de noms de groupes d’utilisateurs séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="01f23-127">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="01f23-128">Les noms sont au format *domaine \\ UserGroupName*.</span><span class="sxs-lookup"><span data-stu-id="01f23-128">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="01f23-129">Si l’utilisateur appartient à l’un de ces groupes d’utilisateurs, l’accès est autorisé.</span><span class="sxs-lookup"><span data-stu-id="01f23-129">If the user belongs to any of these user groups, access will be permitted.</span></span>

</dd> <dt>

<span data-ttu-id="01f23-130">*ProtocolNames* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="01f23-130">*ProtocolNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01f23-131">Liste délimitée par des points-virgules des noms de protocole qui sont activés pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="01f23-131">Semicolon-separated list of protocol names that are enabled for this policy.</span></span> <span data-ttu-id="01f23-132">Les noms doivent correspondre au retour de la méthode [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) de la classe [**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="01f23-132">Names must match the return of the [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) method of the [**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="01f23-133">*PortNumbers* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="01f23-133">*PortNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01f23-134">Liste délimitée par des points-virgules des numéros de port activés pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="01f23-134">Semicolon-separated list of port numbers that are enabled for this policy.</span></span> <span data-ttu-id="01f23-135">Pour autoriser n’importe quel numéro de port, définissez « \* ».</span><span class="sxs-lookup"><span data-stu-id="01f23-135">To allow any port number, set "\*".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01f23-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="01f23-136">Return value</span></span>

<span data-ttu-id="01f23-137">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="01f23-137">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="01f23-138">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="01f23-138">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="01f23-139">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="01f23-139">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="01f23-140">Notes</span><span class="sxs-lookup"><span data-stu-id="01f23-140">Remarks</span></span>

<span data-ttu-id="01f23-141">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="01f23-141">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="01f23-142">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="01f23-142">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="01f23-143">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="01f23-143">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="01f23-144">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="01f23-144">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="01f23-145">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="01f23-145">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="01f23-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01f23-146">Requirements</span></span>



| <span data-ttu-id="01f23-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01f23-147">Requirement</span></span> | <span data-ttu-id="01f23-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="01f23-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="01f23-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01f23-149">Minimum supported client</span></span><br/> | <span data-ttu-id="01f23-150">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="01f23-150">None supported</span></span><br/>                                                                |
| <span data-ttu-id="01f23-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01f23-151">Minimum supported server</span></span><br/> | <span data-ttu-id="01f23-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01f23-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="01f23-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="01f23-153">Namespace</span></span><br/>                | <span data-ttu-id="01f23-154">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="01f23-154">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="01f23-155">MOF</span><span class="sxs-lookup"><span data-stu-id="01f23-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01f23-156"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01f23-156"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="01f23-157">DLL</span><span class="sxs-lookup"><span data-stu-id="01f23-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01f23-158"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01f23-158"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="01f23-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01f23-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01f23-160">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="01f23-160">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

