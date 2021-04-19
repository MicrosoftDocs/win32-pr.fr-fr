---
title: Méthode ActivateServer de la classe Win32_TSLicenseServer
description: Active le serveur de licences Bureau à distance à l’aide d’un identificateur de serveur de licences Bureau à distance qui est obtenu sur le téléphone ou sur Internet.
ms.assetid: 628e87f0-600e-404d-a0b4-35f1570b4fc0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ActivateServer
- Services Bureau à distance de la méthode ActivateServer, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode ActivateServer
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ActivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19db0df0ca9b0bf41fe692ba07fe605dc1e8d5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511395"
---
# <a name="activateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="c834c-106">Méthode ActivateServer de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="c834c-106">ActivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="c834c-107">Active le serveur de licences Bureau à distance à l’aide d’un identificateur de serveur de licences Bureau à distance qui est obtenu sur le téléphone ou sur Internet.</span><span class="sxs-lookup"><span data-stu-id="c834c-107">Activates the Remote Desktop license server by using a Remote Desktop license server identifier that is obtained over the phone or the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="c834c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c834c-108">Syntax</span></span>


```mof
uint32 ActivateServer(
  [in]  string sLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="c834c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c834c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c834c-110">*sLicenseServerId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c834c-110">*sLicenseServerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c834c-111">Bureau à distance ID du serveur de licences qui a été obtenu sur le téléphone ou sur Internet.</span><span class="sxs-lookup"><span data-stu-id="c834c-111">Remote Desktop license server ID that was obtained over the phone or the Internet.</span></span> <span data-ttu-id="c834c-112">Le paramètre *sLicenseServerId* est une chaîne alphanumérique de 35 caractères qui ne peut pas contenir de traits d’Union.</span><span class="sxs-lookup"><span data-stu-id="c834c-112">The *sLicenseServerId* parameter is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="c834c-113">*ActivationStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c834c-113">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c834c-114">L’état d’activation renvoyé peut être l’un des suivants.</span><span class="sxs-lookup"><span data-stu-id="c834c-114">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="c834c-115">0</span><span class="sxs-lookup"><span data-stu-id="c834c-115">0</span></span>
</dt> <dd>

<span data-ttu-id="c834c-116">Le serveur de licences Bureau à distance est activé.</span><span class="sxs-lookup"><span data-stu-id="c834c-116">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="c834c-117">1</span><span class="sxs-lookup"><span data-stu-id="c834c-117">1</span></span>
</dt> <dd>

<span data-ttu-id="c834c-118">Le serveur de licences Bureau à distance n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="c834c-118">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="c834c-119">2</span><span class="sxs-lookup"><span data-stu-id="c834c-119">2</span></span>
</dt> <dd>

<span data-ttu-id="c834c-120">Une erreur inconnue s'est produite.</span><span class="sxs-lookup"><span data-stu-id="c834c-120">An unknown error occurred.</span></span> <span data-ttu-id="c834c-121">Vous ne savez pas si le serveur de licences Bureau à distance est activé.</span><span class="sxs-lookup"><span data-stu-id="c834c-121">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c834c-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c834c-122">Return value</span></span>

<span data-ttu-id="c834c-123">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="c834c-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c834c-124">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="c834c-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c834c-125">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c834c-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c834c-126">Notes</span><span class="sxs-lookup"><span data-stu-id="c834c-126">Remarks</span></span>

<span data-ttu-id="c834c-127">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c834c-127">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c834c-128">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="c834c-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c834c-129">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c834c-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c834c-130">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="c834c-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c834c-131">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c834c-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c834c-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c834c-132">Requirements</span></span>



| <span data-ttu-id="c834c-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c834c-133">Requirement</span></span> | <span data-ttu-id="c834c-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="c834c-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c834c-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c834c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c834c-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c834c-136">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="c834c-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c834c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c834c-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c834c-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c834c-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c834c-139">Namespace</span></span><br/>                | <span data-ttu-id="c834c-140">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="c834c-140">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="c834c-141">MOF</span><span class="sxs-lookup"><span data-stu-id="c834c-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c834c-142"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c834c-142"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c834c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="c834c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c834c-144"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c834c-144"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c834c-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c834c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c834c-146">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="c834c-146">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

