---
title: Classe Win32_TSLicenseReportSummaryEntry
description: Fournit un résumé des Services Bureau à distance installées et émises par les licences d’accès client par utilisateur (RDS \ 160 ; Cal par utilisateur).
ms.assetid: 0FD3BFFE-58B9-4037-969F-8C2323136C9D
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportSummaryEntry de la classe Services Bureau à distance
- Win32_TSLicenseReportSummaryEntry de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportSummaryEntry
- Win32_TSLicenseReportSummaryEntry.ProductVersion
- Win32_TSLicenseReportSummaryEntry.ProductVersionID
- Win32_TSLicenseReportSummaryEntry.TSCALType
- Win32_TSLicenseReportSummaryEntry.InstalledLicenses
- Win32_TSLicenseReportSummaryEntry.IssuedLicenses
- Win32_TSLicenseReportSummaryEntry.TSCALAvailability
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34482e9c6199ef6586024d43d586421a54071ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511737"
---
# <a name="win32_tslicensereportsummaryentry-class"></a><span data-ttu-id="6c3f4-105">\_Classe TSLicenseReportSummaryEntry Win32</span><span class="sxs-lookup"><span data-stu-id="6c3f4-105">Win32\_TSLicenseReportSummaryEntry class</span></span>

<span data-ttu-id="6c3f4-106">Fournit un résumé des Services Bureau à distance installées et émises par les licences d’accès client par utilisateur (licences d’accès client des services Bureau à distance par utilisateur).</span><span class="sxs-lookup"><span data-stu-id="6c3f4-106">Provides a summary of the installed and issued Remote Desktop Services Per User client access licenses (RDS Per User CALs).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c3f4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c3f4-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportSummaryEntry
{
  string ProductVersion;
  uint32 ProductVersionID;
  string TSCALType;
  uint32 InstalledLicenses;
  uint32 IssuedLicenses;
  string TSCALAvailability;
};
```

## <a name="members"></a><span data-ttu-id="6c3f4-108">Membres</span><span class="sxs-lookup"><span data-stu-id="6c3f4-108">Members</span></span>

<span data-ttu-id="6c3f4-109">La classe **Win32 \_ TSLicenseReportSummaryEntry** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6c3f4-109">The **Win32\_TSLicenseReportSummaryEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="6c3f4-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6c3f4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c3f4-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6c3f4-111">Properties</span></span>

<span data-ttu-id="6c3f4-112">La classe **Win32 \_ TSLicenseReportSummaryEntry** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-112">The **Win32\_TSLicenseReportSummaryEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c3f4-113">**InstalledLicenses**</span><span class="sxs-lookup"><span data-stu-id="6c3f4-113">**InstalledLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c3f4-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c3f4-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c3f4-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6c3f4-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c3f4-116">Nombre de licences d’accès client des services Bureau à distance par utilisateur installées.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-116">Number of RDS Per User CALs that are installed.</span></span>

</dd> <dt>

<span data-ttu-id="6c3f4-117">**IssuedLicenses**</span><span class="sxs-lookup"><span data-stu-id="6c3f4-117">**IssuedLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c3f4-118">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c3f4-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c3f4-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6c3f4-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c3f4-120">Nombre de licences d’accès client des services Bureau à distance par utilisateur émises.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-120">Number of RDS Per User CALs that are issued.</span></span>

</dd> <dt>

<span data-ttu-id="6c3f4-121">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="6c3f4-121">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c3f4-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6c3f4-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c3f4-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6c3f4-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c3f4-124">Version de Services Bureau à distance pour laquelle la licence d’accès client des services Bureau à distance a été émise.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-124">Version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span>

<dt>

<span data-ttu-id="6c3f4-125">« Windows Server 2012 »</span><span class="sxs-lookup"><span data-stu-id="6c3f4-125">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="6c3f4-126">Seuls les serveurs exécutant Windows Server 2012, Windows Server 2008 R2 ou Windows Server 2008 sont pris en charge avec cette licence.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-126">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="6c3f4-127">« Windows Server 7 »</span><span class="sxs-lookup"><span data-stu-id="6c3f4-127">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="6c3f4-128">Seuls les serveurs exécutant Windows Server 2008 R2 ou Windows Server 2008 sont pris en charge avec cette licence.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-128">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="6c3f4-129">« Windows Server 2008 »</span><span class="sxs-lookup"><span data-stu-id="6c3f4-129">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="6c3f4-130">Seuls les serveurs exécutant Windows Server 2008 sont pris en charge avec cette licence.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-130">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6c3f4-131">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="6c3f4-131">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c3f4-132">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c3f4-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c3f4-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6c3f4-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c3f4-134">Identificateur de la version du produit pour le Services Bureau à distance le jeu de clés de licence.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-134">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="6c3f4-135">4</span><span class="sxs-lookup"><span data-stu-id="6c3f4-135">4</span></span>
</dt> <dd>

<span data-ttu-id="6c3f4-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6c3f4-136">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="6c3f4-137">3</span><span class="sxs-lookup"><span data-stu-id="6c3f4-137">3</span></span>
</dt> <dd>

<span data-ttu-id="6c3f4-138">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6c3f4-138">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="6c3f4-139">2</span><span class="sxs-lookup"><span data-stu-id="6c3f4-139">2</span></span>
</dt> <dd>

<span data-ttu-id="6c3f4-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c3f4-140">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="6c3f4-141">1</span><span class="sxs-lookup"><span data-stu-id="6c3f4-141">1</span></span>
</dt> <dd>

<span data-ttu-id="6c3f4-142">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-142">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6c3f4-143">0</span><span class="sxs-lookup"><span data-stu-id="6c3f4-143">0</span></span>
</dt> <dd>

<span data-ttu-id="6c3f4-144">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-144">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6c3f4-145">**TSCALAvailability**</span><span class="sxs-lookup"><span data-stu-id="6c3f4-145">**TSCALAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c3f4-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6c3f4-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c3f4-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6c3f4-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c3f4-148">Disponibilité des licences d’accès client des services Bureau à distance par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-148">The availability of the RDS Per User CALs.</span></span> <span data-ttu-id="6c3f4-149">Il s’agit de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-149">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="6c3f4-150">Téléchargé</span><span class="sxs-lookup"><span data-stu-id="6c3f4-150">"Available"</span></span>
</dt> <dd>

<span data-ttu-id="6c3f4-151">Les licences d’accès client des services Bureau à distance par utilisateur sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-151">The RDS Per User CALs are available.</span></span>

</dd> <dt>

<span data-ttu-id="6c3f4-152">Certaine</span><span class="sxs-lookup"><span data-stu-id="6c3f4-152">"Limited"</span></span>
</dt> <dd>

<span data-ttu-id="6c3f4-153">La disponibilité des CAL par utilisateur des services Bureau à distance est limitée.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-153">The availability of the RDS Per User CALs is limited.</span></span>

</dd> <dt>

<span data-ttu-id="6c3f4-154">"None"</span><span class="sxs-lookup"><span data-stu-id="6c3f4-154">"None"</span></span>
</dt> <dd>

<span data-ttu-id="6c3f4-155">Les CAL par utilisateur des services Bureau à distance ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-155">The RDS Per User CALs are not available.</span></span>

</dd> <dt>

<span data-ttu-id="6c3f4-156">« Pas de suivi »</span><span class="sxs-lookup"><span data-stu-id="6c3f4-156">"Not Tracking"</span></span>
</dt> <dd>

<span data-ttu-id="6c3f4-157">La disponibilité des licences d’accès client des services Bureau à distance par utilisateur n’est pas suivie.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-157">The availability of the RDS Per User CALs is not being tracked.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6c3f4-158">**TSCALType**</span><span class="sxs-lookup"><span data-stu-id="6c3f4-158">**TSCALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c3f4-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6c3f4-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c3f4-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6c3f4-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c3f4-161">Type de licences d’accès client aux services Bureau à distance par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-161">The type of RDS Per User CALs.</span></span> <span data-ttu-id="6c3f4-162">Il s’agit de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-162">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="6c3f4-163">« Par appareil »</span><span class="sxs-lookup"><span data-stu-id="6c3f4-163">"Per Device"</span></span>
</dt> <dd>

<span data-ttu-id="6c3f4-164">Les licences d’accès client des services Bureau à distance par utilisateur sont émises par appareil.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-164">The RDS Per User CALs are issued per device.</span></span>

</dd> <dt>

<span data-ttu-id="6c3f4-165">« Par utilisateur »</span><span class="sxs-lookup"><span data-stu-id="6c3f4-165">"Per User"</span></span>
</dt> <dd>

<span data-ttu-id="6c3f4-166">Les licences d’accès client des services Bureau à distance par utilisateur sont émises par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-166">The RDS Per User CALs are issued per user.</span></span>

</dd> <dt>

<span data-ttu-id="6c3f4-167">Connue</span><span class="sxs-lookup"><span data-stu-id="6c3f4-167">"Unknown"</span></span>
</dt> <dd>

<span data-ttu-id="6c3f4-168">Le type de licences d’accès client aux services Bureau à distance par utilisateur est inconnu.</span><span class="sxs-lookup"><span data-stu-id="6c3f4-168">The type of RDS Per User CALs is unknown.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c3f4-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c3f4-169">Requirements</span></span>



| <span data-ttu-id="6c3f4-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c3f4-170">Requirement</span></span> | <span data-ttu-id="6c3f4-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c3f4-171">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c3f4-172">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c3f4-172">Minimum supported client</span></span><br/> | <span data-ttu-id="6c3f4-173">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c3f4-173">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="6c3f4-174">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c3f4-174">Minimum supported server</span></span><br/> | <span data-ttu-id="6c3f4-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c3f4-175">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="6c3f4-176">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6c3f4-176">Namespace</span></span><br/>                | <span data-ttu-id="6c3f4-177">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="6c3f4-177">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="6c3f4-178">MOF</span><span class="sxs-lookup"><span data-stu-id="6c3f4-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c3f4-179"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c3f4-179"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c3f4-180">DLL</span><span class="sxs-lookup"><span data-stu-id="6c3f4-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c3f4-181"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c3f4-181"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



 

 





