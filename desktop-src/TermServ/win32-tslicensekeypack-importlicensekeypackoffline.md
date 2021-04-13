---
title: Méthode ImportLicenseKeyPackOffline de la classe Win32_TSLicenseKeyPack
description: Importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Services Bureau à distance qui utilise un identificateur de licence reçu via Internet ou le téléphone.
ms.assetid: 69D65917-8B82-4C24-AFFA-BBE529D3883C
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ImportLicenseKeyPackOffline
- Services Bureau à distance de la méthode ImportLicenseKeyPackOffline, classe Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de la classe Services Bureau à distance, méthode ImportLicenseKeyPackOffline
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de474cce6eb91cdc605588f7f4a63d97f985769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508637"
---
# <a name="importlicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="b6c0f-106">Méthode ImportLicenseKeyPackOffline de la \_ classe Win32 TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="b6c0f-106">ImportLicenseKeyPackOffline method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="b6c0f-107">Importations, à partir d’un autre serveur de licences Bureau à distance, un jeu de clés de licence Services Bureau à distance qui utilise un identificateur de licence reçu via Internet ou le téléphone.</span><span class="sxs-lookup"><span data-stu-id="b6c0f-107">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that uses a license identifier that was received over the Internet or the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6c0f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6c0f-108">Syntax</span></span>


```mof
uint32 ImportLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="b6c0f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6c0f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6c0f-110">*sLicenseKeyPackId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6c0f-110">*sLicenseKeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c0f-111">Contient le code de licence de 35 caractères.</span><span class="sxs-lookup"><span data-stu-id="b6c0f-111">Contains the 35-character license code.</span></span> <span data-ttu-id="b6c0f-112">Seule la chaîne de caractères alphanumériques de 35 caractères doit être indiquée comme entrée.</span><span class="sxs-lookup"><span data-stu-id="b6c0f-112">Only the 35-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="b6c0f-113">Aucun trait d’Union ne doit être ajouté.</span><span class="sxs-lookup"><span data-stu-id="b6c0f-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="b6c0f-114">*sSourceLSName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6c0f-114">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c0f-115">Nom du serveur de licences Bureau à distance source.</span><span class="sxs-lookup"><span data-stu-id="b6c0f-115">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="b6c0f-116">Il s’agit du nom unique complet ou de l’adresse IP du serveur.</span><span class="sxs-lookup"><span data-stu-id="b6c0f-116">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="b6c0f-117">*sSourceLSProductId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6c0f-117">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c0f-118">Identificateur du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b6c0f-118">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="b6c0f-119">Est une chaîne alphanumérique de 35 caractères qui ne peut pas contenir de traits d’Union.</span><span class="sxs-lookup"><span data-stu-id="b6c0f-119">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="b6c0f-120">*KeyPackId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b6c0f-120">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c0f-121">Reçoit l’identificateur du module de clé.</span><span class="sxs-lookup"><span data-stu-id="b6c0f-121">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6c0f-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6c0f-122">Return value</span></span>

<span data-ttu-id="b6c0f-123">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="b6c0f-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b6c0f-124">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="b6c0f-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b6c0f-125">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b6c0f-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6c0f-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6c0f-126">Requirements</span></span>



| <span data-ttu-id="b6c0f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6c0f-127">Requirement</span></span> | <span data-ttu-id="b6c0f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6c0f-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c0f-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6c0f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b6c0f-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6c0f-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="b6c0f-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6c0f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b6c0f-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6c0f-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="b6c0f-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b6c0f-133">Namespace</span></span><br/>                | <span data-ttu-id="b6c0f-134">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b6c0f-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="b6c0f-135">MOF</span><span class="sxs-lookup"><span data-stu-id="b6c0f-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6c0f-136"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6c0f-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6c0f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b6c0f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6c0f-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6c0f-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6c0f-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6c0f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6c0f-140">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="b6c0f-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





