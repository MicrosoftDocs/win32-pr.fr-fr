---
description: Vérifie l’existence de tous les abonnés temporaires dans le magasin de données. En appelant cette méthode, vous pouvez vous assurer que tous les abonnés temporaires répertoriés dans le magasin de données sont actifs.
ms.assetid: fffdde33-e960-42ef-a089-8ea8a6f33d52
title: 'IEventSystem2 :: VerifyTransientSubscribers, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.VerifyTransientSubscribers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4415f405b95f341b645ca1dccbf254df2ffc7167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950568"
---
# <a name="ieventsystem2verifytransientsubscribers-method"></a><span data-ttu-id="4405f-104">IEventSystem2 :: VerifyTransientSubscribers, méthode</span><span class="sxs-lookup"><span data-stu-id="4405f-104">IEventSystem2::VerifyTransientSubscribers method</span></span>

<span data-ttu-id="4405f-105">Vérifie l’existence de tous les abonnés temporaires dans le magasin de données.</span><span class="sxs-lookup"><span data-stu-id="4405f-105">Verifies the existence of all transient subscribers in the data store.</span></span> <span data-ttu-id="4405f-106">En appelant cette méthode, vous pouvez vous assurer que tous les abonnés temporaires répertoriés dans le magasin de données sont actifs.</span><span class="sxs-lookup"><span data-stu-id="4405f-106">By calling this method, you can ensure that all transient subscribers listed in the data store are active.</span></span>

## <a name="syntax"></a><span data-ttu-id="4405f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4405f-107">Syntax</span></span>


```C++
HRESULT VerifyTransientSubscribers();
```



## <a name="parameters"></a><span data-ttu-id="4405f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4405f-108">Parameters</span></span>

<span data-ttu-id="4405f-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4405f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4405f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4405f-110">Return value</span></span>

<span data-ttu-id="4405f-111">Cette méthode peut retourner les valeurs de retour standard E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inattendue, e \_ Fail et S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4405f-111">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="4405f-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4405f-112">Requirements</span></span>



| <span data-ttu-id="4405f-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4405f-113">Requirement</span></span> | <span data-ttu-id="4405f-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="4405f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4405f-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4405f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4405f-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4405f-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4405f-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4405f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4405f-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4405f-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4405f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4405f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4405f-120">**IEventSystem2**</span><span class="sxs-lookup"><span data-stu-id="4405f-120">**IEventSystem2**</span></span>](ieventsystem2.md)
</dt> </dl>

 

 




