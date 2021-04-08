---
title: TfGuidAtom (msctf. h)
description: Le type de données TfGuidAtom identifie un GUID dans TSF. Un TfGuidAtom est obtenu en appelant ITfCategoryMgr RegisterGUID.
ms.assetid: 91696612-1829-4052-81d1-eddc23278d35
keywords:
- TfGuidAtom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c05d3c9a3bc7d725bf2df38069d7bc6112dad08b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102828"
---
# <a name="tfguidatom"></a><span data-ttu-id="ecb50-105">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="ecb50-105">TfGuidAtom</span></span>

<span data-ttu-id="ecb50-106">Le type de données **TfGuidAtom** identifie un **GUID** dans TSF.</span><span class="sxs-lookup"><span data-stu-id="ecb50-106">The **TfGuidAtom** data type identifies a **GUID** within TSF.</span></span> <span data-ttu-id="ecb50-107">Un **TfGuidAtom** est obtenu en appelant [**ITfCategoryMgr :: RegisterGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span><span class="sxs-lookup"><span data-stu-id="ecb50-107">A **TfGuidAtom** is obtained by calling [**ITfCategoryMgr::RegisterGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span></span>


```C++
typedef DWORD TfGuidAtom;
```



## <a name="remarks"></a><span data-ttu-id="ecb50-108">Notes</span><span class="sxs-lookup"><span data-stu-id="ecb50-108">Remarks</span></span>

<span data-ttu-id="ecb50-109">Une valeur **TfGuidAtom** est valide uniquement dans le processus à partir duquel **ITfCategoryMgr :: RegisterGUID** est appelé.</span><span class="sxs-lookup"><span data-stu-id="ecb50-109">A **TfGuidAtom** value is only valid within the process that **ITfCategoryMgr::RegisterGUID** is called from.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecb50-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecb50-110">Requirements</span></span>



| <span data-ttu-id="ecb50-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecb50-111">Requirement</span></span> | <span data-ttu-id="ecb50-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecb50-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb50-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecb50-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ecb50-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ecb50-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ecb50-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecb50-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ecb50-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ecb50-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ecb50-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="ecb50-117">Redistributable</span></span><br/>          | <span data-ttu-id="ecb50-118">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="ecb50-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="ecb50-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="ecb50-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecb50-120"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecb50-120"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="ecb50-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="ecb50-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ecb50-122"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ecb50-122"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecb50-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecb50-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecb50-124">**ITfCategoryMgr :: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="ecb50-124">**ITfCategoryMgr::GetGUID**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[<span data-ttu-id="ecb50-125">**ITfCategoryMgr::IsEqualTfGuidAtom**</span><span class="sxs-lookup"><span data-stu-id="ecb50-125">**ITfCategoryMgr::IsEqualTfGuidAtom**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-isequaltfguidatom)
</dt> <dt>

[<span data-ttu-id="ecb50-126">**ITfCategoryMgr::RegisterGUID**</span><span class="sxs-lookup"><span data-stu-id="ecb50-126">**ITfCategoryMgr::RegisterGUID**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> </dl>

 

 





