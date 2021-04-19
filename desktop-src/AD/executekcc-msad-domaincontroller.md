---
title: Méthode ExecuteKCC de la classe MSAD_DomainController
description: Appelle la fonction DsReplicaConsistencyCheck, qui appelle le vérificateur de cohérence des connaissances (KCC) pour vérifier la topologie de réplication.
ms.assetid: 958c9a15-cde2-4c74-bd4c-c2d53551cfb0
ms.tgt_platform: multiple
keywords:
- Active Directory de la méthode ExecuteKCC
- Active Directory de la méthode ExecuteKCC, classe MSAD_DomainController
- MSAD_DomainController de la classe Active Directory, méthode ExecuteKCC
topic_type:
- apiref
api_name:
- MSAD_DomainController.ExecuteKCC
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce017f86042181d2e80ae3614e3fc1cbccc676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518091"
---
# <a name="executekcc-method-of-the-msad_domaincontroller-class"></a><span data-ttu-id="83c00-106">Méthode ExecuteKCC de la \_ classe DOMAINCONTROLLER MSAD</span><span class="sxs-lookup"><span data-stu-id="83c00-106">ExecuteKCC method of the MSAD\_DomainController class</span></span>

<span data-ttu-id="83c00-107">Appelle la fonction [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) , qui appelle le vérificateur de cohérence des connaissances (KCC) pour vérifier la topologie de réplication.</span><span class="sxs-lookup"><span data-stu-id="83c00-107">Calls the [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) function, which invokes the Knowledge Consistency Checker (KCC) to verify the replication topology.</span></span>

## <a name="syntax"></a><span data-ttu-id="83c00-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83c00-108">Syntax</span></span>


```mof
void ExecuteKCC(
  [in] uint32 TaskID,
  [in] uint32 dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="83c00-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83c00-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83c00-110">*TaskId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83c00-110">*TaskID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83c00-111">Tâche que le KCC doit exécuter.</span><span class="sxs-lookup"><span data-stu-id="83c00-111">The task that the KCC should execute.</span></span> <span data-ttu-id="83c00-112">**Service d’annuaire \_ La \_ \_ \_ topologie de mise à jour de KCC TaskID** est la seule valeur actuellement prise en charge.</span><span class="sxs-lookup"><span data-stu-id="83c00-112">**DS\_KCC\_TASKID\_UPDATE\_TOPOLOGY** is the only value that is currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="83c00-113">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83c00-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83c00-114">Ensemble d’indicateurs qui modifient le comportement de la méthode **ExecuteKCC** .</span><span class="sxs-lookup"><span data-stu-id="83c00-114">A set of flags that modify the behavior of the **ExecuteKCC** method.</span></span> <span data-ttu-id="83c00-115">Ce paramètre peut avoir la valeur zéro ou une combinaison d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="83c00-115">This parameter can be zero or a combination of one or more of the following values.</span></span>

<dt>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>

<span data-ttu-id="83c00-116"><span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**indicateur KCC des services de domaine Active Directory \_ \_ \_ asynchrone \_**</span><span class="sxs-lookup"><span data-stu-id="83c00-116"><span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**DS\_KCC\_FLAG\_ASYNC\_OP**</span></span>


</dt> <dd>

<span data-ttu-id="83c00-117">La tâche est mise en file d’attente, puis la fonction retourne sans attendre que la tâche se termine.</span><span class="sxs-lookup"><span data-stu-id="83c00-117">The task is queued and then the function returns without waiting for the task to complete.</span></span>

</dd> <dt>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>

<span data-ttu-id="83c00-118"><span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**\_indicateur KCC \_ DS \_ amorti**</span><span class="sxs-lookup"><span data-stu-id="83c00-118"><span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**DS\_KCC\_FLAG\_DAMPED**</span></span>


</dt> <dd>

<span data-ttu-id="83c00-119">La tâche ne sera pas ajoutée à la file d’attente si une autre tâche en file d’attente s’exécutera bientôt.</span><span class="sxs-lookup"><span data-stu-id="83c00-119">The task will not be added to the queue if another queued task will run soon.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83c00-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83c00-120">Return value</span></span>

<span data-ttu-id="83c00-121">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="83c00-121">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="83c00-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83c00-122">Requirements</span></span>



| <span data-ttu-id="83c00-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83c00-123">Requirement</span></span> | <span data-ttu-id="83c00-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="83c00-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83c00-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83c00-125">Minimum supported client</span></span><br/> | <span data-ttu-id="83c00-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="83c00-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="83c00-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83c00-127">Minimum supported server</span></span><br/> | <span data-ttu-id="83c00-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83c00-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="83c00-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="83c00-129">Namespace</span></span><br/>                | <span data-ttu-id="83c00-130">\\MicrosoftActiveDirectory racine</span><span class="sxs-lookup"><span data-stu-id="83c00-130">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="83c00-131">MOF</span><span class="sxs-lookup"><span data-stu-id="83c00-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83c00-132"><dt>ReplProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83c00-132"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="83c00-133">DLL</span><span class="sxs-lookup"><span data-stu-id="83c00-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83c00-134"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83c00-134"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83c00-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83c00-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83c00-136">**MSAD \_ DomainController**</span><span class="sxs-lookup"><span data-stu-id="83c00-136">**MSAD\_DomainController**</span></span>](msad-domaincontroller.md)
</dt> </dl>

 

 





