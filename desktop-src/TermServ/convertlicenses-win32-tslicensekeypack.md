---
title: Méthode ConvertLicenses de la classe Win32_TSLicenseKeyPack
description: Convertit les licences dans le jeu de clés actuel.
ms.assetid: 38600144-8fa2-4f9a-b7a4-7fafc304e7cb
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ConvertLicenses
- Services Bureau à distance de la méthode ConvertLicenses, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode ConvertLicenses
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ConvertLicenses
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f37b1d9804c5f14f89a7ff6b48f5f8fcbdc60b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384080"
---
# <a name="convertlicenses-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="e9b79-106">Méthode ConvertLicenses de la \_ classe Win32 TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="e9b79-106">ConvertLicenses method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="e9b79-107">Convertit les licences dans le jeu de clés actuel.</span><span class="sxs-lookup"><span data-stu-id="e9b79-107">Converts the licenses in the current key pack.</span></span> <span data-ttu-id="e9b79-108">Si la licence est une licence par utilisateur, elle est convertie en licence par appareil.</span><span class="sxs-lookup"><span data-stu-id="e9b79-108">If the license is a per-user license, it is converted to a per-device license.</span></span> <span data-ttu-id="e9b79-109">Si la licence est une licence par appareil, elle est convertie en licence par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e9b79-109">If the license is a per-device license, it is converted to a per-user license.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9b79-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9b79-110">Syntax</span></span>


```mof
uint32 ConvertLicenses(
  [in]  uint32 Count,
  [out] uint32 KeypackID
);
```



## <a name="parameters"></a><span data-ttu-id="e9b79-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9b79-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9b79-112">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9b79-112">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9b79-113">Nombre de licences à convertir.</span><span class="sxs-lookup"><span data-stu-id="e9b79-113">The number of licenses to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="e9b79-114">*KeypackID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e9b79-114">*KeypackID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9b79-115">Identificateur du Pack de clés résultant.</span><span class="sxs-lookup"><span data-stu-id="e9b79-115">The identifier of the resultant key pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9b79-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9b79-116">Return value</span></span>

<span data-ttu-id="e9b79-117">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="e9b79-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e9b79-118">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="e9b79-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e9b79-119">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e9b79-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9b79-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9b79-120">Requirements</span></span>



| <span data-ttu-id="e9b79-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9b79-121">Requirement</span></span> | <span data-ttu-id="e9b79-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9b79-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9b79-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9b79-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e9b79-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9b79-124">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e9b79-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9b79-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e9b79-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e9b79-126">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="e9b79-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e9b79-127">Namespace</span></span><br/>                | <span data-ttu-id="e9b79-128">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e9b79-128">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e9b79-129">MOF</span><span class="sxs-lookup"><span data-stu-id="e9b79-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9b79-130"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9b79-130"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9b79-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e9b79-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9b79-132"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9b79-132"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9b79-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9b79-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9b79-134">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="e9b79-134">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





