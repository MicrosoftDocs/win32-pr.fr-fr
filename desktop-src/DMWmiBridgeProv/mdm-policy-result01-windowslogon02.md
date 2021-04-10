---
title: Classe MDM_Policy_Result01_WindowsLogon02
description: La \_ \_ classe WindowsLogon02 de la stratégie MDM Result01 \_ obtient les paramètres de l’écran de verrouillage et de l’interface utilisateur réseau à l’ouverture de session.
ms.assetid: 4c710e3d-e7d5-4e6e-ad99-b3c7d1813599
keywords:
- Classe MDM_Policy_Result01_WindowsLogon02
- Classe MDM_Policy_Result01_WindowsLogon02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WindowsLogon02
- MDM_Policy_Result01_WindowsLogon02.InstanceID
- MDM_Policy_Result01_WindowsLogon02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de8e9c0e2ebc2e82d5daef174ce9322b5b4b5ec7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102968"
---
# <a name="mdm_policy_result01_windowslogon02-class"></a><span data-ttu-id="9252b-105">\_Classe WindowsLogon02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="9252b-105">MDM\_Policy\_Result01\_WindowsLogon02 class</span></span>

<span data-ttu-id="9252b-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="9252b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9252b-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="9252b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9252b-108">La \_ \_ classe WindowsLogon02 de la stratégie MDM Result01 \_ obtient les paramètres de l’écran de verrouillage et de l’interface utilisateur réseau à l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="9252b-108">The MDM\_Policy\_Result01\_WindowsLogon02 class gets the settings of the lock screen and network user interface at logon.</span></span>

<span data-ttu-id="9252b-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9252b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9252b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9252b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WindowsLogon02
{
  string InstanceID;
  string ParentID;
  string DontDisplayNetworkSelectionUI;
  string DisableLockScreenAppNotifications;
  sint32 HideFastUserSwitching;
};
```

## <a name="members"></a><span data-ttu-id="9252b-111">Membres</span><span class="sxs-lookup"><span data-stu-id="9252b-111">Members</span></span>

<span data-ttu-id="9252b-112">La **classe \_ \_ Result01 \_ WindowsLogon02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9252b-112">The **MDM\_Policy\_Result01\_WindowsLogon02** class has these types of members:</span></span>

-   [<span data-ttu-id="9252b-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9252b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9252b-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9252b-114">Properties</span></span>

<span data-ttu-id="9252b-115">La **classe \_ \_ Result01 \_ WindowsLogon02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9252b-115">The **MDM\_Policy\_Result01\_WindowsLogon02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9252b-116">DisableLockScreenAppNotifications</span><span class="sxs-lookup"><span data-stu-id="9252b-116">DisableLockScreenAppNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-disablelockscreenappnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9252b-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9252b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9252b-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9252b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9252b-119">DontDisplayNetworkSelectionUI</span><span class="sxs-lookup"><span data-stu-id="9252b-119">DontDisplayNetworkSelectionUI</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-dontdisplaynetworkselectionui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9252b-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9252b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9252b-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9252b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9252b-122">HideFastUserSwitching</span><span class="sxs-lookup"><span data-stu-id="9252b-122">HideFastUserSwitching</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-hidefastuserswitching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9252b-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="9252b-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9252b-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9252b-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9252b-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9252b-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9252b-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9252b-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9252b-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9252b-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9252b-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9252b-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9252b-129">**ID**</span><span class="sxs-lookup"><span data-stu-id="9252b-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9252b-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9252b-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9252b-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9252b-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9252b-132">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9252b-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9252b-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9252b-133">Requirements</span></span>



| <span data-ttu-id="9252b-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9252b-134">Requirement</span></span> | <span data-ttu-id="9252b-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="9252b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9252b-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9252b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9252b-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9252b-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9252b-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9252b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9252b-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9252b-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9252b-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9252b-140">Namespace</span></span><br/>                | <span data-ttu-id="9252b-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="9252b-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9252b-142">MOF</span><span class="sxs-lookup"><span data-stu-id="9252b-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9252b-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9252b-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9252b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9252b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9252b-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9252b-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

