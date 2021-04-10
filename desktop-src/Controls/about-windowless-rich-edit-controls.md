---
title: À propos des contrôles RichEdit sans fenêtre
description: Un contrôle RichEdit sans fenêtre, également connu sous le nom d’objet de services de texte, est un objet qui fournit les fonctionnalités d’un contrôle RichEdit sans fournir la fenêtre.
ms.assetid: 880a704d-776a-49d3-be31-0328af408e3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1c8bc685dff5f8ddb041011089a84eb2e12008
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941385"
---
# <a name="about-windowless-rich-edit-controls"></a>À propos des contrôles RichEdit sans fenêtre

Un contrôle RichEdit sans fenêtre, également connu sous le nom d’objet de services de texte, est un objet qui fournit les fonctionnalités d’un [contrôle RichEdit](rich-edit-controls.md) sans fournir la fenêtre. Pour fournir les fonctionnalités d’une fenêtre, telles que la capacité à recevoir des messages et un contexte de périphérique dans lequel elle peut être dessinée, les contrôles d’édition enrichis sans fenêtre utilisent une paire d’interfaces : [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) et [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).

Pour créer un contrôle RichEdit sans fenêtre, appelez la fonction [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) avec un pointeur vers votre implémentation de l’interface [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) . **CreateTextServices** retourne un pointeur [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) que vous pouvez interroger pour récupérer un pointeur vers l’implémentation [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) du contrôle sans fenêtre.

Msftedit.dll exporte un identificateur d’interface (IID) appelé **IID \_ ITextServices** que vous pouvez utiliser pour interroger le pointeur [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) de l’interface [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) . L’exemple suivant montre comment récupérer **IID \_ ITextServices** et l’utiliser pour obtenir l’interface **ITextServices** .


```
    .
    .
    .
    HRESULT hr;
    IUnknown* pUnk = NULL;
    ITextServices* pTextServices =  NULL;
    
    // Create an instance of the application-defined object that implements the 
    // ITextHost interface.
    TextHost* pTextHost = new TextHost();
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from 
    // Msftedit.dll. The hmodRichEdit parameter is a handle to the 
    // Msftedit.dll module retrieved by a previous call to the 
    // GetModuleHandle function.
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, 
        "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    if (FAILED(hr))
        goto errorHandler;
     .
     . 
     .   
     
```



Msftedit.dll exporte également un identificateur d’interface (IID) appelé **IID \_ ITextHost** qui peut être utilisé de la même manière pour interroger l’interface [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) .

L’interface [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) a des méthodes que le contrôle sans fenêtre appelle pour récupérer des informations sur votre fenêtre. Par exemple, l’objet services de texte appelle la méthode [**TxGetDC**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) pour récupérer un contexte de périphérique dans lequel il peut dessiner. Le contrôle sans fenêtre appelle la méthode [**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) pour envoyer des notifications, telles que les messages de notification RichEdit, à l’hôte de texte. L’objet services de texte appelle d’autres méthodes **ITextHost** pour demander à l’hôte de texte d’exécuter d’autres services liés à la fenêtre. Par exemple, la méthode [**TxInvalidateRect**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) demande à l’hôte de texte d’ajouter un rectangle à la région de mise à jour de la fenêtre.

Un contrôle Rich Edit standard comporte une procédure de fenêtre qui traite les messages système et les messages de votre application. Vous pouvez utiliser le handle de fenêtre du contrôle pour envoyer des messages pour l’édition de texte et d’autres opérations. Toutefois, un contrôle RichEdit sans fenêtre n’a pas de procédure de fenêtre pour recevoir et traiter des messages. Au lieu de cela, il fournit une interface [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) . Pour envoyer des messages à un contrôle Rich Edit sans fenêtre, appelez la méthode [**TxSendMessage**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) . Vous pouvez utiliser cette méthode pour envoyer des messages de modification enrichis ou pour transmettre d’autres messages qui affectent le contrôle, tels que des messages système pour la souris ou l’entrée au clavier.

Vous pouvez également créer l’objet de services de texte dans le cadre d’un [objet agrégé par com](/windows/desktop/com/aggregation). Cela facilite l’agrégation de l’objet de services de texte avec un objet COM (Component Object Model) sans fenêtre.

 

 