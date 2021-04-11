---
title: Méthode ReinstallRetailPurchaseLicenseKeyPack de la classe Win32_TSLicenseKeyPack
description: Réinstalle un jeu de clés de licence Services Bureau à distance acheté par le biais d’un canal de vente au détail.
ms.assetid: 19528726-8DEB-4D03-BFA6-647C8A612FA2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ReinstallRetailPurchaseLicenseKeyPack
- Services Bureau à distance de la méthode ReinstallRetailPurchaseLicenseKeyPack, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode ReinstallRetailPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4caa8635eaf28ad823add500883832a7fe885b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032451"
---
# <a name="reinstallretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="2c4f1-106">Méthode ReinstallRetailPurchaseLicenseKeyPack de la \_ classe Win32 TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="2c4f1-106">ReinstallRetailPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="2c4f1-107">Réinstalle un jeu de clés de licence Services Bureau à distance acheté par le biais d’un canal de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="2c4f1-107">Reinstalls a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c4f1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c4f1-108">Syntax</span></span>


```mof
uint32 ReinstallRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="2c4f1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c4f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c4f1-110">*sLicenseCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2c4f1-110">*sLicenseCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c4f1-111">Contient le code de licence de 25 caractères.</span><span class="sxs-lookup"><span data-stu-id="2c4f1-111">Contains the 25-character license code.</span></span> <span data-ttu-id="2c4f1-112">Seule la chaîne de caractères alphanumériques de 25 caractères doit être indiquée comme entrée.</span><span class="sxs-lookup"><span data-stu-id="2c4f1-112">Only the 25-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="2c4f1-113">Aucun trait d’Union ne doit être ajouté.</span><span class="sxs-lookup"><span data-stu-id="2c4f1-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="2c4f1-114">*KeyPackId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2c4f1-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c4f1-115">Reçoit l’identificateur du module de clé.</span><span class="sxs-lookup"><span data-stu-id="2c4f1-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c4f1-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c4f1-116">Return value</span></span>

<span data-ttu-id="2c4f1-117">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="2c4f1-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2c4f1-118">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="2c4f1-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2c4f1-119">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2c4f1-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c4f1-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c4f1-120">Requirements</span></span>



| <span data-ttu-id="2c4f1-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c4f1-121">Requirement</span></span> | <span data-ttu-id="2c4f1-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c4f1-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c4f1-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c4f1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2c4f1-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c4f1-124">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="2c4f1-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c4f1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2c4f1-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c4f1-126">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="2c4f1-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2c4f1-127">Namespace</span></span><br/>                | <span data-ttu-id="2c4f1-128">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="2c4f1-128">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="2c4f1-129">MOF</span><span class="sxs-lookup"><span data-stu-id="2c4f1-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c4f1-130"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c4f1-130"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c4f1-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2c4f1-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c4f1-132"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c4f1-132"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c4f1-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c4f1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c4f1-134">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="2c4f1-134">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





