---
description: Se produit lorsqu’un stylet est dans la plage de détection du digitaliseur.
ms.assetid: 22be233a-fc33-4a8f-91b6-28b2f2910b69
title: 'ITabletEventSink :: CursorInRange, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorInRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: eec2b4f309480ecaecd50de2120d701c916b6fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526305"
---
# <a name="itableteventsinkcursorinrange-method"></a><span data-ttu-id="1e67f-103">ITabletEventSink :: CursorInRange, méthode</span><span class="sxs-lookup"><span data-stu-id="1e67f-103">ITabletEventSink::CursorInRange method</span></span>

<span data-ttu-id="1e67f-104">Se produit lorsqu’un stylet est dans la plage de détection du digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="1e67f-104">Occurs when a stylus comes within the digitizer's range of detection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e67f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e67f-105">Syntax</span></span>


```C++
HRESULT CursorInRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="1e67f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e67f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e67f-107">*TCID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e67f-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e67f-108">Identificateur de l’objet tablette ayant détecté le stylet.</span><span class="sxs-lookup"><span data-stu-id="1e67f-108">The identifier of the tablet object that detected the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="1e67f-109">*confirmation*</span><span class="sxs-lookup"><span data-stu-id="1e67f-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="1e67f-110">Identificateur de l’objet stylet qui est compris dans la plage du digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="1e67f-110">The identifier of the stylus object that has come in range of the digitizer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e67f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e67f-111">Return value</span></span>

<span data-ttu-id="1e67f-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="1e67f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="1e67f-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1e67f-113">Return code</span></span>                                                                            | <span data-ttu-id="1e67f-114">Description</span><span class="sxs-lookup"><span data-stu-id="1e67f-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="1e67f-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1e67f-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="1e67f-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="1e67f-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="1e67f-117"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="1e67f-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="1e67f-118">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="1e67f-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1e67f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e67f-119">Requirements</span></span>



| <span data-ttu-id="1e67f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e67f-120">Requirement</span></span> | <span data-ttu-id="1e67f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e67f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e67f-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e67f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1e67f-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e67f-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1e67f-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e67f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1e67f-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e67f-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1e67f-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1e67f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="1e67f-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1e67f-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e67f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e67f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e67f-129">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="1e67f-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




