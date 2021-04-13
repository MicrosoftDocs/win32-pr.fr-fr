---
title: Méthode UninstallLicenseKeyPack de la classe Win32_TSLicenseKeyPack
description: Désinstalle un jeu de clés de licence Services Bureau à distance.
ms.assetid: AF429AD7-C0DB-40AC-A4C6-591699FBF7E7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode UninstallLicenseKeyPack
- Services Bureau à distance de la méthode UninstallLicenseKeyPack, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode UninstallLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64754ea9ef2a32676b36821cf20c4f6871396415
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383955"
---
# <a name="uninstalllicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="e6adf-106">Méthode UninstallLicenseKeyPack de la \_ classe Win32 TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="e6adf-106">UninstallLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="e6adf-107">Désinstalle un jeu de clés de licence Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e6adf-107">Uninstalls a Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6adf-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6adf-108">Syntax</span></span>


```mof
uint32 UninstallLicenseKeyPack(
  [in] unit32 ProductVersion,
  [in] unit32 ProductType,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a><span data-ttu-id="e6adf-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6adf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6adf-110">*ProductVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6adf-110">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6adf-111">Identificateur de la version du produit pour le Services Bureau à distance le jeu de clés de licence.</span><span class="sxs-lookup"><span data-stu-id="e6adf-111">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="e6adf-112">0</span><span class="sxs-lookup"><span data-stu-id="e6adf-112">0</span></span>
</dt> <dd>

<span data-ttu-id="e6adf-113">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e6adf-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e6adf-114">1</span><span class="sxs-lookup"><span data-stu-id="e6adf-114">1</span></span>
</dt> <dd>

<span data-ttu-id="e6adf-115">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e6adf-115">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e6adf-116">2</span><span class="sxs-lookup"><span data-stu-id="e6adf-116">2</span></span>
</dt> <dd>

<span data-ttu-id="e6adf-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6adf-117">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e6adf-118">*ProductType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6adf-118">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6adf-119">Type de produit du jeu de clés de licence Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e6adf-119">Product type of the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="e6adf-120">0</span><span class="sxs-lookup"><span data-stu-id="e6adf-120">0</span></span>
</dt> <dd>

<span data-ttu-id="e6adf-121">Le type de produit du jeu de clés de licence Services Bureau à distance est par périphérique.</span><span class="sxs-lookup"><span data-stu-id="e6adf-121">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="e6adf-122">Par conséquent, chaque appareil qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence.</span><span class="sxs-lookup"><span data-stu-id="e6adf-122">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="e6adf-123">1</span><span class="sxs-lookup"><span data-stu-id="e6adf-123">1</span></span>
</dt> <dd>

<span data-ttu-id="e6adf-124">Le type de produit du jeu de clés de licence Services Bureau à distance est par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e6adf-124">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="e6adf-125">Par conséquent, chaque utilisateur qui se connecte au serveur hôte de session Bureau à distance doit disposer d’une licence.</span><span class="sxs-lookup"><span data-stu-id="e6adf-125">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="e6adf-126">2</span><span class="sxs-lookup"><span data-stu-id="e6adf-126">2</span></span>
</dt> <dd>

<span data-ttu-id="e6adf-127">Ce type de produit n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e6adf-127">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e6adf-128">*LicenseCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6adf-128">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6adf-129">Nombre de licences à désinstaller.</span><span class="sxs-lookup"><span data-stu-id="e6adf-129">The number of licenses to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6adf-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6adf-130">Return value</span></span>

<span data-ttu-id="e6adf-131">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="e6adf-131">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e6adf-132">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="e6adf-132">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e6adf-133">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e6adf-133">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6adf-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6adf-134">Requirements</span></span>



| <span data-ttu-id="e6adf-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6adf-135">Requirement</span></span> | <span data-ttu-id="e6adf-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6adf-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6adf-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6adf-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e6adf-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6adf-138">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e6adf-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6adf-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e6adf-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6adf-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e6adf-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e6adf-141">Namespace</span></span><br/>                | <span data-ttu-id="e6adf-142">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e6adf-142">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e6adf-143">MOF</span><span class="sxs-lookup"><span data-stu-id="e6adf-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6adf-144"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6adf-144"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6adf-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e6adf-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6adf-146"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6adf-146"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6adf-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6adf-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6adf-148">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="e6adf-148">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





