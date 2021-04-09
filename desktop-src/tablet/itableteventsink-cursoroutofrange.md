---
description: Se produit lorsque le stylet quitte la plage de détection physique (proximité) de la tablette.
ms.assetid: ded01278-126d-415d-9a7b-1e6fe3650a37
title: 'ITabletEventSink :: CursorOutOfRange, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorOutOfRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: e2250401f3888bd07ff250549c11c34e6a54576d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868678"
---
# <a name="itableteventsinkcursoroutofrange-method"></a><span data-ttu-id="90cb6-103">ITabletEventSink :: CursorOutOfRange, méthode</span><span class="sxs-lookup"><span data-stu-id="90cb6-103">ITabletEventSink::CursorOutOfRange method</span></span>

<span data-ttu-id="90cb6-104">Se produit lorsque le stylet quitte la plage de détection physique (proximité) de la tablette.</span><span class="sxs-lookup"><span data-stu-id="90cb6-104">Occurs when the stylus leaves the physical detection range (proximity) of the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="90cb6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90cb6-105">Syntax</span></span>


```C++
HRESULT CursorOutOfRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="90cb6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90cb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90cb6-107">*TCID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="90cb6-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90cb6-108">Identificateur de la tablette.</span><span class="sxs-lookup"><span data-stu-id="90cb6-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="90cb6-109">*confirmation*</span><span class="sxs-lookup"><span data-stu-id="90cb6-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="90cb6-110">Identificateur du stylet.</span><span class="sxs-lookup"><span data-stu-id="90cb6-110">The identifier of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90cb6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="90cb6-111">Return value</span></span>

<span data-ttu-id="90cb6-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="90cb6-112">This method can return one of these values.</span></span>



| <span data-ttu-id="90cb6-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="90cb6-113">Return code</span></span>                                                                            | <span data-ttu-id="90cb6-114">Description</span><span class="sxs-lookup"><span data-stu-id="90cb6-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="90cb6-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="90cb6-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="90cb6-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="90cb6-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="90cb6-117"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="90cb6-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="90cb6-118">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="90cb6-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="90cb6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90cb6-119">Requirements</span></span>



| <span data-ttu-id="90cb6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90cb6-120">Requirement</span></span> | <span data-ttu-id="90cb6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="90cb6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90cb6-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90cb6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="90cb6-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90cb6-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="90cb6-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90cb6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="90cb6-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="90cb6-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="90cb6-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="90cb6-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="90cb6-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="90cb6-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90cb6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90cb6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90cb6-129">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="90cb6-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




