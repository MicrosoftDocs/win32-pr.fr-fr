---
title: Méthode InstallAgreementLicenseKeyPack de la classe Win32_TSLicenseKeyPack
description: Installe un jeu de clés de licence Services Bureau à distance acheté par le biais d’un contrat de licence et se connecte automatiquement via Internet pour valider la licence du Pack de clés.
ms.assetid: 70a0aac3-2709-47ba-bf6a-549393c4c115
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode InstallAgreementLicenseKeyPack
- Services Bureau à distance de la méthode InstallAgreementLicenseKeyPack, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode InstallAgreementLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb891469feae169c1267c12c04af6d21415c309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510573"
---
# <a name="installagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="3c198-106">Méthode InstallAgreementLicenseKeyPack de la \_ classe Win32 TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="3c198-106">InstallAgreementLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="3c198-107">Installe un jeu de clés de licence Services Bureau à distance acheté par le biais d’un contrat de licence et se connecte automatiquement via Internet pour valider la licence du Pack de clés.</span><span class="sxs-lookup"><span data-stu-id="3c198-107">Installs a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c198-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c198-108">Syntax</span></span>


```mof
uint32 InstallAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a><span data-ttu-id="3c198-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c198-109">Parameters</span></span>

<span data-ttu-id="3c198-110">*AgreementType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c198-110">*AgreementType* \[in\]</span></span>

<span data-ttu-id="3c198-111">Type de contrat.</span><span class="sxs-lookup"><span data-stu-id="3c198-111">Agreement type.</span></span>

| <span data-ttu-id="3c198-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c198-112">Value</span></span> | <span data-ttu-id="3c198-113">Description</span><span class="sxs-lookup"><span data-stu-id="3c198-113">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="3c198-114">0</span><span class="sxs-lookup"><span data-stu-id="3c198-114">0</span></span> | <span data-ttu-id="3c198-115">Le jeu de clés de licence provient d’un contrat de licence en volume sélectionné (pour les clients disposant de 250 ordinateurs ou plus).</span><span class="sxs-lookup"><span data-stu-id="3c198-115">The license key pack is from a Select volume license agreement (for customers with 250 or more computers).</span></span> <span data-ttu-id="3c198-116">Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.</span><span class="sxs-lookup"><span data-stu-id="3c198-116">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="3c198-117">1</span><span class="sxs-lookup"><span data-stu-id="3c198-117">1</span></span> | <span data-ttu-id="3c198-118">Le jeu de clés de licence provient d’un contrat de licence en volume entreprise pour les clients disposant de 250 ou plus d’ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="3c198-118">The license key pack is from an Enterprise volume license agreement for customers with 250 or more computers.</span></span> <span data-ttu-id="3c198-119">Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.</span><span class="sxs-lookup"><span data-stu-id="3c198-119">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="3c198-120">2</span><span class="sxs-lookup"><span data-stu-id="3c198-120">2</span></span> | <span data-ttu-id="3c198-121">Le jeu de clés de licence provient d’un contrat de licence en volume campus pour un établissement d’enseignement supérieur.</span><span class="sxs-lookup"><span data-stu-id="3c198-121">The license key pack is from a Campus volume license agreement for a higher education institution.</span></span> <span data-ttu-id="3c198-122">Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.</span><span class="sxs-lookup"><span data-stu-id="3c198-122">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="3c198-123">3</span><span class="sxs-lookup"><span data-stu-id="3c198-123">3</span></span> | <span data-ttu-id="3c198-124">Le jeu de clés de licence provient d’un contrat de licence en volume scolaire pour les institutions primaires et secondaires.</span><span class="sxs-lookup"><span data-stu-id="3c198-124">The license key pack is from a School volume license agreement for primary and secondary institutions.</span></span> <span data-ttu-id="3c198-125">Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.</span><span class="sxs-lookup"><span data-stu-id="3c198-125">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="3c198-126">4</span><span class="sxs-lookup"><span data-stu-id="3c198-126">4</span></span> | <span data-ttu-id="3c198-127">Le jeu de clés de licence provient d’un contrat de licence de fournisseur de services pour les fournisseurs de services de licence pour les logiciels Microsoft sur une base mensuelle.</span><span class="sxs-lookup"><span data-stu-id="3c198-127">The license key pack is from a Service Provider license agreement for service providers to license Microsoft software on a monthly basis.</span></span> <span data-ttu-id="3c198-128">Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.</span><span class="sxs-lookup"><span data-stu-id="3c198-128">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="3c198-129">5</span><span class="sxs-lookup"><span data-stu-id="3c198-129">5</span></span> | <span data-ttu-id="3c198-130">Le jeu de clés de licence provient d’un autre contrat de licence, par exemple Open Value, une licence Open sur plusieurs années et une licence Open Subscription.</span><span class="sxs-lookup"><span data-stu-id="3c198-130">The license key pack is from another license agreement, such as Open Value, Multi-Year Open License, and Open Subscription License.</span></span> <span data-ttu-id="3c198-131">Le paramètre *sAgreementNumber* est le numéro de contrat fourni avec les informations de votre programme.</span><span class="sxs-lookup"><span data-stu-id="3c198-131">The *sAgreementNumber* parameter is the agreement number provided with your program information.</span></span> |

<span data-ttu-id="3c198-132">*sAgreementNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c198-132">*sAgreementNumber* \[in\]</span></span>

<span data-ttu-id="3c198-133">Numéro de contrat ou numéro d’inscription.</span><span class="sxs-lookup"><span data-stu-id="3c198-133">Agreement number or enrollment number.</span></span> <span data-ttu-id="3c198-134">Le paramètre *sAgreementNumber* est une chaîne numérique à sept chiffres sans trait d’Union.</span><span class="sxs-lookup"><span data-stu-id="3c198-134">The *sAgreementNumber* parameter is a seven digit numeric string without hyphens.</span></span>

<span data-ttu-id="3c198-135">*ProductVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c198-135">*ProductVersion* \[in\]</span></span>

<span data-ttu-id="3c198-136">Version du produit.</span><span class="sxs-lookup"><span data-stu-id="3c198-136">Product version.</span></span>

| <span data-ttu-id="3c198-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c198-137">Value</span></span> | <span data-ttu-id="3c198-138">Description</span><span class="sxs-lookup"><span data-stu-id="3c198-138">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="3c198-139">0</span><span class="sxs-lookup"><span data-stu-id="3c198-139">0</span></span> | <span data-ttu-id="3c198-140">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c198-140">Not supported</span></span> |
| <span data-ttu-id="3c198-141">1</span><span class="sxs-lookup"><span data-stu-id="3c198-141">1</span></span> | <span data-ttu-id="3c198-142">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c198-142">Not supported</span></span> |
| <span data-ttu-id="3c198-143">2</span><span class="sxs-lookup"><span data-stu-id="3c198-143">2</span></span> | <span data-ttu-id="3c198-144">Windows Server 2008/Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3c198-144">Windows Server 2008/Windows Server 2008 R2</span></span> |
| <span data-ttu-id="3c198-145">4</span><span class="sxs-lookup"><span data-stu-id="3c198-145">4</span></span> | <span data-ttu-id="3c198-146">Windows Server 2012/Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3c198-146">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="3c198-147">5</span><span class="sxs-lookup"><span data-stu-id="3c198-147">5</span></span> | <span data-ttu-id="3c198-148">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3c198-148">Windows Server 2016</span></span> |
| <span data-ttu-id="3c198-149">6</span><span class="sxs-lookup"><span data-stu-id="3c198-149">6</span></span> | <span data-ttu-id="3c198-150">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="3c198-150">Windows Server 2019</span></span> |

<span data-ttu-id="3c198-151">*ProductType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c198-151">*ProductType* \[in\]</span></span>

<span data-ttu-id="3c198-152">Type de produit.</span><span class="sxs-lookup"><span data-stu-id="3c198-152">Product type.</span></span>

| <span data-ttu-id="3c198-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c198-153">Value</span></span> | <span data-ttu-id="3c198-154">Description</span><span class="sxs-lookup"><span data-stu-id="3c198-154">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="3c198-155">0</span><span class="sxs-lookup"><span data-stu-id="3c198-155">0</span></span> | <span data-ttu-id="3c198-156">Le type de produit du jeu de clés de licence Services Bureau à distance est par périphérique.</span><span class="sxs-lookup"><span data-stu-id="3c198-156">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="3c198-157">Par conséquent, chaque appareil qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence.</span><span class="sxs-lookup"><span data-stu-id="3c198-157">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="3c198-158">1</span><span class="sxs-lookup"><span data-stu-id="3c198-158">1</span></span> | <span data-ttu-id="3c198-159">Le type de produit du jeu de clés de licence Services Bureau à distance est par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3c198-159">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="3c198-160">Par conséquent, chaque utilisateur qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence.</span><span class="sxs-lookup"><span data-stu-id="3c198-160">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="3c198-161">2</span><span class="sxs-lookup"><span data-stu-id="3c198-161">2</span></span> | <span data-ttu-id="3c198-162">Ce type de produit n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3c198-162">This product type is not valid.</span></span> |

<span data-ttu-id="3c198-163">*LicenseCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c198-163">*LicenseCount* \[in\]</span></span>

<span data-ttu-id="3c198-164">Nombre de licences à installer.</span><span class="sxs-lookup"><span data-stu-id="3c198-164">Number of licenses to install.</span></span>

<span data-ttu-id="3c198-165">*KeyPackId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3c198-165">*KeyPackId* \[out\]</span></span>

<span data-ttu-id="3c198-166">Reçoit l’identificateur du module de clé.</span><span class="sxs-lookup"><span data-stu-id="3c198-166">Receives the key pack identifier.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c198-167">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c198-167">Return value</span></span>

<span data-ttu-id="3c198-168">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="3c198-168">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3c198-169">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="3c198-169">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3c198-170">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3c198-170">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3c198-171">Notes</span><span class="sxs-lookup"><span data-stu-id="3c198-171">Remarks</span></span>

<span data-ttu-id="3c198-172">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3c198-172">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="3c198-173">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="3c198-173">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3c198-174">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3c198-174">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3c198-175">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="3c198-175">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3c198-176">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3c198-176">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c198-177">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c198-177">Requirements</span></span>

| <span data-ttu-id="3c198-178">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c198-178">Requirement</span></span> | <span data-ttu-id="3c198-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c198-179">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c198-180">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c198-180">Minimum supported client</span></span><br/> | <span data-ttu-id="3c198-181">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c198-181">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="3c198-182">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c198-182">Minimum supported server</span></span><br/> | <span data-ttu-id="3c198-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c198-183">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="3c198-184">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3c198-184">Namespace</span></span><br/>                | <span data-ttu-id="3c198-185">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="3c198-185">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="3c198-186">MOF</span><span class="sxs-lookup"><span data-stu-id="3c198-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c198-187"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c198-187"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c198-188">DLL</span><span class="sxs-lookup"><span data-stu-id="3c198-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c198-189"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c198-189"><dt>TlsWmiProv.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="3c198-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c198-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c198-191">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="3c198-191">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

