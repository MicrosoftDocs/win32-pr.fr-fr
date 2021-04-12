---
title: Méthode ChangeRole de la classe Win32_TSLicenseServer
description: Modifie l’étendue de la découverte du serveur de licences Bureau à distance. L’étendue de découverte détermine les serveurs de Bureau à distance hôte de session (hôte de session Bureau à distance) sur le réseau qui peuvent détecter automatiquement le serveur de licences.
ms.assetid: 3d98fd8a-4ade-489f-8edd-5df1227f15cd
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ChangeRole
- Services Bureau à distance de la méthode ChangeRole, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode ChangeRole
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ChangeRole
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9746b856c74e9603751fe85bb861e2b6869f03a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464694"
---
# <a name="changerole-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="6d444-107">Méthode ChangeRole de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="6d444-107">ChangeRole method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="6d444-108">Modifie l’étendue de la découverte du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="6d444-108">Changes the discovery scope of the Remote Desktop license server.</span></span> <span data-ttu-id="6d444-109">L’étendue de découverte détermine les serveurs de Bureau à distance hôte de session (hôte de session Bureau à distance) sur le réseau qui peuvent détecter automatiquement le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="6d444-109">The discovery scope determines which Remote Desktop Session Host (RD Session Host) servers on the network can automatically discover the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d444-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d444-110">Syntax</span></span>


```mof
uint32 ChangeRole(
  [in] uint32 ServerRole
);
```



## <a name="parameters"></a><span data-ttu-id="6d444-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d444-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d444-112">*ServerRole* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d444-112">*ServerRole* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d444-113">Étendue de la découverte pour le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="6d444-113">Discovery scope for the Remote Desktop license server.</span></span> <span data-ttu-id="6d444-114">Vous pouvez définir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6d444-114">You can set one of the following values.</span></span>

<dt>

<span data-ttu-id="6d444-115">0</span><span class="sxs-lookup"><span data-stu-id="6d444-115">0</span></span>
</dt> <dd>

<span data-ttu-id="6d444-116">Les serveurs hôtes de session Bureau à distance dans le même groupe de travail peuvent découvrir le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="6d444-116">RD Session Host servers in the same workgroup can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="6d444-117">1</span><span class="sxs-lookup"><span data-stu-id="6d444-117">1</span></span>
</dt> <dd>

<span data-ttu-id="6d444-118">Les serveurs hôtes de session Bureau à distance dans le même domaine peuvent découvrir le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="6d444-118">RD Session Host servers in the same domain can discover the license server.</span></span> <span data-ttu-id="6d444-119">Vous devez être connecté en tant qu’administrateur de domaine pour définir cette valeur.</span><span class="sxs-lookup"><span data-stu-id="6d444-119">You must be logged on as a domain administrator to set this value.</span></span>

</dd> <dt>

<span data-ttu-id="6d444-120">2</span><span class="sxs-lookup"><span data-stu-id="6d444-120">2</span></span>
</dt> <dd>

<span data-ttu-id="6d444-121">Les serveurs hôtes de session Bureau à distance de plusieurs domaines de la même forêt peuvent découvrir le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="6d444-121">RD Session Host servers from multiple domains in the same forest can discover the license server.</span></span> <span data-ttu-id="6d444-122">Vous devez être connecté en tant qu’administrateur d’entreprise pour définir cette valeur.</span><span class="sxs-lookup"><span data-stu-id="6d444-122">You must be logged on as an enterprise administrator to set this value.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d444-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d444-123">Return value</span></span>

<span data-ttu-id="6d444-124">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="6d444-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6d444-125">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="6d444-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6d444-126">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6d444-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6d444-127">Notes</span><span class="sxs-lookup"><span data-stu-id="6d444-127">Remarks</span></span>

<span data-ttu-id="6d444-128">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="6d444-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6d444-129">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="6d444-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6d444-130">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6d444-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6d444-131">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="6d444-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6d444-132">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6d444-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d444-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d444-133">Requirements</span></span>



| <span data-ttu-id="6d444-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d444-134">Requirement</span></span> | <span data-ttu-id="6d444-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d444-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d444-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d444-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6d444-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d444-137">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="6d444-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d444-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6d444-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d444-139">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="6d444-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6d444-140">Namespace</span></span><br/>                | <span data-ttu-id="6d444-141">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="6d444-141">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="6d444-142">MOF</span><span class="sxs-lookup"><span data-stu-id="6d444-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d444-143"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d444-143"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d444-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6d444-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d444-145"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d444-145"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d444-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d444-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d444-147">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="6d444-147">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

