---
title: Méthode ITsSbResourcePluginStoreEx ReleaseTargetLock
description: Libère un verrou sur une cible.
ms.assetid: ab2ae9f3-2d38-4b31-9889-58297c574bd4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ReleaseTargetLock
- Méthode ReleaseTargetLock Services Bureau à distance, interface ITsSbResourcePluginStoreEx
- Services Bureau à distance de l’interface ITsSbResourcePluginStoreEx, méthode ReleaseTargetLock
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.ReleaseTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc34bdb27e40316ea1271bf0faa5d8c6b0abfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104299"
---
# <a name="itssbresourcepluginstoreexreleasetargetlock-method"></a><span data-ttu-id="97772-106">ITsSbResourcePluginStoreEx :: ReleaseTargetLock, méthode</span><span class="sxs-lookup"><span data-stu-id="97772-106">ITsSbResourcePluginStoreEx::ReleaseTargetLock method</span></span>

<span data-ttu-id="97772-107">Libère un verrou sur une cible.</span><span class="sxs-lookup"><span data-stu-id="97772-107">Releases a lock on a target.</span></span>

## <a name="syntax"></a><span data-ttu-id="97772-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97772-108">Syntax</span></span>


```C++
HRESULT ReleaseTargetLock(
  [in] IUnknown *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="97772-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97772-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97772-110">*pContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97772-110">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97772-111">Pointeur vers le contexte retourné par la méthode [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) .</span><span class="sxs-lookup"><span data-stu-id="97772-111">A pointer to the context returned by the [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97772-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97772-112">Return value</span></span>

<span data-ttu-id="97772-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="97772-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="97772-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="97772-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="97772-115">Notes</span><span class="sxs-lookup"><span data-stu-id="97772-115">Remarks</span></span>

<span data-ttu-id="97772-116">Cette méthode est uniquement disponible sur Windows Server 2012 R2 avec [KB3091411](https://support.microsoft.com/kb/3091411) installé dans l’interface [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) .</span><span class="sxs-lookup"><span data-stu-id="97772-116">This method is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) interface.</span></span> <span data-ttu-id="97772-117">Cette méthode est disponible dans l’interface [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) à partir de Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="97772-117">This method is available on the [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface starting with Windows Server 2016.</span></span>

## <a name="requirements"></a><span data-ttu-id="97772-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97772-118">Requirements</span></span>



| <span data-ttu-id="97772-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97772-119">Requirement</span></span> | <span data-ttu-id="97772-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="97772-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="97772-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97772-121">Minimum supported client</span></span><br/> | <span data-ttu-id="97772-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="97772-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="97772-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97772-123">Minimum supported server</span></span><br/> | <span data-ttu-id="97772-124">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="97772-124">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="97772-125">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="97772-125">End of server support</span></span><br/>    | <span data-ttu-id="97772-126">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="97772-126">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="97772-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="97772-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="97772-128"><dt>SbTsV. idl</dt></span><span class="sxs-lookup"><span data-stu-id="97772-128"><dt>SbTsV.idl</dt></span></span> </dl>          |
| <span data-ttu-id="97772-129">IID</span><span class="sxs-lookup"><span data-stu-id="97772-129">IID</span></span><br/>                      | <span data-ttu-id="97772-130">IID \_ ITsSbResourcePluginStoreEx est défini en tant que 80b83ffd-625d-11e5-BEA1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="97772-130">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="97772-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97772-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97772-132">**ITsSbResourcePluginStoreEx**</span><span class="sxs-lookup"><span data-stu-id="97772-132">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





