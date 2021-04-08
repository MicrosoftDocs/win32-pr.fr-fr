---
title: Gestionnaire de documents
description: Gestionnaire de documents
ms.assetid: e30087b6-524a-481e-845d-0348bac3830a
keywords:
- Text Services Framework (TSF), gestionnaire de documents
- TSF (Text Services Framework), gestionnaire de documents
- services de texte, gestionnaire de documents
- Applications compatibles TSF, gestionnaire de documents
- Gestionnaire de documents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2182782218ad6a8aa0a70f296f639560307249
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672142"
---
# <a name="document-manager"></a><span data-ttu-id="d82ab-108">Gestionnaire de documents</span><span class="sxs-lookup"><span data-stu-id="d82ab-108">Document Manager</span></span>

## <a name="applications"></a><span data-ttu-id="d82ab-109">Applications</span><span class="sxs-lookup"><span data-stu-id="d82ab-109">Applications</span></span>

<span data-ttu-id="d82ab-110">Pour créer un objet du gestionnaire de documents, une application appelle [ITfThreadMgr :: CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr).</span><span class="sxs-lookup"><span data-stu-id="d82ab-110">To create a document manager object an application calls [ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr).</span></span> <span data-ttu-id="d82ab-111">L’application crée un objet de gestionnaire de documents distinct pour chaque document individuel géré par l’application.</span><span class="sxs-lookup"><span data-stu-id="d82ab-111">The application creates a separate document manager object for each individual document that the application maintains.</span></span> <span data-ttu-id="d82ab-112">L’application utilise le gestionnaire de documents pour créer des contextes de modification, ajouter un contexte à la pile de contexte et supprimer un contexte de la pile de contexte.</span><span class="sxs-lookup"><span data-stu-id="d82ab-112">The application uses the document manager to create edit contexts, add a context to the context stack and remove a context from the context stack.</span></span>

## <a name="text-services"></a><span data-ttu-id="d82ab-113">Services de texte</span><span class="sxs-lookup"><span data-stu-id="d82ab-113">Text Services</span></span>

<span data-ttu-id="d82ab-114">Un service de texte ne crée jamais un objet de gestionnaire de documents.</span><span class="sxs-lookup"><span data-stu-id="d82ab-114">A text service never creates a document manager object.</span></span> <span data-ttu-id="d82ab-115">Au lieu de cela, le service de texte obtient l’objet actuellement actif du gestionnaire de documents en appelant [ITfThreadMgr :: getFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus).</span><span class="sxs-lookup"><span data-stu-id="d82ab-115">Instead, the text service obtains the currently active document manager object by calling [ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus).</span></span> <span data-ttu-id="d82ab-116">Un service de texte utilise le gestionnaire de documents pour obtenir le contexte en haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="d82ab-116">A text service uses the document manager to obtain the context at the top of the stack.</span></span>

<span data-ttu-id="d82ab-117">Un service de texte peut également utiliser le gestionnaire de documents pour créer son propre contexte et l’ajouter et le supprimer de la pile de contexte.</span><span class="sxs-lookup"><span data-stu-id="d82ab-117">A text service can also use the document manager to create its own context and add and remove it from the context stack.</span></span> <span data-ttu-id="d82ab-118">Cela s’effectue normalement lorsque le service de texte doit afficher une interface utilisateur modale, par exemple lorsqu’une liste de mots est affichée pour permettre à l’utilisateur de sélectionner un mot.</span><span class="sxs-lookup"><span data-stu-id="d82ab-118">This is normally done when the text service must display some modal user interface, such as when a list of words is displayed to enable the user to select a word.</span></span> <span data-ttu-id="d82ab-119">Lorsque la liste est affichée, le service de texte place son propre contexte sur la pile.</span><span class="sxs-lookup"><span data-stu-id="d82ab-119">When the list is displayed, the text service places its own context on the stack.</span></span> <span data-ttu-id="d82ab-120">Quand la liste de mots est fermée, le service de texte supprime son contexte de la pile.</span><span class="sxs-lookup"><span data-stu-id="d82ab-120">When the word list is dismissed, the text service removes its context from the stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d82ab-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d82ab-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d82ab-122">ITfDocumentMgr</span><span class="sxs-lookup"><span data-stu-id="d82ab-122">ITfDocumentMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[<span data-ttu-id="d82ab-123">ITfThreadMgr :: CreateDocumentMgr</span><span class="sxs-lookup"><span data-stu-id="d82ab-123">ITfThreadMgr::CreateDocumentMgr</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)
</dt> <dt>

[<span data-ttu-id="d82ab-124">ITfThreadMgr :: GetFocus</span><span class="sxs-lookup"><span data-stu-id="d82ab-124">ITfThreadMgr::GetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> </dl>

 

 




