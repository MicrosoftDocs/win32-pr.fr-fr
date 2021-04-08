---
title: TS_ATTRID (Textstor. h)
description: Le \_ type de données ATTRID TS est utilisé pour identifier un attribut de texte.
ms.assetid: 5e375609-3d3c-4c12-ae05-dcaa70779162
keywords:
- TS_ATTRID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ea3823a95c123fe9942f69a2a133fd94a8567a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739781"
---
# <a name="ts_attrid"></a><span data-ttu-id="50879-104">\_ATTRID TS</span><span class="sxs-lookup"><span data-stu-id="50879-104">TS\_ATTRID</span></span>

<span data-ttu-id="50879-105">Le type de données **\_ ATTRID TS** est utilisé pour identifier un attribut de texte.</span><span class="sxs-lookup"><span data-stu-id="50879-105">The **TS\_ATTRID** data type is used to identify a text attribute.</span></span>


```C++
typedef GUID TS_ATTRID;
```



## <a name="remarks"></a><span data-ttu-id="50879-106">Notes</span><span class="sxs-lookup"><span data-stu-id="50879-106">Remarks</span></span>

<span data-ttu-id="50879-107">La liste des GUID prédéfinis pour TS \_ ATTRID se trouve dans tsattrs. h.</span><span class="sxs-lookup"><span data-stu-id="50879-107">A list of predefined GUIDs for TS\_ATTRID is in tsattrs.h.</span></span>

<span data-ttu-id="50879-108">Les GUID TSATTRID \_ Text \_ VERTICALWRITING et TSATTRID \_ Text \_ orientation sont utiles pour que les applications correspondent au texte d’entrée à corriger.</span><span class="sxs-lookup"><span data-stu-id="50879-108">The GUIDs TSATTRID\_Text\_VerticalWriting and TSATTRID\_Text\_Orientation are useful for applications to match input text that is to be corrected.</span></span> <span data-ttu-id="50879-109">Des GUID définis par l’utilisateur supplémentaires peuvent être créés.</span><span class="sxs-lookup"><span data-stu-id="50879-109">Additional user-defined GUIDs can be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="50879-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50879-110">Requirements</span></span>



| <span data-ttu-id="50879-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50879-111">Requirement</span></span> | <span data-ttu-id="50879-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="50879-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50879-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50879-113">Minimum supported client</span></span><br/> | <span data-ttu-id="50879-114">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="50879-114">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="50879-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50879-115">Minimum supported server</span></span><br/> | <span data-ttu-id="50879-116">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="50879-116">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="50879-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="50879-117">Redistributable</span></span><br/>          | <span data-ttu-id="50879-118">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="50879-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="50879-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="50879-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="50879-120"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="50879-120"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="50879-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="50879-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50879-122"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50879-122"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50879-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50879-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50879-124">**ITextStoreACP :: FindNextAttrTransition**</span><span class="sxs-lookup"><span data-stu-id="50879-124">**ITextStoreACP::FindNextAttrTransition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="50879-125">**ITextStoreACP :: RequestAttrsAtPosition**</span><span class="sxs-lookup"><span data-stu-id="50879-125">**ITextStoreACP::RequestAttrsAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrsatposition)
</dt> <dt>

[<span data-ttu-id="50879-126">**ITextStoreACP :: RequestAttrsTransitioningAtPosition**</span><span class="sxs-lookup"><span data-stu-id="50879-126">**ITextStoreACP::RequestAttrsTransitioningAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="50879-127">**ITextStoreACP :: RequestSupportedAttrs**</span><span class="sxs-lookup"><span data-stu-id="50879-127">**ITextStoreACP::RequestSupportedAttrs**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestsupportedattrs)
</dt> <dt>

[<span data-ttu-id="50879-128">**ITextStoreACPSink :: OnAttrsChange**</span><span class="sxs-lookup"><span data-stu-id="50879-128">**ITextStoreACPSink::OnAttrsChange**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onattrschange)
</dt> <dt>

[<span data-ttu-id="50879-129">**ITextStoreAnchor::FindNextAttrTransition**</span><span class="sxs-lookup"><span data-stu-id="50879-129">**ITextStoreAnchor::FindNextAttrTransition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="50879-130">**ITextStoreAnchor::RequestAttrsAtPosition**</span><span class="sxs-lookup"><span data-stu-id="50879-130">**ITextStoreAnchor::RequestAttrsAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrsatposition)
</dt> <dt>

[<span data-ttu-id="50879-131">**ITextStoreAnchor::RequestAttrsTransitioningAtPosition**</span><span class="sxs-lookup"><span data-stu-id="50879-131">**ITextStoreAnchor::RequestAttrsTransitioningAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="50879-132">**ITextStoreAnchor::RequestSupportedAttrs**</span><span class="sxs-lookup"><span data-stu-id="50879-132">**ITextStoreAnchor::RequestSupportedAttrs**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestsupportedattrs)
</dt> <dt>

[<span data-ttu-id="50879-133">**ITextStoreAnchorSink::OnAttrsChange**</span><span class="sxs-lookup"><span data-stu-id="50879-133">**ITextStoreAnchorSink::OnAttrsChange**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onattrschange)
</dt> <dt>

[<span data-ttu-id="50879-134">**\_ATTRVAL TS**</span><span class="sxs-lookup"><span data-stu-id="50879-134">**TS\_ATTRVAL**</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> </dl>

 

 





