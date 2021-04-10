---
title: Verrous de document
description: Verrous de document
ms.assetid: 3c623c44-b0d3-4b03-8de9-25f1062b5726
keywords:
- Text Services Framework (TSF), verrous de document
- TSF (Text Services Framework), verrous de document
- Applications compatibles TSF, verrous de document
- verrous de document
- Text Services Framework (TSF), position caractère d’application (ACP)
- TSF (Text Services Framework), ACP (application Character position)
- Applications compatibles TSF, position de caractère d’application (ACP)
- Position du caractère d’application (ACP)
- ACP (position du caractère d’application)
- Text Services Framework (TSF), ancres
- TSF (Text Services Framework), ancres
- Applications compatibles TSF, ancres
- Points d’ancrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438e22d7c77a45d798dfd6d5d7c43eaafa3e09c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196528"
---
# <a name="document-locks"></a>Verrous de document

## <a name="the-document-lock-protocol"></a>Protocole de verrouillage de document

Pour demander un verrou de document pour les applications basées sur ACP, le gestionnaire TSF appelle [ITextStoreACP :: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock). Pour les applications basées sur l’ancre, le gestionnaire TSF appelle [ITextStoreAnchor :: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock). L’application accorde le verrou de document en appelant [ITextStoreACPSink :: Onlockgranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (applications basées sur ACP) ou [ITextStoreAnchorSink :: Onlockgranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (applications basées sur une ancre) à l’intérieur de **RequestLock**. Le verrou est uniquement valide pendant l’appel **Onlockgranted** . Quand **Onlockgranted** retourne, le document est considéré comme déverrouillé.

## <a name="types-of-document-locks"></a>Types de verrous de document

Il existe deux types de verrous de document, en lecture seule et en lecture/écriture. Un verrou en lecture seule permet au responsable de lire le texte, mais il ne peut pas modifier ou insérer du texte. Un verrou en lecture/écriture permet au gestionnaire de lire, modifier et insérer du texte. Un verrou en lecture seule est demandé en spécifiant le saut de la variable TS \_ \_ lu dans *dwFlags*. Un verrou en lecture/écriture est demandé en spécifiant TS \_ LF \_ ReadWrite dans *dwFlags*.

## <a name="asynchronous-and-synchronous-requests"></a>Requêtes asynchrones et synchrones

Une demande de verrouillage peut être synchrone ou asynchrone. Le gestionnaire demande un verrou synchrone à l’aide de \_ l' \_ indicateur de synchronisation TS LF dans *dwFlags*. Si cet indicateur n’est pas présent, la demande est asynchrone.

## <a name="granting-the-lock"></a>Octroi du verrou

Quand **RequestLock** est appelé, l’application doit déterminer si le document est actuellement verrouillé. Si le document n’est pas verrouillé et qu’il n’existe aucune autre raison pour refuser le verrou, l’application doit définir *phrSession* sur S \_ OK et retourner s \_ OK.

Si le document est verrouillé et que la demande de verrou est synchrone, l’application doit définir *phrSession* sur TS \_ E \_ Synchronous et retourner \_ OK. Cela indique qu’une demande synchrone ne peut pas être accordée.

Si le document est verrouillé et que la demande de verrou est asynchrone, l’application doit mettre la demande en file d’attente, définir *phrSession* sur TS \_ S \_ Async et retourner s \_ OK. Lorsque le document devient disponible, l’application doit supprimer la demande de la file d’attente et appeler **Onlockgranted**. Cette mise en file d’attente des demandes de verrou est facultative. une application doit prendre en charge un scénario. Si le document a un verrou en lecture seule, la nouvelle demande de verrou est en lecture/écriture et la demande est asynchrone, l’application a appelé **Onlockgranted** , ce qui a provoqué un appel réentrant à **RequestLock**. L’application doit définir *phrSession* sur TS \_ s \_ Async et retourner s \_ OK. Une fois que l’appel à **Onlockgranted** a été retourné, l’application doit traiter la demande de mise à niveau en appelant à nouveau **Onlockgranted** avec TS \_ LF \_ ReadWrite.

## <a name="lock-enforcement"></a>Application de verrous

L’application doit s’assurer que le type de verrou approprié existe avant d’autoriser l’accès au document. Par exemple, l’application doit vérifier qu’un document a au moins un verrou en lecture seule avant d’autoriser [ITextStoreACP :: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) ou [ITextStoreAnchor :: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) à continuer. Si le verrou approprié n’existe pas, l’application doit retourner TF \_ E \_ NOLOCK.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Magasins de texte](text-stores.md)
</dt> <dt>

[ITextStoreACP :: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[ITextStoreACPSink :: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[ITextStoreACP :: GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext)
</dt> <dt>

[ITextStoreAnchor :: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[ITextStoreAnchorSink :: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> <dt>

[ITextStoreAnchor :: GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext)
</dt> </dl>

 

 




