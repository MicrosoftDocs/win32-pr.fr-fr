---
title: Méthode FetchReportEntries de la classe Win32_TSLicenseReport
description: Récupère les détails de Services Bureau à distance licences d’accès client par utilisateur (RDS \ 160 ; Licences d’accès client par utilisateur) à partir du rapport. Chaque entrée représente un objet RDS \ 160 ; Licence d’accès client par utilisateur en cours d’utilisation.
ms.assetid: 151ff95c-4ad3-4d19-936d-1cb08b4d5056
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode FetchReportEntries
- Services Bureau à distance de la méthode FetchReportEntries, classe Win32_TSLicenseReport
- Win32_TSLicenseReport de la classe Services Bureau à distance, méthode FetchReportEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc64c9591444307ba0519da02cf9c6f13d20252e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509289"
---
# <a name="fetchreportentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="2e043-107">Méthode FetchReportEntries de la \_ classe Win32 TSLicenseReport</span><span class="sxs-lookup"><span data-stu-id="2e043-107">FetchReportEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="2e043-108">Récupère les détails de Services Bureau à distance licences d’accès client par utilisateur (licences d’accès client aux services Bureau à distance par utilisateur) à partir du rapport.</span><span class="sxs-lookup"><span data-stu-id="2e043-108">Retrieves details of Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span> <span data-ttu-id="2e043-109">Chaque entrée représente une licence d’accès client des services Bureau à distance par utilisateur en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="2e043-109">Each entry represents a RDS Per User CAL that is currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e043-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e043-110">Syntax</span></span>


```mof
uint32 FetchReportEntries(
  [in]      uint32                     StartIndex,
  [in, out] uint32                     Count,
  [out]     Win32_TSLicenseReportEntry ReportEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="2e043-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e043-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e043-112">*StartIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e043-112">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e043-113">Index de la première entrée de rapport à recevoir.</span><span class="sxs-lookup"><span data-stu-id="2e043-113">Index of the first report entry to be received.</span></span> <span data-ttu-id="2e043-114">La première entrée de rapport a un index de zéro.</span><span class="sxs-lookup"><span data-stu-id="2e043-114">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="2e043-115">*Nombre* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2e043-115">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e043-116">Nombre d’entrées de rapport à récupérer de l’objet de rapport.</span><span class="sxs-lookup"><span data-stu-id="2e043-116">Number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="2e043-117">La valeur zéro indique que toutes les entrées de rapport à partir de *startIndex* doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="2e043-117">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="2e043-118">Au retour, contient le nombre d’entrées dans le tableau *ReportEntries* .</span><span class="sxs-lookup"><span data-stu-id="2e043-118">On return, contains the number of entries in the *ReportEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="2e043-119">*ReportEntries* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2e043-119">*ReportEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e043-120">Retourne un tableau de [**classes \_ TSLicenseReportEntry Win32**](win32-tslicensereportentry.md) .</span><span class="sxs-lookup"><span data-stu-id="2e043-120">Returns an array of [**Win32\_TSLicenseReportEntry**](win32-tslicensereportentry.md) classes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e043-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e043-121">Return value</span></span>

<span data-ttu-id="2e043-122">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="2e043-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2e043-123">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="2e043-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2e043-124">La valeur **lserver je n’y a \_ \_ plus de \_ \_ données** (0x4001) indique qu’il n’y a plus d’entrées de rapport.</span><span class="sxs-lookup"><span data-stu-id="2e043-124">A value of **LSERVER\_I\_NO\_MORE\_DATA** (0x4001) indicates that there are no more report entries.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e043-125">Notes</span><span class="sxs-lookup"><span data-stu-id="2e043-125">Remarks</span></span>

<span data-ttu-id="2e043-126">Il ne s’agit pas d’une méthode statique.</span><span class="sxs-lookup"><span data-stu-id="2e043-126">This is not a static method.</span></span> <span data-ttu-id="2e043-127">Cette méthode doit être appelée à partir d’un objet de rapport d’utilisation de licence par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2e043-127">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="2e043-128">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="2e043-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="2e043-129">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="2e043-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2e043-130">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2e043-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2e043-131">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="2e043-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2e043-132">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2e043-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e043-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e043-133">Requirements</span></span>



| <span data-ttu-id="2e043-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e043-134">Requirement</span></span> | <span data-ttu-id="2e043-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e043-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e043-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e043-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2e043-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e043-137">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="2e043-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e043-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2e043-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e043-139">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="2e043-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2e043-140">Namespace</span></span><br/>                | <span data-ttu-id="2e043-141">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="2e043-141">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="2e043-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2e043-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e043-143"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e043-143"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e043-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2e043-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e043-145"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e043-145"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e043-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e043-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e043-147">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="2e043-147">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="2e043-148">**\_TSLicenseReportEntry Win32**</span><span class="sxs-lookup"><span data-stu-id="2e043-148">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> </dl>

 

