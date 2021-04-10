---
title: Méthode GetActivationStatus de la classe Win32_TSLicenseServer
description: Récupère l’état d’activation actuel du serveur de licences Bureau à distance.
ms.assetid: 1148ffc5-33c1-41f1-b477-78a5293333d1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetActivationStatus
- Services Bureau à distance de la méthode GetActivationStatus, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode GetActivationStatus
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.GetActivationStatus
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 882f6209cd13c2372316e6a9606a3bc4fcd60fdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104338"
---
# <a name="getactivationstatus-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="cd0e9-106">Méthode GetActivationStatus de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="cd0e9-106">GetActivationStatus method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="cd0e9-107">Récupère l’état d’activation actuel du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="cd0e9-107">Retrieves the current activation status of the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd0e9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd0e9-108">Syntax</span></span>


```mof
uint32 GetActivationStatus(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="cd0e9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd0e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd0e9-110">*ActivationStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cd0e9-110">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd0e9-111">L’état d’activation renvoyé peut être l’un des suivants.</span><span class="sxs-lookup"><span data-stu-id="cd0e9-111">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="cd0e9-112">0</span><span class="sxs-lookup"><span data-stu-id="cd0e9-112">0</span></span>
</dt> <dd>

<span data-ttu-id="cd0e9-113">Le serveur de licences Bureau à distance est activé.</span><span class="sxs-lookup"><span data-stu-id="cd0e9-113">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="cd0e9-114">1</span><span class="sxs-lookup"><span data-stu-id="cd0e9-114">1</span></span>
</dt> <dd>

<span data-ttu-id="cd0e9-115">Le serveur de licences Bureau à distance n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="cd0e9-115">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="cd0e9-116">2</span><span class="sxs-lookup"><span data-stu-id="cd0e9-116">2</span></span>
</dt> <dd>

<span data-ttu-id="cd0e9-117">Une erreur inconnue s'est produite.</span><span class="sxs-lookup"><span data-stu-id="cd0e9-117">An unknown error occurred.</span></span> <span data-ttu-id="cd0e9-118">Vous ne savez pas si le serveur de licences Bureau à distance est activé.</span><span class="sxs-lookup"><span data-stu-id="cd0e9-118">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd0e9-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cd0e9-119">Return value</span></span>

<span data-ttu-id="cd0e9-120">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="cd0e9-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="cd0e9-121">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="cd0e9-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="cd0e9-122">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="cd0e9-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cd0e9-123">Notes</span><span class="sxs-lookup"><span data-stu-id="cd0e9-123">Remarks</span></span>

<span data-ttu-id="cd0e9-124">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="cd0e9-124">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="cd0e9-125">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="cd0e9-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cd0e9-126">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="cd0e9-126">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="cd0e9-127">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="cd0e9-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cd0e9-128">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="cd0e9-128">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd0e9-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd0e9-129">Requirements</span></span>



| <span data-ttu-id="cd0e9-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd0e9-130">Requirement</span></span> | <span data-ttu-id="cd0e9-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd0e9-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd0e9-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd0e9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="cd0e9-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd0e9-133">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="cd0e9-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd0e9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="cd0e9-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd0e9-135">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="cd0e9-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cd0e9-136">Namespace</span></span><br/>                | <span data-ttu-id="cd0e9-137">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="cd0e9-137">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="cd0e9-138">MOF</span><span class="sxs-lookup"><span data-stu-id="cd0e9-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd0e9-139"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd0e9-139"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd0e9-140">DLL</span><span class="sxs-lookup"><span data-stu-id="cd0e9-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd0e9-141"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd0e9-141"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd0e9-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd0e9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd0e9-143">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="cd0e9-143">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

