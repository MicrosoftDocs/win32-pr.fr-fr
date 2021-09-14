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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193535"
---
# <a name="edit-contexts"></a>Modifier les contextes

## <a name="applications"></a>Applications

Pour créer un contexte d’édition, une application appelle [ITfDocumentMgr :: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).

## <a name="text-services"></a>Services de texte

Un service de texte utilise souvent le contexte d’édition actuellement actif. Le contexte d’édition actuellement actif est le contexte d’édition en haut de la pile du gestionnaire de documents actifs. Pour obtenir le contexte actuellement actif, un service de texte appelle [ITfThreadMgr :: getFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) pour obtenir le gestionnaire de documents actifs, puis appelle [ITfDocumentMgr :: GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) pour obtenir le contexte d’édition en haut de la pile.

Dans certains cas, un service de texte requiert son propre contexte d’édition. Pour créer un contexte d’édition, un service de texte appelle **ITfDocumentMgr :: CreateContext**.

## <a name="edit-cookies"></a>Modifier les cookies

De nombreuses méthodes, telles que [ITfRange :: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext), requièrent un moyen d’identifier un contexte d’édition qui a un [verrou de document](document-locks.md)en lecture seule ou en lecture/écriture. Un verrou de document est obtenu via une négociation entre le gestionnaire TSF et l’application. Un service de texte ne peut pas effectuer cette négociation directement. Un service de texte peut uniquement obtenir un verrou en demandant une [session d’édition](edit-sessions.md) avec un contexte spécifique et un accès en lecture seule ou en lecture/écriture. Lorsque la session d’édition est accordée, le service de texte est fourni avec un *cookie de modification* qui identifie le contexte d’édition avec l’accès demandé. Ce cookie est ensuite transmis à la méthode pour identifier le contexte d’édition avec l’accès approprié.

**ITfDocumentMgr :: CreateContext** fournit également un cookie de modification au créateur de contexte. Ce cookie dispose d’un accès en lecture seule et il n’existe aucun moyen de modifier le niveau d’accès. En vérité, le gestionnaire TSF ne négocie pas de verrou de document pour ce cookie de modification. Le cookie est marqué en interne en lecture seule, mais le document n’est pas réellement verrouillé. Par exemple, si le créateur de contexte appelle [ITfContext :: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) avec le cookie Edit retourné par **ITfDocumentMgr :: CreateContext** , l’appel de [ITextStoreACP :: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) ou [ITextStoreAnchor :: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) est alors effectué. Avant d’obtenir la sélection, l’application détermine s’il existe un verrou de document. Étant donné qu’il n’existe aucun verrou, l’application échoue avec TS \_ E \_ NOLOCK. Autrement dit, si une application appelle une méthode avec ce cookie qui entraîne l’appel de l’une des méthodes de magasin de texte de l’application, elle doit gérer ce cas en interne, car l’application n’a pas de verrou de document.

Si le créateur de contexte requiert un cookie de modification avec accès en lecture/écriture, il doit établir sa propre session d’édition.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext)
</dt> <dt>

[ITfDocumentMgr :: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[ITfThreadMgr :: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> <dt>

[ITfDocumentMgr :: GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop)
</dt> <dt>

[ITfRange :: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[Verrous de document](document-locks.md)
</dt> <dt>

[Sessions de modification](edit-sessions.md)
</dt> <dt>

[ITfContext :: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITextStoreACP :: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[ITextStoreAnchor :: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> </dl>

 

 




