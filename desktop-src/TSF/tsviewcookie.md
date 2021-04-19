---
title: TsViewCookie (Textstor. h)
description: Le type de données TsViewCookie identifie un affichage de contexte.
ms.assetid: e649b799-d0d6-4f2d-b9f1-28070eea9b16
keywords:
- TsViewCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb43f888f76410e83e89d037f39ea665ca548ec9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511546"
---
# <a name="tsviewcookie"></a><span data-ttu-id="3c171-104">TsViewCookie</span><span class="sxs-lookup"><span data-stu-id="3c171-104">TsViewCookie</span></span>

<span data-ttu-id="3c171-105">Le type de données **TsViewCookie** identifie un affichage de contexte.</span><span class="sxs-lookup"><span data-stu-id="3c171-105">The **TsViewCookie** data type identifies a context view.</span></span>


```C++
typedef DWORD TsViewCookie;
```



## <a name="remarks"></a><span data-ttu-id="3c171-106">Notes</span><span class="sxs-lookup"><span data-stu-id="3c171-106">Remarks</span></span>

<span data-ttu-id="3c171-107">Une application doit fournir une valeur **TsViewCookie** unique pour chaque vue qu’elle crée.</span><span class="sxs-lookup"><span data-stu-id="3c171-107">An application must supply a unique **TsViewCookie** value for each view it creates.</span></span>

<span data-ttu-id="3c171-108">Le gestionnaire TSF obtient cette valeur à partir de l’application en appelant [ITextStoreACP :: GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) ou [ITextStoreAnchor :: GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview).</span><span class="sxs-lookup"><span data-stu-id="3c171-108">The TSF manager obtains this value from the application by calling [ITextStoreACP::GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) or [ITextStoreAnchor::GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview).</span></span> <span data-ttu-id="3c171-109">Le gestionnaire TSF utilise cette valeur pour identifier la vue lors de l’appel de différentes méthodes [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) ou [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) .</span><span class="sxs-lookup"><span data-stu-id="3c171-109">The TSF manager uses this value to identify the view when calling various [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) or [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c171-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c171-110">Requirements</span></span>



| <span data-ttu-id="3c171-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c171-111">Requirement</span></span> | <span data-ttu-id="3c171-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c171-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c171-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c171-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3c171-114">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="3c171-114">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="3c171-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c171-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3c171-116">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="3c171-116">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="3c171-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="3c171-117">Redistributable</span></span><br/>          | <span data-ttu-id="3c171-118">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="3c171-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="3c171-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c171-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c171-120"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c171-120"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c171-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="3c171-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3c171-122"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3c171-122"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c171-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c171-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c171-124">**ITextStoreACP**</span><span class="sxs-lookup"><span data-stu-id="3c171-124">**ITextStoreACP**</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[<span data-ttu-id="3c171-125">**ITextStoreACP :: GetActiveView**</span><span class="sxs-lookup"><span data-stu-id="3c171-125">**ITextStoreACP::GetActiveView**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview)
</dt> <dt>

[<span data-ttu-id="3c171-126">**ITextStoreAnchor::GetActiveView**</span><span class="sxs-lookup"><span data-stu-id="3c171-126">**ITextStoreAnchor::GetActiveView**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview)
</dt> </dl>

 

 





