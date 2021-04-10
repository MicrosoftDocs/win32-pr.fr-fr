---
description: Demande que l’état du module de plateforme sécurisée soit remplacé par la valeur spécifiée dans le paramètre RequestedTPMState.
ms.assetid: 7ad8bf4e-6263-45d5-8f33-fb842bbf1f1a
title: Méthode RequestTPMStateChange de la classe CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.RequestTPMStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 39bded1a43dd547780c3924f3af9c37cfc79aa1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951654"
---
# <a name="requesttpmstatechange-method-of-the-cim_tpm-class"></a><span data-ttu-id="0d319-103">Méthode RequestTPMStateChange de la \_ classe TPM CIM</span><span class="sxs-lookup"><span data-stu-id="0d319-103">RequestTPMStateChange method of the CIM\_TPM class</span></span>

<span data-ttu-id="0d319-104">Demande que l’état du module de plateforme sécurisée soit remplacé par la valeur spécifiée dans le paramètre *RequestedTPMState* .</span><span class="sxs-lookup"><span data-stu-id="0d319-104">Requests that the state of the TPM be changed to the value specified in the *RequestedTPMState* parameter.</span></span> <span data-ttu-id="0d319-105">Si l’appel de la méthode se termine correctement, la propriété **TPMState** sera égale au paramètre **RequestedTPMState** .</span><span class="sxs-lookup"><span data-stu-id="0d319-105">If the method invocation completes successfully, the **TPMState** property shall be equal to the **RequestedTPMState** parameter.</span></span> <span data-ttu-id="0d319-106">L’appel de la méthode **RequestTPMStateChange** plusieurs fois peut entraîner le remplacement ou la perte des demandes antérieures.</span><span class="sxs-lookup"><span data-stu-id="0d319-106">Invoking the **RequestTPMStateChange** method multiple times could result in earlier requests being overwritten or lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d319-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d319-107">Syntax</span></span>


```mof
uint32 RequestTPMStateChange(
  [in]  uint16              RequestedTPMState,
  [in]  string              AuthorizationToken,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="0d319-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d319-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d319-109">*RequestedTPMState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d319-109">*RequestedTPMState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d319-110">États du module de plateforme sécurisée demandé.</span><span class="sxs-lookup"><span data-stu-id="0d319-110">The requested TPM states.</span></span>

<dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="0d319-111">**S1 activé-propriétaire actif** (2)</span><span class="sxs-lookup"><span data-stu-id="0d319-111">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="0d319-112">**S2 désactivé-actif-propriétaire** (3)</span><span class="sxs-lookup"><span data-stu-id="0d319-112">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="0d319-113">**S3 activé-inactif-détenu** (4)</span><span class="sxs-lookup"><span data-stu-id="0d319-113">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="0d319-114">**S4 désactivé-inactif-détenu** (5)</span><span class="sxs-lookup"><span data-stu-id="0d319-114">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="0d319-115">**S5 activé-actif-sans propriétaire** (6)</span><span class="sxs-lookup"><span data-stu-id="0d319-115">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="0d319-116">**S6 désactivé-actif-non détenu** (7)</span><span class="sxs-lookup"><span data-stu-id="0d319-116">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="0d319-117">**S7 activé-inactif-sans propriétaire** (8)</span><span class="sxs-lookup"><span data-stu-id="0d319-117">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="0d319-118">**S8 désactivé-inactif-sans propriétaire** (9)</span><span class="sxs-lookup"><span data-stu-id="0d319-118">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0d319-119">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="0d319-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0d319-120">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0d319-120">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="0d319-121">*AuthorizationToken* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d319-121">*AuthorizationToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d319-122">Jeton d’autorisation qui peut être nécessaire pour que l’action prenne effet.</span><span class="sxs-lookup"><span data-stu-id="0d319-122">Authorization token that may be required for the action to take effect.</span></span> <span data-ttu-id="0d319-123">Le paramètre *AuthorizationToken* peut être nécessaire pour établir la présence physique, ou pour transmettre le origine, le mot de passe d’autorisation du propriétaire défini par le TCG.</span><span class="sxs-lookup"><span data-stu-id="0d319-123">The *AuthorizationToken* parameter may be required to establish Physical Presence, or to pass the OwnerAuth, the TCG defined owner authorization password.</span></span> <span data-ttu-id="0d319-124">Dans le cas de origine, le \_ SHAREDCREDENTIAL CIM avec la valeur non null du CIM \_ SharedCredential. secret peut être requis.</span><span class="sxs-lookup"><span data-stu-id="0d319-124">In the case of OwnerAuth, the CIM\_SharedCredential with non-null value of the CIM\_SharedCredential.Secret may be required.</span></span> <span data-ttu-id="0d319-125">La \_ propriété CIM SharedCredential. algorithme peut également être spécifiée en fonction de la propriété CIM \_ TPMCapabilities. SupportedPasswordAlgorithms.</span><span class="sxs-lookup"><span data-stu-id="0d319-125">The CIM\_SharedCredential.Algorithm property may also be specified based on the property CIM\_TPMCapabilities.SupportedPasswordAlgorithms.</span></span>

</dd> <dt>

<span data-ttu-id="0d319-126">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0d319-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d319-127">Peut contenir une référence au [**\_ ConcreteJob CIM**](cim-concretejob.md) créé pour effectuer le suivi de la transition d’État initiée par l’appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="0d319-127">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="0d319-128">*TimeoutPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d319-128">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d319-129">Délai d’attente qui spécifie la durée maximale pendant laquelle le client attend la transition vers le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="0d319-129">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="0d319-130">Le format d’intervalle doit être utilisé pour spécifier le *TimeoutPeriod*.</span><span class="sxs-lookup"><span data-stu-id="0d319-130">The interval format must be used to specify the *TimeoutPeriod*.</span></span> <span data-ttu-id="0d319-131">La valeur 0 ou un paramètre null indique que le client n’a aucune exigence de temps pour la transition.</span><span class="sxs-lookup"><span data-stu-id="0d319-131">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d319-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d319-132">Return value</span></span>

<span data-ttu-id="0d319-133">En cas de réussite, retourne 0 ou 4096 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="0d319-133">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="0d319-134">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="0d319-134">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0d319-135">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="0d319-135">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0d319-136">**Erreur inconnue ou non spécifiée** (2)</span><span class="sxs-lookup"><span data-stu-id="0d319-136">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0d319-137">**Impossible de se terminer dans le délai imparti** (3)</span><span class="sxs-lookup"><span data-stu-id="0d319-137">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0d319-138">**Échec** (4)</span><span class="sxs-lookup"><span data-stu-id="0d319-138">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0d319-139">**Paramètre non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="0d319-139">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0d319-140">**En cours d’utilisation** (6)</span><span class="sxs-lookup"><span data-stu-id="0d319-140">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0d319-141">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="0d319-141">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0d319-142">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="0d319-142">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0d319-143">**Transition d’État non valide** (4097)</span><span class="sxs-lookup"><span data-stu-id="0d319-143">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="0d319-144">**Utilisation du paramètre timeout non prise en charge** (4098)</span><span class="sxs-lookup"><span data-stu-id="0d319-144">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="0d319-145">**Occupé** (4099)</span><span class="sxs-lookup"><span data-stu-id="0d319-145">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="0d319-146">**Méthode réservée** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="0d319-146">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="0d319-147">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0d319-147">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0d319-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d319-148">Requirements</span></span>



| <span data-ttu-id="0d319-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d319-149">Requirement</span></span> | <span data-ttu-id="0d319-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d319-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d319-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d319-151">Minimum supported client</span></span><br/> | <span data-ttu-id="0d319-152">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d319-152">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0d319-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d319-153">Minimum supported server</span></span><br/> | <span data-ttu-id="0d319-154">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0d319-154">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0d319-155">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0d319-155">Namespace</span></span><br/>                | <span data-ttu-id="0d319-156">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0d319-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0d319-157">MOF</span><span class="sxs-lookup"><span data-stu-id="0d319-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d319-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d319-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d319-159">DLL</span><span class="sxs-lookup"><span data-stu-id="0d319-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d319-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0d319-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0d319-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d319-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d319-162">**\_TPM CIM**</span><span class="sxs-lookup"><span data-stu-id="0d319-162">**CIM\_TPM**</span></span>](cim-tpm.md)
</dt> </dl>

 

 




