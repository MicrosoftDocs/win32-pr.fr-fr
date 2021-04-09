---
description: Récupère la transaction ou le proxy de transaction associé au contexte actuel, le cas échéant.
ms.assetid: 2f85f395-3ec5-4c5a-a6db-c902cb8f8486
title: 'IContextTransactionInfo :: FetchTransaction, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.FetchTransaction
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0e753974f93539f051465f13a1ea92d7e0e3bfa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110915"
---
# <a name="icontexttransactioninfofetchtransaction-method"></a><span data-ttu-id="64c55-103">IContextTransactionInfo :: FetchTransaction, méthode</span><span class="sxs-lookup"><span data-stu-id="64c55-103">IContextTransactionInfo::FetchTransaction method</span></span>

<span data-ttu-id="64c55-104">Récupère la transaction ou le proxy de transaction associé au contexte actuel, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="64c55-104">Retrieves the transaction or transaction proxy that is associated with the current context, if any.</span></span>

## <a name="syntax"></a><span data-ttu-id="64c55-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64c55-105">Syntax</span></span>


```C++
HRESULT FetchTransaction(
  [out, retval] IUnknown **pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="64c55-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64c55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64c55-107">*punk* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="64c55-107">*pUnk* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="64c55-108">Transaction ou proxy de transaction associé au contexte actuel ; Sinon, **null**.</span><span class="sxs-lookup"><span data-stu-id="64c55-108">The transaction or transaction proxy that is associated with the current context; otherwise, **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64c55-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64c55-109">Return value</span></span>

<span data-ttu-id="64c55-110">Cette méthode peut retourner les valeurs de retour standard E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inattendue et S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="64c55-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="64c55-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64c55-111">Requirements</span></span>



| <span data-ttu-id="64c55-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64c55-112">Requirement</span></span> | <span data-ttu-id="64c55-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="64c55-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="64c55-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64c55-114">Minimum supported client</span></span><br/> | <span data-ttu-id="64c55-115">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64c55-115">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="64c55-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64c55-116">Minimum supported server</span></span><br/> | <span data-ttu-id="64c55-117">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64c55-117">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="64c55-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64c55-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64c55-119">**IContextTransactionInfo**</span><span class="sxs-lookup"><span data-stu-id="64c55-119">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

 




