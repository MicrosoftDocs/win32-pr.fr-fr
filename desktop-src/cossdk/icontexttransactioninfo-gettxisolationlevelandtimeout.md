---
description: Récupère le niveau d’isolation et la valeur de délai d’attente d’une transaction qui est hébergée dans le contexte de transaction racine.
ms.assetid: bb3ff03e-e69e-4a50-af36-4938eb4323df
title: 'IContextTransactionInfo :: GetTxIsolationLevelAndTimeout, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.GetTxIsolationLevelAndTimeout
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8545a697e672af7206a69ffa19618d5b70e055c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515582"
---
# <a name="icontexttransactioninfogettxisolationlevelandtimeout-method"></a><span data-ttu-id="0a5d0-103">IContextTransactionInfo :: GetTxIsolationLevelAndTimeout, méthode</span><span class="sxs-lookup"><span data-stu-id="0a5d0-103">IContextTransactionInfo::GetTxIsolationLevelAndTimeout method</span></span>

<span data-ttu-id="0a5d0-104">Récupère le niveau d’isolation et la valeur de délai d’attente d’une transaction qui est hébergée dans le contexte de transaction racine.</span><span class="sxs-lookup"><span data-stu-id="0a5d0-104">Retrieves the isolation level and timeout value of a transaction that is hosted in the root transaction context.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a5d0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a5d0-105">Syntax</span></span>


```C++
HRESULT GetTxIsolationLevelAndTimeout(
  [out] ISOLEVEL *pIsoLevel,
  [out] DWORD    *dwTime
);
```



## <a name="parameters"></a><span data-ttu-id="0a5d0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a5d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a5d0-107">*pIsoLevel* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0a5d0-107">*pIsoLevel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a5d0-108">Valeur [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) de la transaction.</span><span class="sxs-lookup"><span data-stu-id="0a5d0-108">The [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) value for the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="0a5d0-109">*dwTime* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0a5d0-109">*dwTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a5d0-110">Délai d’expiration de la transaction, en secondes.</span><span class="sxs-lookup"><span data-stu-id="0a5d0-110">The timeout of the transaction, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a5d0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0a5d0-111">Return value</span></span>

<span data-ttu-id="0a5d0-112">Cette méthode peut retourner les valeurs de retour standard E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inattendue et S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0a5d0-112">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a5d0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a5d0-113">Requirements</span></span>



| <span data-ttu-id="0a5d0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a5d0-114">Requirement</span></span> | <span data-ttu-id="0a5d0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a5d0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="0a5d0-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a5d0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0a5d0-117">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a5d0-117">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0a5d0-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a5d0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0a5d0-119">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a5d0-119">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a5d0-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a5d0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a5d0-121">**IContextTransactionInfo**</span><span class="sxs-lookup"><span data-stu-id="0a5d0-121">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

