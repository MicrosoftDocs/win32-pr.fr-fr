---
title: Méthode ImportAgreementLicenseKeyPack de la classe Win32_TSLicenseKeyPack
description: Les importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Services Bureau à distance acheté par le biais d’un contrat de licence et se connecte automatiquement via Internet pour valider la licence du Pack de clés.
ms.assetid: 3C29E691-3734-4D39-A89F-F381F285DC9E
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ImportAgreementLicenseKeyPack
- Services Bureau à distance de la méthode ImportAgreementLicenseKeyPack, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode ImportAgreementLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff61d022f9cf195eb357817f7733f4ec49e2986f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106075"
---
# <a name="importagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="710c4-106">Méthode ImportAgreementLicenseKeyPack de la \_ classe Win32 TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="710c4-106">ImportAgreementLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="710c4-107">Les importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Services Bureau à distance acheté par le biais d’un contrat de licence et se connecte automatiquement via Internet pour valider la licence du Pack de clés.</span><span class="sxs-lookup"><span data-stu-id="710c4-107">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span>

## <a name="syntax"></a><span data-ttu-id="710c4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="710c4-108">Syntax</span></span>


```mof
uint32 ImportAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="710c4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="710c4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="710c4-110">*AgreementType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="710c4-110">*AgreementType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="710c4-111">Type de contrat.</span><span class="sxs-lookup"><span data-stu-id="710c4-111">Agreement type.</span></span>

<dt>

<span data-ttu-id="710c4-112">0</span><span class="sxs-lookup"><span data-stu-id="710c4-112">0</span></span>
</dt> <dd>

<span data-ttu-id="710c4-113">Le jeu de clés de licence provient d’un contrat de licence en volume sélectionné (pour les clients disposant de 250 ordinateurs ou plus).</span><span class="sxs-lookup"><span data-stu-id="710c4-113">The license key pack is from a Select volume license agreement (for customers with 250 or more computers).</span></span> <span data-ttu-id="710c4-114">Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.</span><span class="sxs-lookup"><span data-stu-id="710c4-114">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="710c4-115">1</span><span class="sxs-lookup"><span data-stu-id="710c4-115">1</span></span>
</dt> <dd>

<span data-ttu-id="710c4-116">Le jeu de clés de licence provient d’un contrat de licence en volume entreprise pour les clients disposant de 250 ou plus d’ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="710c4-116">The license key pack is from an Enterprise volume license agreement for customers with 250 or more computers.</span></span> <span data-ttu-id="710c4-117">Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.</span><span class="sxs-lookup"><span data-stu-id="710c4-117">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="710c4-118">2</span><span class="sxs-lookup"><span data-stu-id="710c4-118">2</span></span>
</dt> <dd>

<span data-ttu-id="710c4-119">Le jeu de clés de licence provient d’un contrat de licence en volume campus pour un établissement d’enseignement supérieur.</span><span class="sxs-lookup"><span data-stu-id="710c4-119">The license key pack is from a Campus volume license agreement for a higher education institution.</span></span> <span data-ttu-id="710c4-120">Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.</span><span class="sxs-lookup"><span data-stu-id="710c4-120">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="710c4-121">3</span><span class="sxs-lookup"><span data-stu-id="710c4-121">3</span></span>
</dt> <dd>

<span data-ttu-id="710c4-122">Le jeu de clés de licence provient d’un contrat de licence en volume scolaire pour les institutions primaires et secondaires.</span><span class="sxs-lookup"><span data-stu-id="710c4-122">The license key pack is from a School volume license agreement for primary and secondary institutions.</span></span> <span data-ttu-id="710c4-123">Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.</span><span class="sxs-lookup"><span data-stu-id="710c4-123">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="710c4-124">4</span><span class="sxs-lookup"><span data-stu-id="710c4-124">4</span></span>
</dt> <dd>

<span data-ttu-id="710c4-125">Le jeu de clés de licence provient d’un contrat de licence de fournisseur de services pour les fournisseurs de services de licence pour les logiciels Microsoft sur une base mensuelle.</span><span class="sxs-lookup"><span data-stu-id="710c4-125">The license key pack is from a Service Provider license agreement for service providers to license Microsoft software on a monthly basis.</span></span> <span data-ttu-id="710c4-126">Le paramètre *sAgreementNumber* est le numéro d’inscription (sept chiffres numériques) trouvé dans le formulaire d’accord signé.</span><span class="sxs-lookup"><span data-stu-id="710c4-126">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="710c4-127">5</span><span class="sxs-lookup"><span data-stu-id="710c4-127">5</span></span>
</dt> <dd>

<span data-ttu-id="710c4-128">Le jeu de clés de licence provient d’un autre contrat de licence, par exemple Open Value, une licence Open sur plusieurs années et une licence Open Subscription.</span><span class="sxs-lookup"><span data-stu-id="710c4-128">The license key pack is from another license agreement, such as Open Value, Multi-Year Open License, and Open Subscription License.</span></span> <span data-ttu-id="710c4-129">Le paramètre *sAgreementNumber* est le numéro de contrat fourni avec les informations de votre programme.</span><span class="sxs-lookup"><span data-stu-id="710c4-129">The *sAgreementNumber* parameter is the agreement number provided with your program information.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="710c4-130">*sAgreementNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="710c4-130">*sAgreementNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="710c4-131">Numéro de contrat ou numéro d’inscription.</span><span class="sxs-lookup"><span data-stu-id="710c4-131">Agreement number or enrollment number.</span></span> <span data-ttu-id="710c4-132">Le paramètre *sAgreementNumber* est une chaîne numérique à sept chiffres sans trait d’Union.</span><span class="sxs-lookup"><span data-stu-id="710c4-132">The *sAgreementNumber* parameter is a seven digit numeric string without hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="710c4-133">*ProductVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="710c4-133">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="710c4-134">Version du produit.</span><span class="sxs-lookup"><span data-stu-id="710c4-134">Product version.</span></span>

<dt>

<span data-ttu-id="710c4-135">0</span><span class="sxs-lookup"><span data-stu-id="710c4-135">0</span></span>
</dt> <dd>

<span data-ttu-id="710c4-136">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="710c4-136">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="710c4-137">1</span><span class="sxs-lookup"><span data-stu-id="710c4-137">1</span></span>
</dt> <dd>

<span data-ttu-id="710c4-138">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="710c4-138">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="710c4-139">2</span><span class="sxs-lookup"><span data-stu-id="710c4-139">2</span></span>
</dt> <dd>

<span data-ttu-id="710c4-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="710c4-140">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="710c4-141">*ProductType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="710c4-141">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="710c4-142">Type de produit.</span><span class="sxs-lookup"><span data-stu-id="710c4-142">Product type.</span></span>

<dt>

<span data-ttu-id="710c4-143">0</span><span class="sxs-lookup"><span data-stu-id="710c4-143">0</span></span>
</dt> <dd>

<span data-ttu-id="710c4-144">Le type de produit du jeu de clés de licence Services Bureau à distance est par périphérique.</span><span class="sxs-lookup"><span data-stu-id="710c4-144">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="710c4-145">Par conséquent, chaque appareil qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence.</span><span class="sxs-lookup"><span data-stu-id="710c4-145">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="710c4-146">1</span><span class="sxs-lookup"><span data-stu-id="710c4-146">1</span></span>
</dt> <dd>

<span data-ttu-id="710c4-147">Le type de produit du jeu de clés de licence Services Bureau à distance est par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="710c4-147">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="710c4-148">Par conséquent, chaque utilisateur qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence.</span><span class="sxs-lookup"><span data-stu-id="710c4-148">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="710c4-149">2</span><span class="sxs-lookup"><span data-stu-id="710c4-149">2</span></span>
</dt> <dd>

<span data-ttu-id="710c4-150">Ce type de produit n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="710c4-150">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="710c4-151">*LicenseCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="710c4-151">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="710c4-152">Nombre de licences à importer.</span><span class="sxs-lookup"><span data-stu-id="710c4-152">Number of licenses to import.</span></span>

</dd> <dt>

<span data-ttu-id="710c4-153">*sSourceLSName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="710c4-153">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="710c4-154">Nom du serveur de licences Bureau à distance source.</span><span class="sxs-lookup"><span data-stu-id="710c4-154">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="710c4-155">Il s’agit du nom unique complet ou de l’adresse IP du serveur.</span><span class="sxs-lookup"><span data-stu-id="710c4-155">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="710c4-156">*sSourceLSProductId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="710c4-156">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="710c4-157">Identificateur du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="710c4-157">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="710c4-158">Est une chaîne alphanumérique de 35 caractères qui ne peut pas contenir de traits d’Union.</span><span class="sxs-lookup"><span data-stu-id="710c4-158">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="710c4-159">*KeyPackId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="710c4-159">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="710c4-160">Reçoit l’identificateur du module de clé.</span><span class="sxs-lookup"><span data-stu-id="710c4-160">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="710c4-161">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="710c4-161">Return value</span></span>

<span data-ttu-id="710c4-162">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="710c4-162">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="710c4-163">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="710c4-163">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="710c4-164">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="710c4-164">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="710c4-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="710c4-165">Requirements</span></span>



| <span data-ttu-id="710c4-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="710c4-166">Requirement</span></span> | <span data-ttu-id="710c4-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="710c4-167">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="710c4-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="710c4-168">Minimum supported client</span></span><br/> | <span data-ttu-id="710c4-169">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="710c4-169">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="710c4-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="710c4-170">Minimum supported server</span></span><br/> | <span data-ttu-id="710c4-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="710c4-171">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="710c4-172">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="710c4-172">Namespace</span></span><br/>                | <span data-ttu-id="710c4-173">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="710c4-173">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="710c4-174">MOF</span><span class="sxs-lookup"><span data-stu-id="710c4-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="710c4-175"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="710c4-175"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="710c4-176">DLL</span><span class="sxs-lookup"><span data-stu-id="710c4-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="710c4-177"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="710c4-177"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="710c4-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="710c4-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="710c4-179">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="710c4-179">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





