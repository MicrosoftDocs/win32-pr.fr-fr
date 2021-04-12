---
title: Méthode InstallOpenLicenseKeyPack de la classe Win32_TSLicenseKeyPack
description: Installe un jeu de clés de licence Open License Services Bureau à distance.
ms.assetid: be50e25c-cda3-408b-934b-51ce343f3271
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode InstallOpenLicenseKeyPack
- Services Bureau à distance de la méthode InstallOpenLicenseKeyPack, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode InstallOpenLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallOpenLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7335f25d3118c14f8cd0d27f72fd6a8d4cf1e0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464794"
---
# <a name="installopenlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="21b30-106">Méthode InstallOpenLicenseKeyPack de la \_ classe Win32 TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="21b30-106">InstallOpenLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="21b30-107">Installe un jeu de clés de licence Open License Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="21b30-107">Installs an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="21b30-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21b30-108">Syntax</span></span>


```mof
uint32 InstallOpenLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a><span data-ttu-id="21b30-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21b30-109">Parameters</span></span>

<span data-ttu-id="21b30-110">*sLicenseNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="21b30-110">*sLicenseNumber* \[in\]</span></span>

<span data-ttu-id="21b30-111">chaîne numérique de 8 caractères fournie avec le jeu de clés de licence.</span><span class="sxs-lookup"><span data-stu-id="21b30-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="21b30-112">Le paramètre *sLicenseNumber* ne peut pas contenir de traits d’Union.</span><span class="sxs-lookup"><span data-stu-id="21b30-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

<span data-ttu-id="21b30-113">*sAuthorizationNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="21b30-113">*sAuthorizationNumber* \[in\]</span></span>

<span data-ttu-id="21b30-114">chaîne alphanumérique de 15 caractères fournie avec la clé de licence.</span><span class="sxs-lookup"><span data-stu-id="21b30-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="21b30-115">Le paramètre *sAuthorizationNumber* ne peut pas contenir de traits d’Union.</span><span class="sxs-lookup"><span data-stu-id="21b30-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

<span data-ttu-id="21b30-116">*ProductVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="21b30-116">*ProductVersion* \[in\]</span></span>

<span data-ttu-id="21b30-117">Version du produit.</span><span class="sxs-lookup"><span data-stu-id="21b30-117">Product version.</span></span>

| <span data-ttu-id="21b30-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="21b30-118">Value</span></span> | <span data-ttu-id="21b30-119">Description</span><span class="sxs-lookup"><span data-stu-id="21b30-119">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="21b30-120">0</span><span class="sxs-lookup"><span data-stu-id="21b30-120">0</span></span> | <span data-ttu-id="21b30-121">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="21b30-121">Not supported</span></span> |
| <span data-ttu-id="21b30-122">1</span><span class="sxs-lookup"><span data-stu-id="21b30-122">1</span></span> | <span data-ttu-id="21b30-123">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="21b30-123">Not supported</span></span> |
| <span data-ttu-id="21b30-124">2</span><span class="sxs-lookup"><span data-stu-id="21b30-124">2</span></span> | <span data-ttu-id="21b30-125">Windows Server 2008/Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="21b30-125">Windows Server 2008/Windows Server 2008 R2</span></span> |
| <span data-ttu-id="21b30-126">4</span><span class="sxs-lookup"><span data-stu-id="21b30-126">4</span></span> | <span data-ttu-id="21b30-127">Windows Server 2012/Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="21b30-127">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="21b30-128">5</span><span class="sxs-lookup"><span data-stu-id="21b30-128">5</span></span> | <span data-ttu-id="21b30-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="21b30-129">Windows Server 2016</span></span> |
| <span data-ttu-id="21b30-130">6</span><span class="sxs-lookup"><span data-stu-id="21b30-130">6</span></span> | <span data-ttu-id="21b30-131">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="21b30-131">Windows Server 2019</span></span> |

<span data-ttu-id="21b30-132">*ProductType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="21b30-132">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21b30-133">Type de produit.</span><span class="sxs-lookup"><span data-stu-id="21b30-133">Product type.</span></span>

| <span data-ttu-id="21b30-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="21b30-134">Value</span></span> | <span data-ttu-id="21b30-135">Description</span><span class="sxs-lookup"><span data-stu-id="21b30-135">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="21b30-136">0</span><span class="sxs-lookup"><span data-stu-id="21b30-136">0</span></span> | <span data-ttu-id="21b30-137">Le type de produit du jeu de clés de licence Services Bureau à distance est par périphérique.</span><span class="sxs-lookup"><span data-stu-id="21b30-137">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="21b30-138">Par conséquent, chaque appareil qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence.</span><span class="sxs-lookup"><span data-stu-id="21b30-138">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="21b30-139">1</span><span class="sxs-lookup"><span data-stu-id="21b30-139">1</span></span> | <span data-ttu-id="21b30-140">Le type de produit du jeu de clés de licence Services Bureau à distance est par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="21b30-140">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="21b30-141">Par conséquent, chaque utilisateur qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence.</span><span class="sxs-lookup"><span data-stu-id="21b30-141">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="21b30-142">2</span><span class="sxs-lookup"><span data-stu-id="21b30-142">2</span></span> | <span data-ttu-id="21b30-143">Ce type de produit n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="21b30-143">This product type is not valid.</span></span> |

<span data-ttu-id="21b30-144">*LicenseCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="21b30-144">*LicenseCount* \[in\]</span></span>

<span data-ttu-id="21b30-145">Nombre de licences à installer.</span><span class="sxs-lookup"><span data-stu-id="21b30-145">The number of licenses to install.</span></span>

<span data-ttu-id="21b30-146">*KeyPackId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="21b30-146">*KeyPackId* \[out\]</span></span>

<span data-ttu-id="21b30-147">Reçoit l’identificateur du module de clé.</span><span class="sxs-lookup"><span data-stu-id="21b30-147">Receives the key pack identifier.</span></span>

## <a name="return-value"></a><span data-ttu-id="21b30-148">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="21b30-148">Return value</span></span>

<span data-ttu-id="21b30-149">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="21b30-149">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="21b30-150">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="21b30-150">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="21b30-151">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="21b30-151">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="21b30-152">Notes</span><span class="sxs-lookup"><span data-stu-id="21b30-152">Remarks</span></span>

<span data-ttu-id="21b30-153">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="21b30-153">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="21b30-154">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="21b30-154">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="21b30-155">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="21b30-155">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="21b30-156">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="21b30-156">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="21b30-157">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="21b30-157">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="21b30-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21b30-158">Requirements</span></span>



| <span data-ttu-id="21b30-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21b30-159">Requirement</span></span> | <span data-ttu-id="21b30-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="21b30-160">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="21b30-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21b30-161">Minimum supported client</span></span><br/> | <span data-ttu-id="21b30-162">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="21b30-162">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="21b30-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21b30-163">Minimum supported server</span></span><br/> | <span data-ttu-id="21b30-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21b30-164">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="21b30-165">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="21b30-165">Namespace</span></span><br/>                | <span data-ttu-id="21b30-166">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="21b30-166">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="21b30-167">MOF</span><span class="sxs-lookup"><span data-stu-id="21b30-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21b30-168"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21b30-168"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="21b30-169">DLL</span><span class="sxs-lookup"><span data-stu-id="21b30-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21b30-170"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21b30-170"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21b30-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21b30-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21b30-172">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="21b30-172">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

