---
title: Méthode GetJoinedNodeCount de la classe Win32_RDMSJoinedNode
description: Obtenir le nombre de serveurs sur lesquels sont installés les rôles spécifiés.
ms.assetid: ed2ae0b5-5cbc-4c11-a2ad-065f88dd5842
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetJoinedNodeCount
- Services Bureau à distance de la méthode GetJoinedNodeCount, classe Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode de la classe Services Bureau à distance, méthode GetJoinedNodeCount
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.GetJoinedNodeCount
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ecc5c388814873aa690e9af5adda5081aad4d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106533569"
---
# <a name="getjoinednodecount-method-of-the-win32_rdmsjoinednode-class"></a><span data-ttu-id="1feab-106">Méthode GetJoinedNodeCount de la \_ classe Win32 RDMSJoinedNode</span><span class="sxs-lookup"><span data-stu-id="1feab-106">GetJoinedNodeCount method of the Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="1feab-107">Obtenir le nombre de serveurs sur lesquels sont installés les rôles spécifiés.</span><span class="sxs-lookup"><span data-stu-id="1feab-107">Get number of servers that have the specified roles installed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1feab-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1feab-108">Syntax</span></span>


```mof
uint32 GetJoinedNodeCount(
  [in]  uint32 roleType,
  [out] uint32 Count
);
```



## <a name="parameters"></a><span data-ttu-id="1feab-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1feab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1feab-110">*roleType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1feab-110">*roleType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1feab-111">Champ de type de champ qui spécifie les types de rôles.</span><span class="sxs-lookup"><span data-stu-id="1feab-111">A bitfield that specifies the role types.</span></span>

<dt>

<span data-ttu-id="1feab-112">0</span><span class="sxs-lookup"><span data-stu-id="1feab-112">0</span></span>
</dt> <dd>

<span data-ttu-id="1feab-113">Tous</span><span class="sxs-lookup"><span data-stu-id="1feab-113">All</span></span>

</dd> <dt>

<span data-ttu-id="1feab-114">1</span><span class="sxs-lookup"><span data-stu-id="1feab-114">1</span></span>
</dt> <dd>

<span data-ttu-id="1feab-115">Connexion Bureau à distance Broker (RDCB)</span><span class="sxs-lookup"><span data-stu-id="1feab-115">Remote Desktop Connection Broker (RDCB)</span></span>

</dd> <dt>

<span data-ttu-id="1feab-116">2</span><span class="sxs-lookup"><span data-stu-id="1feab-116">2</span></span>
</dt> <dd>

<span data-ttu-id="1feab-117">Hôte de session Bureau à distance (hôte de session)</span><span class="sxs-lookup"><span data-stu-id="1feab-117">Remote Desktop Session Host (RDSH)</span></span>

</dd> <dt>

<span data-ttu-id="1feab-118">4</span><span class="sxs-lookup"><span data-stu-id="1feab-118">4</span></span>
</dt> <dd>

<span data-ttu-id="1feab-119">Serveur hôte de virtualisation des services Bureau à distance (RDVH)</span><span class="sxs-lookup"><span data-stu-id="1feab-119">Remote Desktop Virtualization Host (RDVH)</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1feab-120">*Nombre* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1feab-120">*Count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1feab-121">En cas de réussite, retourne le nombre de serveurs sur lesquels sont installés les rôles spécifiés.</span><span class="sxs-lookup"><span data-stu-id="1feab-121">On success, returns the number of servers with the specified roles installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1feab-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1feab-122">Return value</span></span>

<span data-ttu-id="1feab-123">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="1feab-123">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1feab-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1feab-124">Requirements</span></span>



| <span data-ttu-id="1feab-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1feab-125">Requirement</span></span> | <span data-ttu-id="1feab-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="1feab-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1feab-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1feab-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1feab-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1feab-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="1feab-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1feab-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1feab-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1feab-130">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="1feab-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1feab-131">Namespace</span></span><br/>                | <span data-ttu-id="1feab-132">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="1feab-132">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="1feab-133">MOF</span><span class="sxs-lookup"><span data-stu-id="1feab-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1feab-134"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1feab-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="1feab-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1feab-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1feab-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1feab-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="1feab-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1feab-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1feab-138">**\_RDMSJoinedNode Win32**</span><span class="sxs-lookup"><span data-stu-id="1feab-138">**Win32\_RDMSJoinedNode**</span></span>](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





