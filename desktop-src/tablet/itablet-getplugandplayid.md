---
description: Retourne une chaîne contenant l’ID de Plug-and-Play pour le périphérique tablette.
ms.assetid: a0b6619b-f80c-470b-aa3f-f0b30a9dbda8
title: 'ITablet :: GetPlugAndPlayId, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetPlugAndPlayId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 3fb6ce7d59cb29aac4b06b7245bc6246b0688a7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529268"
---
# <a name="itabletgetplugandplayid-method"></a><span data-ttu-id="953a8-103">ITablet :: GetPlugAndPlayId, méthode</span><span class="sxs-lookup"><span data-stu-id="953a8-103">ITablet::GetPlugAndPlayId method</span></span>

<span data-ttu-id="953a8-104">Retourne une chaîne contenant l’ID de Plug-and-Play pour le périphérique tablette.</span><span class="sxs-lookup"><span data-stu-id="953a8-104">Returns a string containing the Plug and Play ID for the tablet device.</span></span>

## <a name="syntax"></a><span data-ttu-id="953a8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="953a8-105">Syntax</span></span>


```C++
HRESULT GetPlugAndPlayId(
  [out] LPWSTR *ppwszPPId
);
```



## <a name="parameters"></a><span data-ttu-id="953a8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="953a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="953a8-107">*ppwszPPId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="953a8-107">*ppwszPPId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="953a8-108">Pointeur vers une chaîne contenant l’ID de Plug-and-Play pour le périphérique tablette.</span><span class="sxs-lookup"><span data-stu-id="953a8-108">Pointer to a string containing the Plug and Play ID for the tablet device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="953a8-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="953a8-109">Return value</span></span>

<span data-ttu-id="953a8-110">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="953a8-110">This method can return one of these values.</span></span>



| <span data-ttu-id="953a8-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="953a8-111">Return code</span></span>                                                                            | <span data-ttu-id="953a8-112">Description</span><span class="sxs-lookup"><span data-stu-id="953a8-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="953a8-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="953a8-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="953a8-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="953a8-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="953a8-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="953a8-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="953a8-116">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="953a8-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="953a8-117">Notes</span><span class="sxs-lookup"><span data-stu-id="953a8-117">Remarks</span></span>

<span data-ttu-id="953a8-118">Il incombe à l’appelant de libérer la mémoire retournée à partir de cette méthode à l’aide de [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="953a8-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="953a8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="953a8-119">Requirements</span></span>



| <span data-ttu-id="953a8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="953a8-120">Requirement</span></span> | <span data-ttu-id="953a8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="953a8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="953a8-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="953a8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="953a8-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="953a8-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="953a8-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="953a8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="953a8-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="953a8-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="953a8-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="953a8-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="953a8-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="953a8-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="953a8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="953a8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="953a8-129">**Interface ITablet**</span><span class="sxs-lookup"><span data-stu-id="953a8-129">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

