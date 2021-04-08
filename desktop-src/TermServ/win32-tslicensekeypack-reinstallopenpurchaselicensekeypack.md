---
title: Méthode ReinstallOpenPurchaseLicenseKeyPack de la classe Win32_TSLicenseKeyPack
description: Réinstalle un jeu de clés de licence Open License Services Bureau à distance.
ms.assetid: 3E70711E-284A-466E-A733-1219F5E0B741
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ReinstallOpenPurchaseLicenseKeyPack
- Services Bureau à distance de la méthode ReinstallOpenPurchaseLicenseKeyPack, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode ReinstallOpenPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1eae765b74feed98760ef30c2b89a1090c4200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743269"
---
# <a name="reinstallopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="02070-106">Méthode ReinstallOpenPurchaseLicenseKeyPack de la \_ classe Win32 TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="02070-106">ReinstallOpenPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="02070-107">Réinstalle un jeu de clés de licence Open License Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="02070-107">Reinstalls an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="02070-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02070-108">Syntax</span></span>


```mof
uint32 ReinstallOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="02070-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02070-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02070-110">*sLicenseNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02070-110">*sLicenseNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02070-111">chaîne numérique de 8 caractères fournie avec le jeu de clés de licence.</span><span class="sxs-lookup"><span data-stu-id="02070-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="02070-112">Le paramètre *sLicenseNumber* ne peut pas contenir de traits d’Union.</span><span class="sxs-lookup"><span data-stu-id="02070-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="02070-113">*sAuthorizationNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02070-113">*sAuthorizationNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02070-114">chaîne alphanumérique de 15 caractères fournie avec la clé de licence.</span><span class="sxs-lookup"><span data-stu-id="02070-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="02070-115">Le paramètre *sAuthorizationNumber* ne peut pas contenir de traits d’Union.</span><span class="sxs-lookup"><span data-stu-id="02070-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="02070-116">*ProductVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02070-116">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02070-117">Version du produit.</span><span class="sxs-lookup"><span data-stu-id="02070-117">Product version.</span></span>

<dt>

<span data-ttu-id="02070-118">0</span><span class="sxs-lookup"><span data-stu-id="02070-118">0</span></span>
</dt> <dd>

<span data-ttu-id="02070-119">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="02070-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="02070-120">1</span><span class="sxs-lookup"><span data-stu-id="02070-120">1</span></span>
</dt> <dd>

<span data-ttu-id="02070-121">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="02070-121">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="02070-122">2</span><span class="sxs-lookup"><span data-stu-id="02070-122">2</span></span>
</dt> <dd>

<span data-ttu-id="02070-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02070-123">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="02070-124">*ProductType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02070-124">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02070-125">Type de produit.</span><span class="sxs-lookup"><span data-stu-id="02070-125">Product type.</span></span>

<dt>

<span data-ttu-id="02070-126">0</span><span class="sxs-lookup"><span data-stu-id="02070-126">0</span></span>
</dt> <dd>

<span data-ttu-id="02070-127">Le type de produit du jeu de clés de licence Services Bureau à distance est par périphérique.</span><span class="sxs-lookup"><span data-stu-id="02070-127">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="02070-128">Par conséquent, chaque appareil qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence.</span><span class="sxs-lookup"><span data-stu-id="02070-128">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="02070-129">1</span><span class="sxs-lookup"><span data-stu-id="02070-129">1</span></span>
</dt> <dd>

<span data-ttu-id="02070-130">Le type de produit du jeu de clés de licence Services Bureau à distance est par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="02070-130">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="02070-131">Par conséquent, chaque utilisateur qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence.</span><span class="sxs-lookup"><span data-stu-id="02070-131">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="02070-132">2</span><span class="sxs-lookup"><span data-stu-id="02070-132">2</span></span>
</dt> <dd>

<span data-ttu-id="02070-133">Ce type de produit n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="02070-133">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="02070-134">*LicenseCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02070-134">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02070-135">Nombre de licences à installer.</span><span class="sxs-lookup"><span data-stu-id="02070-135">The number of licenses to install.</span></span>

</dd> <dt>

<span data-ttu-id="02070-136">*KeyPackId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="02070-136">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02070-137">Reçoit l’identificateur du module de clé.</span><span class="sxs-lookup"><span data-stu-id="02070-137">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02070-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02070-138">Return value</span></span>

<span data-ttu-id="02070-139">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="02070-139">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="02070-140">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="02070-140">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="02070-141">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="02070-141">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02070-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02070-142">Requirements</span></span>



| <span data-ttu-id="02070-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02070-143">Requirement</span></span> | <span data-ttu-id="02070-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="02070-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="02070-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02070-145">Minimum supported client</span></span><br/> | <span data-ttu-id="02070-146">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="02070-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="02070-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02070-147">Minimum supported server</span></span><br/> | <span data-ttu-id="02070-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02070-148">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="02070-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="02070-149">Namespace</span></span><br/>                | <span data-ttu-id="02070-150">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="02070-150">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="02070-151">MOF</span><span class="sxs-lookup"><span data-stu-id="02070-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02070-152"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02070-152"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="02070-153">DLL</span><span class="sxs-lookup"><span data-stu-id="02070-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02070-154"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02070-154"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02070-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02070-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02070-156">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="02070-156">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





