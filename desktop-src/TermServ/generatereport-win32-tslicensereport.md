---
title: Méthode GenerateReport de la classe Win32_TSLicenseReport (gpmgmt. h)
description: GenerateReport ne peut plus être utilisé à partir de Windows Server 2012.
ms.assetid: 2d3b16d6-52e8-491f-b6e5-419e9a21013b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GenerateReport
- Services Bureau à distance de la méthode GenerateReport, classe Win32_TSLicenseReport
- Win32_TSLicenseReport de la classe Services Bureau à distance, méthode GenerateReport
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5231c87d379decac8d4f6491042bff735c1ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384992"
---
# <a name="generatereport-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="ebf7b-106">Méthode GenerateReport de la \_ classe Win32 TSLicenseReport</span><span class="sxs-lookup"><span data-stu-id="ebf7b-106">GenerateReport method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="ebf7b-107">\[**GenerateReport** ne peut plus être utilisé à partir de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ebf7b-107">\[**GenerateReport** is no longer available for use as of Windows Server 2012.</span></span> <span data-ttu-id="ebf7b-108">Utilisez plutôt [**GenerateReportEx**](generatereportex-win32-tslicensereport.md).\]</span><span class="sxs-lookup"><span data-stu-id="ebf7b-108">Instead, use [**GenerateReportEx**](generatereportex-win32-tslicensereport.md).\]</span></span>

<span data-ttu-id="ebf7b-109">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ebf7b-109">This method is not supported.</span></span>

<span data-ttu-id="ebf7b-110">**Windows server 2008 R2 et Windows server 2008 :** Génère un rapport d’utilisation des licences par utilisateur actuel sur le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ebf7b-110">**Windows Server 2008 R2 and Windows Server 2008:** Generates a current per user license usage report on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebf7b-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebf7b-111">Syntax</span></span>


```mof
uint32 GenerateReport(
  [in]  uint32 ScopeType,
  [in]  string ScopeValue,
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="ebf7b-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebf7b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebf7b-113">*ScopeType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebf7b-113">*ScopeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebf7b-114">Étendue du rapport d’utilisation de la licence.</span><span class="sxs-lookup"><span data-stu-id="ebf7b-114">Scope of the license usage report.</span></span> <span data-ttu-id="ebf7b-115">Il peut avoir les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ebf7b-115">It can have the following values.</span></span>

<dt>

<span data-ttu-id="ebf7b-116">1</span><span class="sxs-lookup"><span data-stu-id="ebf7b-116">1</span></span>
</dt> <dd>

<span data-ttu-id="ebf7b-117">Le rapport sera généré pour l’ensemble du domaine.</span><span class="sxs-lookup"><span data-stu-id="ebf7b-117">The report will be generated for the entire domain.</span></span>

</dd> <dt>

<span data-ttu-id="ebf7b-118">2</span><span class="sxs-lookup"><span data-stu-id="ebf7b-118">2</span></span>
</dt> <dd>

<span data-ttu-id="ebf7b-119">Le rapport sera généré pour l’unité d’organisation (UO) spécifiée dans le paramètre *ScopeValue* .</span><span class="sxs-lookup"><span data-stu-id="ebf7b-119">The report will be generated for the organizational unit (OU) that is specified in the *ScopeValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ebf7b-120">3</span><span class="sxs-lookup"><span data-stu-id="ebf7b-120">3</span></span>
</dt> <dd>

<span data-ttu-id="ebf7b-121">Le rapport sera généré pour tous les domaines approuvés.</span><span class="sxs-lookup"><span data-stu-id="ebf7b-121">The report will be generated for all trusted domains.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ebf7b-122">*ScopeValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebf7b-122">*ScopeValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebf7b-123">Si le paramètre *ScopeType* est 2, *ScopeType* spécifie l’unité d’organisation pour laquelle le rapport sera généré.</span><span class="sxs-lookup"><span data-stu-id="ebf7b-123">If the *ScopeType* parameter is 2, *ScopeType* specifies the OU for which the report will be generated.</span></span> <span data-ttu-id="ebf7b-124">Vous devez spécifier *ScopeValue* à l’aide du format **ou =**_OUName1_*_, ou =_*_OUName2_*_..._*.</span><span class="sxs-lookup"><span data-stu-id="ebf7b-124">You must specify *ScopeValue* by using the format **OU=**_OUName1_*_,OU=_*_OUName2_*_..._*.</span></span>

</dd> <dt>

<span data-ttu-id="ebf7b-125">*Nom du fichier* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ebf7b-125">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebf7b-126">Nom de fichier du rapport généré.</span><span class="sxs-lookup"><span data-stu-id="ebf7b-126">The file name of the generated report.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebf7b-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ebf7b-127">Return value</span></span>

<span data-ttu-id="ebf7b-128">Retourne **WBEM \_ E \_ non \_ pris en charge**.</span><span class="sxs-lookup"><span data-stu-id="ebf7b-128">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="ebf7b-129">**Windows server 2008 R2 et Windows server 2008 :** Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="ebf7b-129">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ebf7b-130">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="ebf7b-130">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ebf7b-131">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ebf7b-131">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ebf7b-132">Notes</span><span class="sxs-lookup"><span data-stu-id="ebf7b-132">Remarks</span></span>

<span data-ttu-id="ebf7b-133">Il s’agit d’une méthode statique.</span><span class="sxs-lookup"><span data-stu-id="ebf7b-133">This is a static method.</span></span>

<span data-ttu-id="ebf7b-134">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="ebf7b-134">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ebf7b-135">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="ebf7b-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ebf7b-136">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ebf7b-136">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ebf7b-137">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="ebf7b-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ebf7b-138">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ebf7b-138">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ebf7b-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebf7b-139">Requirements</span></span>



| <span data-ttu-id="ebf7b-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebf7b-140">Requirement</span></span> | <span data-ttu-id="ebf7b-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebf7b-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf7b-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebf7b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ebf7b-143">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebf7b-143">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="ebf7b-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebf7b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ebf7b-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebf7b-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ebf7b-146">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="ebf7b-146">End of client support</span></span><br/>    | <span data-ttu-id="ebf7b-147">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebf7b-147">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="ebf7b-148">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="ebf7b-148">End of server support</span></span><br/>    | <span data-ttu-id="ebf7b-149">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ebf7b-149">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="ebf7b-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ebf7b-150">Namespace</span></span><br/>                | <span data-ttu-id="ebf7b-151">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="ebf7b-151">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="ebf7b-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebf7b-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebf7b-153"><dt>Gpmgmt. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebf7b-153"><dt>Gpmgmt.h</dt></span></span> </dl>       |
| <span data-ttu-id="ebf7b-154">MOF</span><span class="sxs-lookup"><span data-stu-id="ebf7b-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ebf7b-155"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ebf7b-155"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ebf7b-156">DLL</span><span class="sxs-lookup"><span data-stu-id="ebf7b-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebf7b-157"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebf7b-157"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebf7b-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebf7b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebf7b-159">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="ebf7b-159">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

