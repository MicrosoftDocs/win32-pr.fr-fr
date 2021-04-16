---
title: Classe Win32_TSLicenseReportEntry
description: Fournit des détails sur la licence d’accès client Services Bureau à distance par utilisateur (RDS \ 160 ; CAL par utilisateur).
ms.assetid: 75fa7f39-af5b-45a0-ba2b-5c667edfec16
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportEntry de la classe Services Bureau à distance
- Win32_TSLicenseReportEntry de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportEntry
- Win32_TSLicenseReportEntry.User
- Win32_TSLicenseReportEntry.ExpirationDate
- Win32_TSLicenseReportEntry.CALType
- Win32_TSLicenseReportEntry.ProductVersion
- Win32_TSLicenseReportEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44fa97a91561a9d4cf3fd571c773288796754858
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383952"
---
# <a name="win32_tslicensereportentry-class"></a><span data-ttu-id="83020-105">\_Classe TSLicenseReportEntry Win32</span><span class="sxs-lookup"><span data-stu-id="83020-105">Win32\_TSLicenseReportEntry class</span></span>

<span data-ttu-id="83020-106">Fournit des détails sur la licence d’accès client par utilisateur Services Bureau à distance émis (RDS par utilisateur).</span><span class="sxs-lookup"><span data-stu-id="83020-106">Provides details of the issued Remote Desktop Services Per User client access license (RDS Per User CAL).</span></span>

## <a name="syntax"></a><span data-ttu-id="83020-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83020-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportEntry
{
  string   User;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="83020-108">Membres</span><span class="sxs-lookup"><span data-stu-id="83020-108">Members</span></span>

<span data-ttu-id="83020-109">La classe **Win32 \_ TSLicenseReportEntry** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="83020-109">The **Win32\_TSLicenseReportEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="83020-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="83020-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83020-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="83020-111">Properties</span></span>

<span data-ttu-id="83020-112">La classe **Win32 \_ TSLicenseReportEntry** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="83020-112">The **Win32\_TSLicenseReportEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83020-113">**CALType**</span><span class="sxs-lookup"><span data-stu-id="83020-113">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83020-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="83020-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83020-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83020-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83020-116">Spécifie le type de licence d’accès client émise.</span><span class="sxs-lookup"><span data-stu-id="83020-116">Specifies the type of CAL issued.</span></span> <span data-ttu-id="83020-117">Il s’agit de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="83020-117">This will be one of the following values.</span></span>

<span data-ttu-id="83020-118">**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="83020-118">**Windows Server 2008 R2 and Windows Server 2008:** This property is not supported.</span></span>

<span data-ttu-id="83020-119">« CAL TS par périphérique » intégrée</span><span class="sxs-lookup"><span data-stu-id="83020-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="83020-120">« CAL TS par périphérique »</span><span class="sxs-lookup"><span data-stu-id="83020-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="83020-121">« CAL du connecteur Internet TS »</span><span class="sxs-lookup"><span data-stu-id="83020-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="83020-122">« CAL TS par utilisateur »</span><span class="sxs-lookup"><span data-stu-id="83020-122">"TS Per User CAL"</span></span>

<span data-ttu-id="83020-123">Licence d’accès client « TS ou RDS par périphérique »</span><span class="sxs-lookup"><span data-stu-id="83020-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="83020-124">Licence d’accès client TS ou RDS par utilisateur</span><span class="sxs-lookup"><span data-stu-id="83020-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="83020-125">« Licence d’abonnement VDI standard suite par périphérique »</span><span class="sxs-lookup"><span data-stu-id="83020-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="83020-126">« Licence d’abonnement VDI Premium suite par appareil »</span><span class="sxs-lookup"><span data-stu-id="83020-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="83020-127">« SERVICES CAL par périphérique »</span><span class="sxs-lookup"><span data-stu-id="83020-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="83020-128">« Licences d’accès client des services Bureau à distance par utilisateur »</span><span class="sxs-lookup"><span data-stu-id="83020-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="83020-129">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="83020-129">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83020-130">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="83020-130">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="83020-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83020-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83020-132">Date d’expiration de la licence émise pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="83020-132">Expiration date of the license that was issued to the user.</span></span>

</dd> <dt>

<span data-ttu-id="83020-133">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="83020-133">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83020-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="83020-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83020-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83020-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83020-136">Version de Services Bureau à distance pour laquelle la licence d’accès client des services Bureau à distance a été émise.</span><span class="sxs-lookup"><span data-stu-id="83020-136">Version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span>

<dt>

<span data-ttu-id="83020-137">« Windows Server 2012 »</span><span class="sxs-lookup"><span data-stu-id="83020-137">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="83020-138">Seuls les serveurs exécutant Windows Server 2012, Windows Server 2008 R2 ou Windows Server 2008 sont pris en charge avec cette licence.</span><span class="sxs-lookup"><span data-stu-id="83020-138">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="83020-139">« Windows Server 7 »</span><span class="sxs-lookup"><span data-stu-id="83020-139">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="83020-140">Seuls les serveurs exécutant Windows Server 2008 R2 ou Windows Server 2008 sont pris en charge avec cette licence.</span><span class="sxs-lookup"><span data-stu-id="83020-140">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="83020-141">« Windows Server 2008 »</span><span class="sxs-lookup"><span data-stu-id="83020-141">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="83020-142">Seuls les serveurs exécutant Windows Server 2008 sont pris en charge avec cette licence.</span><span class="sxs-lookup"><span data-stu-id="83020-142">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="83020-143">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="83020-143">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83020-144">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83020-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83020-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83020-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83020-146">Identificateur de la version du produit pour le Services Bureau à distance le jeu de clés de licence.</span><span class="sxs-lookup"><span data-stu-id="83020-146">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="83020-147">4</span><span class="sxs-lookup"><span data-stu-id="83020-147">4</span></span>
</dt> <dd>

<span data-ttu-id="83020-148">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="83020-148">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="83020-149">3</span><span class="sxs-lookup"><span data-stu-id="83020-149">3</span></span>
</dt> <dd>

<span data-ttu-id="83020-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="83020-150">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="83020-151">2</span><span class="sxs-lookup"><span data-stu-id="83020-151">2</span></span>
</dt> <dd>

<span data-ttu-id="83020-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83020-152">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="83020-153">1</span><span class="sxs-lookup"><span data-stu-id="83020-153">1</span></span>
</dt> <dd>

<span data-ttu-id="83020-154">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="83020-154">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="83020-155">0</span><span class="sxs-lookup"><span data-stu-id="83020-155">0</span></span>
</dt> <dd>

<span data-ttu-id="83020-156">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="83020-156">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="83020-157">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="83020-157">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83020-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="83020-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83020-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83020-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83020-160">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="83020-160">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="83020-161">Nom de l’utilisateur pour lequel la licence a été émise.</span><span class="sxs-lookup"><span data-stu-id="83020-161">Name of the user to whom the license was issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83020-162">Notes</span><span class="sxs-lookup"><span data-stu-id="83020-162">Remarks</span></span>

<span data-ttu-id="83020-163">Pour utiliser cette classe, vous devez être membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="83020-163">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="83020-164">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="83020-164">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="83020-165">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="83020-165">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="83020-166">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="83020-166">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="83020-167">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="83020-167">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="83020-168">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83020-168">Requirements</span></span>



| <span data-ttu-id="83020-169">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83020-169">Requirement</span></span> | <span data-ttu-id="83020-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="83020-170">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="83020-171">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83020-171">Minimum supported client</span></span><br/> | <span data-ttu-id="83020-172">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="83020-172">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="83020-173">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83020-173">Minimum supported server</span></span><br/> | <span data-ttu-id="83020-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83020-174">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="83020-175">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="83020-175">Namespace</span></span><br/>                | <span data-ttu-id="83020-176">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="83020-176">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="83020-177">MOF</span><span class="sxs-lookup"><span data-stu-id="83020-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83020-178"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83020-178"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="83020-179">DLL</span><span class="sxs-lookup"><span data-stu-id="83020-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83020-180"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83020-180"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83020-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83020-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83020-182">**FetchReportEntries**</span><span class="sxs-lookup"><span data-stu-id="83020-182">**FetchReportEntries**</span></span>](fetchreportentries-win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="83020-183">**\_TSIssuedLicense Win32**</span><span class="sxs-lookup"><span data-stu-id="83020-183">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="83020-184">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="83020-184">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="83020-185">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="83020-185">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="83020-186">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="83020-186">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

