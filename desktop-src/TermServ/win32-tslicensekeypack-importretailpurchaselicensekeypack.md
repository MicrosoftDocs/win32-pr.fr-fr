---
title: Méthode ImportRetailPurchaseLicenseKeyPack de la classe Win32_TSLicenseKeyPack
description: Importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Services Bureau à distance acheté par le biais d’un canal de vente au détail.
ms.assetid: B45C3263-216E-4284-89A1-BE2ADE3A8E84
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ImportRetailPurchaseLicenseKeyPack
- Services Bureau à distance de la méthode ImportRetailPurchaseLicenseKeyPack, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode ImportRetailPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2699d1f96827f9ace0f111a4c95adb64d5f8467e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741765"
---
# <a name="importretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="59226-106">Méthode ImportRetailPurchaseLicenseKeyPack de la \_ classe Win32 TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="59226-106">ImportRetailPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="59226-107">Importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Services Bureau à distance acheté par le biais d’un canal de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="59226-107">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="59226-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59226-108">Syntax</span></span>


```mof
uint32 ImportRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="59226-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59226-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59226-110">*sLicenseCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59226-110">*sLicenseCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59226-111">Contient le code de licence de 25 caractères.</span><span class="sxs-lookup"><span data-stu-id="59226-111">Contains the 25-character license code.</span></span> <span data-ttu-id="59226-112">Seule la chaîne de caractères alphanumériques de 25 caractères doit être indiquée comme entrée.</span><span class="sxs-lookup"><span data-stu-id="59226-112">Only the 25-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="59226-113">Aucun trait d’Union ne doit être ajouté.</span><span class="sxs-lookup"><span data-stu-id="59226-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="59226-114">*sSourceLSName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59226-114">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59226-115">Nom du serveur de licences Bureau à distance source.</span><span class="sxs-lookup"><span data-stu-id="59226-115">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="59226-116">Il s’agit du nom unique complet ou de l’adresse IP du serveur.</span><span class="sxs-lookup"><span data-stu-id="59226-116">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="59226-117">*sSourceLSProductId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59226-117">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59226-118">Identificateur du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="59226-118">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="59226-119">Est une chaîne alphanumérique de 35 caractères qui ne peut pas contenir de traits d’Union.</span><span class="sxs-lookup"><span data-stu-id="59226-119">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="59226-120">*KeyPackId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="59226-120">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59226-121">Reçoit l’identificateur du module de clé.</span><span class="sxs-lookup"><span data-stu-id="59226-121">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59226-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59226-122">Return value</span></span>

<span data-ttu-id="59226-123">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="59226-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="59226-124">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="59226-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="59226-125">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="59226-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="59226-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59226-126">Requirements</span></span>



| <span data-ttu-id="59226-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59226-127">Requirement</span></span> | <span data-ttu-id="59226-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="59226-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="59226-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59226-129">Minimum supported client</span></span><br/> | <span data-ttu-id="59226-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="59226-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="59226-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59226-131">Minimum supported server</span></span><br/> | <span data-ttu-id="59226-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59226-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="59226-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="59226-133">Namespace</span></span><br/>                | <span data-ttu-id="59226-134">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="59226-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="59226-135">MOF</span><span class="sxs-lookup"><span data-stu-id="59226-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59226-136"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59226-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="59226-137">DLL</span><span class="sxs-lookup"><span data-stu-id="59226-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59226-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59226-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59226-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59226-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59226-140">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="59226-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





