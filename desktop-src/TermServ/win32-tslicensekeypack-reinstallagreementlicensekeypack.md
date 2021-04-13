---
title: Méthode ReinstallAgreementLicenseKeyPack de la classe Win32_TSLicenseKeyPack
description: Réinstalle un jeu de clés de licence Services Bureau à distance acheté par le biais d’un contrat de licence et se connecte automatiquement via Internet pour valider la licence du Pack de clés.
ms.assetid: BC3C966B-E6CE-45E2-BC1D-2439B75D4C3C
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ReinstallAgreementLicenseKeyPack
- Services Bureau à distance de la méthode ReinstallAgreementLicenseKeyPack, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode ReinstallAgreementLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821ff6dc538a670e03757253b616ff16489dc108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508634"
---
# <a name="reinstallagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="82618-106">Méthode ReinstallAgreementLicenseKeyPack de la \_ classe Win32 TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="82618-106">ReinstallAgreementLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="82618-107">Réinstalle un jeu de clés de licence Services Bureau à distance acheté par le biais d’un contrat de licence et se connecte automatiquement via Internet pour valider la licence du Pack de clés.</span><span class="sxs-lookup"><span data-stu-id="82618-107">Reinstalls a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span>

## <a name="syntax"></a><span data-ttu-id="82618-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82618-108">Syntax</span></span>


```mof
uint32 ReinstallAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="82618-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82618-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82618-110">*AgreementType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82618-110">*AgreementType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82618-111">Type de contrat.</span><span class="sxs-lookup"><span data-stu-id="82618-111">Agreement type.</span></span>

<dt>

<span data-ttu-id="82618-112">0</span><span class="sxs-lookup"><span data-stu-id="82618-112">0</span></span>
</dt> <dd>

<span data-ttu-id="82618-113">Le jeu de clés de licence provient d’un contrat de licence en volume sélectionné (pour les clients disposant de 250 ordinateurs ou plus).</span><span class="sxs-lookup"><span data-stu-id="82618-113">The license key pack is from a Select volume license agreement (for customers with 250 or more computers).</span></span> <span data-ttu-id="82618-114">Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.</span><span class="sxs-lookup"><span data-stu-id="82618-114">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="82618-115">1</span><span class="sxs-lookup"><span data-stu-id="82618-115">1</span></span>
</dt> <dd>

<span data-ttu-id="82618-116">Le jeu de clés de licence provient d’un contrat de licence en volume entreprise pour les clients disposant de 250 ou plus d’ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="82618-116">The license key pack is from an Enterprise volume license agreement for customers with 250 or more computers.</span></span> <span data-ttu-id="82618-117">Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.</span><span class="sxs-lookup"><span data-stu-id="82618-117">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="82618-118">2</span><span class="sxs-lookup"><span data-stu-id="82618-118">2</span></span>
</dt> <dd>

<span data-ttu-id="82618-119">Le jeu de clés de licence provient d’un contrat de licence en volume campus pour un établissement d’enseignement supérieur.</span><span class="sxs-lookup"><span data-stu-id="82618-119">The license key pack is from a Campus volume license agreement for a higher education institution.</span></span> <span data-ttu-id="82618-120">Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.</span><span class="sxs-lookup"><span data-stu-id="82618-120">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="82618-121">3</span><span class="sxs-lookup"><span data-stu-id="82618-121">3</span></span>
</dt> <dd>

<span data-ttu-id="82618-122">Le jeu de clés de licence provient d’un contrat de licence en volume scolaire pour les institutions primaires et secondaires.</span><span class="sxs-lookup"><span data-stu-id="82618-122">The license key pack is from a School volume license agreement for primary and secondary institutions.</span></span> <span data-ttu-id="82618-123">Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.</span><span class="sxs-lookup"><span data-stu-id="82618-123">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="82618-124">4</span><span class="sxs-lookup"><span data-stu-id="82618-124">4</span></span>
</dt> <dd>

<span data-ttu-id="82618-125">Le jeu de clés de licence provient d’un contrat de licence de fournisseur de services pour les fournisseurs de services de licence pour les logiciels Microsoft sur une base mensuelle.</span><span class="sxs-lookup"><span data-stu-id="82618-125">The license key pack is from a Service Provider license agreement for service providers to license Microsoft software on a monthly basis.</span></span> <span data-ttu-id="82618-126">Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.</span><span class="sxs-lookup"><span data-stu-id="82618-126">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="82618-127">5</span><span class="sxs-lookup"><span data-stu-id="82618-127">5</span></span>
</dt> <dd>

<span data-ttu-id="82618-128">Le jeu de clés de licence provient d’un autre contrat de licence, par exemple Open Value, une licence Open sur plusieurs années et une licence Open Subscription.</span><span class="sxs-lookup"><span data-stu-id="82618-128">The license key pack is from another license agreement, such as Open Value, Multi-Year Open License, and Open Subscription License.</span></span> <span data-ttu-id="82618-129">Le paramètre *sAgreementNumber* est le numéro de contrat fourni avec les informations de votre programme.</span><span class="sxs-lookup"><span data-stu-id="82618-129">The *sAgreementNumber* parameter is the agreement number provided with your program information.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="82618-130">*sAgreementNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82618-130">*sAgreementNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82618-131">Numéro de contrat ou numéro d’inscription.</span><span class="sxs-lookup"><span data-stu-id="82618-131">Agreement number or enrollment number.</span></span> <span data-ttu-id="82618-132">Le paramètre *sAgreementNumber* est une chaîne numérique à sept chiffres sans trait d’Union.</span><span class="sxs-lookup"><span data-stu-id="82618-132">The *sAgreementNumber* parameter is a seven digit numeric string without hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="82618-133">*ProductVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82618-133">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82618-134">Version du produit.</span><span class="sxs-lookup"><span data-stu-id="82618-134">Product version.</span></span>

<dt>

<span data-ttu-id="82618-135">0</span><span class="sxs-lookup"><span data-stu-id="82618-135">0</span></span>
</dt> <dd>

<span data-ttu-id="82618-136">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="82618-136">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="82618-137">1</span><span class="sxs-lookup"><span data-stu-id="82618-137">1</span></span>
</dt> <dd>

<span data-ttu-id="82618-138">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="82618-138">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="82618-139">2</span><span class="sxs-lookup"><span data-stu-id="82618-139">2</span></span>
</dt> <dd>

<span data-ttu-id="82618-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82618-140">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="82618-141">*ProductType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82618-141">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82618-142">Type de produit.</span><span class="sxs-lookup"><span data-stu-id="82618-142">Product type.</span></span>

<dt>

<span data-ttu-id="82618-143">0</span><span class="sxs-lookup"><span data-stu-id="82618-143">0</span></span>
</dt> <dd>

<span data-ttu-id="82618-144">Le type de produit du jeu de clés de licence Services Bureau à distance est par périphérique.</span><span class="sxs-lookup"><span data-stu-id="82618-144">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="82618-145">Par conséquent, chaque appareil qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence.</span><span class="sxs-lookup"><span data-stu-id="82618-145">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="82618-146">1</span><span class="sxs-lookup"><span data-stu-id="82618-146">1</span></span>
</dt> <dd>

<span data-ttu-id="82618-147">Le type de produit du jeu de clés de licence Services Bureau à distance est par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="82618-147">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="82618-148">Par conséquent, chaque utilisateur qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence.</span><span class="sxs-lookup"><span data-stu-id="82618-148">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="82618-149">2</span><span class="sxs-lookup"><span data-stu-id="82618-149">2</span></span>
</dt> <dd>

<span data-ttu-id="82618-150">Ce type de produit n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="82618-150">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="82618-151">*LicenseCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82618-151">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82618-152">Nombre de licences à installer.</span><span class="sxs-lookup"><span data-stu-id="82618-152">Number of licenses to install.</span></span>

</dd> <dt>

<span data-ttu-id="82618-153">*KeyPackId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="82618-153">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82618-154">Reçoit l’identificateur du module de clé.</span><span class="sxs-lookup"><span data-stu-id="82618-154">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82618-155">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82618-155">Return value</span></span>

<span data-ttu-id="82618-156">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="82618-156">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="82618-157">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="82618-157">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="82618-158">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="82618-158">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="82618-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82618-159">Requirements</span></span>



| <span data-ttu-id="82618-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82618-160">Requirement</span></span> | <span data-ttu-id="82618-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="82618-161">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="82618-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82618-162">Minimum supported client</span></span><br/> | <span data-ttu-id="82618-163">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="82618-163">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="82618-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82618-164">Minimum supported server</span></span><br/> | <span data-ttu-id="82618-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82618-165">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="82618-166">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="82618-166">Namespace</span></span><br/>                | <span data-ttu-id="82618-167">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="82618-167">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="82618-168">MOF</span><span class="sxs-lookup"><span data-stu-id="82618-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82618-169"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82618-169"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="82618-170">DLL</span><span class="sxs-lookup"><span data-stu-id="82618-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82618-171"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82618-171"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82618-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82618-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82618-173">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="82618-173">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





