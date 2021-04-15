---
title: Créer une méthode de la classe Win32_TSGatewayResourceAuthorizationPolicy
description: Crée une stratégie d’autorisation d’accès aux ressources Bureau à distance (RD \ 160 ; RAP).
ms.assetid: 3301a543-cdf9-4528-a29e-691054ef81c9
ms.tgt_platform: multiple
keywords:
- Créer une méthode Services Bureau à distance
- Create Method Services Bureau à distance, Win32_TSGatewayResourceAuthorizationPolicy Class
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance, Create, méthode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6372706a294902b03f22807049db9a954de4f7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384079"
---
# <a name="create-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="bf848-106">Créer une méthode de la \_ classe TSGatewayResourceAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="bf848-106">Create method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="bf848-107">Crée une stratégie d’autorisation des ressources Bureau à distance (RD RAP).</span><span class="sxs-lookup"><span data-stu-id="bf848-107">Creates a Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="bf848-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf848-108">Syntax</span></span>


```mof
uint32 Create(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupType,
  [in] string  ResourceGroupName,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a><span data-ttu-id="bf848-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf848-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf848-110">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf848-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf848-111">Nom de la RD RAP.</span><span class="sxs-lookup"><span data-stu-id="bf848-111">Name of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="bf848-112">*Description* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf848-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf848-113">Description de la RD RAP.</span><span class="sxs-lookup"><span data-stu-id="bf848-113">Description of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="bf848-114">*Activé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf848-114">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf848-115">Indique si le RAP (RD) doit être activé.</span><span class="sxs-lookup"><span data-stu-id="bf848-115">Indicates whether the RD RAP is to be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="bf848-116">*ResourceGroupType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf848-116">*ResourceGroupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf848-117">Type de groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="bf848-117">Resource group type.</span></span>

<dt>

<span data-ttu-id="bf848-118">ROUTAGE</span><span class="sxs-lookup"><span data-stu-id="bf848-118">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="bf848-119">Groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="bf848-119">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="bf848-120">CG</span><span class="sxs-lookup"><span data-stu-id="bf848-120">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="bf848-121">Groupe d’ordinateurs, tel qu’il est stocké dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="bf848-121">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="bf848-122">TOUS les</span><span class="sxs-lookup"><span data-stu-id="bf848-122">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="bf848-123">Toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="bf848-123">All resources.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bf848-124">*ResourceGroupName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf848-124">*ResourceGroupName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf848-125">Nom du groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="bf848-125">Resource group name.</span></span>

</dd> <dt>

<span data-ttu-id="bf848-126">*UserGroupNames* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf848-126">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf848-127">Liste de noms de groupes d’utilisateurs séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="bf848-127">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="bf848-128">Si l’utilisateur appartient à l’un de ces groupes d’utilisateurs, l’accès est autorisé.</span><span class="sxs-lookup"><span data-stu-id="bf848-128">If the user belongs to any of these user groups, access will be permitted.</span></span> <span data-ttu-id="bf848-129">Les noms des groupes d’utilisateurs doivent être au format *domaine \\ UserGroupName*.</span><span class="sxs-lookup"><span data-stu-id="bf848-129">User group names should be of the format *Domain\\UserGroupName*.</span></span>

</dd> <dt>

<span data-ttu-id="bf848-130">*ProtocolNames* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf848-130">*ProtocolNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf848-131">Liste délimitée par des points-virgules des noms de protocole qui sont activés pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="bf848-131">Semicolon-separated list of protocol names that are enabled for this policy.</span></span> <span data-ttu-id="bf848-132">Les noms doivent correspondre au retour de la méthode [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) de la classe [**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="bf848-132">Names must match the return of the [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) method of the [**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="bf848-133">*PortNumbers* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf848-133">*PortNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf848-134">Liste délimitée par des points-virgules des numéros de port activés pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="bf848-134">Semicolon-separated list of port numbers that are enabled for this policy.</span></span> <span data-ttu-id="bf848-135">Pour autoriser n’importe quel numéro de port, définissez « \* ».</span><span class="sxs-lookup"><span data-stu-id="bf848-135">To allow any port number, set "\*".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf848-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf848-136">Return value</span></span>

<span data-ttu-id="bf848-137">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="bf848-137">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="bf848-138">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="bf848-138">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="bf848-139">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bf848-139">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bf848-140">Notes</span><span class="sxs-lookup"><span data-stu-id="bf848-140">Remarks</span></span>

<span data-ttu-id="bf848-141">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="bf848-141">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="bf848-142">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="bf848-142">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bf848-143">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bf848-143">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bf848-144">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="bf848-144">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bf848-145">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bf848-145">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf848-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf848-146">Requirements</span></span>



| <span data-ttu-id="bf848-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf848-147">Requirement</span></span> | <span data-ttu-id="bf848-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf848-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf848-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf848-149">Minimum supported client</span></span><br/> | <span data-ttu-id="bf848-150">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf848-150">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bf848-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf848-151">Minimum supported server</span></span><br/> | <span data-ttu-id="bf848-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf848-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bf848-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bf848-153">Namespace</span></span><br/>                | <span data-ttu-id="bf848-154">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="bf848-154">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="bf848-155">MOF</span><span class="sxs-lookup"><span data-stu-id="bf848-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf848-156"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf848-156"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf848-157">DLL</span><span class="sxs-lookup"><span data-stu-id="bf848-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf848-158"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf848-158"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bf848-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf848-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf848-160">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="bf848-160">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

