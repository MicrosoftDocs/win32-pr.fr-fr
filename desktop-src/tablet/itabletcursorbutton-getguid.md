---
description: Récupère l’identificateur unique du bouton du stylet.
ms.assetid: 06bd6a84-46cd-4c62-92d6-50caae359e43
title: 'ITabletCursorButton :: GetGuid, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetGuid
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 21d63ef0c934e96bc93b5384cab1e67f9dd452d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034969"
---
# <a name="itabletcursorbuttongetguid-method"></a><span data-ttu-id="edb40-103">ITabletCursorButton :: GetGuid, méthode</span><span class="sxs-lookup"><span data-stu-id="edb40-103">ITabletCursorButton::GetGuid method</span></span>

<span data-ttu-id="edb40-104">Récupère l’identificateur unique du bouton du stylet.</span><span class="sxs-lookup"><span data-stu-id="edb40-104">Retrieves the unique identifier of the stylus button.</span></span>

## <a name="syntax"></a><span data-ttu-id="edb40-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="edb40-105">Syntax</span></span>


```C++
HRESULT GetGuid(
  [out] GUID *pguidBtn
);
```



## <a name="parameters"></a><span data-ttu-id="edb40-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="edb40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edb40-107">*pguidBtn* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="edb40-107">*pguidBtn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edb40-108">Valeur unique qui identifie le bouton du stylet.</span><span class="sxs-lookup"><span data-stu-id="edb40-108">A unique value that identifies the stylus button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edb40-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="edb40-109">Return value</span></span>

<span data-ttu-id="edb40-110">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="edb40-110">This method can return one of these values.</span></span>



| <span data-ttu-id="edb40-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="edb40-111">Return code</span></span>                                                                            | <span data-ttu-id="edb40-112">Description</span><span class="sxs-lookup"><span data-stu-id="edb40-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="edb40-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="edb40-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="edb40-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="edb40-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="edb40-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="edb40-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="edb40-116">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="edb40-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="edb40-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="edb40-117">Requirements</span></span>



| <span data-ttu-id="edb40-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="edb40-118">Requirement</span></span> | <span data-ttu-id="edb40-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="edb40-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="edb40-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edb40-120">Minimum supported client</span></span><br/> | <span data-ttu-id="edb40-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="edb40-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="edb40-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edb40-122">Minimum supported server</span></span><br/> | <span data-ttu-id="edb40-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="edb40-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="edb40-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="edb40-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="edb40-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="edb40-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edb40-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edb40-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edb40-127">**Interface ITabletCursorButton**</span><span class="sxs-lookup"><span data-stu-id="edb40-127">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

 




