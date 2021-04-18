---
title: Méthode InstallRetailPurchaseLicenseKeyPack de la classe Win32_TSLicenseKeyPack
description: Installe un jeu de clés de licence Services Bureau à distance acheté par le biais d’un canal de vente au détail.
ms.assetid: cd33c785-7aa1-4e30-8155-4176b6f4c037
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode InstallRetailPurchaseLicenseKeyPack
- Services Bureau à distance de la méthode InstallRetailPurchaseLicenseKeyPack, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode InstallRetailPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7523e2106a68284d6b9b376d47608114f940c194
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512371"
---
# <a name="installretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="16ceb-106">Méthode InstallRetailPurchaseLicenseKeyPack de la \_ classe Win32 TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="16ceb-106">InstallRetailPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="16ceb-107">Installe un jeu de clés de licence Services Bureau à distance acheté par le biais d’un canal de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="16ceb-107">Installs a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="16ceb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16ceb-108">Syntax</span></span>


```mof
uint32 InstallRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="16ceb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16ceb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16ceb-110">*sLicenseCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16ceb-110">*sLicenseCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16ceb-111">Contient le code de licence de 25 caractères.</span><span class="sxs-lookup"><span data-stu-id="16ceb-111">Contains the 25-character license code.</span></span> <span data-ttu-id="16ceb-112">Seule la chaîne de caractères alphanumériques de 25 caractères doit être indiquée comme entrée.</span><span class="sxs-lookup"><span data-stu-id="16ceb-112">Only the 25-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="16ceb-113">Aucun trait d’Union ne doit être ajouté.</span><span class="sxs-lookup"><span data-stu-id="16ceb-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="16ceb-114">*KeyPackId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="16ceb-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16ceb-115">Reçoit l’identificateur du module de clé.</span><span class="sxs-lookup"><span data-stu-id="16ceb-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16ceb-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16ceb-116">Return value</span></span>

<span data-ttu-id="16ceb-117">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="16ceb-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="16ceb-118">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="16ceb-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="16ceb-119">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="16ceb-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="16ceb-120">Notes</span><span class="sxs-lookup"><span data-stu-id="16ceb-120">Remarks</span></span>

<span data-ttu-id="16ceb-121">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="16ceb-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="16ceb-122">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="16ceb-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="16ceb-123">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="16ceb-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="16ceb-124">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="16ceb-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="16ceb-125">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="16ceb-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="16ceb-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16ceb-126">Requirements</span></span>



| <span data-ttu-id="16ceb-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16ceb-127">Requirement</span></span> | <span data-ttu-id="16ceb-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="16ceb-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="16ceb-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16ceb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="16ceb-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="16ceb-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="16ceb-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16ceb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="16ceb-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16ceb-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="16ceb-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="16ceb-133">Namespace</span></span><br/>                | <span data-ttu-id="16ceb-134">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="16ceb-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="16ceb-135">MOF</span><span class="sxs-lookup"><span data-stu-id="16ceb-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16ceb-136"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16ceb-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="16ceb-137">DLL</span><span class="sxs-lookup"><span data-stu-id="16ceb-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16ceb-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16ceb-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16ceb-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16ceb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16ceb-140">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="16ceb-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

