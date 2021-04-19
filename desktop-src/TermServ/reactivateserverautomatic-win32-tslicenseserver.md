---
title: Méthode ReactivateServerAutomatic de la classe Win32_TSLicenseServer
description: Réactive le serveur de licences Bureau à distance à l’aide d’une connexion automatique à Internet.
ms.assetid: 98b9b8e5-4de4-418c-9175-58e8b84784d5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ReactivateServerAutomatic
- Services Bureau à distance de la méthode ReactivateServerAutomatic, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode ReactivateServerAutomatic
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b9df7314abc3dccf6458322911c50d6120ad10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536920"
---
# <a name="reactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="efbbf-106">Méthode ReactivateServerAutomatic de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="efbbf-106">ReactivateServerAutomatic method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="efbbf-107">Réactive le serveur de licences Bureau à distance à l’aide d’une connexion automatique à Internet.</span><span class="sxs-lookup"><span data-stu-id="efbbf-107">Reactivates the Remote Desktop license server by using an automatic connection to the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="efbbf-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efbbf-108">Syntax</span></span>


```mof
uint32 ReactivateServerAutomatic(
  [in]  uint32 Reason,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="efbbf-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="efbbf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efbbf-110">*Raison* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="efbbf-110">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efbbf-111">Raison de l’activation.</span><span class="sxs-lookup"><span data-stu-id="efbbf-111">Reason for the activation.</span></span> <span data-ttu-id="efbbf-112">Il peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="efbbf-112">It can be one of the following values.</span></span>

<dt>

<span data-ttu-id="efbbf-113">0</span><span class="sxs-lookup"><span data-stu-id="efbbf-113">0</span></span>
</dt> <dd>

<span data-ttu-id="efbbf-114">Le serveur a été redéployé.</span><span class="sxs-lookup"><span data-stu-id="efbbf-114">The server was redeployed.</span></span>

</dd> <dt>

<span data-ttu-id="efbbf-115">1</span><span class="sxs-lookup"><span data-stu-id="efbbf-115">1</span></span>
</dt> <dd>

<span data-ttu-id="efbbf-116">Le certificat est endommagé.</span><span class="sxs-lookup"><span data-stu-id="efbbf-116">The certificate was corrupt.</span></span>

</dd> <dt>

<span data-ttu-id="efbbf-117">2</span><span class="sxs-lookup"><span data-stu-id="efbbf-117">2</span></span>
</dt> <dd>

<span data-ttu-id="efbbf-118">La clé privée a été compromise.</span><span class="sxs-lookup"><span data-stu-id="efbbf-118">The private key was compromised.</span></span>

</dd> <dt>

<span data-ttu-id="efbbf-119">3</span><span class="sxs-lookup"><span data-stu-id="efbbf-119">3</span></span>
</dt> <dd>

<span data-ttu-id="efbbf-120">La clé d’activation a expiré.</span><span class="sxs-lookup"><span data-stu-id="efbbf-120">The activation key expired.</span></span>

</dd> <dt>

<span data-ttu-id="efbbf-121">4</span><span class="sxs-lookup"><span data-stu-id="efbbf-121">4</span></span>
</dt> <dd>

<span data-ttu-id="efbbf-122">Le serveur a été mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="efbbf-122">The server was upgraded.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="efbbf-123">*ActivationStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="efbbf-123">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efbbf-124">L’état d’activation renvoyé peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="efbbf-124">The activation status returned can be one of the following values.</span></span>

<dt>

<span data-ttu-id="efbbf-125">0</span><span class="sxs-lookup"><span data-stu-id="efbbf-125">0</span></span>
</dt> <dd>

<span data-ttu-id="efbbf-126">Le serveur de licences Bureau à distance est activé.</span><span class="sxs-lookup"><span data-stu-id="efbbf-126">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="efbbf-127">1</span><span class="sxs-lookup"><span data-stu-id="efbbf-127">1</span></span>
</dt> <dd>

<span data-ttu-id="efbbf-128">Le serveur de licences Bureau à distance n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="efbbf-128">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="efbbf-129">2</span><span class="sxs-lookup"><span data-stu-id="efbbf-129">2</span></span>
</dt> <dd>

<span data-ttu-id="efbbf-130">Une erreur inconnue s'est produite.</span><span class="sxs-lookup"><span data-stu-id="efbbf-130">An unknown error occurred.</span></span> <span data-ttu-id="efbbf-131">Vous ne savez pas si le serveur de licences Bureau à distance est activé.</span><span class="sxs-lookup"><span data-stu-id="efbbf-131">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efbbf-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="efbbf-132">Return value</span></span>

<span data-ttu-id="efbbf-133">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="efbbf-133">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="efbbf-134">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="efbbf-134">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="efbbf-135">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="efbbf-135">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="efbbf-136">Notes</span><span class="sxs-lookup"><span data-stu-id="efbbf-136">Remarks</span></span>

<span data-ttu-id="efbbf-137">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="efbbf-137">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="efbbf-138">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="efbbf-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="efbbf-139">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="efbbf-139">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="efbbf-140">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="efbbf-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="efbbf-141">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="efbbf-141">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="efbbf-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efbbf-142">Requirements</span></span>



| <span data-ttu-id="efbbf-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="efbbf-143">Requirement</span></span> | <span data-ttu-id="efbbf-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="efbbf-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="efbbf-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efbbf-145">Minimum supported client</span></span><br/> | <span data-ttu-id="efbbf-146">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="efbbf-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="efbbf-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efbbf-147">Minimum supported server</span></span><br/> | <span data-ttu-id="efbbf-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="efbbf-148">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="efbbf-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="efbbf-149">Namespace</span></span><br/>                | <span data-ttu-id="efbbf-150">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="efbbf-150">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="efbbf-151">MOF</span><span class="sxs-lookup"><span data-stu-id="efbbf-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efbbf-152"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="efbbf-152"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="efbbf-153">DLL</span><span class="sxs-lookup"><span data-stu-id="efbbf-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efbbf-154"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efbbf-154"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efbbf-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efbbf-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efbbf-156">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="efbbf-156">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

