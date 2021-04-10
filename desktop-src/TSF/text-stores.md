---
title: Magasins de texte
description: Magasins de texte
ms.assetid: c827999a-0b74-4e5d-901e-4c2fa1d74929
keywords:
- Text Services Framework (TSF), magasins de texte
- TSF (Text Services Framework), magasins de texte
- Applications compatibles TSF, magasins de texte
- magasins de texte
- Text Services Framework (TSF), position caractère d’application (ACP)
- TSF (Text Services Framework), ACP (application Character position)
- Applications compatibles TSF, position de caractère d’application (ACP)
- Position du caractère d’application (ACP)
- ACP (position du caractère d’application)
- Text Services Framework (TSF), ancres
- TSF (Text Services Framework), ancres
- Applications compatibles TSF, ancres
- Points d’ancrage
- Text Services Framework (TSF), verrous de document
- TSF (Text Services Framework), verrous de document
- Applications compatibles TSF, verrous de document
- verrous de document
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1234f71fa799cf911ff7ede89915068f69417a00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031430"
---
# <a name="text-stores"></a>Magasins de texte

## <a name="application-character-position-acp"></a>Position du caractère d’application (ACP)

Un ACP est l’emplacement d’un ou de plusieurs caractères dans un flux de texte exprimé sous la forme du nombre de caractères à partir du début du flux de texte. Étant donné que le modèle ACP est de base zéro, le premier caractère d’un flux de texte a un ACP égal à zéro. Par exemple :


```C++
Text Stream  H | e | l | l | o |   | W | o | r | l | d
ACP          0   1   2   3   4   5   6   7   8   9   10
```



Un magasin de texte implémente un objet qui prend en charge l’interface [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) , ce qui permet d’exprimer le flux de texte dans un ACP. Les méthodes d’interface **ITextStoreACP** utilisent la plage ACP du flux de texte pour modifier le texte.

## <a name="anchor-based-applications"></a>Applications Anchor-Based

Le gestionnaire utilise les méthodes basées sur ACP en mode natif pour manipuler du texte. Toutefois, une approche basée sur l’ancre est disponible pour les clients [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md) qui prennent en charge les [ancres](ranges.md), où le gestionnaire utilise les méthodes [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) et [ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) pour encapsuler les méthodes [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) et [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) .

## <a name="document-access-control"></a>Access Control de documents

Le magasin de texte contrôle l’accès au flux de texte à l’aide de [verrous de document](document-locks.md). Pour lire ou modifier le magasin de texte, le gestionnaire doit d’abord installer un récepteur de notifications qui prend en charge l’interface [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) en appelant la méthode [ITextStoreACP :: AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) et en passant un pointeur vers un récepteur de notifications. Le récepteur de notifications permet au gestionnaire d’obtenir des verrous de document sur le magasin de texte et de recevoir des notifications lorsque le magasin de texte est modifié par un autre nom que le gestionnaire, tel que l’entrée d’utilisateur via l’application. Les récepteurs de notification sont décrits plus loin dans cette rubrique.

## <a name="how-to-initialize-the-text-store"></a>Comment initialiser le magasin de texte

Une application Initialise un magasin de texte en effectuant les étapes suivantes :

1.  Créez un objet de gestionnaire de threads basé sur l’interface [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) en appelant la fonction [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec un pointeur vers un objet de gestionnaire de threads. L’exemple de code suivant illustre l’implémentation d’un objet de gestionnaire de threads.
    ```C++
    hr = CoCreateInstance (CLSID_TF_ThreadMgr, NULL, CLSCTX_INPROC_SERVER, 
                            IID_ITfThreadMgr, (void**)&pThreadMgr);
    ```

    

2.  Activez l’objet de gestionnaire de threads en appelant la méthode [ITfThreadMgr :: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) . Cette méthode fournit un pointeur vers un [identificateur client](tfclientid.md) utilisé pour créer un objet de contexte. Le gestionnaire de thread est utilisé pour implémenter un objet du gestionnaire de documents.
3.  Créez un objet de gestionnaire de documents basé sur l’interface [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) en appelant la méthode [ITfThreadMgr :: CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) avec un pointeur vers l’objet du gestionnaire de documents. L’objet du gestionnaire de documents est utilisé pour implémenter un objet de contexte qui est le magasin de texte.
4.  Créez un objet de contexte à partir du gestionnaire de documents en appelant la méthode [ITfDocumentMgr :: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) avec le pointeur vers l’objet de magasin de texte et un pointeur vers l’identificateur de client à partir de l’activation du gestionnaire de thread. Voici un exemple de création d’un objet de contexte :
    ```C++
    hr = pDocumentMgr->CreateContext(m_ClientID, 0, (ITextStoreACP*)this, 
                                    &pContext, pEditCookie);
    ```

    

5.  Exécute un push de l’objet Context sur la pile avec la méthode [ITfDocumentMgr ::P par émission](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) . Voici un exemple de transmission de l’objet de contexte sur la pile :
    ```C++
    hr = pDocumentMgr->Push(pContext);
    ```

    

## <a name="how-to-modify-the-text-store"></a>Comment modifier le magasin de texte

La méthode **ITfDocumentMgr ::P par émission** appelle **ITextStoreACP :: AdviseSink** avec un pointeur vers l’interface du récepteur de notifications pour installer un nouveau récepteur de notifications ou modifier un récepteur de notifications existant. Le récepteur de notifications reçoit des notifications lorsque le magasin de texte est modifié par un autre nom que le gestionnaire, tel que l’entrée d’utilisateur dans l’application. Les applications doivent appeler la méthode [ITfThreadMgrEventSink :: OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) lorsque la méthode d’entrée obtient le focus. D’autres notifications au gestionnaire de thread sont fournies en appelant les méthodes d’interface **ITextStoreACPSink** appropriées.

Toutefois, les applications ne doivent pas appeler les méthodes de l’interface **ITextStoreACPSink** en réponse aux méthodes de l’interface **ITextStoreACP** . Les applications doivent uniquement appeler les méthodes d’interface **ITextStoreACPSink** lorsque le magasin de texte est modifié par un autre nom que le responsable.

Le contenu du magasin de texte peut être modifié à l’aide d’un état d’entrée temporaire appelé [composition](compositions.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ancres](ranges.md)
</dt> <dt>

[Position](compositions.md)
</dt> <dt>

[Verrous de document](document-locks.md)
</dt> <dt>

[ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)
</dt> <dt>

[ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)
</dt> <dt>

[ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink)
</dt> <dt>

[ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[ITfThreadMgrEventSink :: OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus)
</dt> <dt>

[TfClientId](tfclientid.md)
</dt> <dt>

[Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md)
</dt> </dl>

 

 