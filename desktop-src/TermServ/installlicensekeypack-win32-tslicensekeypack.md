---
title: Méthode InstallLicenseKeyPack de la classe Win32_TSLicenseKeyPack
description: Installe un jeu de clés de licence Services Bureau à distance qui utilise l’identificateur de licence reçu via Internet ou par téléphone.
ms.assetid: 1e545186-cc01-4700-857f-9390e1b73923
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode InstallLicenseKeyPack
- Services Bureau à distance de la méthode InstallLicenseKeyPack, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode InstallLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bee5e03de19783a20eeafa3f652dd60b99e871c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941811"
---
# <a name="installlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="26571-106">Méthode InstallLicenseKeyPack de la \_ classe Win32 TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="26571-106">InstallLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="26571-107">Installe un jeu de clés de licence Services Bureau à distance qui utilise l’identificateur de licence reçu via Internet ou par téléphone.</span><span class="sxs-lookup"><span data-stu-id="26571-107">Installs a Remote Desktop Services license key pack that uses the license identifier that was received over the Internet or the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="26571-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26571-108">Syntax</span></span>


```mof
uint32 InstallLicenseKeyPack(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="26571-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26571-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26571-110">*sLicenseKeyPackId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26571-110">*sLicenseKeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26571-111">Contient le code de licence de 35 caractères.</span><span class="sxs-lookup"><span data-stu-id="26571-111">Contains the 35-character license code.</span></span> <span data-ttu-id="26571-112">Seule la chaîne de caractères alphanumériques de 35 caractères doit être indiquée comme entrée.</span><span class="sxs-lookup"><span data-stu-id="26571-112">Only the 35-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="26571-113">Aucun trait d’Union ne doit être ajouté.</span><span class="sxs-lookup"><span data-stu-id="26571-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="26571-114">*KeyPackId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="26571-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26571-115">Reçoit l’identificateur du module de clé.</span><span class="sxs-lookup"><span data-stu-id="26571-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26571-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26571-116">Return value</span></span>

<span data-ttu-id="26571-117">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="26571-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="26571-118">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="26571-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="26571-119">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="26571-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="26571-120">Notes</span><span class="sxs-lookup"><span data-stu-id="26571-120">Remarks</span></span>

<span data-ttu-id="26571-121">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="26571-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="26571-122">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="26571-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="26571-123">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="26571-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="26571-124">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="26571-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="26571-125">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="26571-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="26571-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26571-126">Requirements</span></span>



| <span data-ttu-id="26571-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26571-127">Requirement</span></span> | <span data-ttu-id="26571-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="26571-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="26571-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26571-129">Minimum supported client</span></span><br/> | <span data-ttu-id="26571-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="26571-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="26571-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26571-131">Minimum supported server</span></span><br/> | <span data-ttu-id="26571-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26571-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="26571-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="26571-133">Namespace</span></span><br/>                | <span data-ttu-id="26571-134">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="26571-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="26571-135">MOF</span><span class="sxs-lookup"><span data-stu-id="26571-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26571-136"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26571-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="26571-137">DLL</span><span class="sxs-lookup"><span data-stu-id="26571-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26571-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26571-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26571-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26571-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26571-140">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="26571-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

