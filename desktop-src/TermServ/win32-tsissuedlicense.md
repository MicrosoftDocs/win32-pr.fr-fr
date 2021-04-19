---
title: Classe Win32_TSIssuedLicense
description: Décrit les instances de licences d’accès client par périphérique Services Bureau à distance (RDS \ 160 ; Cal par périphérique) émises à partir d’un serveur de licences Bureau à distance.
ms.assetid: 15825dc5-9ada-4c11-ac77-beb681e9b33c
ms.tgt_platform: multiple
keywords:
- Win32_TSIssuedLicense de la classe Services Bureau à distance
- Win32_TSIssuedLicense de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense
- Win32_TSIssuedLicense.LicenseId
- Win32_TSIssuedLicense.KeyPackId
- Win32_TSIssuedLicense.sIssuedToUser
- Win32_TSIssuedLicense.sIssuedToComputer
- Win32_TSIssuedLicense.LicenseStatus
- Win32_TSIssuedLicense.IssueDate
- Win32_TSIssuedLicense.ExpirationDate
- Win32_TSIssuedLicense.sHardwareId
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c3d08a68ddcc15a912de4c674403928211a297e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513786"
---
# <a name="win32_tsissuedlicense-class"></a><span data-ttu-id="5879d-105">\_Classe TSIssuedLicense Win32</span><span class="sxs-lookup"><span data-stu-id="5879d-105">Win32\_TSIssuedLicense class</span></span>

<span data-ttu-id="5879d-106">Décrit les instances de licences d’accès client par périphérique (CAL par périphérique) Services Bureau à distance émises par un serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="5879d-106">Describes instances of Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) that are issued from a Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5879d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5879d-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSIssuedLicense
{
  uint32   LicenseId;
  uint32   KeyPackId;
  string   sIssuedToUser;
  string   sIssuedToComputer;
  uint32   LicenseStatus;
  DATETIME IssueDate;
  DATETIME ExpirationDate;
  string   sHardwareId;
};
```

## <a name="members"></a><span data-ttu-id="5879d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="5879d-108">Members</span></span>

<span data-ttu-id="5879d-109">La classe **Win32 \_ TSIssuedLicense** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5879d-109">The **Win32\_TSIssuedLicense** class has these types of members:</span></span>

-   [<span data-ttu-id="5879d-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5879d-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="5879d-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5879d-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5879d-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5879d-112">Methods</span></span>

<span data-ttu-id="5879d-113">La classe **Win32 \_ TSIssuedLicense** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5879d-113">The **Win32\_TSIssuedLicense** class has these methods.</span></span>



| <span data-ttu-id="5879d-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="5879d-114">Method</span></span>                                         | <span data-ttu-id="5879d-115">Description</span><span class="sxs-lookup"><span data-stu-id="5879d-115">Description</span></span>                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5879d-116">**Révoquer**</span><span class="sxs-lookup"><span data-stu-id="5879d-116">**Revoke**</span></span>](revoke-win32-tsissuedlicense.md) | <span data-ttu-id="5879d-117">Révoque les licences d’accès client des services Bureau à distance qui sont représentées par l’objet **Win32 \_ TSIssuedLicense** .</span><span class="sxs-lookup"><span data-stu-id="5879d-117">Revokes the RDS Per Device CALs that are represented by the **Win32\_TSIssuedLicense** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5879d-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5879d-118">Properties</span></span>

<span data-ttu-id="5879d-119">La classe **Win32 \_ TSIssuedLicense** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5879d-119">The **Win32\_TSIssuedLicense** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5879d-120">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="5879d-120">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5879d-121">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5879d-121">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="5879d-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5879d-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5879d-123">Identifie la date d’expiration de la licence.</span><span class="sxs-lookup"><span data-stu-id="5879d-123">Identifies the date that the license will expire.</span></span>

</dd> <dt>

<span data-ttu-id="5879d-124">**Émis**</span><span class="sxs-lookup"><span data-stu-id="5879d-124">**IssueDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5879d-125">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5879d-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="5879d-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5879d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5879d-127">Identifie la date à laquelle la licence a été émise.</span><span class="sxs-lookup"><span data-stu-id="5879d-127">Identifies the date that the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="5879d-128">**KeyPackId**</span><span class="sxs-lookup"><span data-stu-id="5879d-128">**KeyPackId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5879d-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5879d-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5879d-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5879d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5879d-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5879d-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5879d-132">Identifie le jeu de clés de licence Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="5879d-132">Identifies the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="5879d-133">**LicenseId**</span><span class="sxs-lookup"><span data-stu-id="5879d-133">**LicenseId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5879d-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5879d-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5879d-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5879d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5879d-136">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5879d-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5879d-137">Identificateur unique de cette licence.</span><span class="sxs-lookup"><span data-stu-id="5879d-137">Unique identifier for this license.</span></span>

</dd> <dt>

<span data-ttu-id="5879d-138">**LicenseStatus**</span><span class="sxs-lookup"><span data-stu-id="5879d-138">**LicenseStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5879d-139">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5879d-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5879d-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5879d-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5879d-141">État de la licence.</span><span class="sxs-lookup"><span data-stu-id="5879d-141">Status of the license.</span></span>

<dt>

<span data-ttu-id="5879d-142">0</span><span class="sxs-lookup"><span data-stu-id="5879d-142">0</span></span>
</dt> <dd>

<span data-ttu-id="5879d-143">L’état de la licence est inconnu.</span><span class="sxs-lookup"><span data-stu-id="5879d-143">The license status is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="5879d-144">1</span><span class="sxs-lookup"><span data-stu-id="5879d-144">1</span></span>
</dt> <dd>

<span data-ttu-id="5879d-145">La licence est une licence temporaire.</span><span class="sxs-lookup"><span data-stu-id="5879d-145">The license is a temporary license.</span></span>

</dd> <dt>

<span data-ttu-id="5879d-146">2</span><span class="sxs-lookup"><span data-stu-id="5879d-146">2</span></span>
</dt> <dd>

<span data-ttu-id="5879d-147">La licence est active.</span><span class="sxs-lookup"><span data-stu-id="5879d-147">The license is active.</span></span>

</dd> <dt>

<span data-ttu-id="5879d-148">3</span><span class="sxs-lookup"><span data-stu-id="5879d-148">3</span></span>
</dt> <dd>

<span data-ttu-id="5879d-149">La licence est une licence de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="5879d-149">The license is an upgrade license.</span></span>

</dd> <dt>

<span data-ttu-id="5879d-150">4</span><span class="sxs-lookup"><span data-stu-id="5879d-150">4</span></span>
</dt> <dd>

<span data-ttu-id="5879d-151">La licence a été révoquée.</span><span class="sxs-lookup"><span data-stu-id="5879d-151">The license has been revoked.</span></span>

</dd> <dt>

<span data-ttu-id="5879d-152">5</span><span class="sxs-lookup"><span data-stu-id="5879d-152">5</span></span>
</dt> <dd>

<span data-ttu-id="5879d-153">L’état de la licence est en attente.</span><span class="sxs-lookup"><span data-stu-id="5879d-153">The license status is pending.</span></span>

</dd> <dt>

<span data-ttu-id="5879d-154">6</span><span class="sxs-lookup"><span data-stu-id="5879d-154">6</span></span>
</dt> <dd>

<span data-ttu-id="5879d-155">La licence est une licence simultanée.</span><span class="sxs-lookup"><span data-stu-id="5879d-155">The license is a concurrent license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5879d-156">**sHardwareId**</span><span class="sxs-lookup"><span data-stu-id="5879d-156">**sHardwareId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5879d-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5879d-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5879d-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5879d-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5879d-159">Identificateur matériel pour lequel la licence a été émise.</span><span class="sxs-lookup"><span data-stu-id="5879d-159">Hardware identifier for which the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="5879d-160">**sIssuedToComputer**</span><span class="sxs-lookup"><span data-stu-id="5879d-160">**sIssuedToComputer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5879d-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5879d-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5879d-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5879d-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5879d-163">Nom de l’ordinateur pour lequel la licence a été émise.</span><span class="sxs-lookup"><span data-stu-id="5879d-163">Computer name for which the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="5879d-164">**sIssuedToUser**</span><span class="sxs-lookup"><span data-stu-id="5879d-164">**sIssuedToUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5879d-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5879d-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5879d-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5879d-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5879d-167">Nom d’utilisateur pour lequel la licence a été émise.</span><span class="sxs-lookup"><span data-stu-id="5879d-167">User name for which the license was issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5879d-168">Notes</span><span class="sxs-lookup"><span data-stu-id="5879d-168">Remarks</span></span>

<span data-ttu-id="5879d-169">Pour utiliser cette classe, vous devez être membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="5879d-169">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="5879d-170">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="5879d-170">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5879d-171">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5879d-171">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5879d-172">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="5879d-172">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5879d-173">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5879d-173">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5879d-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5879d-174">Requirements</span></span>



| <span data-ttu-id="5879d-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5879d-175">Requirement</span></span> | <span data-ttu-id="5879d-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="5879d-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5879d-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5879d-177">Minimum supported client</span></span><br/> | <span data-ttu-id="5879d-178">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5879d-178">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="5879d-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5879d-179">Minimum supported server</span></span><br/> | <span data-ttu-id="5879d-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5879d-180">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="5879d-181">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5879d-181">Namespace</span></span><br/>                | <span data-ttu-id="5879d-182">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="5879d-182">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="5879d-183">MOF</span><span class="sxs-lookup"><span data-stu-id="5879d-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5879d-184"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5879d-184"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5879d-185">DLL</span><span class="sxs-lookup"><span data-stu-id="5879d-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5879d-186"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5879d-186"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5879d-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5879d-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5879d-188">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="5879d-188">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="5879d-189">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="5879d-189">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="5879d-190">**\_TSLicenseReportEntry Win32**</span><span class="sxs-lookup"><span data-stu-id="5879d-190">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="5879d-191">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="5879d-191">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

