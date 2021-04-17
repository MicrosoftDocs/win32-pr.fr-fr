---
description: Récupère le numéro de version du système d’événements.
ms.assetid: 6355f1b3-e1e7-435f-9795-d92464e004ae
title: 'IEventSystem2 :: GetVersion, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.GetVersion
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2c75538d9fd71cb8ee81e454249fd5116ccd090c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483872"
---
# <a name="ieventsystem2getversion-method"></a><span data-ttu-id="9c264-103">IEventSystem2 :: GetVersion, méthode</span><span class="sxs-lookup"><span data-stu-id="9c264-103">IEventSystem2::GetVersion method</span></span>

<span data-ttu-id="9c264-104">Récupère le numéro de version du système d’événements.</span><span class="sxs-lookup"><span data-stu-id="9c264-104">Retrieves the version number of the event system.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c264-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c264-105">Syntax</span></span>


```C++
HRESULT GetVersion(
  [out] int *pnVersion
);
```



## <a name="parameters"></a><span data-ttu-id="9c264-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c264-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c264-107">*pnVersion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9c264-107">*pnVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c264-108">Numéro de version du système d’événements.</span><span class="sxs-lookup"><span data-stu-id="9c264-108">The version number of the event system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c264-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9c264-109">Return value</span></span>

<span data-ttu-id="9c264-110">Cette méthode peut retourner les valeurs de retour standard E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inattendue, e \_ Fail et S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9c264-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c264-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c264-111">Requirements</span></span>



| <span data-ttu-id="9c264-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c264-112">Requirement</span></span> | <span data-ttu-id="9c264-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c264-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="9c264-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c264-114">Minimum supported client</span></span><br/> | <span data-ttu-id="9c264-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c264-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9c264-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c264-116">Minimum supported server</span></span><br/> | <span data-ttu-id="9c264-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c264-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9c264-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c264-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c264-119">**IEventSystem2**</span><span class="sxs-lookup"><span data-stu-id="9c264-119">**IEventSystem2**</span></span>](ieventsystem2.md)
</dt> </dl>

 

 




