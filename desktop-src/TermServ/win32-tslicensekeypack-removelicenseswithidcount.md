---
title: Méthode RemoveLicensesWithIdCount de la classe Win32_TSLicenseKeyPack
description: Supprime le nombre spécifié de licences Services Bureau à distance du jeu de clés spécifié.
ms.assetid: 36228659-7BE7-490A-A00C-A99FA66BFEB8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoveLicensesWithIdCount
- Services Bureau à distance de la méthode RemoveLicensesWithIdCount, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode RemoveLicensesWithIdCount
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.RemoveLicensesWithIdCount
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b2de1d1e0bfeed538e400436f8a88cd25ac563
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032450"
---
# <a name="removelicenseswithidcount-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="c47ac-106">Méthode RemoveLicensesWithIdCount de la \_ classe Win32 TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="c47ac-106">RemoveLicensesWithIdCount method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="c47ac-107">Supprime le nombre spécifié de licences Services Bureau à distance du jeu de clés spécifié.</span><span class="sxs-lookup"><span data-stu-id="c47ac-107">Removes the specified number of Remote Desktop Services licenses from the specified key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="c47ac-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c47ac-108">Syntax</span></span>


```mof
uint32 RemoveLicensesWithIdCount(
  [in] uint32 KeyPackId,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a><span data-ttu-id="c47ac-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c47ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c47ac-110">*KeyPackId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c47ac-110">*KeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c47ac-111">Identificateur du module de clé qui contient les licences à supprimer.</span><span class="sxs-lookup"><span data-stu-id="c47ac-111">The identifier of the key pack that contains the licenses to remove.</span></span>

</dd> <dt>

<span data-ttu-id="c47ac-112">*LicenseCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c47ac-112">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c47ac-113">Nombre de licences à désinstaller.</span><span class="sxs-lookup"><span data-stu-id="c47ac-113">The number of licenses to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c47ac-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c47ac-114">Return value</span></span>

<span data-ttu-id="c47ac-115">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="c47ac-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c47ac-116">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="c47ac-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c47ac-117">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c47ac-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c47ac-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c47ac-118">Requirements</span></span>



| <span data-ttu-id="c47ac-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c47ac-119">Requirement</span></span> | <span data-ttu-id="c47ac-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c47ac-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c47ac-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c47ac-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c47ac-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c47ac-122">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="c47ac-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c47ac-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c47ac-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c47ac-124">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c47ac-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c47ac-125">Namespace</span></span><br/>                | <span data-ttu-id="c47ac-126">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="c47ac-126">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="c47ac-127">MOF</span><span class="sxs-lookup"><span data-stu-id="c47ac-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c47ac-128"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c47ac-128"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c47ac-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c47ac-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c47ac-130"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c47ac-130"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c47ac-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c47ac-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c47ac-132">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="c47ac-132">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





