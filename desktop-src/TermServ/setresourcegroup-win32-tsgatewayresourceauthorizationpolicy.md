---
title: Méthode SetResourceGroup de la classe Win32_TSGatewayResourceAuthorizationPolicy
description: Définit le type et le nom du groupe de ressources.
ms.assetid: a3dd0ffa-a39b-46f9-8317-fcc90a8afcd1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetResourceGroup
- Services Bureau à distance de la méthode SetResourceGroup, classe Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance, méthode SetResourceGroup
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetResourceGroup
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22c2ceacbbbfc40372d0f0d084cf6525f754934
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843909"
---
# <a name="setresourcegroup-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="2d872-106">Méthode SetResourceGroup de la \_ classe Win32 TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="2d872-106">SetResourceGroup method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="2d872-107">Définit le type et le nom du groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="2d872-107">Sets the resource group type and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d872-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d872-108">Syntax</span></span>


```mof
uint32 SetResourceGroup(
  [in] string ResourceGroupName,
  [in] string ResourceGroupType
);
```



## <a name="parameters"></a><span data-ttu-id="2d872-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d872-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d872-110">*ResourceGroupName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d872-110">*ResourceGroupName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d872-111">Nom du groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="2d872-111">Resource group name.</span></span> <span data-ttu-id="2d872-112">Cette valeur remplace la propriété **ResourceGroupName** existante.</span><span class="sxs-lookup"><span data-stu-id="2d872-112">This value replaces the existing **ResourceGroupName** property.</span></span>

</dd> <dt>

<span data-ttu-id="2d872-113">*ResourceGroupType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d872-113">*ResourceGroupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d872-114">Identifie le type du groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="2d872-114">Identifies the type of the resource group.</span></span> <span data-ttu-id="2d872-115">Cette valeur remplace la propriété **ResourceGroupType** existante.</span><span class="sxs-lookup"><span data-stu-id="2d872-115">This value replaces the existing **ResourceGroupType** property.</span></span>

<dt>

<span data-ttu-id="2d872-116">ROUTAGE</span><span class="sxs-lookup"><span data-stu-id="2d872-116">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="2d872-117">Groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="2d872-117">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="2d872-118">CG</span><span class="sxs-lookup"><span data-stu-id="2d872-118">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="2d872-119">Groupe d’ordinateurs, tel qu’il est stocké dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="2d872-119">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="2d872-120">TOUS les</span><span class="sxs-lookup"><span data-stu-id="2d872-120">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="2d872-121">Toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="2d872-121">All resources.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d872-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d872-122">Return value</span></span>

<span data-ttu-id="2d872-123">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="2d872-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2d872-124">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="2d872-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2d872-125">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2d872-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2d872-126">Notes</span><span class="sxs-lookup"><span data-stu-id="2d872-126">Remarks</span></span>

<span data-ttu-id="2d872-127">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="2d872-127">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="2d872-128">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="2d872-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2d872-129">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2d872-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2d872-130">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="2d872-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2d872-131">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2d872-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d872-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d872-132">Requirements</span></span>



| <span data-ttu-id="2d872-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d872-133">Requirement</span></span> | <span data-ttu-id="2d872-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d872-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d872-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d872-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2d872-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d872-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2d872-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d872-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2d872-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d872-138">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2d872-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2d872-139">Namespace</span></span><br/>                | <span data-ttu-id="2d872-140">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="2d872-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2d872-141">MOF</span><span class="sxs-lookup"><span data-stu-id="2d872-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d872-142"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d872-142"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d872-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2d872-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d872-144"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d872-144"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="2d872-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d872-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d872-146">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="2d872-146">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

