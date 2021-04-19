---
title: Méthode ImportOpenPurchaseLicenseKeyPack de la classe Win32_TSLicenseKeyPack
description: Importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Open License Services Bureau à distance.
ms.assetid: FE1923FF-5292-4080-AB51-88B8A6B2322C
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ImportOpenPurchaseLicenseKeyPack
- Services Bureau à distance de la méthode ImportOpenPurchaseLicenseKeyPack, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode ImportOpenPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 944bb1ce63150caece2cbc247af24542fde2d4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509945"
---
# <a name="importopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="9c02b-106">Méthode ImportOpenPurchaseLicenseKeyPack de la \_ classe Win32 TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="9c02b-106">ImportOpenPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="9c02b-107">Importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Open License Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="9c02b-107">Imports, from another Remote Desktop license server, an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c02b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c02b-108">Syntax</span></span>


```mof
uint32 ImportOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="9c02b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c02b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c02b-110">*sLicenseNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c02b-110">*sLicenseNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c02b-111">chaîne numérique de 8 caractères fournie avec le jeu de clés de licence.</span><span class="sxs-lookup"><span data-stu-id="9c02b-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="9c02b-112">Le paramètre *sLicenseNumber* ne peut pas contenir de traits d’Union.</span><span class="sxs-lookup"><span data-stu-id="9c02b-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="9c02b-113">*sAuthorizationNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c02b-113">*sAuthorizationNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c02b-114">chaîne alphanumérique de 15 caractères fournie avec la clé de licence.</span><span class="sxs-lookup"><span data-stu-id="9c02b-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="9c02b-115">Le paramètre *sAuthorizationNumber* ne peut pas contenir de traits d’Union.</span><span class="sxs-lookup"><span data-stu-id="9c02b-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="9c02b-116">*ProductVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c02b-116">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c02b-117">Version du produit.</span><span class="sxs-lookup"><span data-stu-id="9c02b-117">Product version.</span></span>

<dt>

<span data-ttu-id="9c02b-118">0</span><span class="sxs-lookup"><span data-stu-id="9c02b-118">0</span></span>
</dt> <dd>

<span data-ttu-id="9c02b-119">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9c02b-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9c02b-120">1</span><span class="sxs-lookup"><span data-stu-id="9c02b-120">1</span></span>
</dt> <dd>

<span data-ttu-id="9c02b-121">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9c02b-121">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9c02b-122">2</span><span class="sxs-lookup"><span data-stu-id="9c02b-122">2</span></span>
</dt> <dd>

<span data-ttu-id="9c02b-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c02b-123">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9c02b-124">*ProductType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c02b-124">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c02b-125">Type de produit.</span><span class="sxs-lookup"><span data-stu-id="9c02b-125">Product type.</span></span>

<dt>

<span data-ttu-id="9c02b-126">0</span><span class="sxs-lookup"><span data-stu-id="9c02b-126">0</span></span>
</dt> <dd>

<span data-ttu-id="9c02b-127">Le type de produit du jeu de clés de licence Services Bureau à distance est par périphérique.</span><span class="sxs-lookup"><span data-stu-id="9c02b-127">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="9c02b-128">Par conséquent, chaque appareil qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence.</span><span class="sxs-lookup"><span data-stu-id="9c02b-128">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="9c02b-129">1</span><span class="sxs-lookup"><span data-stu-id="9c02b-129">1</span></span>
</dt> <dd>

<span data-ttu-id="9c02b-130">Le type de produit du jeu de clés de licence Services Bureau à distance est par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9c02b-130">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="9c02b-131">Par conséquent, chaque utilisateur qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence.</span><span class="sxs-lookup"><span data-stu-id="9c02b-131">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="9c02b-132">2</span><span class="sxs-lookup"><span data-stu-id="9c02b-132">2</span></span>
</dt> <dd>

<span data-ttu-id="9c02b-133">Ce type de produit n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9c02b-133">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9c02b-134">*LicenseCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c02b-134">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c02b-135">Nombre de licences à importer</span><span class="sxs-lookup"><span data-stu-id="9c02b-135">The number of licenses to import</span></span>

</dd> <dt>

<span data-ttu-id="9c02b-136">*sSourceLSName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c02b-136">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c02b-137">Nom du serveur de licences Bureau à distance source.</span><span class="sxs-lookup"><span data-stu-id="9c02b-137">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="9c02b-138">Il s’agit du nom unique complet ou de l’adresse IP du serveur.</span><span class="sxs-lookup"><span data-stu-id="9c02b-138">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="9c02b-139">*sSourceLSProductId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c02b-139">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c02b-140">Identificateur du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="9c02b-140">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="9c02b-141">Est une chaîne alphanumérique de 35 caractères qui ne peut pas contenir de traits d’Union.</span><span class="sxs-lookup"><span data-stu-id="9c02b-141">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="9c02b-142">*KeyPackId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9c02b-142">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c02b-143">Reçoit l’identificateur du module de clé.</span><span class="sxs-lookup"><span data-stu-id="9c02b-143">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c02b-144">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9c02b-144">Return value</span></span>

<span data-ttu-id="9c02b-145">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="9c02b-145">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9c02b-146">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="9c02b-146">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9c02b-147">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9c02b-147">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c02b-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c02b-148">Requirements</span></span>



| <span data-ttu-id="9c02b-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c02b-149">Requirement</span></span> | <span data-ttu-id="9c02b-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c02b-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c02b-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c02b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="9c02b-152">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c02b-152">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="9c02b-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c02b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="9c02b-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c02b-154">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="9c02b-155">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9c02b-155">Namespace</span></span><br/>                | <span data-ttu-id="9c02b-156">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="9c02b-156">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="9c02b-157">MOF</span><span class="sxs-lookup"><span data-stu-id="9c02b-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c02b-158"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c02b-158"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c02b-159">DLL</span><span class="sxs-lookup"><span data-stu-id="9c02b-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c02b-160"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c02b-160"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c02b-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c02b-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c02b-162">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="9c02b-162">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





