---
title: Classe MSAD_DomainController
description: Représente le contrôleur de domaine sur lequel s’exécute le fournisseur WMI.
ms.assetid: a7671967-79d7-48f8-8869-dd65272e2ed2
ms.tgt_platform: multiple
keywords:
- MSAD_DomainController de la classe Active Directory
- MSAD_DomainController de la classe Active Directory, Description
topic_type:
- apiref
api_name:
- MSAD_DomainController
- MSAD_DomainController.DistinguishedName
- MSAD_DomainController.CommonName
- MSAD_DomainController.SiteName
- MSAD_DomainController.NTDsaGUID
- MSAD_DomainController.IsGC
- MSAD_DomainController.TimeOfOldestReplSync
- MSAD_DomainController.TimeOfOldestReplAdd
- MSAD_DomainController.TimeOfOldestReplDel
- MSAD_DomainController.TimeOfOldestReplMod
- MSAD_DomainController.TimeOfOldestReplUpdRefs
- MSAD_DomainController.IsNextRIDPoolAvailable
- MSAD_DomainController.PercentOfRIDsLeft
- MSAD_DomainController.IsRegisteredInDNS
- MSAD_DomainController.IsAdvertisingToLocator
- MSAD_DomainController.IsSysVolReady
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303071d3d268953687bc387709c74531f8b40584
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465395"
---
# <a name="msad_domaincontroller-class"></a><span data-ttu-id="92fc0-105">\_Classe DOMAINCONTROLLER MSAD</span><span class="sxs-lookup"><span data-stu-id="92fc0-105">MSAD\_DomainController class</span></span>

<span data-ttu-id="92fc0-106">Représente le contrôleur de domaine sur lequel s’exécute le fournisseur WMI.</span><span class="sxs-lookup"><span data-stu-id="92fc0-106">Represents the domain controller (DC) on which the WMI provider is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="92fc0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92fc0-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class  MSAD_DomainController
{
  String   DistinguishedName;
  String   CommonName;
  String   SiteName;
  String   NTDsaGUID;
  boolean  IsGC = FALSE;
  datetime TimeOfOldestReplSync;
  datetime TimeOfOldestReplAdd;
  datetime TimeOfOldestReplDel;
  datetime TimeOfOldestReplMod;
  datetime TimeOfOldestReplUpdRefs;
  boolean  IsNextRIDPoolAvailable = FALSE;
  uint32   PercentOfRIDsLeft;
  boolean  IsRegisteredInDNS;
  boolean  IsAdvertisingToLocator = FALSE;
  boolean  IsSysVolReady = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="92fc0-108">Membres</span><span class="sxs-lookup"><span data-stu-id="92fc0-108">Members</span></span>

<span data-ttu-id="92fc0-109">La **classe \_ DomainController MSAD** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="92fc0-109">The **MSAD\_DomainController** class has these types of members:</span></span>

-   [<span data-ttu-id="92fc0-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="92fc0-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="92fc0-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="92fc0-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="92fc0-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="92fc0-112">Methods</span></span>

<span data-ttu-id="92fc0-113">La **classe \_ DomainController MSAD** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="92fc0-113">The **MSAD\_DomainController** class has these methods.</span></span>



| <span data-ttu-id="92fc0-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="92fc0-114">Method</span></span>                                                 | <span data-ttu-id="92fc0-115">Description</span><span class="sxs-lookup"><span data-stu-id="92fc0-115">Description</span></span>                                                                              |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="92fc0-116">**ExecuteKCC**</span><span class="sxs-lookup"><span data-stu-id="92fc0-116">**ExecuteKCC**</span></span>](executekcc-msad-domaincontroller.md) | <span data-ttu-id="92fc0-117">Appelle le vérificateur de cohérence des connaissances pour vérifier la topologie de réplication.</span><span class="sxs-lookup"><span data-stu-id="92fc0-117">Invokes the Knowledge Consistency Checker to verify the replication topology.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="92fc0-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="92fc0-118">Properties</span></span>

<span data-ttu-id="92fc0-119">La **classe \_ DomainController MSAD** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="92fc0-119">The **MSAD\_DomainController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92fc0-120">**CommonName**</span><span class="sxs-lookup"><span data-stu-id="92fc0-120">**CommonName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92fc0-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92fc0-121">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="92fc0-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92fc0-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92fc0-123">Obtient le nom commun de l’objet serveur.</span><span class="sxs-lookup"><span data-stu-id="92fc0-123">Gets the common name of the server object.</span></span>

</dd> <dt>

<span data-ttu-id="92fc0-124">**DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="92fc0-124">**DistinguishedName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92fc0-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92fc0-125">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="92fc0-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92fc0-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92fc0-127">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="92fc0-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="92fc0-128">Obtient le chemin d’accès X. 500 de l’objet [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) .</span><span class="sxs-lookup"><span data-stu-id="92fc0-128">Gets the X.500 path of the [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) object.</span></span>

</dd> <dt>

<span data-ttu-id="92fc0-129">**IsAdvertisingToLocator**</span><span class="sxs-lookup"><span data-stu-id="92fc0-129">**IsAdvertisingToLocator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92fc0-130">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="92fc0-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92fc0-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92fc0-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92fc0-132">Obtient la valeur qui indique si le service Localisateur sur le contrôleur de périphérique publie correctement.</span><span class="sxs-lookup"><span data-stu-id="92fc0-132">Gets the value that indicates whether the locator service on the DC is advertising correctly.</span></span> <span data-ttu-id="92fc0-133">**True** si le service de localisation sur le contrôleur de service publie correctement ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="92fc0-133">**TRUE** if the locator service on the DC is advertising correctly; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="92fc0-134">**IsGC**</span><span class="sxs-lookup"><span data-stu-id="92fc0-134">**IsGC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92fc0-135">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="92fc0-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92fc0-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92fc0-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92fc0-137">Obtient la valeur qui indique si le DC est un serveur de catalogue global.</span><span class="sxs-lookup"><span data-stu-id="92fc0-137">Gets the value that indicates whether the DC is a Global Catalog server.</span></span> <span data-ttu-id="92fc0-138">**True** si le contrôleur de périphérique est un serveur de catalogue global ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="92fc0-138">**TRUE** if the DC is a Global Catalog server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="92fc0-139">**IsNextRIDPoolAvailable**</span><span class="sxs-lookup"><span data-stu-id="92fc0-139">**IsNextRIDPoolAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92fc0-140">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="92fc0-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92fc0-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92fc0-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92fc0-142">Obtient la valeur qui indique si le DC a obtenu un autre pool RID.</span><span class="sxs-lookup"><span data-stu-id="92fc0-142">Gets the value that indicates whether the DC has obtained another RID pool.</span></span> <span data-ttu-id="92fc0-143">**True** si le contrôleur de l’objet a obtenu un autre pool RID et que l’allocation d’identificateurs RID sur ce contrôleur de groupe peut se poursuivre même si le pool actuel d’identificateurs RID est épuisé ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="92fc0-143">**TRUE** if the DC has obtained another RID pool and allocation of RIDs on this DC can continue even if the current pool of RIDs is exhausted; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="92fc0-144">**IsRegisteredInDNS**</span><span class="sxs-lookup"><span data-stu-id="92fc0-144">**IsRegisteredInDNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92fc0-145">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="92fc0-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92fc0-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92fc0-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92fc0-147">Obtient la valeur qui indique si le contrôleur de domaine est inscrit correctement dans DNS.</span><span class="sxs-lookup"><span data-stu-id="92fc0-147">Gets the value that indicates whether the DC is registered correctly in DNS.</span></span> <span data-ttu-id="92fc0-148">**True** si le contrôleur de domaine est inscrit correctement dans DNS ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="92fc0-148">**TRUE** if the DC is registered correctly in DNS; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="92fc0-149">**IsSysVolReady**</span><span class="sxs-lookup"><span data-stu-id="92fc0-149">**IsSysVolReady**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92fc0-150">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="92fc0-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92fc0-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92fc0-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92fc0-152">Obtient la valeur qui indique si SysVol a été publié correctement.</span><span class="sxs-lookup"><span data-stu-id="92fc0-152">Gets the value that indicates whether the SysVol has published correctly.</span></span> <span data-ttu-id="92fc0-153">**True** si SYSVOL a été publié correctement ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="92fc0-153">**TRUE** if the SysVol has published correctly; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="92fc0-154">**NTDsaGUID**</span><span class="sxs-lookup"><span data-stu-id="92fc0-154">**NTDsaGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92fc0-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92fc0-155">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="92fc0-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92fc0-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92fc0-157">Obtient le GUID associé à l’objet [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) dans le conteneur de configuration.</span><span class="sxs-lookup"><span data-stu-id="92fc0-157">Gets the GUID that is associated with the [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) object in the configuration container.</span></span> <span data-ttu-id="92fc0-158">L’objet **NTDS-DSA** représente le domaine Active Directory processus DSA du service sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="92fc0-158">The **NTDS-DSA** object represents the Active Directory Domain Service DSA process on the server.</span></span>

</dd> <dt>

<span data-ttu-id="92fc0-159">**PercentOfRIDsLeft**</span><span class="sxs-lookup"><span data-stu-id="92fc0-159">**PercentOfRIDsLeft**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92fc0-160">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92fc0-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92fc0-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92fc0-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92fc0-162">Obtient le pourcentage d’identificateurs RID restants dans le pool RID actuel sur ce contrôleur de périphérique.</span><span class="sxs-lookup"><span data-stu-id="92fc0-162">Gets the percentage of RIDs that are left in the current RID pool on this DC.</span></span>

</dd> <dt>

<span data-ttu-id="92fc0-163">**SiteName**</span><span class="sxs-lookup"><span data-stu-id="92fc0-163">**SiteName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92fc0-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92fc0-164">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="92fc0-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92fc0-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92fc0-166">Obtient le site dans lequel le contrôleur de site existe.</span><span class="sxs-lookup"><span data-stu-id="92fc0-166">Gets the site in which the DC exists.</span></span>

</dd> <dt>

<span data-ttu-id="92fc0-167">**TimeOfOldestReplAdd**</span><span class="sxs-lookup"><span data-stu-id="92fc0-167">**TimeOfOldestReplAdd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92fc0-168">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="92fc0-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="92fc0-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92fc0-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92fc0-170">Obtient l’horodateur de l’opération d’ajout de réplication la plus ancienne qui est encore dans la file d’attente sur ce contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="92fc0-170">Gets the timestamp of the oldest replication add operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="92fc0-171">**TimeOfOldestReplDel**</span><span class="sxs-lookup"><span data-stu-id="92fc0-171">**TimeOfOldestReplDel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92fc0-172">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="92fc0-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="92fc0-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92fc0-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92fc0-174">Obtient l’horodateur de l’opération de suppression de réplication la plus ancienne qui est encore dans la file d’attente sur ce contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="92fc0-174">Gets the timestamp of the oldest replication delete operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="92fc0-175">**TimeOfOldestReplMod**</span><span class="sxs-lookup"><span data-stu-id="92fc0-175">**TimeOfOldestReplMod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92fc0-176">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="92fc0-176">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="92fc0-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92fc0-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92fc0-178">Obtient l’horodateur de l’opération de modification de réplication la plus ancienne qui est encore dans la file d’attente sur ce contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="92fc0-178">Gets the timestamp of the oldest replication modify operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="92fc0-179">**TimeOfOldestReplSync**</span><span class="sxs-lookup"><span data-stu-id="92fc0-179">**TimeOfOldestReplSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92fc0-180">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="92fc0-180">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="92fc0-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92fc0-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92fc0-182">Obtient l’horodateur de l’opération de synchronisation de réplication la plus ancienne qui est encore dans la file d’attente sur ce contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="92fc0-182">Gets the timestamp of the oldest replication sync operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="92fc0-183">**TimeOfOldestReplUpdRefs**</span><span class="sxs-lookup"><span data-stu-id="92fc0-183">**TimeOfOldestReplUpdRefs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92fc0-184">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="92fc0-184">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="92fc0-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92fc0-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92fc0-186">Obtient l’horodateur de l’opération de mise à jour de réplication la plus ancienne qui est encore dans la file d’attente sur ce contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="92fc0-186">Gets the timestamp of the oldest replication update operation that is still in the queue on this domain controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92fc0-187">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92fc0-187">Requirements</span></span>



| <span data-ttu-id="92fc0-188">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92fc0-188">Requirement</span></span> | <span data-ttu-id="92fc0-189">Valeur</span><span class="sxs-lookup"><span data-stu-id="92fc0-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92fc0-190">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92fc0-190">Minimum supported client</span></span><br/> | <span data-ttu-id="92fc0-191">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="92fc0-191">None supported</span></span><br/>                                                               |
| <span data-ttu-id="92fc0-192">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92fc0-192">Minimum supported server</span></span><br/> | <span data-ttu-id="92fc0-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92fc0-193">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="92fc0-194">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="92fc0-194">Namespace</span></span><br/>                | <span data-ttu-id="92fc0-195">\\MicrosoftActiveDirectory racine</span><span class="sxs-lookup"><span data-stu-id="92fc0-195">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="92fc0-196">MOF</span><span class="sxs-lookup"><span data-stu-id="92fc0-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92fc0-197"><dt>ReplProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92fc0-197"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="92fc0-198">DLL</span><span class="sxs-lookup"><span data-stu-id="92fc0-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92fc0-199"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92fc0-199"><dt>Replprov.dll</dt></span></span> </dl> |



 

