---
title: Méthode FetchReportFailedPerUserEntries de la classe Win32_TSLicenseReport
description: Récupère les détails des licences d’accès client en échec Services Bureau à distance par utilisateur (RDS \ 160 ; Licences d’accès client par utilisateur) à partir du rapport.
ms.assetid: 2c16723c-1755-4ec1-a6db-55d769f8b6fd
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode FetchReportFailedPerUserEntries
- Services Bureau à distance de la méthode FetchReportFailedPerUserEntries, classe Win32_TSLicenseReport
- Win32_TSLicenseReport de la classe Services Bureau à distance, méthode FetchReportFailedPerUserEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 159f980944c70dbad4c6948a614d0c9964a5f0cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509286"
---
# <a name="fetchreportfailedperuserentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="cfc2b-106">Méthode FetchReportFailedPerUserEntries de la \_ classe Win32 TSLicenseReport</span><span class="sxs-lookup"><span data-stu-id="cfc2b-106">FetchReportFailedPerUserEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="cfc2b-107">Récupère les détails des licences d’accès client en échec Services Bureau à distance par utilisateur (RDS par utilisateur Cal par utilisateur) à partir du rapport.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-107">Retrieves details of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfc2b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfc2b-108">Syntax</span></span>


```mof
uint32 FetchReportFailedPerUserEntries(
  [in]      uint32                                  StartIndex,
  [in, out] uint32                                  Count,
  [out]     Win32_TSLicenseReportFailedPerUserEntry ReportFailedPerUserEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="cfc2b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cfc2b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfc2b-110">*StartIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cfc2b-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc2b-111">Index de la première entrée de rapport à récupérer.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-111">The index of the first report entry to be retrieved.</span></span> <span data-ttu-id="cfc2b-112">La première entrée de rapport a un index de zéro.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="cfc2b-113">*Nombre* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cfc2b-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc2b-114">Nombre d’entrées de rapport à récupérer de l’objet de rapport.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-114">The number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="cfc2b-115">La valeur zéro indique que toutes les entrées de rapport à partir de *startIndex* doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="cfc2b-116">Au retour, contient le nombre d’entrées dans le tableau *ReportFailedPerUserEntries* .</span><span class="sxs-lookup"><span data-stu-id="cfc2b-116">On return, contains the number of entries in the *ReportFailedPerUserEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="cfc2b-117">*ReportFailedPerUserEntries* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cfc2b-117">*ReportFailedPerUserEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc2b-118">Tableau de classes [**\_ TSLicenseReportFailedPerUserEntry Win32**](win32-tslicensereportfailedperuserentry.md) qui représentent les entrées de licence récupérées.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-118">An array of [**Win32\_TSLicenseReportFailedPerUserEntry**](win32-tslicensereportfailedperuserentry.md) classes that represent the license entries retrieved.</span></span> <span data-ttu-id="cfc2b-119">Le paramètre *Count* contient le nombre d’éléments de ce tableau.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-119">The *Count* parameter contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfc2b-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cfc2b-120">Return value</span></span>

<span data-ttu-id="cfc2b-121">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="cfc2b-122">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="cfc2b-123">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="cfc2b-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfc2b-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cfc2b-124">Requirements</span></span>



| <span data-ttu-id="cfc2b-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cfc2b-125">Requirement</span></span> | <span data-ttu-id="cfc2b-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfc2b-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfc2b-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfc2b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cfc2b-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfc2b-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="cfc2b-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfc2b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cfc2b-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cfc2b-130">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="cfc2b-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cfc2b-131">Namespace</span></span><br/>                | <span data-ttu-id="cfc2b-132">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="cfc2b-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="cfc2b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="cfc2b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cfc2b-134"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cfc2b-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cfc2b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="cfc2b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfc2b-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfc2b-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfc2b-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfc2b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfc2b-138">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="cfc2b-138">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

 





