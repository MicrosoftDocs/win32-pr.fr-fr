---
description: Indique si le stylet est à l’envers.
ms.assetid: 04b05287-000d-455f-88e5-821c7fdb8119
title: 'ITabletCursor :: IsInverted, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.IsInverted
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 041b81c38f3370421c96a4c0d66201254a715e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524327"
---
# <a name="itabletcursorisinverted-method"></a><span data-ttu-id="dbac1-103">ITabletCursor :: IsInverted, méthode</span><span class="sxs-lookup"><span data-stu-id="dbac1-103">ITabletCursor::IsInverted method</span></span>

<span data-ttu-id="dbac1-104">Indique si le stylet est à l’envers.</span><span class="sxs-lookup"><span data-stu-id="dbac1-104">Indicates if the stylus is upside down.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbac1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbac1-105">Syntax</span></span>


```C++
HRESULT IsInverted();
```



## <a name="parameters"></a><span data-ttu-id="dbac1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbac1-106">Parameters</span></span>

<span data-ttu-id="dbac1-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="dbac1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dbac1-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dbac1-108">Return value</span></span>

<span data-ttu-id="dbac1-109">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="dbac1-109">This method can return one of these values.</span></span>



| <span data-ttu-id="dbac1-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dbac1-110">Return code</span></span>                                                                             | <span data-ttu-id="dbac1-111">Description</span><span class="sxs-lookup"><span data-stu-id="dbac1-111">Description</span></span>                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="dbac1-112"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dbac1-112"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="dbac1-113">Le stylet est inversé.</span><span class="sxs-lookup"><span data-stu-id="dbac1-113">The stylus is inverted.</span></span><br/>        |
| <dl> <span data-ttu-id="dbac1-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="dbac1-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="dbac1-115">Le stylet n’est pas inversé.</span><span class="sxs-lookup"><span data-stu-id="dbac1-115">The stylus is not inverted.</span></span><br/>    |
| <dl> <span data-ttu-id="dbac1-116"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="dbac1-116"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="dbac1-117">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="dbac1-117">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dbac1-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbac1-118">Requirements</span></span>



| <span data-ttu-id="dbac1-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbac1-119">Requirement</span></span> | <span data-ttu-id="dbac1-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbac1-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbac1-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbac1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dbac1-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbac1-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dbac1-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbac1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dbac1-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbac1-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dbac1-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dbac1-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="dbac1-126"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dbac1-126"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbac1-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbac1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbac1-128">**ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="dbac1-128">**ITabletCursor**</span></span>](itabletcursor.md)
</dt> <dt>

[<span data-ttu-id="dbac1-129">**Interface ITabletCursorButton**</span><span class="sxs-lookup"><span data-stu-id="dbac1-129">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

 




