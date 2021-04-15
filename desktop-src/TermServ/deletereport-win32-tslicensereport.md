---
title: Méthode DeleteReport de la classe Win32_TSLicenseReport
description: Supprime un objet de rapport sur le serveur de licences Bureau à distance. Il ne s’agit pas d’une méthode statique.
ms.assetid: cc70526c-7ce5-4d55-b72e-8a5e8799b1d8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DeleteReport
- Services Bureau à distance de la méthode DeleteReport, classe Win32_TSLicenseReport
- Win32_TSLicenseReport de la classe Services Bureau à distance, méthode DeleteReport
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.DeleteReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a96c8626e4ecc1f89d0f2fcefa69845fec4df8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508357"
---
# <a name="deletereport-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="18afa-107">Méthode DeleteReport de la \_ classe Win32 TSLicenseReport</span><span class="sxs-lookup"><span data-stu-id="18afa-107">DeleteReport method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="18afa-108">Supprime un objet de rapport sur le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="18afa-108">Deletes a report object on the Remote Desktop license server.</span></span> <span data-ttu-id="18afa-109">Il ne s’agit pas d’une méthode statique.</span><span class="sxs-lookup"><span data-stu-id="18afa-109">This is not a static method.</span></span>

## <a name="syntax"></a><span data-ttu-id="18afa-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18afa-110">Syntax</span></span>


```mof
uint32 DeleteReport();
```



## <a name="parameters"></a><span data-ttu-id="18afa-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18afa-111">Parameters</span></span>

<span data-ttu-id="18afa-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="18afa-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="18afa-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="18afa-113">Return value</span></span>

<span data-ttu-id="18afa-114">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="18afa-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="18afa-115">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="18afa-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="18afa-116">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="18afa-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="18afa-117">Notes</span><span class="sxs-lookup"><span data-stu-id="18afa-117">Remarks</span></span>

<span data-ttu-id="18afa-118">Il ne s’agit pas d’une méthode statique.</span><span class="sxs-lookup"><span data-stu-id="18afa-118">This is not a static method.</span></span> <span data-ttu-id="18afa-119">Cette méthode doit être appelée à partir d’un objet de rapport d’utilisation de licence par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="18afa-119">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="18afa-120">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="18afa-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="18afa-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="18afa-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="18afa-122">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="18afa-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="18afa-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="18afa-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="18afa-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="18afa-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="18afa-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18afa-125">Requirements</span></span>



| <span data-ttu-id="18afa-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18afa-126">Requirement</span></span> | <span data-ttu-id="18afa-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="18afa-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="18afa-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18afa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="18afa-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="18afa-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="18afa-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18afa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="18afa-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18afa-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="18afa-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="18afa-132">Namespace</span></span><br/>                | <span data-ttu-id="18afa-133">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="18afa-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="18afa-134">MOF</span><span class="sxs-lookup"><span data-stu-id="18afa-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18afa-135"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18afa-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="18afa-136">DLL</span><span class="sxs-lookup"><span data-stu-id="18afa-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18afa-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18afa-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18afa-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18afa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18afa-139">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="18afa-139">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

