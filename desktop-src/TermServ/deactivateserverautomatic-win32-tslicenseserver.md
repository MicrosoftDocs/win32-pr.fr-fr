---
title: Méthode DeactivateServerAutomatic de la classe Win32_TSLicenseServer
description: Désactive le serveur de licences Bureau à distance sur Internet.
ms.assetid: 6e049d7f-1753-484d-98b8-fde66d16b5ab
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DeactivateServerAutomatic
- Services Bureau à distance de la méthode DeactivateServerAutomatic, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode DeactivateServerAutomatic
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.DeactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d466b5f7814d6004bafdd01bce161a481eacf26a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032522"
---
# <a name="deactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="6d6cf-106">Méthode DeactivateServerAutomatic de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="6d6cf-106">DeactivateServerAutomatic method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="6d6cf-107">Désactive le serveur de licences Bureau à distance sur Internet.</span><span class="sxs-lookup"><span data-stu-id="6d6cf-107">Deactivates the Remote Desktop license server over the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d6cf-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d6cf-108">Syntax</span></span>


```mof
uint32 DeactivateServerAutomatic(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="6d6cf-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d6cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d6cf-110">*ActivationStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6d6cf-110">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d6cf-111">L’état d’activation renvoyé peut être l’un des suivants.</span><span class="sxs-lookup"><span data-stu-id="6d6cf-111">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="6d6cf-112">0</span><span class="sxs-lookup"><span data-stu-id="6d6cf-112">0</span></span>
</dt> <dd>

<span data-ttu-id="6d6cf-113">Le serveur de licences Bureau à distance est activé.</span><span class="sxs-lookup"><span data-stu-id="6d6cf-113">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="6d6cf-114">1</span><span class="sxs-lookup"><span data-stu-id="6d6cf-114">1</span></span>
</dt> <dd>

<span data-ttu-id="6d6cf-115">Le serveur de licences Bureau à distance n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="6d6cf-115">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="6d6cf-116">2</span><span class="sxs-lookup"><span data-stu-id="6d6cf-116">2</span></span>
</dt> <dd>

<span data-ttu-id="6d6cf-117">Une erreur inconnue s'est produite.</span><span class="sxs-lookup"><span data-stu-id="6d6cf-117">An unknown error occurred.</span></span> <span data-ttu-id="6d6cf-118">Vous ne savez pas si le serveur de licences Bureau à distance est activé.</span><span class="sxs-lookup"><span data-stu-id="6d6cf-118">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d6cf-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d6cf-119">Return value</span></span>

<span data-ttu-id="6d6cf-120">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="6d6cf-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6d6cf-121">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="6d6cf-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6d6cf-122">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6d6cf-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6d6cf-123">Notes</span><span class="sxs-lookup"><span data-stu-id="6d6cf-123">Remarks</span></span>

<span data-ttu-id="6d6cf-124">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="6d6cf-124">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6d6cf-125">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="6d6cf-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6d6cf-126">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6d6cf-126">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6d6cf-127">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="6d6cf-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6d6cf-128">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6d6cf-128">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d6cf-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d6cf-129">Requirements</span></span>



| <span data-ttu-id="6d6cf-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d6cf-130">Requirement</span></span> | <span data-ttu-id="6d6cf-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d6cf-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d6cf-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d6cf-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6d6cf-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d6cf-133">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="6d6cf-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d6cf-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6d6cf-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d6cf-135">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="6d6cf-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6d6cf-136">Namespace</span></span><br/>                | <span data-ttu-id="6d6cf-137">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="6d6cf-137">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="6d6cf-138">MOF</span><span class="sxs-lookup"><span data-stu-id="6d6cf-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d6cf-139"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d6cf-139"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d6cf-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6d6cf-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d6cf-141"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d6cf-141"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d6cf-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d6cf-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d6cf-143">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="6d6cf-143">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

