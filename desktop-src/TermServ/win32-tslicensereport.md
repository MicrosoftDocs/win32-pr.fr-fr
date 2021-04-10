---
title: Classe Win32_TSLicenseReport
description: Fournit des instances de Services Bureau à distance licence d’accès client par utilisateur (RDS \ 160 ; Les rapports d’utilisation des licences d’accès client par utilisateur) qui sont générés sur le serveur de licences Bureau à distance, ainsi que les méthodes de génération, d’extraction et de suppression des rapports de licence.
ms.assetid: 8d67f158-cda3-4cf4-a766-09d08c21c49e
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReport de la classe Services Bureau à distance
- Win32_TSLicenseReport de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport
- Win32_TSLicenseReport.FileName
- Win32_TSLicenseReport.LicenseUsageCount
- Win32_TSLicenseReport.InstalledLicenses
- Win32_TSLicenseReport.GenerationDateTime
- Win32_TSLicenseReport.ScopeType
- Win32_TSLicenseReport.ScopeValue
- Win32_TSLicenseReport.Version
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de997056222c1b525253f320f6fe191f017614f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843177"
---
# <a name="win32_tslicensereport-class"></a><span data-ttu-id="0ee39-105">\_Classe TSLicenseReport Win32</span><span class="sxs-lookup"><span data-stu-id="0ee39-105">Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="0ee39-106">Fournit des instances de Services Bureau à distance les rapports d’utilisation de licence d’accès client par utilisateur (CAL par utilisateur) qui sont générés sur le serveur de licences Bureau à distance et les méthodes pour la génération de rapports de licence, les opérations d’extraction et de suppression.</span><span class="sxs-lookup"><span data-stu-id="0ee39-106">Provides instances of Remote Desktop Services Per User client access license (RDS Per User CAL) usage reports that are generated on the Remote Desktop license server, and methods for license report generation, fetch, and delete operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ee39-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ee39-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseReport
{
  string   FileName;
  uint32   LicenseUsageCount;
  uint32   InstalledLicenses;
  DATETIME GenerationDateTime;
  uint32   ScopeType;
  string   ScopeValue;
  uint32   Version;
};
```

## <a name="members"></a><span data-ttu-id="0ee39-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0ee39-108">Members</span></span>

<span data-ttu-id="0ee39-109">La classe **Win32 \_ TSLicenseReport** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0ee39-109">The **Win32\_TSLicenseReport** class has these types of members:</span></span>

-   [<span data-ttu-id="0ee39-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0ee39-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0ee39-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0ee39-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0ee39-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0ee39-112">Methods</span></span>

<span data-ttu-id="0ee39-113">La classe **Win32 \_ TSLicenseReport** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0ee39-113">The **Win32\_TSLicenseReport** class has these methods.</span></span>



| <span data-ttu-id="0ee39-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="0ee39-114">Method</span></span>                                                                                                         | <span data-ttu-id="0ee39-115">Description</span><span class="sxs-lookup"><span data-stu-id="0ee39-115">Description</span></span>                                                                                                                                                                                     |
|:---------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ee39-116">**DeleteReport**</span><span class="sxs-lookup"><span data-stu-id="0ee39-116">**DeleteReport**</span></span>](deletereport-win32-tslicensereport.md)                                                     | <span data-ttu-id="0ee39-117">Supprime un objet de rapport sur le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="0ee39-117">Deletes a report object on the Remote Desktop license server.</span></span> <span data-ttu-id="0ee39-118">Il ne s’agit pas d’une méthode statique.</span><span class="sxs-lookup"><span data-stu-id="0ee39-118">This is not a static method.</span></span><br/>                                                                                           |
| [<span data-ttu-id="0ee39-119">**FetchReportEntries**</span><span class="sxs-lookup"><span data-stu-id="0ee39-119">**FetchReportEntries**</span></span>](fetchreportentries-win32-tslicensereport.md)                                         | <span data-ttu-id="0ee39-120">Récupère les entrées dans l’objet de rapport.</span><span class="sxs-lookup"><span data-stu-id="0ee39-120">Retrieves entries in the report object.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="0ee39-121">**FetchReportFailedPerUserEntries**</span><span class="sxs-lookup"><span data-stu-id="0ee39-121">**FetchReportFailedPerUserEntries**</span></span>](fetchreportfailedperuserentries-win32-tslicensereport.md)               | <span data-ttu-id="0ee39-122">Récupère les détails des licences d’accès client en échec Services Bureau à distance par utilisateur (RDS par utilisateur Cal par utilisateur) à partir du rapport.</span><span class="sxs-lookup"><span data-stu-id="0ee39-122">Retrieves details of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span><br/>                                                             |
| [<span data-ttu-id="0ee39-123">**FetchReportFailedPerUserSummaryEntries**</span><span class="sxs-lookup"><span data-stu-id="0ee39-123">**FetchReportFailedPerUserSummaryEntries**</span></span>](fetchreportfailedperusersummaryentries-win32-tslicensereport.md) | <span data-ttu-id="0ee39-124">Récupère des informations récapitulatives de la Services Bureau à distance des licences d’accès client par utilisateur (licences d’accès client des services Bureau à distance par utilisateur) ayant échoué à partir du rapport.</span><span class="sxs-lookup"><span data-stu-id="0ee39-124">Retrieves summary information of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span><br/>                                                 |
| [<span data-ttu-id="0ee39-125">**FetchReportPerDeviceEntries**</span><span class="sxs-lookup"><span data-stu-id="0ee39-125">**FetchReportPerDeviceEntries**</span></span>](fetchreportperdeviceentries-win32-tslicensereport.md)                       | <span data-ttu-id="0ee39-126">Récupère des informations sur les licences d’accès client par périphérique Services Bureau à distance émises par périphérique (CAL par périphérique) à partir du rapport.</span><span class="sxs-lookup"><span data-stu-id="0ee39-126">Retrieves information of issued Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) from the report.</span></span><br/>                                                     |
| [<span data-ttu-id="0ee39-127">**FetchReportSummaryEntries**</span><span class="sxs-lookup"><span data-stu-id="0ee39-127">**FetchReportSummaryEntries**</span></span>](win32-tslicensereport-fetchreportsummaryentries.md)                           | <span data-ttu-id="0ee39-128">Récupère des résumés de licence à partir de l’objet de rapport.</span><span class="sxs-lookup"><span data-stu-id="0ee39-128">Retrieves license summaries from the report object.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="0ee39-129">**GenerateReport**</span><span class="sxs-lookup"><span data-stu-id="0ee39-129">**GenerateReport**</span></span>](generatereport-win32-tslicensereport.md)                                                 | <span data-ttu-id="0ee39-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0ee39-130">This method is not supported.</span></span><br/> <span data-ttu-id="0ee39-131">**Windows server 2008 R2 et Windows server 2008 :** Génère un rapport d’utilisation des licences par utilisateur actuel sur le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="0ee39-131">**Windows Server 2008 R2 and Windows Server 2008:** Generates a current per user license usage report on the Remote Desktop license server.</span></span><br/> |
| [<span data-ttu-id="0ee39-132">**GenerateReportEx**</span><span class="sxs-lookup"><span data-stu-id="0ee39-132">**GenerateReportEx**</span></span>](generatereportex-win32-tslicensereport.md)                                             | <span data-ttu-id="0ee39-133">Génère un rapport d’utilisation des licences par utilisateur actuel sur le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="0ee39-133">Generates a current per user license usage report on the Remote Desktop license server.</span></span><br/>                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="0ee39-134">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0ee39-134">Properties</span></span>

<span data-ttu-id="0ee39-135">La classe **Win32 \_ TSLicenseReport** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0ee39-135">The **Win32\_TSLicenseReport** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0ee39-136">**FileName**</span><span class="sxs-lookup"><span data-stu-id="0ee39-136">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ee39-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ee39-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ee39-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ee39-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ee39-139">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0ee39-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0ee39-140">Nom du rapport.</span><span class="sxs-lookup"><span data-stu-id="0ee39-140">The report name.</span></span>

</dd> <dt>

<span data-ttu-id="0ee39-141">**GenerationDateTime**</span><span class="sxs-lookup"><span data-stu-id="0ee39-141">**GenerationDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ee39-142">Type de données : **[DateTime](/windows/desktop/WmiSdk/datetime)**</span><span class="sxs-lookup"><span data-stu-id="0ee39-142">Data type: **[DATETIME](/windows/desktop/WmiSdk/datetime)**</span></span>
</dt> <dt>

<span data-ttu-id="0ee39-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ee39-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ee39-144">Date et heure de génération du rapport du gestionnaire de licences des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="0ee39-144">RD Licensing report generation date and time.</span></span>

</dd> <dt>

<span data-ttu-id="0ee39-145">**InstalledLicenses**</span><span class="sxs-lookup"><span data-stu-id="0ee39-145">**InstalledLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ee39-146">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ee39-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ee39-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ee39-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ee39-148">Qualificateurs : [ **déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0ee39-148">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0ee39-149">Cette propriété n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0ee39-149">This property is not supported.</span></span>

<span data-ttu-id="0ee39-150">**Windows server 2008 R2 et Windows server 2008 :** Nombre de licences d’accès client des services Bureau à distance par utilisateur installées.</span><span class="sxs-lookup"><span data-stu-id="0ee39-150">**Windows Server 2008 R2 and Windows Server 2008:** Number of RDS Per User CALs that are installed.</span></span>

</dd> <dt>

<span data-ttu-id="0ee39-151">**LicenseUsageCount**</span><span class="sxs-lookup"><span data-stu-id="0ee39-151">**LicenseUsageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ee39-152">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ee39-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ee39-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ee39-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ee39-154">Qualificateurs : [ **déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0ee39-154">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0ee39-155">Cette propriété n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0ee39-155">This property is not supported.</span></span>

<span data-ttu-id="0ee39-156">**Windows server 2008 R2 et Windows server 2008 :** Nombre de licences d’accès client aux services Bureau à distance par utilisateur en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="0ee39-156">**Windows Server 2008 R2 and Windows Server 2008:** Number of RDS Per User CALs that are currently in use.</span></span>

</dd> <dt>

<span data-ttu-id="0ee39-157">**ScopeType**</span><span class="sxs-lookup"><span data-stu-id="0ee39-157">**ScopeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ee39-158">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ee39-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ee39-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ee39-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ee39-160">Qualificateurs : [ **déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0ee39-160">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0ee39-161">Cette propriété n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0ee39-161">This property is not supported.</span></span>

<span data-ttu-id="0ee39-162">**Windows server 2008 R2 et Windows server 2008 :** Type d’étendue du rapport de licences des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="0ee39-162">**Windows Server 2008 R2 and Windows Server 2008:** RD Licensing report scope type.</span></span>

</dd> <dt>

<span data-ttu-id="0ee39-163">**ScopeValue**</span><span class="sxs-lookup"><span data-stu-id="0ee39-163">**ScopeValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ee39-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ee39-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ee39-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ee39-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ee39-166">Qualificateurs : [ **déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0ee39-166">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0ee39-167">Cette propriété n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0ee39-167">This property is not supported.</span></span>

<span data-ttu-id="0ee39-168">**Windows server 2008 R2 et Windows server 2008 :** Valeur de l’étendue du rapport de licences des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="0ee39-168">**Windows Server 2008 R2 and Windows Server 2008:** RD Licensing report scope value.</span></span>

</dd> <dt>

<span data-ttu-id="0ee39-169">**Version**</span><span class="sxs-lookup"><span data-stu-id="0ee39-169">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ee39-170">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ee39-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ee39-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ee39-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ee39-172">Version du rapport de licences des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="0ee39-172">RD Licensing report version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ee39-173">Notes</span><span class="sxs-lookup"><span data-stu-id="0ee39-173">Remarks</span></span>

<span data-ttu-id="0ee39-174">Les rapports générés à l’aide de WMI sont affichés dans le gestionnaire de licences des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="0ee39-174">Reports that are generated by using WMI are displayed in RD Licensing Manager.</span></span> <span data-ttu-id="0ee39-175">Les rapports qui sont supprimés à l’aide de WMI sont également supprimés du gestionnaire de licences des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="0ee39-175">Reports that are deleted by using WMI are also deleted from RD Licensing Manager.</span></span>

<span data-ttu-id="0ee39-176">Pour utiliser cette classe, vous devez être membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="0ee39-176">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="0ee39-177">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="0ee39-177">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0ee39-178">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0ee39-178">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0ee39-179">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="0ee39-179">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0ee39-180">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0ee39-180">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ee39-181">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ee39-181">Requirements</span></span>



| <span data-ttu-id="0ee39-182">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ee39-182">Requirement</span></span> | <span data-ttu-id="0ee39-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ee39-183">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ee39-184">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ee39-184">Minimum supported client</span></span><br/> | <span data-ttu-id="0ee39-185">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ee39-185">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="0ee39-186">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ee39-186">Minimum supported server</span></span><br/> | <span data-ttu-id="0ee39-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ee39-187">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="0ee39-188">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0ee39-188">Namespace</span></span><br/>                | <span data-ttu-id="0ee39-189">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="0ee39-189">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="0ee39-190">MOF</span><span class="sxs-lookup"><span data-stu-id="0ee39-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ee39-191"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ee39-191"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ee39-192">DLL</span><span class="sxs-lookup"><span data-stu-id="0ee39-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ee39-193"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ee39-193"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ee39-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ee39-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ee39-195">**\_TSIssuedLicense Win32**</span><span class="sxs-lookup"><span data-stu-id="0ee39-195">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="0ee39-196">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="0ee39-196">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="0ee39-197">**\_TSLicenseReportEntry Win32**</span><span class="sxs-lookup"><span data-stu-id="0ee39-197">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="0ee39-198">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="0ee39-198">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

