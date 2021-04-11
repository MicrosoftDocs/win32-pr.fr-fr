---
title: Classe MDM_Policy_Config01_ErrorReporting02
description: La \_ classe Config01 ErrorReporting02 de la stratégie MDM \_ \_ configure les stratégies de rapport d’erreurs.
ms.assetid: 41067b5e-0db5-43b3-b1d5-2d6c54c35388
keywords:
- Classe MDM_Policy_Config01_ErrorReporting02
- Classe MDM_Policy_Config01_ErrorReporting02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ErrorReporting02
- MDM_Policy_Config01_ErrorReporting02.InstanceID
- MDM_Policy_Config01_ErrorReporting02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1c23cf5b0b01f05fa3712d6b1de11461c6f47da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032663"
---
# <a name="mdm_policy_config01_errorreporting02-class"></a><span data-ttu-id="27e60-105">\_Classe ErrorReporting02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="27e60-105">MDM\_Policy\_Config01\_ErrorReporting02 class</span></span>

<span data-ttu-id="27e60-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="27e60-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="27e60-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="27e60-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="27e60-108">La \_ classe Config01 ErrorReporting02 de la stratégie MDM \_ \_ configure les stratégies de rapport d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="27e60-108">The MDM\_Policy\_Config01\_ErrorReporting02 class configures the error reporting policies.</span></span>

<span data-ttu-id="27e60-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="27e60-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="27e60-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27e60-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ErrorReporting02
{
  string InstanceID;
  string ParentID;
  string CustomizeConsentSettings;
  string DisableWindowsErrorReporting;
  string DisplayErrorNotification;
  string DoNotSendAdditionalData;
  string PreventCriticalErrorDisplay;
};
```

## <a name="members"></a><span data-ttu-id="27e60-111">Membres</span><span class="sxs-lookup"><span data-stu-id="27e60-111">Members</span></span>

<span data-ttu-id="27e60-112">La **classe \_ \_ Config01 \_ ErrorReporting02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="27e60-112">The **MDM\_Policy\_Config01\_ErrorReporting02** class has these types of members:</span></span>

-   [<span data-ttu-id="27e60-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="27e60-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="27e60-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="27e60-114">Properties</span></span>

<span data-ttu-id="27e60-115">La **classe \_ \_ Config01 \_ ErrorReporting02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="27e60-115">The **MDM\_Policy\_Config01\_ErrorReporting02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="27e60-116">CustomizeConsentSettings</span><span class="sxs-lookup"><span data-stu-id="27e60-116">CustomizeConsentSettings</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-customizeconsentsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e60-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="27e60-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e60-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="27e60-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="27e60-119">DisableWindowsErrorReporting</span><span class="sxs-lookup"><span data-stu-id="27e60-119">DisableWindowsErrorReporting</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-disablewindowserrorreporting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e60-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="27e60-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e60-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="27e60-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="27e60-122">DisplayErrorNotification</span><span class="sxs-lookup"><span data-stu-id="27e60-122">DisplayErrorNotification</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-displayerrornotification)
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e60-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="27e60-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e60-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="27e60-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="27e60-125">DoNotSendAdditionalData</span><span class="sxs-lookup"><span data-stu-id="27e60-125">DoNotSendAdditionalData</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-donotsendadditionaldata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e60-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="27e60-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e60-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="27e60-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="27e60-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="27e60-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e60-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="27e60-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e60-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="27e60-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e60-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="27e60-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="27e60-132">**ID**</span><span class="sxs-lookup"><span data-stu-id="27e60-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e60-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="27e60-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e60-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="27e60-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e60-135">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="27e60-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="27e60-136">PreventCriticalErrorDisplay</span><span class="sxs-lookup"><span data-stu-id="27e60-136">PreventCriticalErrorDisplay</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-preventcriticalerrordisplay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e60-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="27e60-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e60-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="27e60-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27e60-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27e60-139">Requirements</span></span>



| <span data-ttu-id="27e60-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27e60-140">Requirement</span></span> | <span data-ttu-id="27e60-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="27e60-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27e60-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27e60-142">Minimum supported client</span></span><br/> | <span data-ttu-id="27e60-143">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27e60-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="27e60-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27e60-144">Minimum supported server</span></span><br/> | <span data-ttu-id="27e60-145">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="27e60-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="27e60-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="27e60-146">Namespace</span></span><br/>                | <span data-ttu-id="27e60-147">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="27e60-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="27e60-148">MOF</span><span class="sxs-lookup"><span data-stu-id="27e60-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27e60-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27e60-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="27e60-150">DLL</span><span class="sxs-lookup"><span data-stu-id="27e60-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27e60-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27e60-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

