---
title: Méthode ActivateServerAutomatic de la classe Win32_TSLicenseServer
description: Active automatiquement le serveur de licences Bureau à distance via Internet.
ms.assetid: a33ba72f-3403-4bd2-94a9-0c5ef1cbb03e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ActivateServerAutomatic
- Services Bureau à distance de la méthode ActivateServerAutomatic, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode ActivateServerAutomatic
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ActivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68879dbc40cc4161edcfef631bf9bb4b72558df8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941884"
---
# <a name="activateserverautomatic-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="a253a-106">Méthode ActivateServerAutomatic de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="a253a-106">ActivateServerAutomatic method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="a253a-107">Active automatiquement le serveur de licences Bureau à distance via Internet.</span><span class="sxs-lookup"><span data-stu-id="a253a-107">Activates the Remote Desktop license server automatically over the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="a253a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a253a-108">Syntax</span></span>


```mof
uint32 ActivateServerAutomatic(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="a253a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a253a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a253a-110">*ActivationStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a253a-110">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a253a-111">L’état d’activation renvoyé peut être l’un des suivants.</span><span class="sxs-lookup"><span data-stu-id="a253a-111">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="a253a-112">0</span><span class="sxs-lookup"><span data-stu-id="a253a-112">0</span></span>
</dt> <dd>

<span data-ttu-id="a253a-113">Le serveur de licences Bureau à distance est activé.</span><span class="sxs-lookup"><span data-stu-id="a253a-113">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="a253a-114">1</span><span class="sxs-lookup"><span data-stu-id="a253a-114">1</span></span>
</dt> <dd>

<span data-ttu-id="a253a-115">Le serveur de licences Bureau à distance n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="a253a-115">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="a253a-116">2</span><span class="sxs-lookup"><span data-stu-id="a253a-116">2</span></span>
</dt> <dd>

<span data-ttu-id="a253a-117">Une erreur inconnue s'est produite.</span><span class="sxs-lookup"><span data-stu-id="a253a-117">An unknown error occurred.</span></span> <span data-ttu-id="a253a-118">Vous ne savez pas si le serveur de licences Bureau à distance est activé.</span><span class="sxs-lookup"><span data-stu-id="a253a-118">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a253a-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a253a-119">Return value</span></span>

<span data-ttu-id="a253a-120">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="a253a-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a253a-121">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="a253a-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a253a-122">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a253a-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a253a-123">Notes</span><span class="sxs-lookup"><span data-stu-id="a253a-123">Remarks</span></span>

<span data-ttu-id="a253a-124">Cette méthode échoue sauf si les propriétés **FirstName**, **LastName**, **Company** et **PaysRégion** sont définies.</span><span class="sxs-lookup"><span data-stu-id="a253a-124">This method fails unless the **FirstName**, **LastName**, **Company**, and **CountryRegion** properties are set.</span></span>

<span data-ttu-id="a253a-125">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a253a-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a253a-126">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="a253a-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a253a-127">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a253a-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a253a-128">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="a253a-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a253a-129">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a253a-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a253a-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a253a-130">Requirements</span></span>



| <span data-ttu-id="a253a-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a253a-131">Requirement</span></span> | <span data-ttu-id="a253a-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a253a-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a253a-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a253a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a253a-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a253a-134">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="a253a-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a253a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a253a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a253a-136">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="a253a-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a253a-137">Namespace</span></span><br/>                | <span data-ttu-id="a253a-138">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="a253a-138">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="a253a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="a253a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a253a-140"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a253a-140"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a253a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a253a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a253a-142"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a253a-142"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a253a-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a253a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a253a-144">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="a253a-144">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

