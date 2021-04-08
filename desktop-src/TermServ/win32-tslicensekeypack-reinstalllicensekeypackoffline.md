---
title: Méthode ReinstallLicenseKeyPackOffline de la classe Win32_TSLicenseKeyPack
description: Réinstalle un jeu de clés de licence Services Bureau à distance qui utilise l’identificateur de licence reçu sur Internet ou sur le téléphone.
ms.assetid: CFDB4C3B-C7C1-4670-BC87-92727057A500
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ReinstallLicenseKeyPackOffline
- Services Bureau à distance de la méthode ReinstallLicenseKeyPackOffline, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode ReinstallLicenseKeyPackOffline
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e805521ea750c018ab2e7965e7fbfba05a92d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843181"
---
# <a name="reinstalllicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="1766c-106">Méthode ReinstallLicenseKeyPackOffline de la \_ classe Win32 TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="1766c-106">ReinstallLicenseKeyPackOffline method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="1766c-107">Réinstalle un jeu de clés de licence Services Bureau à distance qui utilise l’identificateur de licence reçu sur Internet ou sur le téléphone.</span><span class="sxs-lookup"><span data-stu-id="1766c-107">Reinstalls a Remote Desktop Services license key pack that uses the license identifier that was received over the Internet or the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="1766c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1766c-108">Syntax</span></span>


```mof
uint32 ReinstallLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="1766c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1766c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1766c-110">*sLicenseKeyPackId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1766c-110">*sLicenseKeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1766c-111">Contient le code de licence de 35 caractères.</span><span class="sxs-lookup"><span data-stu-id="1766c-111">Contains the 35-character license code.</span></span> <span data-ttu-id="1766c-112">Seule la chaîne de caractères alphanumériques de 35 caractères doit être indiquée comme entrée.</span><span class="sxs-lookup"><span data-stu-id="1766c-112">Only the 35-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="1766c-113">Aucun trait d’Union ne doit être ajouté.</span><span class="sxs-lookup"><span data-stu-id="1766c-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="1766c-114">*KeyPackId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1766c-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1766c-115">Reçoit l’identificateur du module de clé.</span><span class="sxs-lookup"><span data-stu-id="1766c-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1766c-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1766c-116">Return value</span></span>

<span data-ttu-id="1766c-117">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="1766c-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1766c-118">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="1766c-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1766c-119">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1766c-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1766c-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1766c-120">Requirements</span></span>



| <span data-ttu-id="1766c-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1766c-121">Requirement</span></span> | <span data-ttu-id="1766c-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="1766c-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1766c-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1766c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1766c-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1766c-124">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="1766c-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1766c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1766c-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1766c-126">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="1766c-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1766c-127">Namespace</span></span><br/>                | <span data-ttu-id="1766c-128">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="1766c-128">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="1766c-129">MOF</span><span class="sxs-lookup"><span data-stu-id="1766c-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1766c-130"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1766c-130"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1766c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1766c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1766c-132"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1766c-132"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1766c-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1766c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1766c-134">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="1766c-134">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





