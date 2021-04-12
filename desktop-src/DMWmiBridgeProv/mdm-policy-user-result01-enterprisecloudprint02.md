---
title: Classe MDM_Policy_User_Result01_EnterpriseCloudPrint02
description: La \_ \_ classe Result01 EnterpriseCloudPrint02 utilisateur de la stratégie MDM \_ \_ représente les stratégies d’impression Cloud disponibles.
ms.assetid: cf830cb5-2477-4b21-9d98-9fa9989daa7f
keywords:
- Classe MDM_Policy_User_Result01_EnterpriseCloudPrint02
- Classe MDM_Policy_User_Result01_EnterpriseCloudPrint02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_EnterpriseCloudPrint02
- MDM_Policy_User_Result01_EnterpriseCloudPrint02.InstanceID
- MDM_Policy_User_Result01_EnterpriseCloudPrint02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dfa75d102da3a61ff0a9f2094d31e0ba5b4abca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465422"
---
# <a name="mdm_policy_user_result01_enterprisecloudprint02-class"></a><span data-ttu-id="103fb-105">Classe d’utilisateur de la \_ stratégie MDM \_ \_ Result01 \_ EnterpriseCloudPrint02</span><span class="sxs-lookup"><span data-stu-id="103fb-105">MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02 class</span></span>

<span data-ttu-id="103fb-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="103fb-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="103fb-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="103fb-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="103fb-108">La \_ \_ classe Result01 EnterpriseCloudPrint02 utilisateur de la stratégie MDM \_ \_ représente les stratégies d’impression Cloud disponibles.</span><span class="sxs-lookup"><span data-stu-id="103fb-108">The MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02 class represents the available cloud print policies.</span></span>

<span data-ttu-id="103fb-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="103fb-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="103fb-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="103fb-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_EnterpriseCloudPrint02
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

## <a name="members"></a><span data-ttu-id="103fb-111">Membres</span><span class="sxs-lookup"><span data-stu-id="103fb-111">Members</span></span>

<span data-ttu-id="103fb-112">La **classe \_ \_ \_ Result01 \_ EnterpriseCloudPrint02 de la stratégie MDM User** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="103fb-112">The **MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02** class has these types of members:</span></span>

-   [<span data-ttu-id="103fb-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="103fb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="103fb-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="103fb-114">Properties</span></span>

<span data-ttu-id="103fb-115">La **classe \_ \_ \_ Result01 \_ EnterpriseCloudPrint02 de la stratégie MDM User** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="103fb-115">The **MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="103fb-116">CloudPrinterDiscoveryEndPoint</span><span class="sxs-lookup"><span data-stu-id="103fb-116">CloudPrinterDiscoveryEndPoint</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprinterdiscoveryendpoint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="103fb-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="103fb-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="103fb-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="103fb-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="103fb-119">CloudPrintOAuthAuthority</span><span class="sxs-lookup"><span data-stu-id="103fb-119">CloudPrintOAuthAuthority</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthauthority)
</dt> <dd> <dl> <dt>

<span data-ttu-id="103fb-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="103fb-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="103fb-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="103fb-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="103fb-122">CloudPrintOAuthClientId</span><span class="sxs-lookup"><span data-stu-id="103fb-122">CloudPrintOAuthClientId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthclientid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="103fb-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="103fb-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="103fb-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="103fb-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="103fb-125">CloudPrintResourceId</span><span class="sxs-lookup"><span data-stu-id="103fb-125">CloudPrintResourceId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintresourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="103fb-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="103fb-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="103fb-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="103fb-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="103fb-128">DiscoveryMaxPrinterLimit</span><span class="sxs-lookup"><span data-stu-id="103fb-128">DiscoveryMaxPrinterLimit</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-discoverymaxprinterlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="103fb-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="103fb-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="103fb-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="103fb-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="103fb-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="103fb-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103fb-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="103fb-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="103fb-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="103fb-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="103fb-134">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="103fb-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="103fb-135">MopriaDiscoveryResourceId</span><span class="sxs-lookup"><span data-stu-id="103fb-135">MopriaDiscoveryResourceId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-mopriadiscoveryresourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="103fb-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="103fb-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="103fb-137">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="103fb-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="103fb-138">**ID**</span><span class="sxs-lookup"><span data-stu-id="103fb-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103fb-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="103fb-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="103fb-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="103fb-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="103fb-141">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="103fb-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="103fb-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="103fb-142">Requirements</span></span>



| <span data-ttu-id="103fb-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="103fb-143">Requirement</span></span> | <span data-ttu-id="103fb-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="103fb-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="103fb-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="103fb-145">Minimum supported client</span></span><br/> | <span data-ttu-id="103fb-146">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="103fb-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="103fb-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="103fb-147">Minimum supported server</span></span><br/> | <span data-ttu-id="103fb-148">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="103fb-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="103fb-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="103fb-149">Namespace</span></span><br/>                | <span data-ttu-id="103fb-150">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="103fb-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="103fb-151">MOF</span><span class="sxs-lookup"><span data-stu-id="103fb-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="103fb-152"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="103fb-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="103fb-153">DLL</span><span class="sxs-lookup"><span data-stu-id="103fb-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="103fb-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="103fb-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

