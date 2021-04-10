---
description: Récupère un rectangle qui représente la zone d’entrée maximale de la tablette.
ms.assetid: 98facd24-b019-40d1-afe1-28c9a78cae80
title: 'ITablet :: GetMaxInputRect, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetMaxInputRect
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: de2649fe7410e6d335f653c09bfe86a8ddaac813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867098"
---
# <a name="itabletgetmaxinputrect-method"></a><span data-ttu-id="60e83-103">ITablet :: GetMaxInputRect, méthode</span><span class="sxs-lookup"><span data-stu-id="60e83-103">ITablet::GetMaxInputRect method</span></span>

<span data-ttu-id="60e83-104">Récupère un rectangle qui représente la zone d’entrée maximale de la tablette.</span><span class="sxs-lookup"><span data-stu-id="60e83-104">Retrieves a rectangle that represents maximum input area of the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="60e83-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60e83-105">Syntax</span></span>


```C++
HRESULT GetMaxInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a><span data-ttu-id="60e83-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60e83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60e83-107">*prcInput* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="60e83-107">*prcInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60e83-108">Pointeur vers le rectangle qui représente la zone d’entrée maximale de la tablette.</span><span class="sxs-lookup"><span data-stu-id="60e83-108">Pointer to rectangle that represents maximum input area of the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60e83-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60e83-109">Return value</span></span>

<span data-ttu-id="60e83-110">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="60e83-110">This method can return one of these values.</span></span>



| <span data-ttu-id="60e83-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="60e83-111">Return code</span></span>                                                                            | <span data-ttu-id="60e83-112">Description</span><span class="sxs-lookup"><span data-stu-id="60e83-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="60e83-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="60e83-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="60e83-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="60e83-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="60e83-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="60e83-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="60e83-116">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="60e83-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="60e83-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60e83-117">Requirements</span></span>



| <span data-ttu-id="60e83-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60e83-118">Requirement</span></span> | <span data-ttu-id="60e83-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="60e83-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="60e83-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60e83-120">Minimum supported client</span></span><br/> | <span data-ttu-id="60e83-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60e83-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="60e83-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60e83-122">Minimum supported server</span></span><br/> | <span data-ttu-id="60e83-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="60e83-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="60e83-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="60e83-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="60e83-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="60e83-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60e83-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60e83-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e83-127">**Interface ITablet**</span><span class="sxs-lookup"><span data-stu-id="60e83-127">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




