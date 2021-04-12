---
title: Méthode ReactivateServer de la classe Win32_TSLicenseServer
description: Réactive le serveur de licences Bureau à distance à l’aide d’un nouvel identificateur qui a été obtenu sur le téléphone ou sur Internet.
ms.assetid: dd9ff938-a683-4f60-b7cc-7580892953b6
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ReactivateServer
- Services Bureau à distance de la méthode ReactivateServer, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode ReactivateServer
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50e84eb0bed0b52ad463fce50ce334d6c8eb8d80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465303"
---
# <a name="reactivateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="af2e8-106">Méthode ReactivateServer de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="af2e8-106">ReactivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="af2e8-107">Réactive le serveur de licences Bureau à distance à l’aide d’un nouvel identificateur qui a été obtenu sur le téléphone ou sur Internet.</span><span class="sxs-lookup"><span data-stu-id="af2e8-107">Reactivates the Remote Desktop license server by using a new identifier that was obtained over the phone or the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="af2e8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af2e8-108">Syntax</span></span>


```mof
uint32 ReactivateServer(
  [in]  string sNewLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="af2e8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af2e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af2e8-110">*sNewLicenseServerId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af2e8-110">*sNewLicenseServerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af2e8-111">Bureau à distance ID du serveur de licences qui a été obtenu sur le téléphone ou sur Internet.</span><span class="sxs-lookup"><span data-stu-id="af2e8-111">Remote Desktop license server ID that was obtained over the phone or the Internet.</span></span>

</dd> <dt>

<span data-ttu-id="af2e8-112">*ActivationStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="af2e8-112">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af2e8-113">L’état d’activation renvoyé peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="af2e8-113">The activation status returned can be one of the following values.</span></span>

<dt>

<span data-ttu-id="af2e8-114">0</span><span class="sxs-lookup"><span data-stu-id="af2e8-114">0</span></span>
</dt> <dd>

<span data-ttu-id="af2e8-115">Le serveur de licences Bureau à distance est activé.</span><span class="sxs-lookup"><span data-stu-id="af2e8-115">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="af2e8-116">1</span><span class="sxs-lookup"><span data-stu-id="af2e8-116">1</span></span>
</dt> <dd>

<span data-ttu-id="af2e8-117">Le serveur de licences Bureau à distance n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="af2e8-117">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="af2e8-118">2</span><span class="sxs-lookup"><span data-stu-id="af2e8-118">2</span></span>
</dt> <dd>

<span data-ttu-id="af2e8-119">Une erreur inconnue s'est produite.</span><span class="sxs-lookup"><span data-stu-id="af2e8-119">An unknown error occurred.</span></span> <span data-ttu-id="af2e8-120">Vous ne savez pas si le serveur de licences Bureau à distance est activé.</span><span class="sxs-lookup"><span data-stu-id="af2e8-120">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af2e8-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af2e8-121">Return value</span></span>

<span data-ttu-id="af2e8-122">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="af2e8-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="af2e8-123">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="af2e8-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="af2e8-124">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="af2e8-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="af2e8-125">Notes</span><span class="sxs-lookup"><span data-stu-id="af2e8-125">Remarks</span></span>

<span data-ttu-id="af2e8-126">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="af2e8-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="af2e8-127">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="af2e8-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="af2e8-128">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="af2e8-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="af2e8-129">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="af2e8-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="af2e8-130">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="af2e8-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="af2e8-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af2e8-131">Requirements</span></span>



| <span data-ttu-id="af2e8-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af2e8-132">Requirement</span></span> | <span data-ttu-id="af2e8-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="af2e8-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="af2e8-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af2e8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="af2e8-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="af2e8-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="af2e8-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af2e8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="af2e8-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af2e8-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="af2e8-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="af2e8-138">Namespace</span></span><br/>                | <span data-ttu-id="af2e8-139">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="af2e8-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="af2e8-140">MOF</span><span class="sxs-lookup"><span data-stu-id="af2e8-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af2e8-141"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af2e8-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="af2e8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="af2e8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af2e8-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af2e8-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af2e8-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af2e8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af2e8-145">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="af2e8-145">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

