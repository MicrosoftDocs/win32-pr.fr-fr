---
title: Classe MDM_HealthAttestation
description: La \_ classe MDM HealthAttestation permet aux responsables informatiques d’entreprise d’évaluer l’intégrité des appareils gérés et de prendre des mesures de stratégie d’entreprise.
ms.assetid: 64f40ccc-98f6-48d6-bcd4-793375e3dbfb
keywords:
- Classe MDM_HealthAttestation
- Classe MDM_HealthAttestation, Description
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7f76af135e7eac09b3b104e924b26efbb359b256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464858"
---
# <a name="mdm_healthattestation-class"></a><span data-ttu-id="7f8e7-105">\_Classe HEALTHATTESTATION MDM</span><span class="sxs-lookup"><span data-stu-id="7f8e7-105">MDM\_HealthAttestation class</span></span>

<span data-ttu-id="7f8e7-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="7f8e7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7f8e7-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="7f8e7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7f8e7-108">La classe **MDM \_ HealthAttestation** permet aux responsables informatiques d’entreprise d’évaluer l’intégrité des appareils gérés et de prendre des mesures de stratégie d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="7f8e7-108">The **MDM\_HealthAttestation** class enables enterprise IT managers to assess the health of managed devices and take enterprise policy actions.</span></span>

<span data-ttu-id="7f8e7-109">La liste suivante répertorie les fonctions effectuées par le CSP HealthAttestation :</span><span class="sxs-lookup"><span data-stu-id="7f8e7-109">The following is a list of functions performed by the HealthAttestation CSP:</span></span>

-   <span data-ttu-id="7f8e7-110">Collecte les données utilisées pour vérifier les États d’intégrité des appareils</span><span class="sxs-lookup"><span data-stu-id="7f8e7-110">Collects data that is used in verifying a devices health states</span></span>
-   <span data-ttu-id="7f8e7-111">Il transfère ces données au service d’attestation d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="7f8e7-111">Forwards the data to the Health Attestation Service (HAS)</span></span>
-   <span data-ttu-id="7f8e7-112">Met en service le certificat d’attestation d’intégrité qu’il reçoit de.</span><span class="sxs-lookup"><span data-stu-id="7f8e7-112">Provisions the Health Attestation Certificate that it receives from HAS</span></span>
-   <span data-ttu-id="7f8e7-113">À la demande, transfère le certificat d’attestation d’intégrité (reçu de l’offre) et les informations d’exécution associées au serveur MDM à des fins de vérification.</span><span class="sxs-lookup"><span data-stu-id="7f8e7-113">Upon request, forwards the Health Attestation Certificate (received from HAS) and related runtime information to the MDM Server for verification</span></span>

<span data-ttu-id="7f8e7-114">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7f8e7-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f8e7-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f8e7-115">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_HealthAttestation
{
  string  InstanceID;
  string  ParentID;
  sint32  Status;
  boolean ForceRetrieve;
  string  Certificate;
  string  Nonce;
  string  CorrelationID;
  sint32  TpmReadyStatus;
  sint32  MaxSupportedProtocolVersion;
  sint32  PreferredMaxProtocolVersion;
  sint32  CurrentProtocolVersion;
  string  HASEndpoint;
};
```

## <a name="members"></a><span data-ttu-id="7f8e7-116">Membres</span><span class="sxs-lookup"><span data-stu-id="7f8e7-116">Members</span></span>

<span data-ttu-id="7f8e7-117">La **classe \_ HealthAttestation MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7f8e7-117">The **MDM\_HealthAttestation** class has these types of members:</span></span>

-   [<span data-ttu-id="7f8e7-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7f8e7-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="7f8e7-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7f8e7-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7f8e7-120">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7f8e7-120">Methods</span></span>

<span data-ttu-id="7f8e7-121">La classe **MDM \_ HealthAttestation** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="7f8e7-121">The **MDM\_HealthAttestation** class has these methods.</span></span>



| <span data-ttu-id="7f8e7-122">Méthode</span><span class="sxs-lookup"><span data-stu-id="7f8e7-122">Method</span></span>                                                                 | <span data-ttu-id="7f8e7-123">Description</span><span class="sxs-lookup"><span data-stu-id="7f8e7-123">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f8e7-124">**VerifyHealthMethod**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-124">**VerifyHealthMethod**</span></span>](mdm-healthattestation-verifyhealthmethod.md) | <span data-ttu-id="7f8e7-125">Méthode pour informer l’appareil de la préparation d’une demande de vérification du certificat d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="7f8e7-125">Method to notify the device to prepare a health certificate verification request.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7f8e7-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7f8e7-126">Properties</span></span>

<span data-ttu-id="7f8e7-127">La **classe \_ HealthAttestation MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7f8e7-127">The **MDM\_HealthAttestation** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7f8e7-128">Certificate</span><span class="sxs-lookup"><span data-stu-id="7f8e7-128">Certificate</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f8e7-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f8e7-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7f8e7-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7f8e7-131">Qualificateurs : **Octetstring**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-131">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7f8e7-132">CorrelationID</span><span class="sxs-lookup"><span data-stu-id="7f8e7-132">CorrelationID</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f8e7-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f8e7-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7f8e7-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7f8e7-135">**CurrentProtocolVersion**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-135">**CurrentProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f8e7-136">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f8e7-137">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7f8e7-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7f8e7-138">TBD</span><span class="sxs-lookup"><span data-stu-id="7f8e7-138">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="7f8e7-139">ForceRetrieve</span><span class="sxs-lookup"><span data-stu-id="7f8e7-139">ForceRetrieve</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f8e7-140">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f8e7-141">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7f8e7-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7f8e7-142">HASEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f8e7-142">HASEndpoint</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f8e7-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f8e7-144">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7f8e7-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7f8e7-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f8e7-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f8e7-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f8e7-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f8e7-148">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7f8e7-148">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7f8e7-149">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="7f8e7-149">Identifies the name of the parent node.</span></span> <span data-ttu-id="7f8e7-150">Pour cette classe, la chaîne est « HealthAttestation ».</span><span class="sxs-lookup"><span data-stu-id="7f8e7-150">For this class, the string is "HealthAttestation".</span></span>

</dd> <dt>

<span data-ttu-id="7f8e7-151">**MaxSupportedProtocolVersion**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-151">**MaxSupportedProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f8e7-152">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-152">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f8e7-153">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7f8e7-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7f8e7-154">TBD</span><span class="sxs-lookup"><span data-stu-id="7f8e7-154">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="7f8e7-155">Unique</span><span class="sxs-lookup"><span data-stu-id="7f8e7-155">Nonce</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f8e7-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f8e7-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7f8e7-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7f8e7-158">**ID**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-158">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f8e7-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f8e7-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7f8e7-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f8e7-161">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7f8e7-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7f8e7-162">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="7f8e7-162">Describes the full path to the parent node.</span></span> <span data-ttu-id="7f8e7-163">Pour cette classe, la chaîne est « ./Vendor/MSFT/ »</span><span class="sxs-lookup"><span data-stu-id="7f8e7-163">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

<span data-ttu-id="7f8e7-164">**PreferredMaxProtocolVersion**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-164">**PreferredMaxProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f8e7-165">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f8e7-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7f8e7-166">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7f8e7-167">TBD</span><span class="sxs-lookup"><span data-stu-id="7f8e7-167">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="7f8e7-168">État</span><span class="sxs-lookup"><span data-stu-id="7f8e7-168">Status</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f8e7-169">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-169">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f8e7-170">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7f8e7-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7f8e7-171">TpmReadyStatus</span><span class="sxs-lookup"><span data-stu-id="7f8e7-171">TpmReadyStatus</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f8e7-172">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="7f8e7-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f8e7-173">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7f8e7-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7f8e7-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f8e7-174">Requirements</span></span>



| <span data-ttu-id="7f8e7-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f8e7-175">Requirement</span></span> | <span data-ttu-id="7f8e7-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f8e7-176">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f8e7-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f8e7-177">Minimum supported client</span></span><br/> | <span data-ttu-id="7f8e7-178">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f8e7-178">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7f8e7-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f8e7-179">Minimum supported server</span></span><br/> | <span data-ttu-id="7f8e7-180">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f8e7-180">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7f8e7-181">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7f8e7-181">Namespace</span></span><br/>                | <span data-ttu-id="7f8e7-182">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="7f8e7-182">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7f8e7-183">MOF</span><span class="sxs-lookup"><span data-stu-id="7f8e7-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f8e7-184"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f8e7-184"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f8e7-185">DLL</span><span class="sxs-lookup"><span data-stu-id="7f8e7-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f8e7-186"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f8e7-186"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f8e7-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f8e7-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f8e7-188">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="7f8e7-188">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

