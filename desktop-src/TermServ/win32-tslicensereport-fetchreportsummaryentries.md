---
title: Méthode FetchReportSummaryEntries de la classe Win32_TSLicenseReport
description: Récupère des résumés de Services Bureau à distance licences d’accès client par utilisateur (RDS \ 160 ; Licences d’accès client par utilisateur) à partir du rapport.
ms.assetid: 0312B787-83E9-42FC-B21B-904B804C5C94
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode FetchReportSummaryEntries
- Services Bureau à distance de la méthode FetchReportSummaryEntries, classe Win32_TSLicenseReport
- Win32_TSLicenseReport de la classe Services Bureau à distance, méthode FetchReportSummaryEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e47100c71e195cacb6a1004975955eae778765a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103009"
---
# <a name="fetchreportsummaryentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="7f331-106">Méthode FetchReportSummaryEntries de la \_ classe Win32 TSLicenseReport</span><span class="sxs-lookup"><span data-stu-id="7f331-106">FetchReportSummaryEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="7f331-107">Récupère des résumés de Services Bureau à distance licences d’accès client par utilisateur (licences d’accès client aux services Bureau à distance par utilisateur) à partir du rapport.</span><span class="sxs-lookup"><span data-stu-id="7f331-107">Retrieves summaries of Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f331-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f331-108">Syntax</span></span>


```mof
uint32 FetchReportSummaryEntries(
  [in]      uint32                            StartIndex,
  [in, out] uint32                            Count,
  [out]     Win32_TSLicenseReportSummaryEntry ReportSummaryEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="7f331-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f331-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f331-110">*StartIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f331-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f331-111">Index de la première entrée de rapport à recevoir.</span><span class="sxs-lookup"><span data-stu-id="7f331-111">Index of the first report entry to be received.</span></span> <span data-ttu-id="7f331-112">La première entrée de rapport a un index de zéro.</span><span class="sxs-lookup"><span data-stu-id="7f331-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="7f331-113">*Nombre* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7f331-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f331-114">Nombre d’entrées de rapport à récupérer de l’objet de rapport.</span><span class="sxs-lookup"><span data-stu-id="7f331-114">Number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="7f331-115">La valeur zéro indique que toutes les entrées de rapport à partir de *startIndex* doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="7f331-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="7f331-116">Au retour, contient le nombre d’entrées dans le tableau *ReportSummaryEntries* .</span><span class="sxs-lookup"><span data-stu-id="7f331-116">On return, contains the number of entries in the *ReportSummaryEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="7f331-117">*ReportSummaryEntries* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7f331-117">*ReportSummaryEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f331-118">Retourne un tableau de [**classes \_ TSLicenseReportSummaryEntry Win32**](win32-tslicensereportsummaryentry.md) .</span><span class="sxs-lookup"><span data-stu-id="7f331-118">Returns an array of [**Win32\_TSLicenseReportSummaryEntry**](win32-tslicensereportsummaryentry.md) classes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f331-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f331-119">Return value</span></span>

<span data-ttu-id="7f331-120">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="7f331-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="7f331-121">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="7f331-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="7f331-122">La valeur **lserver je n’y a \_ \_ plus de \_ \_ données** (0x4001) indique qu’il n’y a plus d’entrées de rapport.</span><span class="sxs-lookup"><span data-stu-id="7f331-122">A value of **LSERVER\_I\_NO\_MORE\_DATA** (0x4001) indicates that there are no more report entries.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f331-123">Notes</span><span class="sxs-lookup"><span data-stu-id="7f331-123">Remarks</span></span>

<span data-ttu-id="7f331-124">Il ne s’agit pas d’une méthode statique.</span><span class="sxs-lookup"><span data-stu-id="7f331-124">This is not a static method.</span></span> <span data-ttu-id="7f331-125">Cette méthode doit être appelée à partir d’un objet de rapport d’utilisation de licence par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7f331-125">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="7f331-126">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="7f331-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="7f331-127">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="7f331-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7f331-128">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7f331-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7f331-129">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="7f331-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7f331-130">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7f331-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f331-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f331-131">Requirements</span></span>



| <span data-ttu-id="7f331-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f331-132">Requirement</span></span> | <span data-ttu-id="7f331-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f331-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f331-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f331-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7f331-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f331-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="7f331-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f331-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7f331-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f331-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="7f331-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7f331-138">Namespace</span></span><br/>                | <span data-ttu-id="7f331-139">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="7f331-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="7f331-140">MOF</span><span class="sxs-lookup"><span data-stu-id="7f331-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f331-141"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f331-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f331-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7f331-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f331-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f331-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f331-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f331-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f331-145">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="7f331-145">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="7f331-146">**\_TSLicenseReportSummaryEntry Win32**</span><span class="sxs-lookup"><span data-stu-id="7f331-146">**Win32\_TSLicenseReportSummaryEntry**</span></span>](win32-tslicensereportsummaryentry.md)
</dt> </dl>

 

