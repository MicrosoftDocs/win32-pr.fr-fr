---
description: Se produit lors de la création d’un nouveau contexte de tablette.
ms.assetid: 64e1f778-90c1-417d-a80b-37aeecffd411
title: 'ITabletEventSink :: ContextCreate, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.ContextCreate
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: e622a246c7c317cf9e3373cbd3791108ed071e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320741"
---
# <a name="itableteventsinkcontextcreate-method"></a><span data-ttu-id="eca94-103">ITabletEventSink :: ContextCreate, méthode</span><span class="sxs-lookup"><span data-stu-id="eca94-103">ITabletEventSink::ContextCreate method</span></span>

<span data-ttu-id="eca94-104">Se produit lors de la création d’un nouveau contexte de tablette.</span><span class="sxs-lookup"><span data-stu-id="eca94-104">Occurs when a new tablet context is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="eca94-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eca94-105">Syntax</span></span>


```C++
HRESULT ContextCreate(
  [in] TABLET_CONTEXT_ID tcid
);
```



## <a name="parameters"></a><span data-ttu-id="eca94-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eca94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eca94-107">*TCID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eca94-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eca94-108">Identificateur du contexte de tablette en cours de création.</span><span class="sxs-lookup"><span data-stu-id="eca94-108">The identifier of the tablet context being created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eca94-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eca94-109">Return value</span></span>

<span data-ttu-id="eca94-110">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="eca94-110">This method can return one of these values.</span></span>



| <span data-ttu-id="eca94-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="eca94-111">Return code</span></span>                                                                            | <span data-ttu-id="eca94-112">Description</span><span class="sxs-lookup"><span data-stu-id="eca94-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="eca94-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eca94-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="eca94-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="eca94-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="eca94-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="eca94-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="eca94-116">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="eca94-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="eca94-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eca94-117">Requirements</span></span>



| <span data-ttu-id="eca94-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eca94-118">Requirement</span></span> | <span data-ttu-id="eca94-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="eca94-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eca94-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eca94-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eca94-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eca94-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="eca94-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eca94-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eca94-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="eca94-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="eca94-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eca94-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="eca94-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eca94-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eca94-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eca94-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eca94-127">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="eca94-127">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




