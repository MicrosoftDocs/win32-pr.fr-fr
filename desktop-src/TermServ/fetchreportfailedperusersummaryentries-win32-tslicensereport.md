---
title: Méthode FetchReportFailedPerUserSummaryEntries de la classe Win32_TSLicenseReport
description: Récupère les informations récapitulatives des licences d’accès client Services Bureau à distance par utilisateur ayant échoué (RDS \ 160 ; Licences d’accès client par utilisateur) à partir du rapport.
ms.assetid: dc9c4a36-b2a8-407e-b902-ee9d51227909
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode FetchReportFailedPerUserSummaryEntries
- Services Bureau à distance de la méthode FetchReportFailedPerUserSummaryEntries, classe Win32_TSLicenseReport
- Win32_TSLicenseReport de la classe Services Bureau à distance, méthode FetchReportFailedPerUserSummaryEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5219c2c854e04dabf8b5bfe0b5b70a07bbc3c57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510779"
---
# <a name="fetchreportfailedperusersummaryentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="3abba-106">Méthode FetchReportFailedPerUserSummaryEntries de la \_ classe Win32 TSLicenseReport</span><span class="sxs-lookup"><span data-stu-id="3abba-106">FetchReportFailedPerUserSummaryEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="3abba-107">Récupère des informations récapitulatives de la Services Bureau à distance des licences d’accès client par utilisateur (licences d’accès client des services Bureau à distance par utilisateur) ayant échoué à partir du rapport.</span><span class="sxs-lookup"><span data-stu-id="3abba-107">Retrieves summary information of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="3abba-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3abba-108">Syntax</span></span>


```mof
uint32 FetchReportFailedPerUserSummaryEntries(
  [in]      uint32                                         StartIndex,
  [in, out] uint32                                         Count,
  [out]     Win32_TSLicenseReportFailedPerUserSummaryEntry ReportFailedPerUserSummaryEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="3abba-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3abba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3abba-110">*StartIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3abba-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3abba-111">Index de la première entrée de rapport à récupérer.</span><span class="sxs-lookup"><span data-stu-id="3abba-111">The index of the first report entry to be retrieved.</span></span> <span data-ttu-id="3abba-112">La première entrée de rapport a un index de zéro.</span><span class="sxs-lookup"><span data-stu-id="3abba-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="3abba-113">*Nombre* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3abba-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3abba-114">Nombre d’entrées de rapport à récupérer de l’objet de rapport.</span><span class="sxs-lookup"><span data-stu-id="3abba-114">The number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="3abba-115">La valeur zéro indique que toutes les entrées de rapport à partir de *startIndex* doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="3abba-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="3abba-116">Au retour, contient le nombre d’entrées dans le tableau *ReportFailedPerUserSummaryEntries* .</span><span class="sxs-lookup"><span data-stu-id="3abba-116">On return, contains the number of entries in the *ReportFailedPerUserSummaryEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="3abba-117">*ReportFailedPerUserSummaryEntries* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3abba-117">*ReportFailedPerUserSummaryEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3abba-118">Tableau de classes [**\_ TSLicenseReportFailedPerUserSummaryEntry Win32**](win32-tslicensereportfailedperusersummaryentry.md) qui représentent les entrées de licence récupérées.</span><span class="sxs-lookup"><span data-stu-id="3abba-118">An array of [**Win32\_TSLicenseReportFailedPerUserSummaryEntry**](win32-tslicensereportfailedperusersummaryentry.md) classes that represent the license entries retrieved.</span></span> <span data-ttu-id="3abba-119">Le paramètre *Count* contient le nombre d’éléments de ce tableau.</span><span class="sxs-lookup"><span data-stu-id="3abba-119">The *Count* parameter contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3abba-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3abba-120">Return value</span></span>

<span data-ttu-id="3abba-121">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="3abba-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3abba-122">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="3abba-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3abba-123">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3abba-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3abba-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3abba-124">Requirements</span></span>



| <span data-ttu-id="3abba-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3abba-125">Requirement</span></span> | <span data-ttu-id="3abba-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3abba-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3abba-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3abba-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3abba-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3abba-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="3abba-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3abba-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3abba-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3abba-130">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="3abba-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3abba-131">Namespace</span></span><br/>                | <span data-ttu-id="3abba-132">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="3abba-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="3abba-133">MOF</span><span class="sxs-lookup"><span data-stu-id="3abba-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3abba-134"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3abba-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3abba-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3abba-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3abba-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3abba-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3abba-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3abba-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3abba-138">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="3abba-138">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

 





