---
description: Récupère les paramètres de contexte par défaut pour la tablette.
ms.assetid: 59d1bab0-a8b8-4e23-9311-2921f9035dc4
title: 'ITablet :: GetDefaultContextSettings, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetDefaultContextSettings
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7e2f0977257553d8405b337dcc1f22d8b0fdff5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757348"
---
# <a name="itabletgetdefaultcontextsettings-method"></a><span data-ttu-id="3ae09-103">ITablet :: GetDefaultContextSettings, méthode</span><span class="sxs-lookup"><span data-stu-id="3ae09-103">ITablet::GetDefaultContextSettings method</span></span>

<span data-ttu-id="3ae09-104">Récupère les paramètres de contexte par défaut pour la tablette.</span><span class="sxs-lookup"><span data-stu-id="3ae09-104">Retrieves the default context settings for the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ae09-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ae09-105">Syntax</span></span>


```C++
HRESULT GetDefaultContextSettings(
  [out] TABLET_CONTEXT_SETTINGS **ppTCS
);
```



## <a name="parameters"></a><span data-ttu-id="3ae09-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ae09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ae09-107">*ppTCS* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3ae09-107">*ppTCS* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ae09-108">Paramètres de contexte par défaut pour la tablette.</span><span class="sxs-lookup"><span data-stu-id="3ae09-108">The default context settings for the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ae09-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3ae09-109">Return value</span></span>

<span data-ttu-id="3ae09-110">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="3ae09-110">This method can return one of these values.</span></span>



| <span data-ttu-id="3ae09-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3ae09-111">Return code</span></span>                                                                            | <span data-ttu-id="3ae09-112">Description</span><span class="sxs-lookup"><span data-stu-id="3ae09-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="3ae09-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3ae09-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="3ae09-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="3ae09-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="3ae09-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="3ae09-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="3ae09-116">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="3ae09-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3ae09-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3ae09-117">Remarks</span></span>

<span data-ttu-id="3ae09-118">Il incombe à l’appelant de libérer la mémoire retournée à partir de cette méthode à l’aide de [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="3ae09-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ae09-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ae09-119">Requirements</span></span>



| <span data-ttu-id="3ae09-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ae09-120">Requirement</span></span> | <span data-ttu-id="3ae09-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ae09-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ae09-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ae09-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3ae09-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ae09-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3ae09-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ae09-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3ae09-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ae09-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3ae09-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3ae09-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ae09-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ae09-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ae09-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ae09-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ae09-129">**Interface ITablet**</span><span class="sxs-lookup"><span data-stu-id="3ae09-129">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

