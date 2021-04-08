---
title: Classe MDM_Policy_User_Config01_EnterpriseCloudPrint02
description: La \_ \_ classe Config01 EnterpriseCloudPrint02 utilisateur de la stratégie MDM \_ \_ représente les stratégies d’impression Cloud disponibles.
ms.assetid: cc885184-1197-48c4-ba48-a2944a416534
keywords:
- Classe MDM_Policy_User_Config01_EnterpriseCloudPrint02
- Classe MDM_Policy_User_Config01_EnterpriseCloudPrint02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_EnterpriseCloudPrint02
- MDM_Policy_User_Config01_EnterpriseCloudPrint02.InstanceID
- MDM_Policy_User_Config01_EnterpriseCloudPrint02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2b9d42afbab4d3f17d91b6db630ef67faf6ccc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843633"
---
# <a name="mdm_policy_user_config01_enterprisecloudprint02-class"></a><span data-ttu-id="a73eb-105">Classe d’utilisateur de la \_ stratégie MDM \_ \_ Config01 \_ EnterpriseCloudPrint02</span><span class="sxs-lookup"><span data-stu-id="a73eb-105">MDM\_Policy\_User\_Config01\_EnterpriseCloudPrint02 class</span></span>

<span data-ttu-id="a73eb-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="a73eb-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a73eb-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="a73eb-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a73eb-108">La \_ \_ classe Config01 EnterpriseCloudPrint02 utilisateur de la stratégie MDM \_ \_ représente les stratégies d’impression Cloud disponibles.</span><span class="sxs-lookup"><span data-stu-id="a73eb-108">The MDM\_Policy\_User\_Config01\_EnterpriseCloudPrint02 class represents the available cloud print policies.</span></span>

<span data-ttu-id="a73eb-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a73eb-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a73eb-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a73eb-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_EnterpriseCloudPrint02
{
  string InstanceID;
  string ParentID;
  string CloudPrinterDiscoveryEndPoint;
  string CloudPrintOAuthAuthority;
  string CloudPrintOAuthClientId;
  string CloudPrintResourceId;
  sint32 DiscoveryMaxPrinterLimit;
  string MopriaDiscoveryResourceId;
};
```

## <a name="members"></a><span data-ttu-id="a73eb-111">Membres</span><span class="sxs-lookup"><span data-stu-id="a73eb-111">Members</span></span>

<span data-ttu-id="a73eb-112">La **classe \_ \_ \_ Config01 \_ EnterpriseCloudPrint02 de la stratégie MDM User** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a73eb-112">The **MDM\_Policy\_User\_Config01\_EnterpriseCloudPrint02** class has these types of members:</span></span>

-   [<span data-ttu-id="a73eb-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a73eb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a73eb-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a73eb-114">Properties</span></span>

<span data-ttu-id="a73eb-115">La **classe \_ \_ \_ Config01 \_ EnterpriseCloudPrint02 de la stratégie MDM User** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a73eb-115">The **MDM\_Policy\_User\_Config01\_EnterpriseCloudPrint02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a73eb-116">CloudPrinterDiscoveryEndPoint</span><span class="sxs-lookup"><span data-stu-id="a73eb-116">CloudPrinterDiscoveryEndPoint</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprinterdiscoveryendpoint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73eb-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a73eb-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a73eb-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a73eb-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a73eb-119">CloudPrintOAuthAuthority</span><span class="sxs-lookup"><span data-stu-id="a73eb-119">CloudPrintOAuthAuthority</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthauthority)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73eb-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a73eb-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a73eb-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a73eb-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a73eb-122">CloudPrintOAuthClientId</span><span class="sxs-lookup"><span data-stu-id="a73eb-122">CloudPrintOAuthClientId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthclientid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73eb-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a73eb-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a73eb-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a73eb-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a73eb-125">CloudPrintResourceId</span><span class="sxs-lookup"><span data-stu-id="a73eb-125">CloudPrintResourceId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintresourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73eb-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a73eb-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a73eb-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a73eb-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a73eb-128">DiscoveryMaxPrinterLimit</span><span class="sxs-lookup"><span data-stu-id="a73eb-128">DiscoveryMaxPrinterLimit</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-discoverymaxprinterlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73eb-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="a73eb-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a73eb-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a73eb-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a73eb-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a73eb-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73eb-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a73eb-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a73eb-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a73eb-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a73eb-134">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a73eb-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a73eb-135">MopriaDiscoveryResourceId</span><span class="sxs-lookup"><span data-stu-id="a73eb-135">MopriaDiscoveryResourceId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-mopriadiscoveryresourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73eb-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a73eb-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a73eb-137">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a73eb-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a73eb-138">**ID**</span><span class="sxs-lookup"><span data-stu-id="a73eb-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73eb-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a73eb-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a73eb-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a73eb-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a73eb-141">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a73eb-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a73eb-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a73eb-142">Requirements</span></span>



| <span data-ttu-id="a73eb-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a73eb-143">Requirement</span></span> | <span data-ttu-id="a73eb-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="a73eb-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a73eb-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a73eb-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a73eb-146">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a73eb-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a73eb-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a73eb-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a73eb-148">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a73eb-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a73eb-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a73eb-149">Namespace</span></span><br/>                | <span data-ttu-id="a73eb-150">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="a73eb-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a73eb-151">MOF</span><span class="sxs-lookup"><span data-stu-id="a73eb-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a73eb-152"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a73eb-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a73eb-153">DLL</span><span class="sxs-lookup"><span data-stu-id="a73eb-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a73eb-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a73eb-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

