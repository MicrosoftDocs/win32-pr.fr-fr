---
title: TfEditCookie (msctf. h)
description: Le type de données TfEditCookie identifie une session d’édition qui a un verrou.
ms.assetid: 1de17286-5d56-4302-a144-5fe6ca7d5557
keywords:
- TfEditCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69281bc38b5df6c22dd5306877aecdb8025af84a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032312"
---
# <a name="tfeditcookie"></a><span data-ttu-id="600b5-104">TfEditCookie</span><span class="sxs-lookup"><span data-stu-id="600b5-104">TfEditCookie</span></span>

<span data-ttu-id="600b5-105">Le type de données **TfEditCookie** identifie une session d’édition qui a un verrou.</span><span class="sxs-lookup"><span data-stu-id="600b5-105">The **TfEditCookie** data type identifies an edit session that has a lock.</span></span>


```C++
typedef DWORD TfEditCookie;
```



## <a name="remarks"></a><span data-ttu-id="600b5-106">Notes</span><span class="sxs-lookup"><span data-stu-id="600b5-106">Remarks</span></span>

<span data-ttu-id="600b5-107">Le type de données **TfEditCookie** est fourni par le gestionnaire TSF et est utilisé par un client (application ou service de texte) pour identifier une session d’édition avec un verrou en lecture seule ou en lecture/écriture dans différentes méthodes.</span><span class="sxs-lookup"><span data-stu-id="600b5-107">The **TfEditCookie** data type is supplied by the TSF manager and is used by a client (application or text service) to identify an edit session with a read-only or read/write lock in various methods.</span></span>

<span data-ttu-id="600b5-108">Une valeur **TfEditCookie** est obtenue de l’une des manières suivantes.</span><span class="sxs-lookup"><span data-stu-id="600b5-108">A **TfEditCookie** value is obtained in one of the following ways.</span></span>

-   <span data-ttu-id="600b5-109">Le client appelle [ITfDocumentMgr :: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span><span class="sxs-lookup"><span data-stu-id="600b5-109">The client calls [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span></span>
-   <span data-ttu-id="600b5-110">Le gestionnaire TSF appelle la méthode client [ITfEditSession ::D oeditsession](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) .</span><span class="sxs-lookup"><span data-stu-id="600b5-110">The TSF manager calls the client [ITfEditSession::DoEditSession](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) method.</span></span>
-   <span data-ttu-id="600b5-111">Le gestionnaire TSF appelle la méthode cliente [ITfCompositionSink :: OnCompositionTerminated](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) .</span><span class="sxs-lookup"><span data-stu-id="600b5-111">The TSF manager calls the client [ITfCompositionSink::OnCompositionTerminated](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) method.</span></span>
-   <span data-ttu-id="600b5-112">Le gestionnaire TSF appelle la méthode cliente [ITfCleanupContextSink :: OnCleanupContext](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) .</span><span class="sxs-lookup"><span data-stu-id="600b5-112">The TSF manager calls the client [ITfCleanupContextSink::OnCleanupContext](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) method.</span></span>
-   <span data-ttu-id="600b5-113">Le gestionnaire TSF appelle la méthode cliente [ITfTextEditSink :: OnEndEdit](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) .</span><span class="sxs-lookup"><span data-stu-id="600b5-113">The TSF manager calls the client [ITfTextEditSink::OnEndEdit](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="600b5-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="600b5-114">Requirements</span></span>



| <span data-ttu-id="600b5-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="600b5-115">Requirement</span></span> | <span data-ttu-id="600b5-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="600b5-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="600b5-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="600b5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="600b5-118">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="600b5-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                    |
| <span data-ttu-id="600b5-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="600b5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="600b5-120">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="600b5-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="600b5-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="600b5-121">Redistributable</span></span><br/>          | <span data-ttu-id="600b5-122">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="600b5-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="600b5-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="600b5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="600b5-124"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="600b5-124"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="600b5-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="600b5-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="600b5-126"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="600b5-126"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="600b5-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="600b5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="600b5-128">**ITfCleanupContextSink::OnCleanupContext**</span><span class="sxs-lookup"><span data-stu-id="600b5-128">**ITfCleanupContextSink::OnCleanupContext**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext)
</dt> <dt>

[<span data-ttu-id="600b5-129">**ITfCompositionSink::OnCompositionTerminated**</span><span class="sxs-lookup"><span data-stu-id="600b5-129">**ITfCompositionSink::OnCompositionTerminated**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated)
</dt> <dt>

[<span data-ttu-id="600b5-130">**ITfDocumentMgr :: CreateContext**</span><span class="sxs-lookup"><span data-stu-id="600b5-130">**ITfDocumentMgr::CreateContext**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[<span data-ttu-id="600b5-131">**ITfEditSession ::D oEditSession**</span><span class="sxs-lookup"><span data-stu-id="600b5-131">**ITfEditSession::DoEditSession**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession)
</dt> <dt>

[<span data-ttu-id="600b5-132">**ITfTextEditSink::OnEndEdit**</span><span class="sxs-lookup"><span data-stu-id="600b5-132">**ITfTextEditSink::OnEndEdit**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit)
</dt> </dl>

 

 





