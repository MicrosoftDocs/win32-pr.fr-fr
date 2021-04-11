---
title: Classe MDM_Policy_Result01_WirelessDisplay02
description: La \_ classe Result01 WirelessDisplay02 de la stratégie MDM \_ \_ représente les stratégies d’affichage sans fil disponibles.
ms.assetid: fbdfa785-8747-47b4-9802-da1c245ca222
keywords:
- Classe MDM_Policy_Result01_WirelessDisplay02
- Classe MDM_Policy_Result01_WirelessDisplay02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WirelessDisplay02
- MDM_Policy_Result01_WirelessDisplay02.InstanceID
- MDM_Policy_Result01_WirelessDisplay02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90f4e309d1c54f12d99dfbeaa0b80807249e61fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032401"
---
# <a name="mdm_policy_result01_wirelessdisplay02-class"></a><span data-ttu-id="00c3e-105">\_Classe WirelessDisplay02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="00c3e-105">MDM\_Policy\_Result01\_WirelessDisplay02 class</span></span>

<span data-ttu-id="00c3e-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="00c3e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="00c3e-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="00c3e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="00c3e-108">La **classe \_ \_ Result01 \_ WirelessDisplay02 de la stratégie MDM** représente les stratégies d’affichage sans fil disponibles.</span><span class="sxs-lookup"><span data-stu-id="00c3e-108">The **MDM\_Policy\_Result01\_WirelessDisplay02** class represents the wireless display policies available.</span></span>

<span data-ttu-id="00c3e-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="00c3e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="00c3e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00c3e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WirelessDisplay02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMdnsDiscovery;
  sint32 AllowMdnsAdvertisement;
  sint32 AllowProjectionFromPCOverInfrastructure;
  sint32 AllowProjectionFromPC;
  sint32 AllowProjectionToPC;
  sint32 AllowProjectionToPCOverInfrastructure;
  sint32 AllowUserInputFromWirelessDisplayReceiver;
  sint32 RequirePinForPairing;
};
```

## <a name="members"></a><span data-ttu-id="00c3e-111">Membres</span><span class="sxs-lookup"><span data-stu-id="00c3e-111">Members</span></span>

<span data-ttu-id="00c3e-112">La **classe \_ \_ Result01 \_ WirelessDisplay02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="00c3e-112">The **MDM\_Policy\_Result01\_WirelessDisplay02** class has these types of members:</span></span>

-   [<span data-ttu-id="00c3e-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="00c3e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00c3e-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="00c3e-114">Properties</span></span>

<span data-ttu-id="00c3e-115">La **classe \_ \_ Result01 \_ WirelessDisplay02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="00c3e-115">The **MDM\_Policy\_Result01\_WirelessDisplay02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="00c3e-116">AllowMdnsAdvertisement</span><span class="sxs-lookup"><span data-stu-id="00c3e-116">AllowMdnsAdvertisement</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsadvertisement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c3e-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="00c3e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="00c3e-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="00c3e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="00c3e-119">AllowMdnsDiscovery</span><span class="sxs-lookup"><span data-stu-id="00c3e-119">AllowMdnsDiscovery</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsdiscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c3e-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="00c3e-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="00c3e-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="00c3e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="00c3e-122">AllowProjectionFromPC</span><span class="sxs-lookup"><span data-stu-id="00c3e-122">AllowProjectionFromPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c3e-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="00c3e-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="00c3e-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="00c3e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="00c3e-125">AllowProjectionFromPCOverInfrastructure</span><span class="sxs-lookup"><span data-stu-id="00c3e-125">AllowProjectionFromPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c3e-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="00c3e-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="00c3e-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="00c3e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="00c3e-128">AllowProjectionToPC</span><span class="sxs-lookup"><span data-stu-id="00c3e-128">AllowProjectionToPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c3e-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="00c3e-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="00c3e-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="00c3e-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="00c3e-131">AllowProjectionToPCOverInfrastructure</span><span class="sxs-lookup"><span data-stu-id="00c3e-131">AllowProjectionToPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c3e-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="00c3e-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="00c3e-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="00c3e-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="00c3e-134">AllowUserInputFromWirelessDisplayReceiver</span><span class="sxs-lookup"><span data-stu-id="00c3e-134">AllowUserInputFromWirelessDisplayReceiver</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowuserinputfromwirelessdisplayreceiver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c3e-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="00c3e-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="00c3e-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="00c3e-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="00c3e-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="00c3e-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c3e-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c3e-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c3e-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c3e-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c3e-140">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="00c3e-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="00c3e-141">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="00c3e-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="00c3e-142">Pour cette classe, la chaîne est « WirelessDisplay ».</span><span class="sxs-lookup"><span data-stu-id="00c3e-142">For this class, the string is "WirelessDisplay".</span></span>

</dd> <dt>

<span data-ttu-id="00c3e-143">**ID**</span><span class="sxs-lookup"><span data-stu-id="00c3e-143">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c3e-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c3e-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c3e-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c3e-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c3e-146">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="00c3e-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="00c3e-147">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="00c3e-147">Describes the full path to the parent node.</span></span> <span data-ttu-id="00c3e-148">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="00c3e-148">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="00c3e-149">RequirePinForPairing</span><span class="sxs-lookup"><span data-stu-id="00c3e-149">RequirePinForPairing</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-requirepinforpairing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c3e-150">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="00c3e-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="00c3e-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="00c3e-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00c3e-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00c3e-152">Requirements</span></span>



| <span data-ttu-id="00c3e-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00c3e-153">Requirement</span></span> | <span data-ttu-id="00c3e-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="00c3e-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00c3e-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00c3e-155">Minimum supported client</span></span><br/> | <span data-ttu-id="00c3e-156">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00c3e-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="00c3e-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00c3e-157">Minimum supported server</span></span><br/> | <span data-ttu-id="00c3e-158">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="00c3e-158">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="00c3e-159">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="00c3e-159">Namespace</span></span><br/>                | <span data-ttu-id="00c3e-160">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="00c3e-160">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="00c3e-161">MOF</span><span class="sxs-lookup"><span data-stu-id="00c3e-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00c3e-162"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00c3e-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="00c3e-163">DLL</span><span class="sxs-lookup"><span data-stu-id="00c3e-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00c3e-164"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="00c3e-164"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

