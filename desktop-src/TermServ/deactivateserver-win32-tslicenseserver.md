---
title: Méthode DeactivateServer de la classe Win32_TSLicenseServer
description: Désactive le serveur de licences Bureau à distance à l’aide d’un code de confirmation reçu sur le téléphone.
ms.assetid: 84e069b7-9a4f-4843-b656-839f936ac727
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DeactivateServer
- Services Bureau à distance de la méthode DeactivateServer, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode DeactivateServer
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.DeactivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b851a8d8049c9194bce163afc4b7bad5d4aa15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941759"
---
# <a name="deactivateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="4f0b8-106">Méthode DeactivateServer de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="4f0b8-106">DeactivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="4f0b8-107">Désactive le serveur de licences Bureau à distance à l’aide d’un code de confirmation reçu sur le téléphone.</span><span class="sxs-lookup"><span data-stu-id="4f0b8-107">Deactivates the Remote Desktop license server by using a confirmation code that is received over the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f0b8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f0b8-108">Syntax</span></span>


```mof
uint32 DeactivateServer(
  [in]  string sConfirmCode,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="4f0b8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f0b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f0b8-110">*sConfirmCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4f0b8-110">*sConfirmCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f0b8-111">Code de confirmation.</span><span class="sxs-lookup"><span data-stu-id="4f0b8-111">Confirmation code.</span></span>

</dd> <dt>

<span data-ttu-id="4f0b8-112">*ActivationStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4f0b8-112">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f0b8-113">L’état d’activation renvoyé peut être l’un des suivants.</span><span class="sxs-lookup"><span data-stu-id="4f0b8-113">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="4f0b8-114">0</span><span class="sxs-lookup"><span data-stu-id="4f0b8-114">0</span></span>
</dt> <dd>

<span data-ttu-id="4f0b8-115">Le serveur de licences Bureau à distance est activé.</span><span class="sxs-lookup"><span data-stu-id="4f0b8-115">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="4f0b8-116">1</span><span class="sxs-lookup"><span data-stu-id="4f0b8-116">1</span></span>
</dt> <dd>

<span data-ttu-id="4f0b8-117">Le serveur de licences Bureau à distance n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="4f0b8-117">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="4f0b8-118">2</span><span class="sxs-lookup"><span data-stu-id="4f0b8-118">2</span></span>
</dt> <dd>

<span data-ttu-id="4f0b8-119">Une erreur inconnue s'est produite.</span><span class="sxs-lookup"><span data-stu-id="4f0b8-119">An unknown error occurred.</span></span> <span data-ttu-id="4f0b8-120">Vous ne savez pas si le serveur de licences Services Bureau à distance est activé.</span><span class="sxs-lookup"><span data-stu-id="4f0b8-120">It is not known whether the Remote Desktop Services license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f0b8-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4f0b8-121">Return value</span></span>

<span data-ttu-id="4f0b8-122">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="4f0b8-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4f0b8-123">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="4f0b8-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4f0b8-124">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4f0b8-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4f0b8-125">Notes</span><span class="sxs-lookup"><span data-stu-id="4f0b8-125">Remarks</span></span>

<span data-ttu-id="4f0b8-126">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4f0b8-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="4f0b8-127">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="4f0b8-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4f0b8-128">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4f0b8-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4f0b8-129">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="4f0b8-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4f0b8-130">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4f0b8-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f0b8-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f0b8-131">Requirements</span></span>



| <span data-ttu-id="4f0b8-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f0b8-132">Requirement</span></span> | <span data-ttu-id="4f0b8-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f0b8-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f0b8-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f0b8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4f0b8-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f0b8-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="4f0b8-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f0b8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4f0b8-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f0b8-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="4f0b8-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4f0b8-138">Namespace</span></span><br/>                | <span data-ttu-id="4f0b8-139">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="4f0b8-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="4f0b8-140">MOF</span><span class="sxs-lookup"><span data-stu-id="4f0b8-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f0b8-141"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f0b8-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f0b8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4f0b8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f0b8-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f0b8-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f0b8-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f0b8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f0b8-145">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="4f0b8-145">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

