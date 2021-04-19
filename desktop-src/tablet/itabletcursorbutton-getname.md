---
description: Récupère le nom du bouton du stylet.
ms.assetid: 26fad9bc-43c2-4b00-b76b-bf9f1242da77
title: 'ITabletCursorButton :: GetName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b21fd92823fb0f60c0936f662982d176a938b4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523257"
---
# <a name="itabletcursorbuttongetname-method"></a><span data-ttu-id="40cde-103">ITabletCursorButton :: GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="40cde-103">ITabletCursorButton::GetName method</span></span>

<span data-ttu-id="40cde-104">Récupère le nom du bouton du stylet.</span><span class="sxs-lookup"><span data-stu-id="40cde-104">Retrieves the name of the stylus button.</span></span>

## <a name="syntax"></a><span data-ttu-id="40cde-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40cde-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="40cde-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40cde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40cde-107">*ppwszName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="40cde-107">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40cde-108">Le nom du bouton du stylet.</span><span class="sxs-lookup"><span data-stu-id="40cde-108">The name of the stylus button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40cde-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40cde-109">Return value</span></span>

<span data-ttu-id="40cde-110">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="40cde-110">This method can return one of these values.</span></span>



| <span data-ttu-id="40cde-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="40cde-111">Return code</span></span>                                                                            | <span data-ttu-id="40cde-112">Description</span><span class="sxs-lookup"><span data-stu-id="40cde-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="40cde-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="40cde-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="40cde-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="40cde-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="40cde-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="40cde-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="40cde-116">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="40cde-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="40cde-117">Notes</span><span class="sxs-lookup"><span data-stu-id="40cde-117">Remarks</span></span>

<span data-ttu-id="40cde-118">Il incombe à l’appelant de libérer la mémoire retournée à partir de cette méthode à l’aide de [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="40cde-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="40cde-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40cde-119">Requirements</span></span>



| <span data-ttu-id="40cde-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40cde-120">Requirement</span></span> | <span data-ttu-id="40cde-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="40cde-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40cde-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40cde-122">Minimum supported client</span></span><br/> | <span data-ttu-id="40cde-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40cde-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="40cde-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40cde-124">Minimum supported server</span></span><br/> | <span data-ttu-id="40cde-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="40cde-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="40cde-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="40cde-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="40cde-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="40cde-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40cde-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40cde-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40cde-129">**Interface ITabletCursorButton**</span><span class="sxs-lookup"><span data-stu-id="40cde-129">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

