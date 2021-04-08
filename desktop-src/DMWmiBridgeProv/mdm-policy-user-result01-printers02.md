---
title: Classe MDM_Policy_User_Result01_Printers02
description: La \_ \_ classe Result01 Printers02 utilisateur de la stratégie MDM \_ \_ représente les stratégies d’imprimante disponibles.
ms.assetid: c9555ba3-589c-4b9f-8fad-86fcda031555
keywords:
- Classe MDM_Policy_User_Result01_Printers02
- Classe MDM_Policy_User_Result01_Printers02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Printers02
- MDM_Policy_User_Result01_Printers02.InstanceID
- MDM_Policy_User_Result01_Printers02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88a93e2547fbdd8d2d8883d187fca758d5d0b592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740085"
---
# <a name="mdm_policy_user_result01_printers02-class"></a><span data-ttu-id="84f10-105">Classe d’utilisateur de la \_ stratégie MDM \_ \_ Result01 \_ Printers02</span><span class="sxs-lookup"><span data-stu-id="84f10-105">MDM\_Policy\_User\_Result01\_Printers02 class</span></span>

<span data-ttu-id="84f10-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="84f10-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="84f10-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="84f10-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="84f10-108">La \_ \_ classe Result01 Printers02 utilisateur de la stratégie MDM \_ \_ représente les stratégies d’imprimante disponibles.</span><span class="sxs-lookup"><span data-stu-id="84f10-108">The MDM\_Policy\_User\_Result01\_Printers02 class represents the available printer policies.</span></span>

<span data-ttu-id="84f10-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="84f10-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f10-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84f10-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Printers02
{
  string InstanceID;
  string ParentID;
  string PointAndPrintRestrictions_User;
};
```

## <a name="members"></a><span data-ttu-id="84f10-111">Membres</span><span class="sxs-lookup"><span data-stu-id="84f10-111">Members</span></span>

<span data-ttu-id="84f10-112">La **classe \_ \_ \_ Result01 \_ Printers02 de la stratégie MDM User** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="84f10-112">The **MDM\_Policy\_User\_Result01\_Printers02** class has these types of members:</span></span>

-   [<span data-ttu-id="84f10-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="84f10-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84f10-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="84f10-114">Properties</span></span>

<span data-ttu-id="84f10-115">La **classe \_ \_ \_ Result01 \_ Printers02 de la stratégie MDM User** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="84f10-115">The **MDM\_Policy\_User\_Result01\_Printers02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84f10-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="84f10-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f10-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="84f10-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f10-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="84f10-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f10-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="84f10-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84f10-120">**ID**</span><span class="sxs-lookup"><span data-stu-id="84f10-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f10-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="84f10-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f10-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="84f10-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f10-123">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="84f10-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84f10-124">\_Utilisateur PointAndPrintRestrictions</span><span class="sxs-lookup"><span data-stu-id="84f10-124">PointAndPrintRestrictions\_User</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-pointandprintrestrictions-user)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f10-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="84f10-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f10-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="84f10-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84f10-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84f10-127">Requirements</span></span>



| <span data-ttu-id="84f10-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84f10-128">Requirement</span></span> | <span data-ttu-id="84f10-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="84f10-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84f10-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84f10-130">Minimum supported client</span></span><br/> | <span data-ttu-id="84f10-131">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84f10-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84f10-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84f10-132">Minimum supported server</span></span><br/> | <span data-ttu-id="84f10-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="84f10-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="84f10-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="84f10-134">Namespace</span></span><br/>                | <span data-ttu-id="84f10-135">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="84f10-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="84f10-136">MOF</span><span class="sxs-lookup"><span data-stu-id="84f10-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84f10-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84f10-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="84f10-138">DLL</span><span class="sxs-lookup"><span data-stu-id="84f10-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84f10-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84f10-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

