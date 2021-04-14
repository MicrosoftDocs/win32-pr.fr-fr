---
description: Récupère l’identificateur du stylet.
ms.assetid: 27320a2f-1e4a-4d7d-a1f8-5244f4a03415
title: 'ITabletCursor :: GetId, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5d4f71d2cd465bfd2d1ff4c245154a300c431df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393719"
---
# <a name="itabletcursorgetid-method"></a><span data-ttu-id="2b129-103">ITabletCursor :: GetId, méthode</span><span class="sxs-lookup"><span data-stu-id="2b129-103">ITabletCursor::GetId method</span></span>

<span data-ttu-id="2b129-104">Récupère l’identificateur du stylet.</span><span class="sxs-lookup"><span data-stu-id="2b129-104">Retrieves the stylus identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b129-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b129-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] CURSOR_ID *pCid
);
```



## <a name="parameters"></a><span data-ttu-id="2b129-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b129-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b129-107">*pCid* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2b129-107">*pCid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b129-108">Identificateur du stylet du Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="2b129-108">The identifier of the tablet stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b129-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2b129-109">Return value</span></span>

<span data-ttu-id="2b129-110">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="2b129-110">This method can return one of these values.</span></span>



| <span data-ttu-id="2b129-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2b129-111">Return code</span></span>                                                                            | <span data-ttu-id="2b129-112">Description</span><span class="sxs-lookup"><span data-stu-id="2b129-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="2b129-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2b129-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="2b129-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="2b129-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="2b129-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="2b129-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="2b129-116">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="2b129-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2b129-117">Notes</span><span class="sxs-lookup"><span data-stu-id="2b129-117">Remarks</span></span>

<span data-ttu-id="2b129-118">L' \_ ID de curseur est défini en tant que DWORD.</span><span class="sxs-lookup"><span data-stu-id="2b129-118">CURSOR\_ID is defined as a DWORD.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b129-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b129-119">Requirements</span></span>



| <span data-ttu-id="2b129-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b129-120">Requirement</span></span> | <span data-ttu-id="2b129-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b129-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b129-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b129-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2b129-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b129-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2b129-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b129-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2b129-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b129-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2b129-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2b129-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="2b129-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2b129-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b129-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b129-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b129-129">**Interface ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="2b129-129">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




