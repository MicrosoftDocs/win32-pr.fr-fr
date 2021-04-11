---
title: Méthode ITsSbResourcePluginStoreEx AcquireTargetLock
description: Verrouille une cible.
ms.assetid: 76707f1d-1f13-4d81-8954-2acf05cda2cd
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AcquireTargetLock
- Méthode AcquireTargetLock Services Bureau à distance, interface ITsSbResourcePluginStoreEx
- Services Bureau à distance de l’interface ITsSbResourcePluginStoreEx, méthode AcquireTargetLock
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.AcquireTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c18be0a544ebcea2d2cecb40dcea3a08e4bd35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103156"
---
# <a name="itssbresourcepluginstoreexacquiretargetlock-method"></a><span data-ttu-id="443ad-106">ITsSbResourcePluginStoreEx :: AcquireTargetLock, méthode</span><span class="sxs-lookup"><span data-stu-id="443ad-106">ITsSbResourcePluginStoreEx::AcquireTargetLock method</span></span>

<span data-ttu-id="443ad-107">Verrouille une cible.</span><span class="sxs-lookup"><span data-stu-id="443ad-107">Locks a target.</span></span>

## <a name="syntax"></a><span data-ttu-id="443ad-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="443ad-108">Syntax</span></span>


```C++
HRESULT AcquireTargetLock(
  [in]  BSTR     targetName,
  [in]  DWORD    dwTimeout,
  [out] IUnknown **ppContext
);
```



## <a name="parameters"></a><span data-ttu-id="443ad-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="443ad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="443ad-110">*TargetName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="443ad-110">*targetName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="443ad-111">Nom de la cible à verrouiller.</span><span class="sxs-lookup"><span data-stu-id="443ad-111">The name of the target to lock.</span></span>

</dd> <dt>

<span data-ttu-id="443ad-112">*dwTimeout* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="443ad-112">*dwTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="443ad-113">Délai d’attente de l’opération, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="443ad-113">The timeout for the operation, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="443ad-114">*ppContext* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="443ad-114">*ppContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="443ad-115">Retourne un pointeur vers le contexte du verrou.</span><span class="sxs-lookup"><span data-stu-id="443ad-115">Returns a pointer to the context of the lock.</span></span> <span data-ttu-id="443ad-116">Pour libérer le verrou, fournissez ce pointeur à la méthode [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) .</span><span class="sxs-lookup"><span data-stu-id="443ad-116">To release the lock, supply this pointer to the [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="443ad-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="443ad-117">Return value</span></span>

<span data-ttu-id="443ad-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="443ad-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="443ad-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="443ad-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="443ad-120">Notes</span><span class="sxs-lookup"><span data-stu-id="443ad-120">Remarks</span></span>

<span data-ttu-id="443ad-121">Une fois le verrou acquis, le thread appelant est supposé avoir un accès exclusif à l’objet cible et, par conséquent, aucun autre thread (au sein du même ordinateur) ne peut le mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="443ad-121">After the lock is acquired, the calling thread is assumed to have exclusive access to the target object and therefore no other thread (within the same machine) can update it.</span></span> <span data-ttu-id="443ad-122">Par conséquent, le thread appelant doit appeler la méthode [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) dès qu’il a effectué les mises à jour nécessaires de l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="443ad-122">Therefore the calling thread must call the [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) method as soon as it has made the necessary updates to the target object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="443ad-123">ce verrou n’empêche pas complètement la modification des objets cibles en externe s’il existe plusieurs Service Broker pour les connexions dans le déploiement.</span><span class="sxs-lookup"><span data-stu-id="443ad-123">this lock does not completely prevent target objects from being modified externally if more than one Connection Broker exists in the deployment.</span></span> <span data-ttu-id="443ad-124">Le thread appelant doit être prêt à gérer une défaillance de manière appropriée et à retenter la mise à jour cible.</span><span class="sxs-lookup"><span data-stu-id="443ad-124">The calling thread must be prepared to handle a failure gracefully and retry the target update.</span></span>

 

<span data-ttu-id="443ad-125">Cette méthode est disponible sur Windows Server 2012 R2 avec [KB3091411](https://support.microsoft.com/kb/3091411) installé dans l’interface [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) .</span><span class="sxs-lookup"><span data-stu-id="443ad-125">This method is available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="443ad-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="443ad-126">Requirements</span></span>



| <span data-ttu-id="443ad-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="443ad-127">Requirement</span></span> | <span data-ttu-id="443ad-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="443ad-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="443ad-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="443ad-129">Minimum supported client</span></span><br/> | <span data-ttu-id="443ad-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="443ad-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="443ad-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="443ad-131">Minimum supported server</span></span><br/> | <span data-ttu-id="443ad-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="443ad-132">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="443ad-133">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="443ad-133">End of server support</span></span><br/>    | <span data-ttu-id="443ad-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="443ad-134">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="443ad-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="443ad-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="443ad-136"><dt>SbTsV. idl</dt></span><span class="sxs-lookup"><span data-stu-id="443ad-136"><dt>SbTsV.idl</dt></span></span> </dl>          |
| <span data-ttu-id="443ad-137">IID</span><span class="sxs-lookup"><span data-stu-id="443ad-137">IID</span></span><br/>                      | <span data-ttu-id="443ad-138">IID \_ ITsSbResourcePluginStoreEx est défini en tant que 80b83ffd-625d-11e5-BEA1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="443ad-138">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="443ad-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="443ad-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="443ad-140">**ITsSbResourcePluginStoreEx**</span><span class="sxs-lookup"><span data-stu-id="443ad-140">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





