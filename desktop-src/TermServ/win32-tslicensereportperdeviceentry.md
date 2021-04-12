---
title: Classe Win32_TSLicenseReportPerDeviceEntry
description: Fournit des détails sur la licence d’accès client par périphérique Services Bureau à distance par périphérique (RDS \ 160 ; Licence d’accès client par périphérique).
ms.assetid: b26f2518-439c-4562-9492-a0cfa60c457a
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportPerDeviceEntry de la classe Services Bureau à distance
- Win32_TSLicenseReportPerDeviceEntry de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportPerDeviceEntry
- Win32_TSLicenseReportPerDeviceEntry.sIssuedToComputer
- Win32_TSLicenseReportPerDeviceEntry.sHardwareId
- Win32_TSLicenseReportPerDeviceEntry.ExpirationDate
- Win32_TSLicenseReportPerDeviceEntry.CALType
- Win32_TSLicenseReportPerDeviceEntry.ProductVersion
- Win32_TSLicenseReportPerDeviceEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a120d477ff03675f160d94f1506f59cdf1462fa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464471"
---
# <a name="win32_tslicensereportperdeviceentry-class"></a><span data-ttu-id="8c094-105">\_Classe TSLicenseReportPerDeviceEntry Win32</span><span class="sxs-lookup"><span data-stu-id="8c094-105">Win32\_TSLicenseReportPerDeviceEntry class</span></span>

<span data-ttu-id="8c094-106">Fournit des détails sur la licence d’accès client par périphérique (CAL par périphérique) qui a échoué Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="8c094-106">Provides details about the failed Remote Desktop Services Per Device client access license (RDS Per Device CAL).</span></span>

<span data-ttu-id="8c094-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8c094-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c094-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c094-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportPerDeviceEntry
{
  string   sIssuedToComputer;
  string   sHardwareId;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="8c094-109">Membres</span><span class="sxs-lookup"><span data-stu-id="8c094-109">Members</span></span>

<span data-ttu-id="8c094-110">La classe **Win32 \_ TSLicenseReportPerDeviceEntry** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8c094-110">The **Win32\_TSLicenseReportPerDeviceEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="8c094-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8c094-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c094-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8c094-112">Properties</span></span>

<span data-ttu-id="8c094-113">La classe **Win32 \_ TSLicenseReportPerDeviceEntry** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8c094-113">The **Win32\_TSLicenseReportPerDeviceEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c094-114">**CALType**</span><span class="sxs-lookup"><span data-stu-id="8c094-114">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c094-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c094-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c094-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8c094-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c094-117">Spécifie le type de licence d’accès client émise.</span><span class="sxs-lookup"><span data-stu-id="8c094-117">Specifies the type of CAL issued.</span></span> <span data-ttu-id="8c094-118">Il s’agit de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8c094-118">This will be one of the following values.</span></span>

<span data-ttu-id="8c094-119">« CAL TS par périphérique » intégrée</span><span class="sxs-lookup"><span data-stu-id="8c094-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="8c094-120">« CAL TS par périphérique »</span><span class="sxs-lookup"><span data-stu-id="8c094-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="8c094-121">« CAL du connecteur Internet TS »</span><span class="sxs-lookup"><span data-stu-id="8c094-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="8c094-122">« CAL TS par utilisateur »</span><span class="sxs-lookup"><span data-stu-id="8c094-122">"TS Per User CAL"</span></span>

<span data-ttu-id="8c094-123">Licence d’accès client « TS ou RDS par périphérique »</span><span class="sxs-lookup"><span data-stu-id="8c094-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="8c094-124">Licence d’accès client TS ou RDS par utilisateur</span><span class="sxs-lookup"><span data-stu-id="8c094-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="8c094-125">« Licence d’abonnement VDI standard suite par périphérique »</span><span class="sxs-lookup"><span data-stu-id="8c094-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="8c094-126">« Licence d’abonnement VDI Premium suite par appareil »</span><span class="sxs-lookup"><span data-stu-id="8c094-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="8c094-127">« SERVICES CAL par périphérique »</span><span class="sxs-lookup"><span data-stu-id="8c094-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="8c094-128">« Licences d’accès client des services Bureau à distance par utilisateur »</span><span class="sxs-lookup"><span data-stu-id="8c094-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="8c094-129">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="8c094-129">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c094-130">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8c094-130">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="8c094-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8c094-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c094-132">Date d’expiration de la licence.</span><span class="sxs-lookup"><span data-stu-id="8c094-132">The expiration date of the license.</span></span>

</dd> <dt>

<span data-ttu-id="8c094-133">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="8c094-133">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c094-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c094-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c094-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8c094-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c094-136">Version de Services Bureau à distance pour laquelle la licence d’accès client des services Bureau à distance a été émise.</span><span class="sxs-lookup"><span data-stu-id="8c094-136">The version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span> <span data-ttu-id="8c094-137">Il s’agit de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8c094-137">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="8c094-138">« Windows Server 2012 »</span><span class="sxs-lookup"><span data-stu-id="8c094-138">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="8c094-139">Seuls les serveurs exécutant Windows Server 2012, Windows Server 2008 R2 ou Windows Server 2008 sont pris en charge avec cette licence.</span><span class="sxs-lookup"><span data-stu-id="8c094-139">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="8c094-140">« Windows Server 7 »</span><span class="sxs-lookup"><span data-stu-id="8c094-140">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="8c094-141">Seuls les serveurs exécutant Windows Server 2008 R2 ou Windows Server 2008 sont pris en charge avec cette licence.</span><span class="sxs-lookup"><span data-stu-id="8c094-141">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="8c094-142">« Windows Server 2008 »</span><span class="sxs-lookup"><span data-stu-id="8c094-142">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="8c094-143">Seuls les serveurs exécutant Windows Server 2008 sont pris en charge avec cette licence.</span><span class="sxs-lookup"><span data-stu-id="8c094-143">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8c094-144">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="8c094-144">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c094-145">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8c094-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c094-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8c094-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c094-147">Identificateur de la version du produit pour le Services Bureau à distance le jeu de clés de licence.</span><span class="sxs-lookup"><span data-stu-id="8c094-147">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="8c094-148">4</span><span class="sxs-lookup"><span data-stu-id="8c094-148">4</span></span>
</dt> <dd>

<span data-ttu-id="8c094-149">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8c094-149">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="8c094-150">3</span><span class="sxs-lookup"><span data-stu-id="8c094-150">3</span></span>
</dt> <dd>

<span data-ttu-id="8c094-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8c094-151">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="8c094-152">2</span><span class="sxs-lookup"><span data-stu-id="8c094-152">2</span></span>
</dt> <dd>

<span data-ttu-id="8c094-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c094-153">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="8c094-154">1</span><span class="sxs-lookup"><span data-stu-id="8c094-154">1</span></span>
</dt> <dd>

<span data-ttu-id="8c094-155">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8c094-155">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8c094-156">0</span><span class="sxs-lookup"><span data-stu-id="8c094-156">0</span></span>
</dt> <dd>

<span data-ttu-id="8c094-157">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8c094-157">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8c094-158">**sHardwareId**</span><span class="sxs-lookup"><span data-stu-id="8c094-158">**sHardwareId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c094-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c094-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c094-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8c094-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c094-161">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8c094-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8c094-162">Identificateur matériel de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8c094-162">The hardware identifier of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="8c094-163">**sIssuedToComputer**</span><span class="sxs-lookup"><span data-stu-id="8c094-163">**sIssuedToComputer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c094-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c094-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c094-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8c094-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c094-166">Nom de l’ordinateur pour lequel l’émission de la licence a été tentée.</span><span class="sxs-lookup"><span data-stu-id="8c094-166">The name of the computer that the license issuance was attempted for.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c094-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c094-167">Requirements</span></span>



| <span data-ttu-id="8c094-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c094-168">Requirement</span></span> | <span data-ttu-id="8c094-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c094-169">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c094-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c094-170">Minimum supported client</span></span><br/> | <span data-ttu-id="8c094-171">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c094-171">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="8c094-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c094-172">Minimum supported server</span></span><br/> | <span data-ttu-id="8c094-173">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8c094-173">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="8c094-174">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8c094-174">Namespace</span></span><br/>                | <span data-ttu-id="8c094-175">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="8c094-175">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="8c094-176">MOF</span><span class="sxs-lookup"><span data-stu-id="8c094-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c094-177"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c094-177"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c094-178">DLL</span><span class="sxs-lookup"><span data-stu-id="8c094-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c094-179"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c094-179"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c094-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c094-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c094-181">**FetchReportPerDeviceEntries**</span><span class="sxs-lookup"><span data-stu-id="8c094-181">**FetchReportPerDeviceEntries**</span></span>](fetchreportperdeviceentries-win32-tslicensereport.md)
</dt> </dl>

 

