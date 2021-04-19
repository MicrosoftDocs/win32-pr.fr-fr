---
description: Retourne le nombre d’objets Cursor associés à la tablette.
ms.assetid: 7aa5802c-1255-41a4-b1fa-23e5f56c0b80
title: 'ITablet :: GetCursorCount, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetCursorCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 2309384e4aa36383277ba72cc407cabef7ab4b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524400"
---
# <a name="itabletgetcursorcount-method"></a><span data-ttu-id="ada81-103">ITablet :: GetCursorCount, méthode</span><span class="sxs-lookup"><span data-stu-id="ada81-103">ITablet::GetCursorCount method</span></span>

<span data-ttu-id="ada81-104">Retourne le nombre d’objets Cursor associés à la tablette.</span><span class="sxs-lookup"><span data-stu-id="ada81-104">Returns the number of cursor objects associated with the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="ada81-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ada81-105">Syntax</span></span>


```C++
HRESULT GetCursorCount(
  [out] ULONG *pcCurs
);
```



## <a name="parameters"></a><span data-ttu-id="ada81-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ada81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ada81-107">*pcCurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ada81-107">*pcCurs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ada81-108">Nombre d’objets Cursor associés à la tablette.</span><span class="sxs-lookup"><span data-stu-id="ada81-108">The number of cursor objects associated with the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ada81-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ada81-109">Return value</span></span>

<span data-ttu-id="ada81-110">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="ada81-110">This method can return one of these values.</span></span>



| <span data-ttu-id="ada81-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ada81-111">Return code</span></span>                                                                            | <span data-ttu-id="ada81-112">Description</span><span class="sxs-lookup"><span data-stu-id="ada81-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="ada81-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ada81-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="ada81-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="ada81-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="ada81-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="ada81-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="ada81-116">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="ada81-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ada81-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ada81-117">Requirements</span></span>



| <span data-ttu-id="ada81-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ada81-118">Requirement</span></span> | <span data-ttu-id="ada81-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ada81-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ada81-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ada81-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ada81-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ada81-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ada81-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ada81-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ada81-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ada81-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ada81-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ada81-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="ada81-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ada81-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ada81-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ada81-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ada81-127">**Interface ITablet**</span><span class="sxs-lookup"><span data-stu-id="ada81-127">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




