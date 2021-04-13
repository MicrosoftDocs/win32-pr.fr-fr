---
title: Classe Win32_TSLicenseReportFailedPerUserEntry
description: Fournit des détails sur la licence d’accès client Services Bureau à distance par utilisateur (RDS \ 160 ; CAL par utilisateur).
ms.assetid: 27d155a4-938e-4bca-8d15-03c44740e506
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportFailedPerUserEntry de la classe Services Bureau à distance
- Win32_TSLicenseReportFailedPerUserEntry de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserEntry
- Win32_TSLicenseReportFailedPerUserEntry.User
- Win32_TSLicenseReportFailedPerUserEntry.TriedIssuanceOn
- Win32_TSLicenseReportFailedPerUserEntry.CALType
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersion
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18098ce0510a39f6083edcf688a18c10a3e20278
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383951"
---
# <a name="win32_tslicensereportfailedperuserentry-class"></a><span data-ttu-id="c993a-105">\_Classe TSLicenseReportFailedPerUserEntry Win32</span><span class="sxs-lookup"><span data-stu-id="c993a-105">Win32\_TSLicenseReportFailedPerUserEntry class</span></span>

<span data-ttu-id="c993a-106">Fournit des détails sur l’échec de la licence d’accès client par utilisateur (CAL par utilisateur) Services Bureau à distance par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c993a-106">Provides details about the failed Remote Desktop Services Per User client access license (RDS Per User CAL).</span></span>

<span data-ttu-id="c993a-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c993a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c993a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c993a-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserEntry
{
  string   User;
  DATETIME TriedIssuanceOn;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="c993a-109">Membres</span><span class="sxs-lookup"><span data-stu-id="c993a-109">Members</span></span>

<span data-ttu-id="c993a-110">La classe **Win32 \_ TSLicenseReportFailedPerUserEntry** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c993a-110">The **Win32\_TSLicenseReportFailedPerUserEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="c993a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c993a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c993a-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c993a-112">Properties</span></span>

<span data-ttu-id="c993a-113">La classe **Win32 \_ TSLicenseReportFailedPerUserEntry** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c993a-113">The **Win32\_TSLicenseReportFailedPerUserEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c993a-114">**CALType**</span><span class="sxs-lookup"><span data-stu-id="c993a-114">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c993a-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c993a-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c993a-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c993a-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c993a-117">Spécifie le type de licence d’accès client émise.</span><span class="sxs-lookup"><span data-stu-id="c993a-117">Specifies the type of CAL issued.</span></span> <span data-ttu-id="c993a-118">Il s’agit de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c993a-118">This will be one of the following values.</span></span>

<span data-ttu-id="c993a-119">« CAL TS par périphérique » intégrée</span><span class="sxs-lookup"><span data-stu-id="c993a-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="c993a-120">« CAL TS par périphérique »</span><span class="sxs-lookup"><span data-stu-id="c993a-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="c993a-121">« CAL du connecteur Internet TS »</span><span class="sxs-lookup"><span data-stu-id="c993a-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="c993a-122">« CAL TS par utilisateur »</span><span class="sxs-lookup"><span data-stu-id="c993a-122">"TS Per User CAL"</span></span>

<span data-ttu-id="c993a-123">Licence d’accès client « TS ou RDS par périphérique »</span><span class="sxs-lookup"><span data-stu-id="c993a-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="c993a-124">Licence d’accès client TS ou RDS par utilisateur</span><span class="sxs-lookup"><span data-stu-id="c993a-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="c993a-125">« Licence d’abonnement VDI standard suite par périphérique »</span><span class="sxs-lookup"><span data-stu-id="c993a-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="c993a-126">« Licence d’abonnement VDI Premium suite par appareil »</span><span class="sxs-lookup"><span data-stu-id="c993a-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="c993a-127">« SERVICES CAL par périphérique »</span><span class="sxs-lookup"><span data-stu-id="c993a-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="c993a-128">« Licences d’accès client des services Bureau à distance par utilisateur »</span><span class="sxs-lookup"><span data-stu-id="c993a-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="c993a-129">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="c993a-129">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c993a-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c993a-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c993a-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c993a-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c993a-132">Version de Services Bureau à distance pour laquelle la licence d’accès client des services Bureau à distance a été émise.</span><span class="sxs-lookup"><span data-stu-id="c993a-132">The version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span> <span data-ttu-id="c993a-133">Il s’agit de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c993a-133">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="c993a-134">« Windows Server 2012 »</span><span class="sxs-lookup"><span data-stu-id="c993a-134">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="c993a-135">Seuls les serveurs exécutant Windows Server 2012, Windows Server 2008 R2 ou Windows Server 2008 sont pris en charge avec cette licence.</span><span class="sxs-lookup"><span data-stu-id="c993a-135">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="c993a-136">« Windows Server 7 »</span><span class="sxs-lookup"><span data-stu-id="c993a-136">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="c993a-137">Seuls les serveurs exécutant Windows Server 2008 R2 ou Windows Server 2008 sont pris en charge avec cette licence.</span><span class="sxs-lookup"><span data-stu-id="c993a-137">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="c993a-138">« Windows Server 2008 »</span><span class="sxs-lookup"><span data-stu-id="c993a-138">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="c993a-139">Seuls les serveurs exécutant Windows Server 2008 sont pris en charge avec cette licence.</span><span class="sxs-lookup"><span data-stu-id="c993a-139">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c993a-140">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="c993a-140">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c993a-141">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c993a-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c993a-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c993a-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c993a-143">Identificateur de la version du produit pour le Services Bureau à distance le jeu de clés de licence.</span><span class="sxs-lookup"><span data-stu-id="c993a-143">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="c993a-144">4</span><span class="sxs-lookup"><span data-stu-id="c993a-144">4</span></span>
</dt> <dd>

<span data-ttu-id="c993a-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c993a-145">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="c993a-146">3</span><span class="sxs-lookup"><span data-stu-id="c993a-146">3</span></span>
</dt> <dd>

<span data-ttu-id="c993a-147">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c993a-147">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="c993a-148">2</span><span class="sxs-lookup"><span data-stu-id="c993a-148">2</span></span>
</dt> <dd>

<span data-ttu-id="c993a-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c993a-149">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="c993a-150">1</span><span class="sxs-lookup"><span data-stu-id="c993a-150">1</span></span>
</dt> <dd>

<span data-ttu-id="c993a-151">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c993a-151">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c993a-152">0</span><span class="sxs-lookup"><span data-stu-id="c993a-152">0</span></span>
</dt> <dd>

<span data-ttu-id="c993a-153">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c993a-153">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c993a-154">**TriedIssuanceOn**</span><span class="sxs-lookup"><span data-stu-id="c993a-154">**TriedIssuanceOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c993a-155">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c993a-155">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="c993a-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c993a-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c993a-157">Date à laquelle l’émission de la licence a été tentée.</span><span class="sxs-lookup"><span data-stu-id="c993a-157">The date on which license issuance was attempted.</span></span>

</dd> <dt>

<span data-ttu-id="c993a-158">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="c993a-158">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c993a-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c993a-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c993a-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c993a-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c993a-161">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c993a-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c993a-162">Nom de l’utilisateur pour lequel l’émission de la licence a été tentée.</span><span class="sxs-lookup"><span data-stu-id="c993a-162">The name of the user to whom the license issuance was attempted.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c993a-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c993a-163">Requirements</span></span>



| <span data-ttu-id="c993a-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c993a-164">Requirement</span></span> | <span data-ttu-id="c993a-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="c993a-165">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c993a-166">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c993a-166">Minimum supported client</span></span><br/> | <span data-ttu-id="c993a-167">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c993a-167">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="c993a-168">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c993a-168">Minimum supported server</span></span><br/> | <span data-ttu-id="c993a-169">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c993a-169">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="c993a-170">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c993a-170">Namespace</span></span><br/>                | <span data-ttu-id="c993a-171">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="c993a-171">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="c993a-172">MOF</span><span class="sxs-lookup"><span data-stu-id="c993a-172">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c993a-173"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c993a-173"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c993a-174">DLL</span><span class="sxs-lookup"><span data-stu-id="c993a-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c993a-175"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c993a-175"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c993a-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c993a-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c993a-177">**FetchReportFailedPerUserEntries**</span><span class="sxs-lookup"><span data-stu-id="c993a-177">**FetchReportFailedPerUserEntries**</span></span>](fetchreportfailedperuserentries-win32-tslicensereport.md)
</dt> </dl>

 

