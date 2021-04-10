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
# <a name="about-windowless-rich-edit-controls"></a><span data-ttu-id="f0252-103">À propos des contrôles RichEdit sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="f0252-103">About Windowless Rich Edit Controls</span></span>

<span data-ttu-id="f0252-104">Un contrôle RichEdit sans fenêtre, également connu sous le nom d’objet de services de texte, est un objet qui fournit les fonctionnalités d’un [contrôle RichEdit](rich-edit-controls.md) sans fournir la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f0252-104">A windowless rich edit control, also known as a text services object, is an object that provides the functionality of a [rich edit control](rich-edit-controls.md) without providing the window.</span></span> <span data-ttu-id="f0252-105">Pour fournir les fonctionnalités d’une fenêtre, telles que la capacité à recevoir des messages et un contexte de périphérique dans lequel elle peut être dessinée, les contrôles d’édition enrichis sans fenêtre utilisent une paire d’interfaces : [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) et [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span><span class="sxs-lookup"><span data-stu-id="f0252-105">To provide the functionality of a window, such as the ability to receive messages and a device context into which it can draw, windowless rich edit controls use a pair of interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span></span>

<span data-ttu-id="f0252-106">Pour créer un contrôle RichEdit sans fenêtre, appelez la fonction [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) avec un pointeur vers votre implémentation de l’interface [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) .</span><span class="sxs-lookup"><span data-stu-id="f0252-106">To create a windowless rich edit control, call the [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) function with a pointer to your implementation of the [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface.</span></span> <span data-ttu-id="f0252-107">**CreateTextServices** retourne un pointeur [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) que vous pouvez interroger pour récupérer un pointeur vers l’implémentation [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) du contrôle sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f0252-107">**CreateTextServices** returns an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer that you can query to retrieve a pointer to the [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) implementation of the windowless control.</span></span>

<span data-ttu-id="f0252-108">Msftedit.dll exporte un identificateur d’interface (IID) appelé **IID \_ ITextServices** que vous pouvez utiliser pour interroger le pointeur [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) de l’interface [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) .</span><span class="sxs-lookup"><span data-stu-id="f0252-108">Msftedit.dll exports an interface identifier (IID) called **IID\_ITextServices** that you can use to query the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer for the [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) interface.</span></span> <span data-ttu-id="f0252-109">L’exemple suivant montre comment récupérer **IID \_ ITextServices** et l’utiliser pour obtenir l’interface **ITextServices** .</span><span class="sxs-lookup"><span data-stu-id="f0252-109">The following example shows how to retrieve **IID\_ITextServices** and use it to get the **ITextServices** interface.</span></span>


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



<span data-ttu-id="f0252-110">Msftedit.dll exporte également un identificateur d’interface (IID) appelé **IID \_ ITextHost** qui peut être utilisé de la même manière pour interroger l’interface [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) .</span><span class="sxs-lookup"><span data-stu-id="f0252-110">Msftedit.dll also exports an interface identifier (IID) called **IID\_ITextHost** that can be used in a similar manner to query for the [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface.</span></span>

<span data-ttu-id="f0252-111">L’interface [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) a des méthodes que le contrôle sans fenêtre appelle pour récupérer des informations sur votre fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f0252-111">The [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface has methods that the windowless control calls to retrieve information about your window.</span></span> <span data-ttu-id="f0252-112">Par exemple, l’objet services de texte appelle la méthode [**TxGetDC**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) pour récupérer un contexte de périphérique dans lequel il peut dessiner.</span><span class="sxs-lookup"><span data-stu-id="f0252-112">For example, the text services object calls the [**TxGetDC**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) method to retrieve a device context into which it can draw.</span></span> <span data-ttu-id="f0252-113">Le contrôle sans fenêtre appelle la méthode [**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) pour envoyer des notifications, telles que les messages de notification RichEdit, à l’hôte de texte.</span><span class="sxs-lookup"><span data-stu-id="f0252-113">The windowless control calls the [**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method to send notifications, such as the rich edit notification messages, to the text host.</span></span> <span data-ttu-id="f0252-114">L’objet services de texte appelle d’autres méthodes **ITextHost** pour demander à l’hôte de texte d’exécuter d’autres services liés à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f0252-114">The text services object calls other **ITextHost** methods to request the text host to perform other window-related services.</span></span> <span data-ttu-id="f0252-115">Par exemple, la méthode [**TxInvalidateRect**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) demande à l’hôte de texte d’ajouter un rectangle à la région de mise à jour de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f0252-115">For example, the [**TxInvalidateRect**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) method requests the text host to add a rectangle to the window's update region.</span></span>

<span data-ttu-id="f0252-116">Un contrôle Rich Edit standard comporte une procédure de fenêtre qui traite les messages système et les messages de votre application.</span><span class="sxs-lookup"><span data-stu-id="f0252-116">A standard rich edit control has a window procedure that processes system messages and messages from your application.</span></span> <span data-ttu-id="f0252-117">Vous pouvez utiliser le handle de fenêtre du contrôle pour envoyer des messages pour l’édition de texte et d’autres opérations.</span><span class="sxs-lookup"><span data-stu-id="f0252-117">You can use the control's window handle to send it messages for performing text editing and other operations.</span></span> <span data-ttu-id="f0252-118">Toutefois, un contrôle RichEdit sans fenêtre n’a pas de procédure de fenêtre pour recevoir et traiter des messages.</span><span class="sxs-lookup"><span data-stu-id="f0252-118">But a windowless rich edit control has no window procedure to receive and process messages.</span></span> <span data-ttu-id="f0252-119">Au lieu de cela, il fournit une interface [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) .</span><span class="sxs-lookup"><span data-stu-id="f0252-119">Instead, it provides an [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) interface.</span></span> <span data-ttu-id="f0252-120">Pour envoyer des messages à un contrôle Rich Edit sans fenêtre, appelez la méthode [**TxSendMessage**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) .</span><span class="sxs-lookup"><span data-stu-id="f0252-120">To send messages to a windowless rich edit control, call the [**TxSendMessage**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) method.</span></span> <span data-ttu-id="f0252-121">Vous pouvez utiliser cette méthode pour envoyer des messages de modification enrichis ou pour transmettre d’autres messages qui affectent le contrôle, tels que des messages système pour la souris ou l’entrée au clavier.</span><span class="sxs-lookup"><span data-stu-id="f0252-121">You can use this method to send any of the rich edit messages or to pass on other messages that affect the control, such as system messages for mouse or keyboard input.</span></span>

<span data-ttu-id="f0252-122">Vous pouvez également créer l’objet de services de texte dans le cadre d’un [objet agrégé par com](/windows/desktop/com/aggregation).</span><span class="sxs-lookup"><span data-stu-id="f0252-122">You can also create the text services object as part of a [COM-aggregated object](/windows/desktop/com/aggregation).</span></span> <span data-ttu-id="f0252-123">Cela facilite l’agrégation de l’objet de services de texte avec un objet COM (Component Object Model) sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f0252-123">This makes it easy to aggregate the text services object with a windowless Component Object Model (COM) object.</span></span>

 

 