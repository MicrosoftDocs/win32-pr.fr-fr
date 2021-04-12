---
title: Utilisation de échange dynamique de données
description: Cette rubrique fournit des exemples de code relatifs à l’échange dynamique de données.
ms.assetid: 6d94403b-64b4-4763-868a-3b94431dab79
keywords:
- Échange dynamique de données (DDE), conversations
- DDE (échange dynamique de données), conversations
- échange de données, échange dynamique de données (DDE)
- Échange dynamique de données (DDE), exemples
- DDE (échange dynamique de données), exemples
- Échange dynamique de données (DDE), commandes dans les applications serveur
- DDE (échange dynamique de données), commandes dans les applications serveur
- Échange dynamique de données (DDE), liaisons de données
- DDE (échange dynamique de données), liaisons de données
- Échange dynamique de données (DDE), éléments
- DDE (échange dynamique de données), éléments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe20c4dedc38303fe9bcb9c4b0fae42d03ee536
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315462"
---
# <a name="using-dynamic-data-exchange"></a><span data-ttu-id="27a84-114">Utilisation de échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="27a84-114">Using Dynamic Data Exchange</span></span>

<span data-ttu-id="27a84-115">Cette section contient des exemples de code sur les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="27a84-115">This section has code samples on the following tasks:</span></span>

-   [<span data-ttu-id="27a84-116">Initiation d’une conversation</span><span class="sxs-lookup"><span data-stu-id="27a84-116">Initiating a Conversation</span></span>](#initiating-a-conversation)
-   [<span data-ttu-id="27a84-117">Transfert d’un seul élément</span><span class="sxs-lookup"><span data-stu-id="27a84-117">Transferring a Single Item</span></span>](#transferring-a-single-item)
    -   [<span data-ttu-id="27a84-118">Récupération d’un élément à partir du serveur</span><span class="sxs-lookup"><span data-stu-id="27a84-118">Retrieving an Item from the Server</span></span>](#retrieving-an-item-from-the-server)
    -   [<span data-ttu-id="27a84-119">Envoi d’un élément au serveur</span><span class="sxs-lookup"><span data-stu-id="27a84-119">Submitting an Item to the Server</span></span>](#submitting-an-item-to-the-server)
-   [<span data-ttu-id="27a84-120">Établissement d’une liaison de données permanente</span><span class="sxs-lookup"><span data-stu-id="27a84-120">Establishing a Permanent Data Link</span></span>](#establishing-a-permanent-data-link)
    -   [<span data-ttu-id="27a84-121">Lancement d’une liaison de données</span><span class="sxs-lookup"><span data-stu-id="27a84-121">Initiating a Data Link</span></span>](#initiating-a-data-link)
    -   [<span data-ttu-id="27a84-122">Lancement d’une liaison de données avec la commande Coller le lien</span><span class="sxs-lookup"><span data-stu-id="27a84-122">Initiating a Data Link with the Paste Link Command</span></span>](#initiating-a-data-link-with-the-paste-link-command)
    -   [<span data-ttu-id="27a84-123">Notification au client que les données ont été modifiées</span><span class="sxs-lookup"><span data-stu-id="27a84-123">Notifying the Client that Data Has Changed</span></span>](#notifying-the-client-that-data-has-changed)
    -   [<span data-ttu-id="27a84-124">Arrêt d’une liaison de données</span><span class="sxs-lookup"><span data-stu-id="27a84-124">Terminating a Data Link</span></span>](#terminating-a-data-link)
-   [<span data-ttu-id="27a84-125">Exécution de commandes dans une application serveur</span><span class="sxs-lookup"><span data-stu-id="27a84-125">Carrying Out Commands in a Server Application</span></span>](#carrying-out-commands-in-a-server-application)
-   [<span data-ttu-id="27a84-126">Arrêt d’une conversation</span><span class="sxs-lookup"><span data-stu-id="27a84-126">Terminating a Conversation</span></span>](#terminating-a-conversation)

## <a name="initiating-a-conversation"></a><span data-ttu-id="27a84-127">Initiation d’une conversation</span><span class="sxs-lookup"><span data-stu-id="27a84-127">Initiating a Conversation</span></span>

<span data-ttu-id="27a84-128">Pour initier une conversation d’échange dynamique de données (DDE), le client envoie un message de [**\_ \_ lancement DDE**](wm-dde-initiate.md) .</span><span class="sxs-lookup"><span data-stu-id="27a84-128">To initiate a Dynamic Data Exchange (DDE) conversation, the client sends a [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message.</span></span> <span data-ttu-id="27a84-129">En règle générale, le client diffuse ce message en appelant [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), avec-1 comme premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="27a84-129">Usually, the client broadcasts this message by calling [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), with –1 as the first parameter.</span></span> <span data-ttu-id="27a84-130">Si l’application possède déjà le handle de fenêtre pour l’application serveur, elle peut envoyer le message directement à cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="27a84-130">If the application already has the window handle to the server application, it can send the message directly to that window.</span></span> <span data-ttu-id="27a84-131">Le client prépare les atomes pour le nom de l’application et le nom de la rubrique en appelant [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma).</span><span class="sxs-lookup"><span data-stu-id="27a84-131">The client prepares atoms for the application name and topic name by calling [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma).</span></span> <span data-ttu-id="27a84-132">Le client peut demander des conversations avec toute application serveur potentielle et pour toute rubrique potentielle en fournissant des atomes **null** (caractère générique) pour l’application et la rubrique.</span><span class="sxs-lookup"><span data-stu-id="27a84-132">The client can request conversations with any potential server application and for any potential topic by supplying **NULL** (wildcard) atoms for the application and topic.</span></span>

<span data-ttu-id="27a84-133">L’exemple suivant illustre la façon dont le client initie une conversation, où l’application et la rubrique sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="27a84-133">The following example illustrates how the client initiates a conversation, where both the application and topic are specified.</span></span>


```
    static BOOL fInInitiate = FALSE; 
    char *szApplication; 
    char *szTopic; 
    atomApplication = *szApplication == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szApplication); 
    atomTopic = *szTopic == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szTopic); 
 
    fInInitiate = TRUE; 
    SendMessage((HWND) HWND_BROADCAST, // broadcasts message 
        WM_DDE_INITIATE,               // initiates conversation 
        (WPARAM) hwndClientDDE,        // handle to client DDE window 
        MAKELONG(atomApplication,      // application-name atom 
            atomTopic));               // topic-name atom 
    fInInitiate = FALSE; 
    if (atomApplication != NULL) 
        GlobalDeleteAtom(atomApplication); 
    if (atomTopic != NULL) 
        GlobalDeleteAtom(atomTopic);
```



> [!Note]  
> <span data-ttu-id="27a84-134">Si votre application utilise des atomes **null** , vous n’avez pas besoin d’utiliser les fonctions [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) et [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) .</span><span class="sxs-lookup"><span data-stu-id="27a84-134">If your application uses **NULL** atoms, you need not use the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) and [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) functions.</span></span> <span data-ttu-id="27a84-135">Dans cet exemple, l’application cliente crée deux atomes globaux contenant le nom du serveur et le nom de la rubrique, respectivement.</span><span class="sxs-lookup"><span data-stu-id="27a84-135">In this example, the client application creates two global atoms containing the name of the server and the name of the topic, respectively.</span></span>

 

<span data-ttu-id="27a84-136">L’application cliente envoie un message [**WM de \_ \_ lancement DDE**](wm-dde-initiate.md) avec ces deux atomes dans le paramètre *lParam* du message.</span><span class="sxs-lookup"><span data-stu-id="27a84-136">The client application sends a [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message with these two atoms in the *lParam* parameter of the message.</span></span> <span data-ttu-id="27a84-137">Dans l’appel à la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , le handle de fenêtre spécial – 1 indique au système d’envoyer ce message à toutes les autres applications actives.</span><span class="sxs-lookup"><span data-stu-id="27a84-137">In the call to the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function, the special window handle –1 directs the system to send this message to all other active applications.</span></span> <span data-ttu-id="27a84-138">**SendMessage** ne retourne pas à l’application cliente tant que toutes les applications qui reçoivent le message n’ont pas retourné le contrôle au système.</span><span class="sxs-lookup"><span data-stu-id="27a84-138">**SendMessage** does not return to the client application until all applications that receive the message have, in turn, returned control to the system.</span></span> <span data-ttu-id="27a84-139">Cela signifie que tous les messages d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE qui sont envoyés en réponse par les applications serveur sont assurés d’être traités par le client au moment où l’appel **SendMessage** est retourné.</span><span class="sxs-lookup"><span data-stu-id="27a84-139">This means that all [**WM\_DDE\_ACK**](wm-dde-ack.md) messages sent in reply by the server applications are guaranteed to have been processed by the client by the time the **SendMessage** call has returned.</span></span>

<span data-ttu-id="27a84-140">Une fois [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) retourné, l’application cliente supprime les atomes globaux.</span><span class="sxs-lookup"><span data-stu-id="27a84-140">After [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, the client application deletes the global atoms.</span></span>

<span data-ttu-id="27a84-141">Les applications serveur répondent selon la logique illustrée dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="27a84-141">Server applications respond according to the logic illustrated in the following diagram.</span></span>

![logique de réponse de l’application serveur](images/csdde-01.png)

<span data-ttu-id="27a84-143">Pour accuser réception d’une ou plusieurs rubriques, le serveur doit créer des atomes pour chaque conversation (nécessitant des atomes de nom d’application en double s’il existe plusieurs rubriques) et envoyer un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE pour chaque conversation, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="27a84-143">To acknowledge one or more topics, the server must create atoms for each conversation (requiring duplicate application-name atoms if there are multiple topics) and send a [**WM\_DDE\_ACK**](wm-dde-ack.md) message for each conversation, as illustrated in the following example.</span></span>


```
if ((atomApplication = GlobalAddAtom("Server")) != 0) 
{ 
    if ((atomTopic = GlobalAddAtom(szTopic)) != 0) 
    { 
        SendMessage(hwndClientDDE, 
            WM_DDE_ACK, 
            (WPARAM) hwndServerDDE, 
            MAKELONG(atomApplication, atomTopic)); 
        GlobalDeleteAtom(atomApplication); 
    } 
 
    GlobalDeleteAtom(atomTopic); 
} 
 
if ((atomApplication == 0) || (atomTopic == 0)) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="27a84-144">Lorsqu’un serveur répond avec un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE, l’application cliente doit enregistrer un descripteur dans la fenêtre du serveur.</span><span class="sxs-lookup"><span data-stu-id="27a84-144">When a server responds with a [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the client application should save a handle to the server window.</span></span> <span data-ttu-id="27a84-145">Le client recevant le descripteur en tant que paramètre *wParam* du message d’accusé de réception **\_ DDE \_ de WM** envoie ensuite tous les messages DDE suivants à la fenêtre du serveur que ce descripteur identifie.</span><span class="sxs-lookup"><span data-stu-id="27a84-145">The client receiving the handle as the *wParam* parameter of the **WM\_DDE\_ACK** message then sends all subsequent DDE messages to the server window this handle identifies.</span></span>

<span data-ttu-id="27a84-146">Si votre application cliente utilise un atome **null** pour le nom de l’application ou le nom de la rubrique, attendez-vous à ce que l’application reçoive des accusés de réception de plusieurs applications serveur.</span><span class="sxs-lookup"><span data-stu-id="27a84-146">If your client application uses a **NULL** atom for the application name or topic name, expect the application to receive acknowledgments from more than one server application.</span></span> <span data-ttu-id="27a84-147">Plusieurs accusés de réception peuvent également provenir de plusieurs instances d’un serveur DDE, même si votre application cliente n’utilise pas les atomes **null** .</span><span class="sxs-lookup"><span data-stu-id="27a84-147">Multiple acknowledgements can also come from multiple instances of a DDE server, even if your client application does not **NULL** use atoms.</span></span> <span data-ttu-id="27a84-148">Un serveur doit toujours utiliser une fenêtre unique pour chaque conversation.</span><span class="sxs-lookup"><span data-stu-id="27a84-148">A server should always use a unique window for each conversation.</span></span> <span data-ttu-id="27a84-149">La procédure de fenêtre de l’application cliente peut utiliser un descripteur de la fenêtre du serveur (fourni comme paramètre *lParam* de l' [**\_ \_ initialisation DDE WM**](wm-dde-initiate.md)) pour effectuer le suivi de plusieurs conversations.</span><span class="sxs-lookup"><span data-stu-id="27a84-149">The window procedure in the client application can use a handle to the server window (provided as the *lParam* parameter of [**WM\_DDE\_INITIATE**](wm-dde-initiate.md)) to track multiple conversations.</span></span> <span data-ttu-id="27a84-150">Cela permet à une seule fenêtre cliente de traiter plusieurs conversations sans avoir à arrêter et à se reconnecter avec une nouvelle fenêtre client pour chaque conversation.</span><span class="sxs-lookup"><span data-stu-id="27a84-150">This allows a single client window to process several conversations without needing to terminate and reconnect with a new client window for each conversation.</span></span>

## <a name="transferring-a-single-item"></a><span data-ttu-id="27a84-151">Transfert d’un seul élément</span><span class="sxs-lookup"><span data-stu-id="27a84-151">Transferring a Single Item</span></span>

<span data-ttu-id="27a84-152">Une fois qu’une conversation DDE a été établie, le client peut récupérer la valeur d’un élément de données à partir du serveur en émettant le message de [**\_ \_ requête**](wm-dde-request.md) de l’échange de données (DDE) WM ou envoyer une valeur d’élément de données au serveur en émettant le composant [**WM \_ DDE \_**](wm-dde-poke.md).</span><span class="sxs-lookup"><span data-stu-id="27a84-152">Once a DDE conversation has been established, the client can either retrieve the value of a data item from the server by issuing the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message, or submit a data-item value to the server by issuing [**WM\_DDE\_POKE**](wm-dde-poke.md).</span></span>

-   [<span data-ttu-id="27a84-153">Récupération d’un élément à partir du serveur</span><span class="sxs-lookup"><span data-stu-id="27a84-153">Retrieving an Item from the Server</span></span>](#retrieving-an-item-from-the-server)
-   [<span data-ttu-id="27a84-154">Envoi d’un élément au serveur</span><span class="sxs-lookup"><span data-stu-id="27a84-154">Submitting an Item to the Server</span></span>](#submitting-an-item-to-the-server)

### <a name="retrieving-an-item-from-the-server"></a><span data-ttu-id="27a84-155">Récupération d’un élément à partir du serveur</span><span class="sxs-lookup"><span data-stu-id="27a84-155">Retrieving an Item from the Server</span></span>

<span data-ttu-id="27a84-156">Pour récupérer un élément à partir du serveur, le client envoie un message [**de \_ \_ requête**](wm-dde-request.md) de l’échange de messages WM au serveur en spécifiant l’élément et le format à récupérer, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="27a84-156">To retrieve an item from the server, the client sends the server a [**WM\_DDE\_REQUEST**](wm-dde-request.md) message specifying the item and format to retrieve, as shown in the following example.</span></span>


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_REQUEST, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_REQUEST, CF_TEXT, atomItem))) 
    {
        GlobalDeleteAtom(atomItem); 
    }
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="27a84-157">Dans cet exemple, le client spécifie le format **de \_ texte clair** du presse-papiers comme format préféré pour l’élément de données demandé.</span><span class="sxs-lookup"><span data-stu-id="27a84-157">In this example, the client specifies the clipboard format **CF\_TEXT** as the preferred format for the requested data item.</span></span>

<span data-ttu-id="27a84-158">Le récepteur (serveur) du message [**de \_ \_ demande DDE WM**](wm-dde-request.md) doit en général supprimer l’élément Atom, mais si l’appel [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) échoue, le client doit supprimer l’atome.</span><span class="sxs-lookup"><span data-stu-id="27a84-158">The receiver (server) of the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message typically must delete the item atom, but if the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) call fails, the client must delete the atom.</span></span>

<span data-ttu-id="27a84-159">Si le serveur a accès à l’élément demandé et peut le rendre dans le format demandé, le serveur copie la valeur de l’élément en tant qu’objet mémoire partagée et envoie un message de données de l' [**\_ échange de \_ données (DDE**](wm-dde-data.md) ) au client, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="27a84-159">If the server has access to the requested item and can render it in the requested format, the server copies the item value as a shared memory object and sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message, as illustrated in the following example.</span></span>


```
// Allocate the size of the DDE data header, plus the data: a 
// string,<CR><LF><NULL>. The byte for the string's terminating 
// null character is counted by DDEDATA.Value[1].

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEDATA) + *pcch + 2)))  
{
    return; 
}
 
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData)))  
{
    GlobalFree(hData); 
    return; 
} 
 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpData->Value, *pcch +1, (LPCSTR) szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
} 
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItemName)) != 0) 
{ 
    lParam = PackDDElParam(WM_DDE_ACK, (UINT) hData, atomItem); 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            lParam)) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_ACK, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors.  
}
```



<span data-ttu-id="27a84-160">Dans cet exemple, l’application serveur alloue un objet mémoire pour contenir l’élément de données.</span><span class="sxs-lookup"><span data-stu-id="27a84-160">In this example, the server application allocates a memory object to contain the data item.</span></span> <span data-ttu-id="27a84-161">L’objet de données est initialisé comme une structure [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) .</span><span class="sxs-lookup"><span data-stu-id="27a84-161">The data object is initialized as a [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure.</span></span>

<span data-ttu-id="27a84-162">L’application serveur définit ensuite le membre **cfFormat** de la structure sur le \_ texte CF pour informer l’application cliente que les données sont au format texte.</span><span class="sxs-lookup"><span data-stu-id="27a84-162">The server application then sets the **cfFormat** member of the structure to CF\_TEXT to inform the client application that the data is in text format.</span></span> <span data-ttu-id="27a84-163">Le client répond en copiant la valeur des données demandées dans le membre **value** de la structure [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) .</span><span class="sxs-lookup"><span data-stu-id="27a84-163">The client responds by copying the value of the requested data into the **Value** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure.</span></span> <span data-ttu-id="27a84-164">Une fois que le serveur a rempli l’objet de données, le serveur déverrouille les données et crée un atome global contenant le nom de l’élément de données.</span><span class="sxs-lookup"><span data-stu-id="27a84-164">After the server has filled the data object, the server unlocks the data and creates a global atom containing the name of the data item.</span></span>

<span data-ttu-id="27a84-165">Enfin, le serveur émet le message de [**\_ \_ données DDE WM**](wm-dde-data.md) en appelant [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea).</span><span class="sxs-lookup"><span data-stu-id="27a84-165">Finally, the server issues the [**WM\_DDE\_DATA**](wm-dde-data.md) message by calling [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea).</span></span> <span data-ttu-id="27a84-166">Le descripteur de l’objet de données et l’Atom contenant le nom de l’élément sont empaquetés dans le paramètre *lParam* du message par la fonction [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) .</span><span class="sxs-lookup"><span data-stu-id="27a84-166">The handle to the data object and the atom containing the item name are packed into the *lParam* parameter of the message by the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function.</span></span>

<span data-ttu-id="27a84-167">Si [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) échoue, le serveur doit utiliser la fonction [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) pour libérer le paramètre condensé *lParam* .</span><span class="sxs-lookup"><span data-stu-id="27a84-167">If [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) fails, the server must use the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function to free the packed *lParam* parameter.</span></span> <span data-ttu-id="27a84-168">Le serveur doit également libérer le paramètre *lParam* condensé pour le message de [**\_ \_ requête DDE WM**](wm-dde-request.md) qu’il a reçu.</span><span class="sxs-lookup"><span data-stu-id="27a84-168">The server must also free the packed *lParam* parameter for the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message it received.</span></span>

<span data-ttu-id="27a84-169">Si le serveur ne peut pas répondre à la demande, il envoie un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE négatif négatif au client, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="27a84-169">If the server cannot satisfy the request, it sends a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message to the client, as shown in the following example.</span></span>


```
// Negative acknowledgment. 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 0, atomItem));
```



<span data-ttu-id="27a84-170">À la réception d’un message de [**\_ \_ données DDE WM**](wm-dde-data.md) , le client traite la valeur de l’élément de données comme il convient.</span><span class="sxs-lookup"><span data-stu-id="27a84-170">Upon receiving a [**WM\_DDE\_DATA**](wm-dde-data.md) message, the client processes the data-item value as appropriate.</span></span> <span data-ttu-id="27a84-171">Ensuite, si le membre **fAckReq** désigné dans le message **de \_ \_ données de DDE de WM** est 1, le client doit envoyer au serveur un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE positif, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="27a84-171">Then, if the **fAckReq** member pointed to in the **WM\_DDE\_DATA** message is 1, the client must send the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message, as shown in the following example.</span></span>


```
UnpackDDElParam(WM_DDE_DATA, lParam, (PUINT) &hData, 
    (PUINT) &atomItem); 
if (!(lpDDEData = (DDEDATA FAR*) GlobalLock(hData)) 
        || (lpDDEData->cfFormat != CF_TEXT)) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // Negative ACK. 
} 
 
// Copy data from lpDDEData here. 
 
if (lpDDEData->fAckReq) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0x8000, 
            atomItem)); // Positive ACK 
} 
 
bRelease = lpDDEData->fRelease; 
GlobalUnlock(hData); 
if (bRelease) 
    GlobalFree(hData);
```



<span data-ttu-id="27a84-172">Dans cet exemple, le client examine le format des données.</span><span class="sxs-lookup"><span data-stu-id="27a84-172">In this example, the client examines the format of the data.</span></span> <span data-ttu-id="27a84-173">Si le format n’est pas du **\_ texte CF** (ou si le client ne peut pas verrouiller la mémoire pour les données), le client envoie un message d’accusé de réception [**\_ DDE \_ de WM**](wm-dde-ack.md) négatif pour indiquer qu’il ne peut pas traiter les données.</span><span class="sxs-lookup"><span data-stu-id="27a84-173">If the format is not **CF\_TEXT** (or if the client cannot lock the memory for the data), the client sends a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message to indicate that it cannot process the data.</span></span> <span data-ttu-id="27a84-174">Si le client ne peut pas verrouiller un handle de données parce que le handle contient le membre **fAckReq** , le client ne doit pas envoyer de message d' **\_ \_ accusé** de réception DDE négatif négatif.</span><span class="sxs-lookup"><span data-stu-id="27a84-174">If the client cannot lock a data handle because the handle contains the **fAckReq** member, the client should not send a negative **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="27a84-175">Au lieu de cela, le client doit mettre fin à la conversation.</span><span class="sxs-lookup"><span data-stu-id="27a84-175">Instead, the client should terminate the conversation.</span></span>

<span data-ttu-id="27a84-176">Si un client envoie un accusé de réception négatif en réponse à un message de données de l' [**\_ échange de \_ données (DDE**](wm-dde-data.md) ), le serveur est responsable de la libération de la mémoire (mais pas du paramètre *lParam* ) référencée par le message de données de l' **échange de \_ \_ données (DDE) WM** associé à l’accusé de réception négatif.</span><span class="sxs-lookup"><span data-stu-id="27a84-176">If a client sends a negative acknowledgment in response to a [**WM\_DDE\_DATA**](wm-dde-data.md) message, the server is responsible for freeing the memory (but not the *lParam* parameter) referenced by the **WM\_DDE\_DATA** message associated with the negative acknowledgment.</span></span>

<span data-ttu-id="27a84-177">S’il peut traiter les données, le client examine le membre **fAckReq** de la structure [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) pour déterminer si le serveur a demandé qu’il soit informé que le client a reçu et traité correctement les données.</span><span class="sxs-lookup"><span data-stu-id="27a84-177">If it can process the data, the client examines the **fAckReq** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to determine whether the server requested that it be informed that the client received and processed the data successfully.</span></span> <span data-ttu-id="27a84-178">Si le serveur a demandé cette information, le client envoie un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE positif au serveur.</span><span class="sxs-lookup"><span data-stu-id="27a84-178">If the server did request this information, the client sends the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="27a84-179">Étant donné que le déverrouillage des données invalide le pointeur vers les données, le client enregistre la valeur du membre **fRelease** avant de déverrouiller l’objet de données.</span><span class="sxs-lookup"><span data-stu-id="27a84-179">Because unlocking data invalidates the pointer to the data, the client saves the value of the **fRelease** member before unlocking the data object.</span></span> <span data-ttu-id="27a84-180">Après avoir enregistré la valeur, le client l’examine pour déterminer si l’application serveur a demandé au client de libérer la mémoire qui contient les données. le client agit en conséquence.</span><span class="sxs-lookup"><span data-stu-id="27a84-180">After saving the value, the client then examines it to determine whether the server application requested the client to free the memory containing the data; the client acts accordingly.</span></span>

<span data-ttu-id="27a84-181">Lors de la réception d’un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE de WM négatif, le client peut demander à nouveau la même valeur d’élément, en spécifiant un autre format de presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="27a84-181">Upon receiving a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the client can ask for the same item value again, specifying a different clipboard format.</span></span> <span data-ttu-id="27a84-182">En règle générale, un client demande tout d’abord le format le plus complexe qu’il peut prendre en charge, puis pas à pas détaillé si nécessaire par le biais de formats progressivement plus simples jusqu’à ce qu’il trouve un serveur.</span><span class="sxs-lookup"><span data-stu-id="27a84-182">Typically, a client will first ask for the most complex format it can support, then step down if necessary through progressively simpler formats until it finds one the server can provide.</span></span>

<span data-ttu-id="27a84-183">Si le serveur prend en charge l’élément formats de la rubrique système, le client peut déterminer à quel moment le format du presse-papiers est pris en charge par le serveur, au lieu de les déterminer chaque fois que le client demande un élément.</span><span class="sxs-lookup"><span data-stu-id="27a84-183">If the server supports the Formats item of the system topic, the client can determine once what clipboard formats the server supports, instead of determining them each time the client requests an item.</span></span>

### <a name="submitting-an-item-to-the-server"></a><span data-ttu-id="27a84-184">Envoi d’un élément au serveur</span><span class="sxs-lookup"><span data-stu-id="27a84-184">Submitting an Item to the Server</span></span>

<span data-ttu-id="27a84-185">Le client peut envoyer une valeur d’élément au serveur à l’aide du message d’échange de messages de l' [**\_ échange \_**](wm-dde-poke.md) de messages WM.</span><span class="sxs-lookup"><span data-stu-id="27a84-185">The client may send an item value to the server by using the [**WM\_DDE\_POKE**](wm-dde-poke.md) message.</span></span> <span data-ttu-id="27a84-186">Le client restitue l’élément à envoyer et envoie le message de pagination **WM \_ DDE \_** , comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="27a84-186">The client renders the item to be sent and sends the **WM\_DDE\_POKE** message, as illustrated in the following example.</span></span>


```
size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hPokeData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEPOKE) + *pcch + 2))) 
{
    return; 
}
 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData))) 
{ 
    GlobalFree(hPokeData); 
    return; 
} 
 
lpPokeData->fRelease = TRUE; 
lpPokeData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpPokeData->Value, *pcch +1, (LPCSTR) szValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpPokeData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hPokeData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItem)) != 0) 
{ 
 
        if (!PostMessage(hwndServerDDE, 
                WM_DDE_POKE, 
                (WPARAM) hwndClientDDE, 
                PackDDElParam(WM_DDE_POKE, (UINT) hPokeData, 
                    atomItem))) 
        { 
            GlobalDeleteAtom(atomItem); 
            GlobalFree(hPokeData); 
        } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
} 
```



> [!Note]  
> <span data-ttu-id="27a84-187">L’envoi de données à l’aide d’un message Colors de l' [**\_ échange \_**](wm-dde-poke.md) de données par l’intermédiaire de WM revient essentiellement à les envoyer à l’aide de [**\_ \_ données DDE WM**](wm-dde-data.md), à la différence que **WM \_ DDE \_** est envoyé du client au serveur.</span><span class="sxs-lookup"><span data-stu-id="27a84-187">Sending data by using a [**WM\_DDE\_POKE**](wm-dde-poke.md) message is essentially the same as sending it by using [**WM\_DDE\_DATA**](wm-dde-data.md), except that **WM\_DDE\_POKE** is sent from the client to the server.</span></span>

 

<span data-ttu-id="27a84-188">Si le serveur est en mesure d’accepter la valeur de l’élément de données dans le format affiché par le client, le serveur traite la valeur de l’élément de manière appropriée et envoie au client un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE positif positif.</span><span class="sxs-lookup"><span data-stu-id="27a84-188">If the server is able to accept the data-item value in the format rendered by the client, the server processes the item value as appropriate and sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span> <span data-ttu-id="27a84-189">S’il ne parvient pas à traiter la valeur de l’élément, en raison de son format ou pour d’autres raisons, le serveur envoie au client un message d' **\_ \_ accusé** de réception DDE négatif négatif.</span><span class="sxs-lookup"><span data-stu-id="27a84-189">If it is unable to process the item value, because of its format or for other reasons, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>


```
UnpackDDElParam(WM_DDE_POKE, lParam, (PUINT) &hPokeData, 
    (PUINT) &atomItem); 
GlobalGetAtomName(atomItem, szItemName, ITEM_NAME_MAX_SIZE); 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData)) 
        || lpPokeData->cfFormat != CF_TEXT 
        || !IsItemSupportedByServer(szItemName)) 
{ 
    PostMessage(hwndClientDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndServerDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // negative ACK  
}
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
} 
hResult = StringCchCopy(szItemValue, *pcch +1, lpPokeData->Value); // copies value 
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
bRelease = lpPokeData->fRelease; 
GlobalUnlock(hPokeData); 
if (bRelease) 
{ 
    GlobalFree(hPokeData); 
} 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 
         0x8000, atomItem));    // positive ACK.
```



<span data-ttu-id="27a84-190">Dans cet exemple, le serveur appelle [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) pour récupérer le nom de l’élément envoyé par le client.</span><span class="sxs-lookup"><span data-stu-id="27a84-190">In this example, the server calls [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) to retrieve the name of the item the client sent.</span></span> <span data-ttu-id="27a84-191">Le serveur détermine ensuite s’il prend en charge l’élément et si l’élément est rendu dans le format approprié (autrement dit, le \_ texte CF).</span><span class="sxs-lookup"><span data-stu-id="27a84-191">The server then determines whether it supports the item and whether the item is rendered in the correct format (that is, CF\_TEXT).</span></span> <span data-ttu-id="27a84-192">Si l’élément n’est pas pris en charge et n’est pas rendu dans le format approprié, ou si le serveur ne peut pas verrouiller la mémoire pour les données, le serveur renvoie un accusé de réception négatif à l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="27a84-192">If the item is not supported and not rendered in the correct format, or if the server cannot lock the memory for the data, the server sends a negative acknowledgment back to the client application.</span></span> <span data-ttu-id="27a84-193">Notez que dans ce cas, l’envoi d’un accusé de réception négatif est correct, car les messages d’entourage [**\_ \_ DDE**](wm-dde-poke.md) sont toujours supposés avoir le membre **fAckReq** défini.</span><span class="sxs-lookup"><span data-stu-id="27a84-193">Note that in this case, sending a negative acknowledgment is correct because [**WM\_DDE\_POKE**](wm-dde-poke.md) messages are always assumed to have the **fAckReq** member set.</span></span> <span data-ttu-id="27a84-194">Le serveur doit ignorer le membre.</span><span class="sxs-lookup"><span data-stu-id="27a84-194">The server should ignore the member.</span></span>

<span data-ttu-id="27a84-195">Si un serveur envoie un accusé de réception négatif en réponse à un message [**WM \_ DDE \_**](wm-dde-poke.md) , le client est responsable de la libération de la mémoire (mais pas du paramètre *lParam* ) référencée par le message d’action de l' **\_ échange \_** de messages WM associé à l’accusé de réception négatif.</span><span class="sxs-lookup"><span data-stu-id="27a84-195">If a server sends a negative acknowledgment in response to a [**WM\_DDE\_POKE**](wm-dde-poke.md) message, the client is responsible for freeing the memory (but not the *lParam* parameter) referenced by the **WM\_DDE\_POKE** message associated with the negative acknowledgment.</span></span>

## <a name="establishing-a-permanent-data-link"></a><span data-ttu-id="27a84-196">Établissement d’une liaison de données permanente</span><span class="sxs-lookup"><span data-stu-id="27a84-196">Establishing a Permanent Data Link</span></span>

<span data-ttu-id="27a84-197">Une application cliente peut utiliser DDE pour établir un lien vers un élément dans une application serveur.</span><span class="sxs-lookup"><span data-stu-id="27a84-197">A client application can use DDE to establish a link to an item in a server application.</span></span> <span data-ttu-id="27a84-198">Une fois ce lien établi, le serveur envoie des mises à jour périodiques de l’élément lié au client, en général, chaque fois que la valeur de l’élément change.</span><span class="sxs-lookup"><span data-stu-id="27a84-198">After such a link is established, the server sends periodic updates of the linked item to the client, typically, whenever the value of the item changes.</span></span> <span data-ttu-id="27a84-199">Par conséquent, un flux de données permanent est établi entre les deux applications. ce flux de données reste en place jusqu’à ce qu’il soit explicitement déconnecté.</span><span class="sxs-lookup"><span data-stu-id="27a84-199">Thus, a permanent data stream is established between the two applications; this data stream remains in place until it is explicitly disconnected.</span></span>

### <a name="initiating-a-data-link"></a><span data-ttu-id="27a84-200">Lancement d’une liaison de données</span><span class="sxs-lookup"><span data-stu-id="27a84-200">Initiating a Data Link</span></span>

<span data-ttu-id="27a84-201">Le client initie une liaison de données en publiant un message de [**\_ \_ notification**](wm-dde-advise.md) de l’échange de données (DDE) WM, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="27a84-201">The client initiates a data link by posting a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, as shown in the following example.</span></span>


```
if (!(hOptions = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(DDEADVISE)))) 
    return; 
if (!(lpOptions = (DDEADVISE FAR*) GlobalLock(hOptions))) 
{ 
    GlobalFree(hOptions); 
    return; 
} 
 
lpOptions->cfFormat = CF_TEXT; 
lpOptions->fAckReq = TRUE; 
lpOptions->fDeferUpd = FALSE; 
GlobalUnlock(hOptions); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!(PostMessage(hwndServerDDE, 
            WM_DDE_ADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_ADVISE, (UINT) hOptions, 
                atomItem)))) 
    { 
        GlobalDeleteAtom(atomItem); 
        GlobalFree(hOptions); 
        FreeDDElParam(WM_DDE_ADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors 
 
}
```



<span data-ttu-id="27a84-202">Dans cet exemple, l’application cliente affecte à l’indicateur **fDeferUpd** du message de [**\_ \_ notification DDE WM**](wm-dde-advise.md) la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="27a84-202">In this example, the client application sets the **fDeferUpd** flag of the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to **FALSE**.</span></span> <span data-ttu-id="27a84-203">Cela indique à l’application serveur d’envoyer les données au client chaque fois que les données sont modifiées.</span><span class="sxs-lookup"><span data-stu-id="27a84-203">This directs the server application to send the data to the client whenever the data changes.</span></span>

<span data-ttu-id="27a84-204">Si le serveur ne parvient pas à traiter la demande de [**\_ \_ notification DDE de WM**](wm-dde-advise.md) , il envoie un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE négatif négatif au client.</span><span class="sxs-lookup"><span data-stu-id="27a84-204">If the server is unable to service the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) request, it sends the client a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span> <span data-ttu-id="27a84-205">Toutefois, si le serveur a accès à l’élément et peut le rendre dans le format demandé, le serveur remarque le nouveau lien (en rappelant les indicateurs spécifiés dans le paramètre *hOptions* ) et envoie au client un message d' **\_ \_ accusé** de réception DDE positif positif.</span><span class="sxs-lookup"><span data-stu-id="27a84-205">But if the server has access to the item and can render it in the requested format, the server notes the new link (recalling the flags specified in the *hOptions* parameter) and sends the client a positive **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="27a84-206">À partir de là, jusqu’à ce que le client envoie un message d' [**\_ \_ invites WM DDE**](wm-dde-unadvise.md) correspondant, le serveur envoie les nouvelles données au client chaque fois que la valeur de l’élément change dans le serveur.</span><span class="sxs-lookup"><span data-stu-id="27a84-206">From then on, until the client issues a matching [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message, the server sends the new data to the client every time the value of the item changes in the server.</span></span>

<span data-ttu-id="27a84-207">Le message de [**\_ \_ notification DDE de WM**](wm-dde-advise.md) établit le format des données à échanger pendant la liaison.</span><span class="sxs-lookup"><span data-stu-id="27a84-207">The [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message establishes the format of the data to be exchanged during the link.</span></span> <span data-ttu-id="27a84-208">Si le client tente d’établir un autre lien avec le même élément mais utilise un format de données différent, le serveur peut choisir de rejeter le deuxième format de données ou de tenter de le prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="27a84-208">If the client attempts to establish another link with the same item but is using a different data format, the server can choose to reject the second data format or attempt to support it.</span></span> <span data-ttu-id="27a84-209">Si un lien à chaud a été établi pour un élément de données, le serveur ne peut prendre en charge qu’un seul format de données à la fois.</span><span class="sxs-lookup"><span data-stu-id="27a84-209">If a warm link has been established for any data item, the server can support only one data format at a time.</span></span> <span data-ttu-id="27a84-210">Cela est dû au fait que le message de [**\_ \_ données de DDE WM**](wm-dde-data.md) pour un lien chaud a un handle de données **null** , qui contient des informations de format.</span><span class="sxs-lookup"><span data-stu-id="27a84-210">This is because the [**WM\_DDE\_DATA**](wm-dde-data.md) message for a warm link has a **NULL** data handle, which otherwise contains the format information.</span></span> <span data-ttu-id="27a84-211">Par conséquent, un serveur doit rejeter tous les liens semi-chauffants pour un élément déjà lié et doit rejeter tous les liens pour un élément qui a des liens chauds.</span><span class="sxs-lookup"><span data-stu-id="27a84-211">Thus, a server must reject all warm links for an item already linked, and must reject all links for an item that has warm links.</span></span> <span data-ttu-id="27a84-212">Une autre interprétation peut être que le serveur modifie le format et l’état chaud ou chaud d’un lien lorsqu’un deuxième lien est demandé pour le même élément de données.</span><span class="sxs-lookup"><span data-stu-id="27a84-212">Another interpretation may be that the server changes the format and the hot or warm state of a link when a second link is requested for the same data item.</span></span>

<span data-ttu-id="27a84-213">En général, les applications clientes ne doivent pas tenter d’établir plusieurs liens à la fois pour un élément de données.</span><span class="sxs-lookup"><span data-stu-id="27a84-213">In general, client applications should not attempt to establish more than one link at a time for a data item.</span></span>

### <a name="initiating-a-data-link-with-the-paste-link-command"></a><span data-ttu-id="27a84-214">Lancement d’une liaison de données avec la commande Coller le lien</span><span class="sxs-lookup"><span data-stu-id="27a84-214">Initiating a Data Link with the Paste Link Command</span></span>

<span data-ttu-id="27a84-215">Les applications qui prennent en charge les liaisons de données à chaud ou à chaud prennent en charge un format de presse-papiers enregistré nommé Link.</span><span class="sxs-lookup"><span data-stu-id="27a84-215">Applications that support hot or warm data links typically support a registered clipboard format named Link.</span></span> <span data-ttu-id="27a84-216">Lorsqu’il est associé aux commandes de lien copier et coller de l’application, ce format de presse-papiers permet à l’utilisateur d’établir des conversations DDE entre les applications en copiant simplement un élément de données dans l’application serveur et en le collant dans l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="27a84-216">When associated with the application's Copy and Paste Link commands, this clipboard format enables the user to establish DDE conversations between applications simply by copying a data item in the server application and pasting it into the client application.</span></span>

<span data-ttu-id="27a84-217">Une application serveur prend en charge le format de lien du presse-papiers en plaçant dans le presse-papiers une chaîne contenant les noms de l’application, de la rubrique et de l’élément lorsque l’utilisateur choisit la commande **copier** dans le menu **Edition** .</span><span class="sxs-lookup"><span data-stu-id="27a84-217">A server application supports the Link clipboard format by placing in the clipboard a string containing the application, topic, and item names when the user chooses the **Copy** command from the **Edit** menu.</span></span> <span data-ttu-id="27a84-218">Le format de lien standard est le suivant :</span><span class="sxs-lookup"><span data-stu-id="27a84-218">Following is the standard Link format:</span></span>

<span data-ttu-id="27a84-219">\*rubrique \***\\ 0 de l’application 0\*\*\*\* \* \* 0 ***\\ 0*** \\ \\**</span><span class="sxs-lookup"><span data-stu-id="27a84-219">*application ***\\0*** topic ***\\0*** item\*\*\*\\0\\0*\*</span></span>

<span data-ttu-id="27a84-220">Un caractère null unique sépare les noms et deux caractères null terminent la chaîne entière.</span><span class="sxs-lookup"><span data-stu-id="27a84-220">A single null character separates the names, and two null characters terminate the entire string.</span></span>

<span data-ttu-id="27a84-221">Les applications client et serveur doivent enregistrer le format du presse-papiers de liens, comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="27a84-221">Both the client and server applications must register the Link clipboard format, as shown:</span></span>


```
cfLink = RegisterClipboardFormat("Link");
```



<span data-ttu-id="27a84-222">Une application cliente prend en charge le format de lien du presse-papiers au moyen d’une commande Coller le lien dans son menu Edition.</span><span class="sxs-lookup"><span data-stu-id="27a84-222">A client application supports the Link clipboard format by means of a Paste Link command on its Edit menu.</span></span> <span data-ttu-id="27a84-223">Quand l’utilisateur choisit cette commande, l’application cliente analyse les noms d’application, de rubrique et d’élément à partir des données du presse-papiers au format de lien.</span><span class="sxs-lookup"><span data-stu-id="27a84-223">When the user chooses this command, the client application parses the application, topic, and item names from the Link-format clipboard data.</span></span> <span data-ttu-id="27a84-224">À l’aide de ces noms, l’application cliente lance une conversation pour l’application et la rubrique, si une telle conversation n’existe pas encore.</span><span class="sxs-lookup"><span data-stu-id="27a84-224">Using these names, the client application initiates a conversation for the application and topic, if such a conversation does not already exist.</span></span> <span data-ttu-id="27a84-225">L’application cliente envoie alors un message de [**\_ \_ notification**](wm-dde-advise.md) de l’échange de données (DDE) WM à l’application serveur, en spécifiant le nom de l’élément contenu dans les données du presse-papiers au format de lien.</span><span class="sxs-lookup"><span data-stu-id="27a84-225">The client application then sends a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to the server application, specifying the item name contained in the Link-format clipboard data.</span></span>

<span data-ttu-id="27a84-226">Voici un exemple de réponse d’une application cliente lorsque l’utilisateur choisit la commande Coller le lien.</span><span class="sxs-lookup"><span data-stu-id="27a84-226">Following is an example of a client application's response when the user chooses the Paste Link command.</span></span>


```
void DoPasteLink(hwndClientDDE) 
HWND hwndClientDDE; 
{ 
    HANDLE hData; 
    LPSTR lpData; 
    HWND hwndServerDDE; 
    CHAR szApplication[APP_MAX_SIZE + 1]; 
    CHAR szTopic[TOPIC_MAX_SIZE + 1]; 
    CHAR szItem[ITEM_MAX_SIZE + 1]; 
    size_t * nBufLen; 
 HRESULT hResult;
 
    if (OpenClipboard(hwndClientDDE)) 
    { 
        if (!(hData = GetClipboardData(cfLink)) || 
                !(lpData = GlobalLock(hData))) 
        { 
            CloseClipboard(); 
            return; 
        } 
 
        // Parse the clipboard data.
  hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
// TODO: Write error handler.
  return;
 }
 if (*nBufLen >= APP_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szApplication, APP_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
// TODO: Write error handler.
  return;
 }
        lpData += (*nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= TOPIC_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szTopic, TOPIC_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 }
        lpData += (nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= ITEM_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }

 hResult = StringCchCopy(szItem, ITEM_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 } 
        GlobalUnlock(hData); 
        CloseClipboard(); 
 
        if (hwndServerDDE = 
                FindServerGivenAppTopic(szApplication, szTopic)) 
        { 
            // App/topic conversation is already started. 
 
            if (DoesAdviseAlreadyExist(hwndServerDDE, szItem)) 
            {
                MessageBox(hwndMain, 
                    "Advisory already established", 
                    "Client", MB_ICONEXCLAMATION | MB_OK); 
            }
            else SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
        } 
        else 
        { 
            // Client must initiate a new conversation first. 
            SendInitiate(szApplication, szTopic); 
            if (hwndServerDDE = 
                    FindServerGivenAppTopic(szApplication, 
                        szTopic)) 
            {
                SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
            }
        } 
    } 
    return; 
}
```



<span data-ttu-id="27a84-227">Dans cet exemple, l’application cliente ouvre le presse-papiers et détermine si elle contient des données au format de lien (autrement dit, cfLink) qu’elle avait précédemment inscrites.</span><span class="sxs-lookup"><span data-stu-id="27a84-227">In this example, the client application opens the clipboard and determines whether it contains data in the Link format (that is, cfLink) it had previously registered.</span></span> <span data-ttu-id="27a84-228">Si ce n’est pas le cas, ou s’il ne peut pas verrouiller les données dans le presse-papiers, le client retourne.</span><span class="sxs-lookup"><span data-stu-id="27a84-228">If not, or if it cannot lock the data in the clipboard, the client returns.</span></span>

<span data-ttu-id="27a84-229">Une fois que l’application cliente a récupéré un pointeur vers les données du presse-papiers, elle analyse les données pour extraire les noms d’application, de rubrique et d’élément.</span><span class="sxs-lookup"><span data-stu-id="27a84-229">After the client application retrieves a pointer to the clipboard data, it parses the data to extract the application, topic, and item names.</span></span>

<span data-ttu-id="27a84-230">L’application cliente détermine si une conversation sur la rubrique existe déjà entre elle et l’application serveur.</span><span class="sxs-lookup"><span data-stu-id="27a84-230">The client application determines whether a conversation on the topic already exists between it and the server application.</span></span> <span data-ttu-id="27a84-231">Si une conversation existe, le client vérifie s’il existe déjà un lien pour l’élément de données.</span><span class="sxs-lookup"><span data-stu-id="27a84-231">If a conversation does exist, the client checks whether a link already exists for the data item.</span></span> <span data-ttu-id="27a84-232">Si un tel lien existe, le client affiche une boîte de message à l’utilisateur ; dans le cas contraire, elle appelle sa propre fonction *SendAdvise* pour envoyer un message de [**\_ \_ notification**](wm-dde-advise.md) de l’échange de messages. WM au serveur pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="27a84-232">If such a link exists, the client displays a message box to the user; otherwise, it calls its own *SendAdvise* function to send a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to the server for the item.</span></span>

<span data-ttu-id="27a84-233">Si une conversation sur la rubrique n’existe pas déjà entre le client et le serveur, le client appelle d’abord sa propre fonction *SendInitiate* pour diffuser le message de [**\_ \_ lancement DDE**](wm-dde-initiate.md) pour demander une conversation et, ensuite, appelle sa propre fonction *FindServerGivenAppTopic* pour établir la conversation avec la fenêtre qui répond pour le compte de l’application serveur.</span><span class="sxs-lookup"><span data-stu-id="27a84-233">If a conversation on the topic does not already exist between the client and the server, the client first calls its own *SendInitiate* function to broadcast the [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message to request a conversation and, second, calls its own *FindServerGivenAppTopic* function to establish the conversation with the window that responds on behalf of the server application.</span></span> <span data-ttu-id="27a84-234">Une fois la conversation commencée, l’application cliente appelle *SendAdvise* pour demander le lien.</span><span class="sxs-lookup"><span data-stu-id="27a84-234">After the conversation has begun, the client application calls *SendAdvise* to request the link.</span></span>

### <a name="notifying-the-client-that-data-has-changed"></a><span data-ttu-id="27a84-235">Notification au client que les données ont été modifiées</span><span class="sxs-lookup"><span data-stu-id="27a84-235">Notifying the Client that Data Has Changed</span></span>

<span data-ttu-id="27a84-236">Lorsque le client établit un lien à l’aide du message de [**\_ \_ notification DDE WM**](wm-dde-advise.md) , avec le membre **fDeferUpd** non défini (autrement dit, égal à zéro) dans la structure [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) , le client a demandé au serveur d’envoyer l’élément de données chaque fois que la valeur de l’élément est modifiée.</span><span class="sxs-lookup"><span data-stu-id="27a84-236">When the client establishes a link by using the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, with the **fDeferUpd** member not set (that is, equal to zero) in the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure, the client has requested the server send the data item each time the item's value changes.</span></span> <span data-ttu-id="27a84-237">Dans ce cas, le serveur restitue la nouvelle valeur de l’élément de données dans le format spécifié précédemment et envoie au client un message de données de l' [**\_ échange de \_ données (DDE) WM**](wm-dde-data.md) , comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="27a84-237">In such cases, the server renders the new value of the data item in the previously specified format and sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message, as shown in the following example.</span></span>


```
// Allocate the size of a DDE data header, plus data (a string), 
// plus a <CR><LF><NULL> 

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  sizeof(DDEDATA) + *pcch + 3))) 
{
    return; 
}
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData))) 
{ 
    GlobalFree(hData); 
    return; 
} 
lpData->fAckReq = bAckRequest;       // as in original WM_DDE_ADVISE 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy(lpData->Value, *pcch +1, szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
// add CR/LF for CF_TEXT format
hResult = StringCchCat(lpData->Value, *pcch + 3, "\r\n");
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            PackDDElParam(WM_DDE_DATA, (UINT) hData, atomItem))) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_DATA, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
 
}
```



<span data-ttu-id="27a84-238">Dans cet exemple, le client traite la valeur de l’élément selon le cas.</span><span class="sxs-lookup"><span data-stu-id="27a84-238">In this example, the client processes the item value as appropriate.</span></span> <span data-ttu-id="27a84-239">Si l’indicateur **fAckReq** de l’élément est défini, le client envoie un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE positif au serveur.</span><span class="sxs-lookup"><span data-stu-id="27a84-239">If the **fAckReq** flag for the item is set, the client sends the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="27a84-240">Lorsque le client établit le lien, avec le jeu de membres **fDeferUpd** (autrement dit, égal à 1), le client a demandé que seule une notification, et non les données lui-même, soit envoyée chaque fois que les données sont modifiées.</span><span class="sxs-lookup"><span data-stu-id="27a84-240">When the client establishes the link, with the **fDeferUpd** member set (that is, equal to 1), the client has requested that only a notification, not the data itself, be sent each time the data changes.</span></span> <span data-ttu-id="27a84-241">Dans ce cas, lorsque la valeur de l’élément change, le serveur n’affiche pas la valeur, mais envoie simplement au client un message de [**\_ \_ données de l’échange WM**](wm-dde-data.md) avec un descripteur de données null, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="27a84-241">In such cases, when the item value changes, the server does not render the value but simply sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message with a null data handle, as illustrated in the following example.</span></span>


```
if (bDeferUpd)      // check whether flag was set in WM_DDE_ADVISE
{
    if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
    { 
        if (!PostMessage(hwndClientDDE, 
                WM_DDE_DATA, 
                (WPARAM) hwndServerDDE, 
                PackDDElParam(WM_DDE_DATA, 0, 
                    atomItem)))                  // NULL data
        {
            GlobalDeleteAtom(atomItem); 
            FreeDDElParam(WM_DDE_DATA, lParam); 
        } 
    } 
} 
 
if (atomItem == 0) 
{ 
     // Handle errors. 
} 
```



<span data-ttu-id="27a84-242">Si nécessaire, le client peut demander la valeur la plus récente de l’élément de données en émettant un message de [**\_ \_ requête DDE**](wm-dde-request.md) normal, ou il peut simplement ignorer la notification du serveur dont les données ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="27a84-242">As necessary, the client can request the latest value of the data item by issuing a normal [**WM\_DDE\_REQUEST**](wm-dde-request.md) message, or it can simply ignore the notice from the server that the data has changed.</span></span> <span data-ttu-id="27a84-243">Dans les deux cas, si **fAckReq** est égal à 1, le client est supposé envoyer un message [**d' \_ \_ accusé**](wm-dde-ack.md) de réception DDE positif positif au serveur.</span><span class="sxs-lookup"><span data-stu-id="27a84-243">In either case, if **fAckReq** is equal to 1, the client is expected to send a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message to the server.</span></span>

### <a name="terminating-a-data-link"></a><span data-ttu-id="27a84-244">Arrêt d’une liaison de données</span><span class="sxs-lookup"><span data-stu-id="27a84-244">Terminating a Data Link</span></span>

<span data-ttu-id="27a84-245">Si le client demande l’arrêt d’un lien de données spécifique, le client envoie un message de [**\_ \_ notification**](wm-dde-unadvise.md) de l’échange de données à un serveur WM, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="27a84-245">If the client requests that a specific data link be terminated, the client sends the server a [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message, as shown in the following example.</span></span>


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_UNADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_UNADVISE, 0, atomItem))) 
    { 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_UNADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="27a84-246">Le serveur vérifie si le client dispose actuellement d’un lien vers l’élément spécifique de cette conversation.</span><span class="sxs-lookup"><span data-stu-id="27a84-246">The server checks whether the client currently has a link to the specific item in this conversation.</span></span> <span data-ttu-id="27a84-247">Si un lien existe, le serveur envoie au client un message [**d' \_ \_ accusé**](wm-dde-ack.md) de réception DDE positif positif ; le serveur n’est alors plus nécessaire pour envoyer des mises à jour concernant l’élément.</span><span class="sxs-lookup"><span data-stu-id="27a84-247">If a link exists, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; the server is then no longer required to send updates about the item.</span></span> <span data-ttu-id="27a84-248">S’il n’existe pas de lien, le serveur envoie un message d' **\_ \_ accusé** de réception DDE négatif négatif au client.</span><span class="sxs-lookup"><span data-stu-id="27a84-248">If no link exists, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>

<span data-ttu-id="27a84-249">Le message [**WM \_ DDE \_ Unadvise**](wm-dde-unadvise.md) spécifie un format de données.</span><span class="sxs-lookup"><span data-stu-id="27a84-249">The [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message specifies a data format.</span></span> <span data-ttu-id="27a84-250">Un format de zéro indique au serveur d’arrêter tous les liens pour l’élément spécifié, même si plusieurs liens sensibles sont établis et chacun utilise un format différent.</span><span class="sxs-lookup"><span data-stu-id="27a84-250">A format of zero informs the server to stop all links for the specified item, even if several hot links are established and each uses a different format.</span></span>

<span data-ttu-id="27a84-251">Pour mettre fin à tous les liens d’une conversation, l’application cliente envoie au serveur un message [**WM \_ DDE \_ Unadvise**](wm-dde-unadvise.md) avec un atome d’élément null.</span><span class="sxs-lookup"><span data-stu-id="27a84-251">To terminate all links for a conversation, the client application sends the server a [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message with a null item atom.</span></span> <span data-ttu-id="27a84-252">Le serveur détermine si la conversation a au moins un lien actuellement établi.</span><span class="sxs-lookup"><span data-stu-id="27a84-252">The server determines whether the conversation has at least one link currently established.</span></span> <span data-ttu-id="27a84-253">Si un lien existe, le serveur envoie au client un message [**d' \_ \_ accusé**](wm-dde-ack.md) de réception DDE positif positif ; le serveur n’a plus à envoyer de mise à jour dans la conversation.</span><span class="sxs-lookup"><span data-stu-id="27a84-253">If a link exists, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; the server then no longer has to send any updates in the conversation.</span></span> <span data-ttu-id="27a84-254">S’il n’existe pas de lien, le serveur envoie un message d' **\_ \_ accusé** de réception DDE négatif négatif au client.</span><span class="sxs-lookup"><span data-stu-id="27a84-254">If no link exists, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>

## <a name="carrying-out-commands-in-a-server-application"></a><span data-ttu-id="27a84-255">Exécution de commandes dans une application serveur</span><span class="sxs-lookup"><span data-stu-id="27a84-255">Carrying Out Commands in a Server Application</span></span>

<span data-ttu-id="27a84-256">Les applications peuvent utiliser le message d' [**\_ \_ exécution DDE de WM**](wm-dde-execute.md) pour déclencher l’exécution d’une certaine commande ou d’une série de commandes dans une autre application.</span><span class="sxs-lookup"><span data-stu-id="27a84-256">Applications can use the [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message to cause a certain command or series of commands to be carried out in another application.</span></span> <span data-ttu-id="27a84-257">Pour ce faire, le client envoie au serveur un message **WM d' \_ \_ exécution DDE** contenant un handle vers une chaîne de commande, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="27a84-257">To do this, the client sends the server a **WM\_DDE\_EXECUTE** message containing a handle to a command string, as shown in the following example.</span></span>


```
HRESULT hResult;
  
if (!(hCommand = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(szCommandString) + 1))) 
{
    return; 
}
if (!(lpCommand = GlobalLock(hCommand))) 
{ 
    GlobalFree(hCommand); 
    return; 
} 

hResult = StringCbCopy(lpCommand, sizeof(szCommandString), szCommandString);
if (hResult != S_OK)
{
// TODO: Write error handler.
 return;
}
 
GlobalUnlock(hCommand); 
if (!PostMessage(hwndServerDDE, 
        WM_DDE_EXECUTE, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_EXECUTE, 0, (UINT) hCommand))) 
{ 
    GlobalFree(hCommand); 
    FreeDDElParam(WM_DDE_EXECUTE, lParam); 
}
```



<span data-ttu-id="27a84-258">Dans cet exemple, le serveur tente d’exécuter la chaîne de commande spécifiée.</span><span class="sxs-lookup"><span data-stu-id="27a84-258">In this example, the server attempts to carry out the specified command string.</span></span> <span data-ttu-id="27a84-259">En cas de tentative, le serveur envoie au client un message [**d' \_ \_ accusé**](wm-dde-ack.md) de réception DDE positif positif ; sinon, il envoie un message d' **\_ \_ accusé** de réception DDE négatif négatif.</span><span class="sxs-lookup"><span data-stu-id="27a84-259">If it succeeds, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; otherwise, it sends a negative **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="27a84-260">Ce message d' **\_ \_ accusé** de réception DDE de WM réutilise le descripteur *hCommand* passé dans le message d' [**\_ \_ exécution DDE DDE**](wm-dde-execute.md) d’origine.</span><span class="sxs-lookup"><span data-stu-id="27a84-260">This **WM\_DDE\_ACK** message reuses the *hCommand* handle passed in the original [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message.</span></span>

<span data-ttu-id="27a84-261">Si la chaîne d’exécution de la commande du client demande que le serveur s’arrête, le serveur doit répondre en envoyant un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE positif, puis envoyer un message [**WM \_ DDE \_ Terminate**](wm-dde-terminate.md) avant de se terminer.</span><span class="sxs-lookup"><span data-stu-id="27a84-261">If the client's command execution string requests that the server terminate, the server should respond by sending a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message and then post a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message before terminating.</span></span> <span data-ttu-id="27a84-262">Toutes les autres commandes envoyées avec un message d' [**\_ \_ exécution DDE de WM**](wm-dde-execute.md) doivent être exécutées de façon synchrone ; autrement dit, le serveur doit envoyer un message d’accusé de réception **\_ DDE \_ de WM** uniquement après la fin de la commande.</span><span class="sxs-lookup"><span data-stu-id="27a84-262">All other commands sent with a [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message should be executed synchronously; that is, the server should send a **WM\_DDE\_ACK** message only after successfully completing the command.</span></span>

## <a name="terminating-a-conversation"></a><span data-ttu-id="27a84-263">Arrêt d’une conversation</span><span class="sxs-lookup"><span data-stu-id="27a84-263">Terminating a Conversation</span></span>

<span data-ttu-id="27a84-264">Le client ou le serveur peut émettre un message [**WM \_ DDE \_ Terminate**](wm-dde-terminate.md) pour mettre fin à une conversation à tout moment.</span><span class="sxs-lookup"><span data-stu-id="27a84-264">Either the client or the server can issue a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message to terminate a conversation at any time.</span></span> <span data-ttu-id="27a84-265">De même, les applications client et serveur doivent être prêtes à recevoir ce message à tout moment.</span><span class="sxs-lookup"><span data-stu-id="27a84-265">Similarly, both the client and server applications should be prepared to receive this message at any time.</span></span> <span data-ttu-id="27a84-266">Une application doit mettre fin à toutes ses conversations avant de s’arrêter.</span><span class="sxs-lookup"><span data-stu-id="27a84-266">An application must terminate all of its conversations before shutting down.</span></span>

<span data-ttu-id="27a84-267">Dans l’exemple suivant, l’application qui termine la conversation publie un message [**WM \_ DDE \_ Terminate**](wm-dde-terminate.md) .</span><span class="sxs-lookup"><span data-stu-id="27a84-267">In the following example, the application terminating the conversation posts a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message.</span></span>


```
PostMessage(hwndServerDDE, WM_DDE_TERMINATE, 
    (WPARAM) hwndClientDDE, 0);
```



<span data-ttu-id="27a84-268">Cela indique à l’autre application que l’application émettrice n’enverra pas de messages supplémentaires et que le destinataire pourra fermer sa fenêtre.</span><span class="sxs-lookup"><span data-stu-id="27a84-268">This informs the other application that the sending application will send no further messages and the recipient can close its window.</span></span> <span data-ttu-id="27a84-269">Dans tous les cas, le destinataire est censé répondre rapidement en envoyant un message [**WM de \_ \_ fin DDE**](wm-dde-terminate.md) .</span><span class="sxs-lookup"><span data-stu-id="27a84-269">The recipient is expected in all cases to respond promptly by sending a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message.</span></span> <span data-ttu-id="27a84-270">Le destinataire ne doit pas envoyer un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE négatif, occupé ou positif.</span><span class="sxs-lookup"><span data-stu-id="27a84-270">The recipient must not send a negative, busy, or positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="27a84-271">Une fois qu’une application a envoyé le message de [**\_ \_ fin**](wm-dde-terminate.md) de l’échange de messages avec le protocole WM DDE au partenaire dans une conversation DDE, elle ne doit pas répondre aux messages de ce partenaire, car le partenaire a peut-être détruit la fenêtre à laquelle la réponse est envoyée.</span><span class="sxs-lookup"><span data-stu-id="27a84-271">After an application has sent the [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message to the partner in a DDE conversation, it must not respond to messages from that partner, since the partner might have destroyed the window to which the response would be sent.</span></span>

<span data-ttu-id="27a84-272">Si une application reçoit un message DDE autre que [**WM \_ DDE \_ Terminate**](wm-dde-terminate.md) après qu’elle a publié **WM \_ DDE \_ Terminate**, elle doit libérer tous les objets associés aux messages reçus, à l’exception des handles de données pour les [**\_ \_ données DDE WM**](wm-dde-data.md) ou des messages coscripteur [**WM \_ DDE \_**](wm-dde-poke.md) qui n’ont **pas** de membre **fRelease** .</span><span class="sxs-lookup"><span data-stu-id="27a84-272">If an application receives a DDE message other than [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) after it has posted **WM\_DDE\_TERMINATE**, it should free all objects associated with the received messages except the data handles for [**WM\_DDE\_DATA**](wm-dde-data.md) or [**WM\_DDE\_POKE**](wm-dde-poke.md) messages that do **not** have the **fRelease** member set.</span></span>

<span data-ttu-id="27a84-273">Quand une application est sur le lieu de s’arrêter, elle doit mettre fin à toutes les conversations DDE actives avant de terminer le traitement du message [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="27a84-273">When an application is about to terminate, it should end all active DDE conversations before completing processing of the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span> <span data-ttu-id="27a84-274">Toutefois, si une application ne termine pas ses conversations DDE actives, le système met fin à toutes les conversations DDE associées à une fenêtre lorsque celle-ci est détruite.</span><span class="sxs-lookup"><span data-stu-id="27a84-274">However, if an application does not end its active DDE conversations, the system will terminate any DDE conversations associated with a window when the window is destroyed.</span></span> <span data-ttu-id="27a84-275">L’exemple suivant montre comment une application serveur met fin à toutes les conversations DDE.</span><span class="sxs-lookup"><span data-stu-id="27a84-275">The following example shows how a server application terminates all DDE conversations.</span></span>


```
void TerminateConversations(hwndServerDDE) 
HWND hwndServerDDE; 
{ 
    HWND hwndClientDDE; 
 
    // Terminate each active conversation. 
 
    while (hwndClientDDE = GetNextLink(hwndClientDDE)) 
    { 
        SendTerminate(hwndServerDDE, hwndClientDDE); 
    } 
    return; 
} 
 
BOOL AtLeastOneLinkActive(VOID) 
{ 
    return TRUE; 
} 
 
HWND GetNextLink(hwndDummy) 
    HWND hwndDummy; 
{ 
    return (HWND) 1; 
} 
 
VOID SendTerminate(HWND hwndServerDDE, HWND hwndClientDDE) 
{ 
    return; 
}
```



 

 