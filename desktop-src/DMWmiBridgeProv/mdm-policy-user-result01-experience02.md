---
title: Classe MDM_Policy_User_Result01_Experience02
description: La \_ \_ classe Result01 Experience02 utilisateur de la stratégie MDM \_ \_ représente les stratégies d’expérience disponibles.
ms.assetid: 729dfc75-7458-426f-8173-9ba75b4ee306
keywords:
- Classe MDM_Policy_User_Result01_Experience02
- Classe MDM_Policy_User_Result01_Experience02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Experience02
- MDM_Policy_User_Result01_Experience02.InstanceID
- MDM_Policy_User_Result01_Experience02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320941108309264a2cce3be6e63edca305c1cd40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843626"
---
# <a name="mdm_policy_user_result01_experience02-class"></a><span data-ttu-id="d9995-105">Classe d’utilisateur de la \_ stratégie MDM \_ \_ Result01 \_ Experience02</span><span class="sxs-lookup"><span data-stu-id="d9995-105">MDM\_Policy\_User\_Result01\_Experience02 class</span></span>

<span data-ttu-id="d9995-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="d9995-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d9995-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="d9995-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d9995-108">La **classe \_ \_ \_ Result01 \_ Experience02 utilisateur de la stratégie MDM** représente les stratégies d’expérience disponibles.</span><span class="sxs-lookup"><span data-stu-id="d9995-108">The **MDM\_Policy\_User\_Result01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="d9995-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d9995-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9995-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9995-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowTailoredExperiencesWithDiagnosticData;
  sint32 AllowWindowsConsumerFeatures;
  sint32 AllowWindowsSpotlight;
  sint32 AllowWindowsSpotlightWindowsWelcomeExperience;
  sint32 AllowWindowsSpotlightOnActionCenter;
  sint32 ConfigureWindowsSpotlightOnLockScreen;
  sint32 AllowThirdPartySuggestionsInWindowsSpotlight;
};
```

## <a name="members"></a><span data-ttu-id="d9995-111">Membres</span><span class="sxs-lookup"><span data-stu-id="d9995-111">Members</span></span>

<span data-ttu-id="d9995-112">La **classe \_ \_ \_ Result01 \_ Experience02 de la stratégie MDM User** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d9995-112">The **MDM\_Policy\_User\_Result01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="d9995-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d9995-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d9995-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d9995-114">Properties</span></span>

<span data-ttu-id="d9995-115">La **classe \_ \_ \_ Result01 \_ Experience02 de la stratégie MDM User** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d9995-115">The **MDM\_Policy\_User\_Result01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d9995-116">AllowTailoredExperiencesWithDiagnosticData</span><span class="sxs-lookup"><span data-stu-id="d9995-116">AllowTailoredExperiencesWithDiagnosticData</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowtailoredexperienceswithdiagnosticdata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9995-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d9995-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9995-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d9995-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d9995-119">AllowThirdPartySuggestionsInWindowsSpotlight</span><span class="sxs-lookup"><span data-stu-id="d9995-119">AllowThirdPartySuggestionsInWindowsSpotlight</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowthirdpartysuggestionsinwindowsspotlight)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9995-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d9995-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9995-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d9995-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d9995-122">AllowWindowsConsumerFeatures</span><span class="sxs-lookup"><span data-stu-id="d9995-122">AllowWindowsConsumerFeatures</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsconsumerfeatures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9995-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d9995-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9995-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d9995-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d9995-125">AllowWindowsSpotlight</span><span class="sxs-lookup"><span data-stu-id="d9995-125">AllowWindowsSpotlight</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlight)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9995-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d9995-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9995-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d9995-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d9995-128">AllowWindowsSpotlightOnActionCenter</span><span class="sxs-lookup"><span data-stu-id="d9995-128">AllowWindowsSpotlightOnActionCenter</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightonactioncenter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9995-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d9995-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9995-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d9995-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d9995-131">AllowWindowsSpotlightWindowsWelcomeExperience</span><span class="sxs-lookup"><span data-stu-id="d9995-131">AllowWindowsSpotlightWindowsWelcomeExperience</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightwindowswelcomeexperience)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9995-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d9995-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9995-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d9995-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d9995-134">ConfigureWindowsSpotlightOnLockScreen</span><span class="sxs-lookup"><span data-stu-id="d9995-134">ConfigureWindowsSpotlightOnLockScreen</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-configurewindowsspotlightonlockscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9995-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d9995-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9995-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d9995-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d9995-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d9995-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9995-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d9995-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9995-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9995-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9995-140">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d9995-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d9995-141">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="d9995-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="d9995-142">Pour cette classe, la chaîne est « experience ».</span><span class="sxs-lookup"><span data-stu-id="d9995-142">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="d9995-143">**ID**</span><span class="sxs-lookup"><span data-stu-id="d9995-143">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9995-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d9995-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9995-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d9995-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9995-146">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d9995-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d9995-147">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="d9995-147">Describes the full path to the parent node.</span></span> <span data-ttu-id="d9995-148">Pour cette classe, la chaîne est « ./User/Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="d9995-148">For this class, the string is "./User/Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d9995-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9995-149">Requirements</span></span>



| <span data-ttu-id="d9995-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9995-150">Requirement</span></span> | <span data-ttu-id="d9995-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9995-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9995-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9995-152">Minimum supported client</span></span><br/> | <span data-ttu-id="d9995-153">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9995-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d9995-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9995-154">Minimum supported server</span></span><br/> | <span data-ttu-id="d9995-155">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9995-155">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="d9995-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d9995-156">Namespace</span></span><br/>                | <span data-ttu-id="d9995-157">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="d9995-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="d9995-158">MOF</span><span class="sxs-lookup"><span data-stu-id="d9995-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9995-159"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9995-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="d9995-160">DLL</span><span class="sxs-lookup"><span data-stu-id="d9995-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9995-161"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="d9995-161"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

