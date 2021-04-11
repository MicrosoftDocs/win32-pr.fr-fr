---
title: Classe MDM_Policy_Config01_Power02
description: La \_ classe Config01 Power02 de la stratégie MDM \_ \_ configure les stratégies d’alimentation.
ms.assetid: 8913c38c-0d8d-456f-a412-d47c2ccd5d13
keywords:
- Classe MDM_Policy_Config01_Power02
- Classe MDM_Policy_Config01_Power02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Power02
- MDM_Policy_Config01_Power02.InstanceID
- MDM_Policy_Config01_Power02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9bdda57bbd85100e8bccb87990d928f448a972
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103616"
---
# <a name="mdm_policy_config01_power02-class"></a><span data-ttu-id="8c598-105">\_Classe Power02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="8c598-105">MDM\_Policy\_Config01\_Power02 class</span></span>

<span data-ttu-id="8c598-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="8c598-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8c598-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="8c598-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8c598-108">La \_ classe Config01 Power02 de la stratégie MDM \_ \_ configure les stratégies d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="8c598-108">The MDM\_Policy\_Config01\_Power02 class configures the power policies.</span></span>

<span data-ttu-id="8c598-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8c598-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c598-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c598-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Power02
{
  string InstanceID;
  string ParentID;
  string AllowStandbyWhenSleepingPluggedIn;
  string HibernateTimeoutPluggedIn;
  string HibernateTimeoutOnBattery;
  string DisplayOffTimeoutPluggedIn;
  string DisplayOffTimeoutOnBattery;
  string RequirePasswordWhenComputerWakesOnBattery;
  string RequirePasswordWhenComputerWakesPluggedIn;
  string StandbyTimeoutPluggedIn;
  string StandbyTimeoutOnBattery;
};
```

## <a name="members"></a><span data-ttu-id="8c598-111">Membres</span><span class="sxs-lookup"><span data-stu-id="8c598-111">Members</span></span>

<span data-ttu-id="8c598-112">La **classe \_ \_ Config01 \_ Power02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8c598-112">The **MDM\_Policy\_Config01\_Power02** class has these types of members:</span></span>

-   [<span data-ttu-id="8c598-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8c598-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c598-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8c598-114">Properties</span></span>

<span data-ttu-id="8c598-115">La **classe \_ \_ Config01 \_ Power02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8c598-115">The **MDM\_Policy\_Config01\_Power02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8c598-116">AllowStandbyWhenSleepingPluggedIn</span><span class="sxs-lookup"><span data-stu-id="8c598-116">AllowStandbyWhenSleepingPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-allowstandbywhensleepingpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c598-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c598-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c598-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8c598-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8c598-119">DisplayOffTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="8c598-119">DisplayOffTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c598-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c598-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c598-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8c598-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8c598-122">DisplayOffTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="8c598-122">DisplayOffTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c598-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c598-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c598-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8c598-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8c598-125">HibernateTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="8c598-125">HibernateTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c598-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c598-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c598-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8c598-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8c598-128">HibernateTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="8c598-128">HibernateTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c598-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c598-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c598-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8c598-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8c598-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8c598-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c598-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c598-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c598-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8c598-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c598-134">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8c598-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8c598-135">**ID**</span><span class="sxs-lookup"><span data-stu-id="8c598-135">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c598-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c598-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c598-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8c598-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c598-138">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8c598-138">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8c598-139">RequirePasswordWhenComputerWakesOnBattery</span><span class="sxs-lookup"><span data-stu-id="8c598-139">RequirePasswordWhenComputerWakesOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakesonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c598-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c598-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c598-141">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8c598-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8c598-142">RequirePasswordWhenComputerWakesPluggedIn</span><span class="sxs-lookup"><span data-stu-id="8c598-142">RequirePasswordWhenComputerWakesPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakespluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c598-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c598-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c598-144">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8c598-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8c598-145">StandbyTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="8c598-145">StandbyTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c598-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c598-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c598-147">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8c598-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8c598-148">StandbyTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="8c598-148">StandbyTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c598-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c598-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c598-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8c598-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c598-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c598-151">Requirements</span></span>



| <span data-ttu-id="8c598-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c598-152">Requirement</span></span> | <span data-ttu-id="8c598-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c598-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c598-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c598-154">Minimum supported client</span></span><br/> | <span data-ttu-id="8c598-155">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c598-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8c598-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c598-156">Minimum supported server</span></span><br/> | <span data-ttu-id="8c598-157">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c598-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8c598-158">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8c598-158">Namespace</span></span><br/>                | <span data-ttu-id="8c598-159">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="8c598-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8c598-160">MOF</span><span class="sxs-lookup"><span data-stu-id="8c598-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c598-161"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c598-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c598-162">DLL</span><span class="sxs-lookup"><span data-stu-id="8c598-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c598-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c598-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

