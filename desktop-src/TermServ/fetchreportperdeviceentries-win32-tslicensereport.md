---
title: Méthode FetchReportPerDeviceEntries de la classe Win32_TSLicenseReport
description: Récupère des informations sur les licences d’accès client par périphérique Services Bureau à distance émises par périphérique (RDS \ 160 ; Licences d’accès client par périphérique) à partir du rapport.
ms.assetid: 3f632a65-d6e0-4efd-9498-d04a05f9ddec
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode FetchReportPerDeviceEntries
- Services Bureau à distance de la méthode FetchReportPerDeviceEntries, classe Win32_TSLicenseReport
- Win32_TSLicenseReport de la classe Services Bureau à distance, méthode FetchReportPerDeviceEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportPerDeviceEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce77fce941dd0a24fb6ee17e0aeb67b4e78bdae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510356"
---
# <a name="fetchreportperdeviceentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="82032-106">Méthode FetchReportPerDeviceEntries de la \_ classe Win32 TSLicenseReport</span><span class="sxs-lookup"><span data-stu-id="82032-106">FetchReportPerDeviceEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="82032-107">Récupère des informations sur les licences d’accès client par périphérique Services Bureau à distance émises par périphérique (CAL par périphérique) à partir du rapport.</span><span class="sxs-lookup"><span data-stu-id="82032-107">Retrieves information of issued Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="82032-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82032-108">Syntax</span></span>


```mof
uint32 FetchReportPerDeviceEntries(
  [in]      uint32                              StartIndex,
  [in, out] uint32                              Count,
  [out]     Win32_TSLicenseReportPerDeviceEntry ReportPerDeviceEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="82032-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82032-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82032-110">*StartIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82032-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82032-111">Index de la première entrée de rapport à récupérer.</span><span class="sxs-lookup"><span data-stu-id="82032-111">The index of the first report entry to be retrieved.</span></span> <span data-ttu-id="82032-112">La première entrée de rapport a un index de zéro.</span><span class="sxs-lookup"><span data-stu-id="82032-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="82032-113">*Nombre* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="82032-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="82032-114">Nombre d’entrées de rapport à récupérer de l’objet de rapport.</span><span class="sxs-lookup"><span data-stu-id="82032-114">The number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="82032-115">La valeur zéro indique que toutes les entrées de rapport à partir de *startIndex* doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="82032-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="82032-116">Au retour, contient le nombre d’entrées dans le tableau *ReportPerDeviceEntries* .</span><span class="sxs-lookup"><span data-stu-id="82032-116">On return, contains the number of entries in the *ReportPerDeviceEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="82032-117">*ReportPerDeviceEntries* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="82032-117">*ReportPerDeviceEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82032-118">Tableau de classes [**\_ TSLicenseReportPerDeviceEntry Win32**](win32-tslicensereportperdeviceentry.md) qui représentent les entrées de licence récupérées.</span><span class="sxs-lookup"><span data-stu-id="82032-118">An array of [**Win32\_TSLicenseReportPerDeviceEntry**](win32-tslicensereportperdeviceentry.md) classes the represent the license entries retrieved.</span></span> <span data-ttu-id="82032-119">Le paramètre *Count* contient le nombre d’éléments de ce tableau.</span><span class="sxs-lookup"><span data-stu-id="82032-119">The *Count* parameter contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82032-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82032-120">Return value</span></span>

<span data-ttu-id="82032-121">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="82032-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="82032-122">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="82032-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="82032-123">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="82032-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="82032-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82032-124">Requirements</span></span>



| <span data-ttu-id="82032-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82032-125">Requirement</span></span> | <span data-ttu-id="82032-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="82032-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="82032-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82032-127">Minimum supported client</span></span><br/> | <span data-ttu-id="82032-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="82032-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="82032-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82032-129">Minimum supported server</span></span><br/> | <span data-ttu-id="82032-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="82032-130">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="82032-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="82032-131">Namespace</span></span><br/>                | <span data-ttu-id="82032-132">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="82032-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="82032-133">MOF</span><span class="sxs-lookup"><span data-stu-id="82032-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82032-134"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82032-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="82032-135">DLL</span><span class="sxs-lookup"><span data-stu-id="82032-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82032-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82032-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82032-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82032-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82032-138">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="82032-138">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

 





