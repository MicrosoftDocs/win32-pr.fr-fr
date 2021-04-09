---
description: Récupère le nom du stylet du Tablet PC.
ms.assetid: 94955c04-f699-428b-b4bf-53919b61b1ab
title: 'ITabletCursor :: GetName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b9d984d5eb711c2344ba0f9fb2dbf410a7d49bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952914"
---
# <a name="itabletcursorgetname-method"></a><span data-ttu-id="582b0-103">ITabletCursor :: GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="582b0-103">ITabletCursor::GetName method</span></span>

<span data-ttu-id="582b0-104">Récupère le nom du stylet du Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="582b0-104">Retrieves the name of the tablet stylus.</span></span>

## <a name="syntax"></a><span data-ttu-id="582b0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="582b0-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="582b0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="582b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="582b0-107">*ppwszName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="582b0-107">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="582b0-108">Nom du stylet du Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="582b0-108">The name of the tablet stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="582b0-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="582b0-109">Return value</span></span>

<span data-ttu-id="582b0-110">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="582b0-110">This method can return one of these values.</span></span>



| <span data-ttu-id="582b0-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="582b0-111">Return code</span></span>                                                                            | <span data-ttu-id="582b0-112">Description</span><span class="sxs-lookup"><span data-stu-id="582b0-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="582b0-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="582b0-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="582b0-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="582b0-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="582b0-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="582b0-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="582b0-116">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="582b0-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="582b0-117">Notes</span><span class="sxs-lookup"><span data-stu-id="582b0-117">Remarks</span></span>

<span data-ttu-id="582b0-118">Il incombe à l’appelant de libérer la mémoire retournée à partir de cette méthode à l’aide de [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="582b0-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="582b0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="582b0-119">Requirements</span></span>



| <span data-ttu-id="582b0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="582b0-120">Requirement</span></span> | <span data-ttu-id="582b0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="582b0-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="582b0-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="582b0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="582b0-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="582b0-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="582b0-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="582b0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="582b0-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="582b0-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="582b0-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="582b0-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="582b0-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="582b0-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="582b0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="582b0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="582b0-129">**ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="582b0-129">**ITabletCursor**</span></span>](itabletcursor.md)
</dt> <dt>

[<span data-ttu-id="582b0-130">**Interface ITabletCursorButton**</span><span class="sxs-lookup"><span data-stu-id="582b0-130">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

