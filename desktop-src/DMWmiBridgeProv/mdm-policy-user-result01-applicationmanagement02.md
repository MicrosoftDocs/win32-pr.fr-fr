---
title: Classe MDM_Policy_User_Result01_ApplicationManagement02
description: La \_ \_ classe Result01 ApplicationManagement02 utilisateur de la stratégie MDM \_ \_ représente les stratégies de démarrage disponibles pour chaque utilisateur.
ms.assetid: 62545af1-9c26-481e-9668-cd253cf592e7
keywords:
- Classe MDM_Policy_User_Result01_ApplicationManagement02
- Classe MDM_Policy_User_Result01_ApplicationManagement02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_ApplicationManagement02
- MDM_Policy_User_Result01_ApplicationManagement02.InstanceID
- MDM_Policy_User_Result01_ApplicationManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18177046691e5c9fe5ca8cb61ee0518a41533c59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103858"
---
# <a name="mdm_policy_user_result01_applicationmanagement02-class"></a><span data-ttu-id="d5d13-105">Classe d’utilisateur de la \_ stratégie MDM \_ \_ Result01 \_ ApplicationManagement02</span><span class="sxs-lookup"><span data-stu-id="d5d13-105">MDM\_Policy\_User\_Result01\_ApplicationManagement02 class</span></span>

<span data-ttu-id="d5d13-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="d5d13-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d5d13-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="d5d13-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d5d13-108">La **classe \_ \_ \_ Result01 \_ ApplicationManagement02 utilisateur de la stratégie MDM** représente les stratégies de démarrage disponibles pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d5d13-108">The **MDM\_Policy\_User\_Result01\_ApplicationManagement02** class represents the start policies available that are set on a per-user basis.</span></span>

<span data-ttu-id="d5d13-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d5d13-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5d13-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5d13-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_ApplicationManagement02
{
  string InstanceID;
  string ParentID;
  sint32 RequirePrivateStoreOnly;
};
```

## <a name="members"></a><span data-ttu-id="d5d13-111">Membres</span><span class="sxs-lookup"><span data-stu-id="d5d13-111">Members</span></span>

<span data-ttu-id="d5d13-112">La **classe \_ \_ \_ Result01 \_ ApplicationManagement02 de la stratégie MDM User** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d5d13-112">The **MDM\_Policy\_User\_Result01\_ApplicationManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="d5d13-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d5d13-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d5d13-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d5d13-114">Properties</span></span>

<span data-ttu-id="d5d13-115">La **classe \_ \_ \_ Result01 \_ ApplicationManagement02 de la stratégie MDM User** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d5d13-115">The **MDM\_Policy\_User\_Result01\_ApplicationManagement02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d5d13-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d5d13-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d13-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d5d13-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5d13-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d5d13-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5d13-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d5d13-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d5d13-120">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="d5d13-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="d5d13-121">Pour cette classe, la chaîne est « ApplicationManagement ».</span><span class="sxs-lookup"><span data-stu-id="d5d13-121">For this class, the string is "ApplicationManagement"</span></span>

</dd> <dt>

<span data-ttu-id="d5d13-122">**ID**</span><span class="sxs-lookup"><span data-stu-id="d5d13-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d13-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d5d13-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5d13-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d5d13-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5d13-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d5d13-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d5d13-126">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="d5d13-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="d5d13-127">Pour cette classe, la chaîne est « ./User/Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="d5d13-127">For this class, the string is "./User/Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="d5d13-128">RequirePrivateStoreOnly</span><span class="sxs-lookup"><span data-stu-id="d5d13-128">RequirePrivateStoreOnly</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-requireprivatestoreonly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d13-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d5d13-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5d13-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d5d13-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5d13-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5d13-131">Requirements</span></span>



| <span data-ttu-id="d5d13-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5d13-132">Requirement</span></span> | <span data-ttu-id="d5d13-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5d13-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d13-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5d13-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d5d13-135">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5d13-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d5d13-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5d13-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d5d13-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5d13-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d5d13-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d5d13-138">Namespace</span></span><br/>                | <span data-ttu-id="d5d13-139">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="d5d13-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d5d13-140">MOF</span><span class="sxs-lookup"><span data-stu-id="d5d13-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5d13-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5d13-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5d13-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d5d13-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5d13-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5d13-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5d13-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5d13-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5d13-145">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="d5d13-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

