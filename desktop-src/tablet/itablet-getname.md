---
description: Retourne une chaîne contenant le nom du périphérique tablette.
ms.assetid: 025620b5-ab68-4e36-ae26-2226a2fdeb61
title: 'ITablet :: GetName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c2d6bd20a011b1bf5cfbe7582445de45728bbd7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203248"
---
# <a name="itabletgetname-method"></a><span data-ttu-id="4aaf6-103">ITablet :: GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="4aaf6-103">ITablet::GetName method</span></span>

<span data-ttu-id="4aaf6-104">Retourne une chaîne contenant le nom du périphérique tablette.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-104">Returns a string containing the name of the tablet device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aaf6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4aaf6-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="4aaf6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4aaf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aaf6-107">*ppwszName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4aaf6-107">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4aaf6-108">Pointeur vers une chaîne contenant le nom du périphérique tablette.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-108">Pointer to a string containing the name of the tablet device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aaf6-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4aaf6-109">Return value</span></span>

<span data-ttu-id="4aaf6-110">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-110">This method can return one of these values.</span></span>



| <span data-ttu-id="4aaf6-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4aaf6-111">Return code</span></span>                                                                            | <span data-ttu-id="4aaf6-112">Description</span><span class="sxs-lookup"><span data-stu-id="4aaf6-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="4aaf6-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4aaf6-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="4aaf6-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="4aaf6-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="4aaf6-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="4aaf6-116">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4aaf6-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4aaf6-117">Remarks</span></span>

<span data-ttu-id="4aaf6-118">Il incombe à l’appelant de libérer la mémoire retournée à partir de cette méthode à l’aide de [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="4aaf6-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="4aaf6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4aaf6-119">Requirements</span></span>



| <span data-ttu-id="4aaf6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4aaf6-120">Requirement</span></span> | <span data-ttu-id="4aaf6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="4aaf6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4aaf6-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4aaf6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4aaf6-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4aaf6-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4aaf6-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4aaf6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4aaf6-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4aaf6-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4aaf6-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4aaf6-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="4aaf6-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4aaf6-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aaf6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4aaf6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aaf6-129">**Interface ITablet**</span><span class="sxs-lookup"><span data-stu-id="4aaf6-129">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

