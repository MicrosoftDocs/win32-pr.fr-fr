---
title: Méthode Join de la classe Win32_RDMSJoinedNode
description: Ajoute un nœud à Bureau à distance Management Services (RDMS).
ms.assetid: 7451d12a-ace2-4564-bf6d-fb0169be967f
ms.tgt_platform: multiple
keywords:
- Méthode Join Services Bureau à distance
- Méthode Join Services Bureau à distance, classe Win32_RDMSJoinedNode
- Services Bureau à distance de la classe Win32_RDMSJoinedNode, méthode Join
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Join
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587e68758971453e8c4e307ccb37ce6cede262f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384155"
---
# <a name="join-method-of-the-win32_rdmsjoinednode-class"></a><span data-ttu-id="70ed2-106">Méthode Join de la \_ classe RDMSJoinedNode Win32</span><span class="sxs-lookup"><span data-stu-id="70ed2-106">Join method of the Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="70ed2-107">Ajoute un nœud à Bureau à distance Management Services (RDMS).</span><span class="sxs-lookup"><span data-stu-id="70ed2-107">Adds a node to Remote Desktop Management Services (RDMS).</span></span>

## <a name="syntax"></a><span data-ttu-id="70ed2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70ed2-108">Syntax</span></span>


```mof
uint32 Join(
  [in] string NodeFQDN,
  [in] string NodeSID
);
```



## <a name="parameters"></a><span data-ttu-id="70ed2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70ed2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70ed2-110">*NodeFQDN* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="70ed2-110">*NodeFQDN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70ed2-111">Nom de domaine complet du nœud.</span><span class="sxs-lookup"><span data-stu-id="70ed2-111">The fully qualified domain name of the node.</span></span>

</dd> <dt>

<span data-ttu-id="70ed2-112">*NodeSID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="70ed2-112">*NodeSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70ed2-113">Identificateur de sécurité (SID) du nœud.</span><span class="sxs-lookup"><span data-stu-id="70ed2-113">The security identifier (SID) of the node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70ed2-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="70ed2-114">Return value</span></span>

<span data-ttu-id="70ed2-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="70ed2-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="70ed2-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70ed2-116">Requirements</span></span>



| <span data-ttu-id="70ed2-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70ed2-117">Requirement</span></span> | <span data-ttu-id="70ed2-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="70ed2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="70ed2-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70ed2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="70ed2-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="70ed2-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="70ed2-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70ed2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="70ed2-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="70ed2-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="70ed2-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="70ed2-123">Namespace</span></span><br/>                | <span data-ttu-id="70ed2-124">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="70ed2-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="70ed2-125">MOF</span><span class="sxs-lookup"><span data-stu-id="70ed2-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70ed2-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70ed2-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="70ed2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="70ed2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70ed2-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70ed2-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="70ed2-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70ed2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70ed2-130">**\_RDMSJoinedNode Win32**</span><span class="sxs-lookup"><span data-stu-id="70ed2-130">**Win32\_RDMSJoinedNode**</span></span>](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





