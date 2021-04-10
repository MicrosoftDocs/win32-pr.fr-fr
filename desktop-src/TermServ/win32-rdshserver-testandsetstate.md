---
title: Méthode TestAndSetState de la classe Win32_RDSHServer
description: Compare l’état actuel à l’objet comparand spécifié ; Si les deux correspondent, l’État est défini sur une nouvelle valeur. Quelle que soit la correspondance, l’état actuel est également retourné.
ms.assetid: f1bb0076-251b-4c0d-92f9-1c460e1b26bb
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode TestAndSetState
- Services Bureau à distance de la méthode TestAndSetState, classe Win32_RDSHServer
- Win32_RDSHServer de la classe Services Bureau à distance, méthode TestAndSetState
topic_type:
- apiref
api_name:
- Win32_RDSHServer.TestAndSetState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff4c9b616c2a288f5f39b240d71b2611e25d45f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103984"
---
# <a name="testandsetstate-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="43b5a-107">Méthode TestAndSetState de la \_ classe Win32 RDSHServer</span><span class="sxs-lookup"><span data-stu-id="43b5a-107">TestAndSetState method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="43b5a-108">Compare l’état actuel à l’objet comparand spécifié ; Si les deux correspondent, l’État est défini sur une nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="43b5a-108">Compares the current state to the specified comparand; if the two match, the state is set to a new value.</span></span> <span data-ttu-id="43b5a-109">Quelle que soit la correspondance, l’état actuel est également retourné.</span><span class="sxs-lookup"><span data-stu-id="43b5a-109">Regardless of the match, the current state is also returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="43b5a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43b5a-110">Syntax</span></span>


```mof
uint32 TestAndSetState(
  [in]  uint32 Comparand,
  [in]  uint32 NewState,
  [out] uint32 InitState
);
```



## <a name="parameters"></a><span data-ttu-id="43b5a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43b5a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43b5a-112">*Comparand* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="43b5a-112">*Comparand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43b5a-113">Valeur à comparer à l’état actuel. Si les deux valeurs correspondent, l’État est défini sur *NewState*.</span><span class="sxs-lookup"><span data-stu-id="43b5a-113">A value to compare to the current state; if the two values match, the state is set to *NewState*.</span></span>

</dd> <dt>

<span data-ttu-id="43b5a-114">*NewState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="43b5a-114">*NewState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43b5a-115">Nouvelle valeur de l’État.</span><span class="sxs-lookup"><span data-stu-id="43b5a-115">The new value of the state.</span></span>

</dd> <dt>

<span data-ttu-id="43b5a-116">*InitState* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="43b5a-116">*InitState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43b5a-117">En cas de réussite ou d’échec, retourne l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="43b5a-117">On success or failure, returns the current state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43b5a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43b5a-118">Requirements</span></span>



| <span data-ttu-id="43b5a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43b5a-119">Requirement</span></span> | <span data-ttu-id="43b5a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="43b5a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="43b5a-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43b5a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="43b5a-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="43b5a-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="43b5a-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43b5a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="43b5a-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="43b5a-124">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="43b5a-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="43b5a-125">Namespace</span></span><br/>                | <span data-ttu-id="43b5a-126">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="43b5a-126">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="43b5a-127">MOF</span><span class="sxs-lookup"><span data-stu-id="43b5a-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43b5a-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43b5a-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="43b5a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="43b5a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43b5a-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43b5a-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="43b5a-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43b5a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43b5a-132">**\_RDSHServer Win32**</span><span class="sxs-lookup"><span data-stu-id="43b5a-132">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





