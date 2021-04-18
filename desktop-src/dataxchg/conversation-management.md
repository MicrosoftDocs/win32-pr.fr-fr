---
title: Gestion des conversations
description: Cette rubrique décrit les conversations entre un client et un serveur.
ms.assetid: 4e5ff1a1-d46a-4e2a-a37c-8df951f2a1ee
keywords:
- Interface utilisateur Windows, échange dynamique de données (DDE)
- Échange dynamique de données (DDE), conversations
- DDE (échange dynamique de données), conversations
- échange de données, échange dynamique de données (DDE)
- Interface utilisateur Windows, bibliothèque de gestion des échange dynamique de données (DDEML)
- Bibliothèque de gestion des échange dynamique de données (DDEML), conversations
- DDEML (bibliothèque de gestion échange dynamique de données), conversations
- échange de données, bibliothèque de gestion des échange dynamique de données (DDEML)
- Échange dynamique de données (DDE), plusieurs conversations
- DDE (échange dynamique de données), plusieurs conversations
- Bibliothèque de gestion des échange dynamique de données (DDEML), plusieurs conversations
- DDEML (bibliothèque de gestion échange dynamique de données), plusieurs conversations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca1a0a8e02bceb6b2f69051d89df289871fdd42
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512470"
---
# <a name="conversation-management"></a><span data-ttu-id="4075b-115">Gestion des conversations</span><span class="sxs-lookup"><span data-stu-id="4075b-115">Conversation Management</span></span>

<span data-ttu-id="4075b-116">Une conversation entre un client et un serveur est toujours établie à la demande du client.</span><span class="sxs-lookup"><span data-stu-id="4075b-116">A conversation between a client and a server is always established at the request of the client.</span></span> <span data-ttu-id="4075b-117">Lorsqu’une conversation est établie, chaque partenaire reçoit un descripteur qui identifie la conversation.</span><span class="sxs-lookup"><span data-stu-id="4075b-117">When a conversation is established, each partner receives a handle that identifies the conversation.</span></span> <span data-ttu-id="4075b-118">Les partenaires utilisent ce handle dans d’autres fonctions de la bibliothèque de gestion des échange dynamique de données (DDEML) pour envoyer des transactions et gérer la conversation.</span><span class="sxs-lookup"><span data-stu-id="4075b-118">The partners use this handle in other Dynamic Data Exchange Management Library (DDEML) functions to send transactions and manage the conversation.</span></span> <span data-ttu-id="4075b-119">Un client peut demander une conversation avec un seul serveur, ou il peut demander plusieurs conversations avec un ou plusieurs serveurs.</span><span class="sxs-lookup"><span data-stu-id="4075b-119">A client can request a conversation with a single server, or it can request multiple conversations with one or more servers.</span></span>

<span data-ttu-id="4075b-120">Les rubriques suivantes décrivent comment une application établit de nouvelles conversations et obtient des informations sur les conversations existantes.</span><span class="sxs-lookup"><span data-stu-id="4075b-120">The following topics describe how an application establishes new conversations and gets information about existing conversations.</span></span>

-   [<span data-ttu-id="4075b-121">Conversations uniques</span><span class="sxs-lookup"><span data-stu-id="4075b-121">Single Conversations</span></span>](#single-conversations)
-   [<span data-ttu-id="4075b-122">Conversations multiples</span><span class="sxs-lookup"><span data-stu-id="4075b-122">Multiple Conversations</span></span>](#multiple-conversations)

## <a name="single-conversations"></a><span data-ttu-id="4075b-123">Conversations uniques</span><span class="sxs-lookup"><span data-stu-id="4075b-123">Single Conversations</span></span>

<span data-ttu-id="4075b-124">Une application cliente demande une conversation unique avec un serveur en appelant la fonction [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) et en spécifiant des handles de chaîne qui identifient les chaînes contenant le nom de service de l’application serveur et le nom de la rubrique pour la conversation.</span><span class="sxs-lookup"><span data-stu-id="4075b-124">A client application requests a single conversation with a server by calling the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function and specifying string handles that identify the strings containing the service name of the server application and the topic name for the conversation.</span></span> <span data-ttu-id="4075b-125">Le DDEML répond en envoyant la transaction [**XTYP \_ Connect**](xtyp-connect.md) à la fonction de rappel échange dynamique de données (DDE) de chaque application serveur qui a inscrit un nom de service qui correspond à celui spécifié dans **DdeConnect** ou a désactivé le filtrage du nom de service en appelant [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice).</span><span class="sxs-lookup"><span data-stu-id="4075b-125">The DDEML responds by sending the [**XTYP\_CONNECT**](xtyp-connect.md) transaction to the Dynamic Data Exchange (DDE) callback function of each server application that either has registered a service name that matches the one specified in **DdeConnect** or has turned service name filtering off by calling [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice).</span></span> <span data-ttu-id="4075b-126">Un serveur peut également filtrer les transactions **XTYP \_ Connect** en spécifiant \_ l' \_ indicateur de filtre des connexions en échec CBF dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="4075b-126">A server can also filter **XTYP\_CONNECT** transactions by specifying the CBF\_FAIL\_CONNECTIONS filter flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span> <span data-ttu-id="4075b-127">Au cours de la transaction **XTYP \_ Connect** , Ddeml transmet le nom du service et le nom de la rubrique au serveur.</span><span class="sxs-lookup"><span data-stu-id="4075b-127">During the **XTYP\_CONNECT** transaction, the DDEML passes the service name and the topic name to the server.</span></span> <span data-ttu-id="4075b-128">Le serveur doit examiner les noms et retourner la **valeur true** s’il prend en charge la paire nom du service et nom de la rubrique, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4075b-128">The server must examine the names and return **TRUE** if it supports the service name and topic name pair or **FALSE** if it does not.</span></span>

<span data-ttu-id="4075b-129">Si aucun serveur ne répond de manière positive à la demande de connexion du client, le client reçoit la **valeur null** de [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) et aucune conversation n’est établie.</span><span class="sxs-lookup"><span data-stu-id="4075b-129">If no server responds positively to the client's request to connect, the client receives **NULL** from [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) and no conversation is established.</span></span> <span data-ttu-id="4075b-130">Si un serveur retourne la **valeur true**, une conversation est établie et le client reçoit un descripteur de conversation (valeur **DWORD** qui identifie la conversation).</span><span class="sxs-lookup"><span data-stu-id="4075b-130">If a server returns **TRUE**, a conversation is established and the client receives a conversation handle — a **DWORD** value that identifies the conversation.</span></span> <span data-ttu-id="4075b-131">Le client utilise le handle dans les appels DDEML suivants pour obtenir des données à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="4075b-131">The client uses the handle in subsequent DDEML calls to obtain data from the server.</span></span> <span data-ttu-id="4075b-132">Le serveur reçoit la [**transaction \_ \_ Confirm XTYP Connect**](xtyp-connect-confirm.md) (à moins que le serveur n’ait spécifié l' \_ indicateur de filtre CBF Skip \_ Connect \_ Confirm).</span><span class="sxs-lookup"><span data-stu-id="4075b-132">The server receives the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction (unless the server specified the CBF\_SKIP\_CONNECT\_CONFIRMS filter flag).</span></span> <span data-ttu-id="4075b-133">Cette transaction transmet le descripteur de conversation au serveur.</span><span class="sxs-lookup"><span data-stu-id="4075b-133">This transaction passes the conversation handle to the server.</span></span>

<span data-ttu-id="4075b-134">L’exemple suivant demande une conversation sur la rubrique du système avec un serveur qui reconnaît le nom du service MyServer.</span><span class="sxs-lookup"><span data-stu-id="4075b-134">The following example requests a conversation on the System topic with a server that recognizes the service name MyServer.</span></span> <span data-ttu-id="4075b-135">Les paramètres *hszServName* et *hszSysTopic* sont des handles de chaîne créés précédemment.</span><span class="sxs-lookup"><span data-stu-id="4075b-135">The *hszServName* and *hszSysTopic* parameters are previously created string handles.</span></span>


```
HCONV hConv;         // conversation handle 
HWND hwndParent;     // parent window handle 
HSZ hszServName;     // service name string handle 
HSZ hszSysTopic;     // System topic string handle 
 
hConv = DdeConnect( 
    idInst,               // instance identifier 
    hszServName,          // service name string handle 
    hszSysTopic,          // System topic string handle 
    (PCONVCONTEXT) NULL); // use default context 
 
if (hConv == NULL) 
{ 
    MessageBox(hwndParent, "MyServer is unavailable.", 
        (LPSTR) NULL, MB_OK); 
    return FALSE; 
} 
```



<span data-ttu-id="4075b-136">Dans l’exemple précédent, [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) force la fonction de rappel DDE de l’application monserveur à recevoir une transaction [**XTYP \_ Connect**](xtyp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="4075b-136">In the preceding example, [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) causes the DDE callback function of the MyServer application to receive an [**XTYP\_CONNECT**](xtyp-connect.md) transaction.</span></span>

<span data-ttu-id="4075b-137">Dans l’exemple suivant, le serveur répond à la transaction [**XTYP \_ Connect**](xtyp-connect.md) en comparant la chaîne de nom de la rubrique gérer les Ddeml passés au serveur avec chaque élément du tableau de handles de chaîne de nom de rubrique que le serveur prend en charge.</span><span class="sxs-lookup"><span data-stu-id="4075b-137">In the following example, the server responds to the [**XTYP\_CONNECT**](xtyp-connect.md) transaction by comparing the topic name string handle the DDEML passed to the server with each element in the array of topic name string handles the server supports.</span></span> <span data-ttu-id="4075b-138">Si le serveur trouve une correspondance, il établit la conversation.</span><span class="sxs-lookup"><span data-stu-id="4075b-138">If the server finds a match, it establishes the conversation.</span></span>


```
#define CTOPICS 5 
 
HSZ hsz1;                  // string handle passed by DDEML 
HSZ ahszTopics[CTOPICS];   // array of supported topics 
int i;                     // loop counter 
 
// Use a switch statement to examine transaction types. 
// Here is the connect case.
 
    case XTYP_CONNECT: 
        for (i = 0; i < CTOPICS; i++) 
        { 
            if (hsz1 == ahszTopics[i]) 
                return TRUE;   // establish a conversation 
        } 
 
        return FALSE; // Topic not supported; deny conversation.  
 
// Process other transaction types. 
```



<span data-ttu-id="4075b-139">Si le serveur retourne la **valeur true** en réponse à la transaction [**XTYP \_ Connect**](xtyp-connect.md) , Ddeml envoie une transaction de [**\_ \_ confirmation de connexion XTYP**](xtyp-connect-confirm.md) à la fonction de rappel DDE du serveur.</span><span class="sxs-lookup"><span data-stu-id="4075b-139">If the server returns **TRUE** in response to the [**XTYP\_CONNECT**](xtyp-connect.md) transaction, the DDEML sends an [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server's DDE callback function.</span></span> <span data-ttu-id="4075b-140">Le serveur peut obtenir le descripteur de la conversation en traitant cette transaction.</span><span class="sxs-lookup"><span data-stu-id="4075b-140">The server can obtain the handle to the conversation by processing this transaction.</span></span>

<span data-ttu-id="4075b-141">Un client peut établir une conversation générique en spécifiant **null** pour le descripteur de chaîne de nom de service, le handle de chaîne de nom de rubrique ou les deux dans un appel à [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect).</span><span class="sxs-lookup"><span data-stu-id="4075b-141">A client can establish a wildcard conversation by specifying **NULL** for the service name string handle, the topic name string handle, or both in a call to [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect).</span></span> <span data-ttu-id="4075b-142">Si au moins l’un des descripteurs de chaîne a la **valeur null**, Ddeml envoie la transaction [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) aux fonctions de rappel de toutes les applications DDE (à l’exception de celles qui filtrent la transaction **\_ WILDCONNECT XTYP** ).</span><span class="sxs-lookup"><span data-stu-id="4075b-142">If at least one of the string handles is **NULL**, the DDEML sends the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction to the callback functions of all DDE applications (except those that filter the **XTYP\_WILDCONNECT** transaction).</span></span> <span data-ttu-id="4075b-143">Chaque application serveur doit répondre en retournant un handle de données qui identifie un tableau de structures [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) se terminant par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="4075b-143">Each server application should respond by returning a data handle that identifies a null-terminated array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="4075b-144">Si l’application serveur n’a pas appelé [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) pour enregistrer ses noms de service et si le filtrage est activé, le serveur ne reçoit pas de transactions **XTYP \_ WILDCONNECT** .</span><span class="sxs-lookup"><span data-stu-id="4075b-144">If the server application has not called [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) to register its service names and if filtering is on, the server does not receive **XTYP\_WILDCONNECT** transactions.</span></span> <span data-ttu-id="4075b-145">Pour plus d’informations sur les handles de données, consultez [gestion des données](data-management.md).</span><span class="sxs-lookup"><span data-stu-id="4075b-145">For more information about data handles, see [Data Management](data-management.md).</span></span>

<span data-ttu-id="4075b-146">Le tableau doit contenir une structure pour chaque paire nom de service/nom de rubrique qui correspond à la paire spécifiée par le client.</span><span class="sxs-lookup"><span data-stu-id="4075b-146">The array must contain one structure for each service name and topic name pair that matches the pair specified by the client.</span></span> <span data-ttu-id="4075b-147">Le DDEML sélectionne l’une des paires pour établir une conversation et retourne au client un descripteur qui identifie la conversation.</span><span class="sxs-lookup"><span data-stu-id="4075b-147">The DDEML selects one of the pairs to establish a conversation and returns to the client a handle that identifies the conversation.</span></span> <span data-ttu-id="4075b-148">DDEML envoie la transaction [**de \_ \_ confirmation de connexion XTYP**](xtyp-connect-confirm.md) au serveur (sauf si le serveur filtre cette transaction).</span><span class="sxs-lookup"><span data-stu-id="4075b-148">The DDEML sends the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server (unless the server filters this transaction).</span></span> <span data-ttu-id="4075b-149">L’exemple suivant montre une réponse de serveur typique à la transaction [**\_ WILDCONNECT XTYP**](xtyp-wildconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="4075b-149">The following example shows a typical server response to the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction.</span></span>


```
#define CTOPICS 2 
 
UINT uType; 
HSZPAIR ahszp[(CTOPICS + 1)]; 
HSZ ahszTopicList[CTOPICS]; 
HSZ hszServ, hszTopic; 
WORD i, j; 
 
if (uType == XTYP_WILDCONNECT) 
{ 
    // Scan the topic list and create an array of HSZPAIR structures. 
 
    j = 0; 
    for (i = 0; i < CTOPICS; i++) 
    { 
        if (hszTopic == (HSZ) NULL || 
                hszTopic == ahszTopicList[i]) 
        { 
            ahszp[j].hszSvc = hszServ; 
            ahszp[j++].hszTopic = ahszTopicList[i]; 
        } 
    } 
 
    // End the list with an HSZPAIR structure that contains NULL 
    // string handles as its members. 
 
    ahszp[j].hszSvc = NULL; 
    ahszp[j++].hszTopic = NULL; 
 
    // Return a handle to a global memory object containing the 
    // HSZPAIR structures. 
 
    return DdeCreateDataHandle( 
        idInst,          // instance identifier 
        (LPBYTE) &ahszp, // pointer to HSZPAIR array 
        sizeof(HSZ) * j, // length of the array 
        0,               // start at the beginning 
        (HSZ) NULL,      // no item name string 
        0,               // return the same format 
        0);              // let the system own it 
} 
```



<span data-ttu-id="4075b-150">Le client ou le serveur peut mettre fin à une conversation à tout moment en appelant la fonction [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) .</span><span class="sxs-lookup"><span data-stu-id="4075b-150">Either the client or the server can terminate a conversation at any time by calling the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function.</span></span> <span data-ttu-id="4075b-151">Cette fonction permet à la fonction de rappel du partenaire de la conversation de recevoir la transaction de [**\_ déconnexion XTYP**](xtyp-disconnect.md) (sauf si le partenaire a spécifié l' \_ indicateur de filtre CBF Skip \_ deconnections).</span><span class="sxs-lookup"><span data-stu-id="4075b-151">This function causes the callback function of the partner in the conversation to receive the [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transaction (unless the partner specified the CBF\_SKIP\_DISCONNECTS filter flag).</span></span> <span data-ttu-id="4075b-152">En règle générale, une application répond à la transaction de **\_ déconnexion XTYP** à l’aide de la fonction [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) pour obtenir des informations sur la conversation qui s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="4075b-152">Typically, an application responds to the **XTYP\_DISCONNECT** transaction by using the [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) function to obtain information about the conversation that terminated.</span></span> <span data-ttu-id="4075b-153">Une fois que la fonction de rappel a retourné le traitement de la transaction de **\_ déconnexion XTYP** , le descripteur de conversation n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="4075b-153">After the callback function returns from processing the **XTYP\_DISCONNECT** transaction, the conversation handle is no longer valid.</span></span>

<span data-ttu-id="4075b-154">Une application cliente qui reçoit une transaction de [**\_ déconnexion XTYP**](xtyp-disconnect.md) dans sa fonction de rappel DDE peut tenter de rétablir la conversation en appelant la fonction [**DdeReconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) .</span><span class="sxs-lookup"><span data-stu-id="4075b-154">A client application that receives an [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transaction in its DDE callback function can attempt to reestablish the conversation by calling the [**DdeReconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) function.</span></span> <span data-ttu-id="4075b-155">Le client doit appeler **DdeReconnect** à partir de sa fonction de rappel DDE.</span><span class="sxs-lookup"><span data-stu-id="4075b-155">The client must call **DdeReconnect** from within its DDE callback function.</span></span>

## <a name="multiple-conversations"></a><span data-ttu-id="4075b-156">Conversations multiples</span><span class="sxs-lookup"><span data-stu-id="4075b-156">Multiple Conversations</span></span>

<span data-ttu-id="4075b-157">Une application cliente peut utiliser la fonction [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) pour déterminer si des serveurs intéressants sont disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="4075b-157">A client application can use the [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) function to determine whether any servers of interest are available in the system.</span></span> <span data-ttu-id="4075b-158">Un client spécifie un nom de service et un nom de rubrique lors de l’appel de **DdeConnectList**, ce qui amène le Ddeml à diffuser la transaction [**\_ WILDCONNECT XTYP**](xtyp-wildconnect.md) vers les fonctions de rappel DDE de tous les serveurs qui correspondent au nom du service (sauf ceux qui filtrent la transaction).</span><span class="sxs-lookup"><span data-stu-id="4075b-158">A client specifies a service name and topic name when it calls **DdeConnectList**, causing the DDEML to broadcast the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction to the DDE callback functions of all servers that match the service name (except those that filter the transaction).</span></span> <span data-ttu-id="4075b-159">La fonction de rappel d’un serveur doit retourner un handle de données qui identifie un tableau de structures [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) terminé par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="4075b-159">A server's callback function should return a data handle that identifies a null-terminated array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="4075b-160">Le tableau doit contenir une structure pour chaque paire nom de service/nom de rubrique qui correspond à la paire spécifiée par le client.</span><span class="sxs-lookup"><span data-stu-id="4075b-160">The array should contain one structure for each service name and topic name pair that matches the pair specified by the client.</span></span> <span data-ttu-id="4075b-161">Le DDEML établit une conversation pour chaque structure **HSZPAIR** remplie par le serveur et retourne un descripteur de liste de conversations au client.</span><span class="sxs-lookup"><span data-stu-id="4075b-161">The DDEML establishes a conversation for each **HSZPAIR** structure filled by the server and returns a conversation list handle to the client.</span></span> <span data-ttu-id="4075b-162">Le serveur reçoit le descripteur de conversation par le biais de la transaction [**XTYP \_ Connect**](xtyp-connect.md) (sauf si le serveur filtre cette transaction).</span><span class="sxs-lookup"><span data-stu-id="4075b-162">The server receives the conversation handle by way of the [**XTYP\_CONNECT**](xtyp-connect.md) transaction (unless the server filters this transaction).</span></span>

<span data-ttu-id="4075b-163">Un client peut spécifier la **valeur null** pour le nom du service, le nom de la rubrique, ou les deux lorsqu’il appelle [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span><span class="sxs-lookup"><span data-stu-id="4075b-163">A client can specify **NULL** for the service name, topic name, or both when it calls [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="4075b-164">Si le nom du service est **null**, tous les serveurs du système qui prennent en charge le nom de la rubrique spécifiée répondent.</span><span class="sxs-lookup"><span data-stu-id="4075b-164">If the service name is **NULL**, all servers in the system that support the specified topic name respond.</span></span> <span data-ttu-id="4075b-165">Une conversation est établie avec chaque serveur qui répond, y compris plusieurs instances du même serveur.</span><span class="sxs-lookup"><span data-stu-id="4075b-165">A conversation is established with each responding server, including multiple instances of the same server.</span></span> <span data-ttu-id="4075b-166">Si le nom de la rubrique est **null**, une conversation est établie sur chaque rubrique reconnue par chaque serveur qui correspond au nom du service.</span><span class="sxs-lookup"><span data-stu-id="4075b-166">If the topic name is **NULL**, a conversation is established on each topic recognized by each server that matches the service name.</span></span>

<span data-ttu-id="4075b-167">Un client peut utiliser les fonctions [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) et [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) pour identifier les serveurs qui répondent à [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span><span class="sxs-lookup"><span data-stu-id="4075b-167">A client can use the [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) and [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) functions to identify the servers that respond to [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="4075b-168">**DdeQueryNextServer** retourne le descripteur de conversation suivant dans une liste de conversations et **DdeQueryConvInfo** remplit une structure [**CONVINFO**](/windows/win32/api/ddeml/ns-ddeml-convinfo) avec des informations sur la conversation.</span><span class="sxs-lookup"><span data-stu-id="4075b-168">**DdeQueryNextServer** returns the next conversation handle in a conversation list, and **DdeQueryConvInfo** fills a [**CONVINFO**](/windows/win32/api/ddeml/ns-ddeml-convinfo) structure with information about the conversation.</span></span> <span data-ttu-id="4075b-169">Le client peut conserver les descripteurs de conversation dont il a besoin et ignorer le reste de la liste de conversations.</span><span class="sxs-lookup"><span data-stu-id="4075b-169">The client can keep the conversation handles that it needs and discard the rest from the conversation list.</span></span>

<span data-ttu-id="4075b-170">L’exemple suivant utilise [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) pour établir des conversations avec tous les serveurs qui prennent en charge la rubrique système, puis utilise les fonctions [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) et [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) pour obtenir les handles de chaîne de nom de service des serveurs et les stocker dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="4075b-170">The following example uses [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) to establish conversations with all servers that support the System topic and then uses the [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) and [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) functions to obtain the servers' service name string handles and store them in a buffer.</span></span>


```
HCONVLIST hconvList; // conversation list 
DWORD idInst;        // instance identifier 
HSZ hszSystem;       // System topic 
HCONV hconv = NULL;  // conversation handle 
CONVINFO ci;         // holds conversation data 
UINT cConv = 0;      // count of conv. handles 
HSZ *pHsz, *aHsz;    // point to string handles 
 
// Connect to all servers that support the System topic. 
 
hconvList = DdeConnectList(idInst, NULL, hszSystem, NULL, NULL); 
 
// Count the number of handles in the conversation list. 
 
while ((hconv = DdeQueryNextServer(hconvList, hconv)) != NULL) 
    cConv++; 
 
// Allocate a buffer for the string handles. 
 
hconv = NULL; 
aHsz = (HSZ *) LocalAlloc(LMEM_FIXED, cConv * sizeof(HSZ)); 
 
// Copy the string handles to the buffer. 
 
pHsz = aHsz; 
while ((hconv = DdeQueryNextServer(hconvList, hconv)) != NULL) 
{ 
    DdeQueryConvInfo(hconv, QID_SYNC, (PCONVINFO) &ci); 
    DdeKeepStringHandle(idInst, ci.hszSvcPartner); 
    *pHsz++ = ci.hszSvcPartner; 
} 
 
// Use the handles; converse with the servers. 
 
// Free the memory and terminate the conversations. 
 
LocalFree((HANDLE) aHsz); 
DdeDisconnectList(hconvList); 
```



<span data-ttu-id="4075b-171">Une application peut mettre fin à une conversation individuelle dans une liste de conversations en appelant la fonction [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) .</span><span class="sxs-lookup"><span data-stu-id="4075b-171">An application can terminate an individual conversation in a conversation list by calling the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function.</span></span> <span data-ttu-id="4075b-172">Une application peut mettre fin à toutes les conversations d’une liste de conversations en appelant la fonction [**DdeDisconnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) .</span><span class="sxs-lookup"><span data-stu-id="4075b-172">An application can terminate all conversations in a conversation list by calling the [**DdeDisconnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) function.</span></span> <span data-ttu-id="4075b-173">Les deux fonctions obligent le DDEML à envoyer des transactions de [**\_ déconnexion XTYP**](xtyp-disconnect.md) à la fonction de rappel DDE de chaque partenaire.</span><span class="sxs-lookup"><span data-stu-id="4075b-173">Both functions cause the DDEML to send [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transactions to each partner's DDE callback function.</span></span> <span data-ttu-id="4075b-174">**DdeDisconnectList** envoie une transaction de **\_ déconnexion XTYP** pour chaque descripteur de conversation de la liste.</span><span class="sxs-lookup"><span data-stu-id="4075b-174">**DdeDisconnectList** sends an **XTYP\_DISCONNECT** transaction for each conversation handle in the list.</span></span>

<span data-ttu-id="4075b-175">Un client peut récupérer une liste des descripteurs de conversation dans une liste de conversations en passant un handle de liste de conversations existant à [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span><span class="sxs-lookup"><span data-stu-id="4075b-175">A client can retrieve a list of the conversation handles in a conversation list by passing an existing conversation list handle to [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="4075b-176">Le processus d’énumération supprime les descripteurs des conversations terminées de la liste, et les conversations non dupliquées qui correspondent au nom du service et au nom de la rubrique spécifiées sont ajoutées.</span><span class="sxs-lookup"><span data-stu-id="4075b-176">The enumeration process removes the handles of terminated conversations from the list, and nonduplicate conversations that fit the specified service name and topic name are added.</span></span>

<span data-ttu-id="4075b-177">Si [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) spécifie un descripteur de liste de conversations existant, la fonction crée une nouvelle liste de conversations qui contient les handles de toutes les nouvelles conversations et les descripteurs de la liste existante.</span><span class="sxs-lookup"><span data-stu-id="4075b-177">If [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) specifies an existing conversation list handle, the function creates a new conversation list that contains the handles of any new conversations and the handles from the existing list.</span></span>

<span data-ttu-id="4075b-178">Si des conversations en double existent, [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) tente d’éviter les doublons de handles de conversation dans la liste de conversations.</span><span class="sxs-lookup"><span data-stu-id="4075b-178">If duplicate conversations exist, [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) attempts to prevent duplicate conversation handles in the conversation list.</span></span> <span data-ttu-id="4075b-179">Une conversation dupliquée est une deuxième conversation avec le même serveur sur le même nom de service et le même nom de rubrique.</span><span class="sxs-lookup"><span data-stu-id="4075b-179">A duplicate conversation is a second conversation with the same server on the same service name and topic name.</span></span> <span data-ttu-id="4075b-180">Deux conversations de ce type ont des descripteurs différents, mais elles identifient la même conversation.</span><span class="sxs-lookup"><span data-stu-id="4075b-180">Two such conversations would have different handles, yet they would identify the same conversation.</span></span>

 

 




