---
title: Modifier les contextes
description: Modifier les contextes
ms.assetid: cf8bbe66-d2ad-49b3-9e7c-246e4ca50149
keywords:
- Text Services Framework (TSF), modifier les contextes
- TSF (Text Services Framework), modifier les contextes
- services de texte, modifier les contextes
- Applications compatibles TSF, modifier les contextes
- modifier les contextes
- Text Services Framework (TSF), modifier les cookies
- TSF (Text Services Framework), modifier les cookies
- services de texte, modifier les cookies
- Applications compatibles TSF, modifier les cookies
- modifier les cookies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020ca8713d66d9d14e387381fc21157db8bdedf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839826"
---
# <a name="edit-contexts"></a><span data-ttu-id="87973-113">Modifier les contextes</span><span class="sxs-lookup"><span data-stu-id="87973-113">Edit Contexts</span></span>

## <a name="applications"></a><span data-ttu-id="87973-114">Applications</span><span class="sxs-lookup"><span data-stu-id="87973-114">Applications</span></span>

<span data-ttu-id="87973-115">Pour créer un contexte d’édition, une application appelle [ITfDocumentMgr :: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span><span class="sxs-lookup"><span data-stu-id="87973-115">To create an edit context, an application calls [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span></span>

## <a name="text-services"></a><span data-ttu-id="87973-116">Services de texte</span><span class="sxs-lookup"><span data-stu-id="87973-116">Text Services</span></span>

<span data-ttu-id="87973-117">Un service de texte utilise souvent le contexte d’édition actuellement actif.</span><span class="sxs-lookup"><span data-stu-id="87973-117">A text service often uses the currently active edit context.</span></span> <span data-ttu-id="87973-118">Le contexte d’édition actuellement actif est le contexte d’édition en haut de la pile du gestionnaire de documents actifs.</span><span class="sxs-lookup"><span data-stu-id="87973-118">The currently active edit context is the edit context at the top of the stack of the active document manager.</span></span> <span data-ttu-id="87973-119">Pour obtenir le contexte actuellement actif, un service de texte appelle [ITfThreadMgr :: getFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) pour obtenir le gestionnaire de documents actifs, puis appelle [ITfDocumentMgr :: GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) pour obtenir le contexte d’édition en haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="87973-119">To obtain the currently active context, a text service calls [ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) to obtain the active document manager and then calls [ITfDocumentMgr::GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) to obtain the edit context at the top of the stack.</span></span>

<span data-ttu-id="87973-120">Dans certains cas, un service de texte requiert son propre contexte d’édition.</span><span class="sxs-lookup"><span data-stu-id="87973-120">In some cases, a text service requires its own edit context.</span></span> <span data-ttu-id="87973-121">Pour créer un contexte d’édition, un service de texte appelle **ITfDocumentMgr :: CreateContext**.</span><span class="sxs-lookup"><span data-stu-id="87973-121">To create an edit context, a text service calls **ITfDocumentMgr::CreateContext**.</span></span>

## <a name="edit-cookies"></a><span data-ttu-id="87973-122">Modifier les cookies</span><span class="sxs-lookup"><span data-stu-id="87973-122">Edit Cookies</span></span>

<span data-ttu-id="87973-123">De nombreuses méthodes, telles que [ITfRange :: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext), requièrent un moyen d’identifier un contexte d’édition qui a un [verrou de document](document-locks.md)en lecture seule ou en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="87973-123">Many methods, such as [ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext), require a way to identify an edit context that has a read-only or read/write [document lock](document-locks.md).</span></span> <span data-ttu-id="87973-124">Un verrou de document est obtenu via une négociation entre le gestionnaire TSF et l’application.</span><span class="sxs-lookup"><span data-stu-id="87973-124">A document lock is obtained through a negotiation between the TSF manager and the application.</span></span> <span data-ttu-id="87973-125">Un service de texte ne peut pas effectuer cette négociation directement.</span><span class="sxs-lookup"><span data-stu-id="87973-125">A text service cannot perform this negotiation directly.</span></span> <span data-ttu-id="87973-126">Un service de texte peut uniquement obtenir un verrou en demandant une [session d’édition](edit-sessions.md) avec un contexte spécifique et un accès en lecture seule ou en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="87973-126">A text service can only obtain a lock by requesting an [edit session](edit-sessions.md) with a specific context and read-only or read/write access.</span></span> <span data-ttu-id="87973-127">Lorsque la session d’édition est accordée, le service de texte est fourni avec un *cookie de modification* qui identifie le contexte d’édition avec l’accès demandé.</span><span class="sxs-lookup"><span data-stu-id="87973-127">When the edit session is granted, the text service is supplied with an *edit cookie* that identifies the edit context with the requested access.</span></span> <span data-ttu-id="87973-128">Ce cookie est ensuite transmis à la méthode pour identifier le contexte d’édition avec l’accès approprié.</span><span class="sxs-lookup"><span data-stu-id="87973-128">This cookie is then passed to the method to identify the edit context with the proper access.</span></span>

<span data-ttu-id="87973-129">**ITfDocumentMgr :: CreateContext** fournit également un cookie de modification au créateur de contexte.</span><span class="sxs-lookup"><span data-stu-id="87973-129">**ITfDocumentMgr::CreateContext** also supplies an edit cookie to the context creator.</span></span> <span data-ttu-id="87973-130">Ce cookie dispose d’un accès en lecture seule et il n’existe aucun moyen de modifier le niveau d’accès.</span><span class="sxs-lookup"><span data-stu-id="87973-130">This cookie has read-only access and there is no way to modify the access level.</span></span> <span data-ttu-id="87973-131">En vérité, le gestionnaire TSF ne négocie pas de verrou de document pour ce cookie de modification.</span><span class="sxs-lookup"><span data-stu-id="87973-131">In truth, the TSF manager does not negotiate a document lock for this edit cookie.</span></span> <span data-ttu-id="87973-132">Le cookie est marqué en interne en lecture seule, mais le document n’est pas réellement verrouillé.</span><span class="sxs-lookup"><span data-stu-id="87973-132">The cookie is internally marked read-only, but the document is not actually locked.</span></span> <span data-ttu-id="87973-133">Par exemple, si le créateur de contexte appelle [ITfContext :: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) avec le cookie Edit retourné par **ITfDocumentMgr :: CreateContext** , l’appel de [ITextStoreACP :: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) ou [ITextStoreAnchor :: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) est alors effectué.</span><span class="sxs-lookup"><span data-stu-id="87973-133">For example, if the context creator calls [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) with the edit cookie returned by **ITfDocumentMgr::CreateContext** , this results in the application's [ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) or [ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) being called.</span></span> <span data-ttu-id="87973-134">Avant d’obtenir la sélection, l’application détermine s’il existe un verrou de document.</span><span class="sxs-lookup"><span data-stu-id="87973-134">Before obtaining the selection, the application will determine if a document lock exists.</span></span> <span data-ttu-id="87973-135">Étant donné qu’il n’existe aucun verrou, l’application échoue avec TS \_ E \_ NOLOCK.</span><span class="sxs-lookup"><span data-stu-id="87973-135">Because no lock exists, the application will fail with TS\_E\_NOLOCK.</span></span> <span data-ttu-id="87973-136">Autrement dit, si une application appelle une méthode avec ce cookie qui entraîne l’appel de l’une des méthodes de magasin de texte de l’application, elle doit gérer ce cas en interne, car l’application n’a pas de verrou de document.</span><span class="sxs-lookup"><span data-stu-id="87973-136">That is, if an application calls a method with this cookie that results in one of the application's text store methods being called, it must handle this case internally because the application will not actually have a document lock.</span></span>

<span data-ttu-id="87973-137">Si le créateur de contexte requiert un cookie de modification avec accès en lecture/écriture, il doit établir sa propre session d’édition.</span><span class="sxs-lookup"><span data-stu-id="87973-137">If the context creator requires an edit cookie with read/write access, it must establish its own edit session.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87973-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="87973-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87973-139">ITfContext</span><span class="sxs-lookup"><span data-stu-id="87973-139">ITfContext</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcontext)
</dt> <dt>

[<span data-ttu-id="87973-140">ITfDocumentMgr :: CreateContext</span><span class="sxs-lookup"><span data-stu-id="87973-140">ITfDocumentMgr::CreateContext</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[<span data-ttu-id="87973-141">ITfThreadMgr :: GetFocus</span><span class="sxs-lookup"><span data-stu-id="87973-141">ITfThreadMgr::GetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> <dt>

[<span data-ttu-id="87973-142">ITfDocumentMgr :: GetTop</span><span class="sxs-lookup"><span data-stu-id="87973-142">ITfDocumentMgr::GetTop</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop)
</dt> <dt>

[<span data-ttu-id="87973-143">ITfRange :: SetText</span><span class="sxs-lookup"><span data-stu-id="87973-143">ITfRange::SetText</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[<span data-ttu-id="87973-144">Verrous de document</span><span class="sxs-lookup"><span data-stu-id="87973-144">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="87973-145">Sessions de modification</span><span class="sxs-lookup"><span data-stu-id="87973-145">Edit Sessions</span></span>](edit-sessions.md)
</dt> <dt>

[<span data-ttu-id="87973-146">ITfContext :: GetSelection</span><span class="sxs-lookup"><span data-stu-id="87973-146">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="87973-147">ITextStoreACP :: GetSelection</span><span class="sxs-lookup"><span data-stu-id="87973-147">ITextStoreACP::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[<span data-ttu-id="87973-148">ITextStoreAnchor :: GetSelection</span><span class="sxs-lookup"><span data-stu-id="87973-148">ITextStoreAnchor::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> </dl>

 

 




