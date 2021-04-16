---
description: Se produit lorsqu’un contexte de tablette est en cours de destruction.
ms.assetid: 805289d8-267e-488b-8092-6b07b37dd6d4
title: 'ITabletEventSink :: ContextDestroy, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.ContextDestroy
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c9b5d78d4ce4032c1a7a2082fb749afc5a39949a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530033"
---
# <a name="itableteventsinkcontextdestroy-method"></a><span data-ttu-id="e3b38-103">ITabletEventSink :: ContextDestroy, méthode</span><span class="sxs-lookup"><span data-stu-id="e3b38-103">ITabletEventSink::ContextDestroy method</span></span>

<span data-ttu-id="e3b38-104">Se produit lorsqu’un contexte de tablette est en cours de destruction.</span><span class="sxs-lookup"><span data-stu-id="e3b38-104">Occurs when a tablet context is being destroyed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b38-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3b38-105">Syntax</span></span>


```C++
HRESULT ContextDestroy(
  [in] TABLET_CONTEXT_ID tcid
);
```



## <a name="parameters"></a><span data-ttu-id="e3b38-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3b38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3b38-107">*TCID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e3b38-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b38-108">Identificateur du contexte de tablette qui est détruit.</span><span class="sxs-lookup"><span data-stu-id="e3b38-108">The identifier of the tablet context being destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3b38-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e3b38-109">Return value</span></span>

<span data-ttu-id="e3b38-110">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="e3b38-110">This method can return one of these values.</span></span>



| <span data-ttu-id="e3b38-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e3b38-111">Return code</span></span>                                                                            | <span data-ttu-id="e3b38-112">Description</span><span class="sxs-lookup"><span data-stu-id="e3b38-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="e3b38-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e3b38-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="e3b38-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="e3b38-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="e3b38-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="e3b38-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="e3b38-116">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="e3b38-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e3b38-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3b38-117">Requirements</span></span>



| <span data-ttu-id="e3b38-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3b38-118">Requirement</span></span> | <span data-ttu-id="e3b38-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3b38-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b38-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3b38-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e3b38-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3b38-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e3b38-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3b38-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e3b38-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3b38-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e3b38-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e3b38-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="e3b38-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e3b38-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3b38-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3b38-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b38-127">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="e3b38-127">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




