---
title: Gestion des conversations
description: Cette rubrique décrit les conversations entre un client et un serveur.
ms.assetid: 4e5ff1a1-d46a-4e2a-a37c-8df951f2a1ee
keywords:
- Windows Interface utilisateur, échange dynamique de données (DDE)
- échange dynamique de données (DDE), conversations
- DDE (échange dynamique de données), conversations
- échange de données, échange dynamique de données (DDE)
- Windows Interface utilisateur, échange dynamique de données Management Library (DDEML)
- bibliothèque de gestion des échange dynamique de données (DDEML), conversations
- DDEML (bibliothèque de gestion échange dynamique de données), conversations
- échange de données, bibliothèque de gestion des échange dynamique de données (DDEML)
- échange dynamique de données (DDE), plusieurs conversations
- DDE (échange dynamique de données), plusieurs conversations
- bibliothèque de gestion des échange dynamique de données (DDEML), plusieurs conversations
- DDEML (bibliothèque de gestion échange dynamique de données), plusieurs conversations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3531cc396a3b4d0eca5d7c11e3677aec9ea2ee35dcdac110455daee252f798
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991329"
---
# <a name="conversation-management"></a>Gestion des conversations

Une conversation entre un client et un serveur est toujours établie à la demande du client. Lorsqu’une conversation est établie, chaque partenaire reçoit un descripteur qui identifie la conversation. les partenaires utilisent ce handle dans d’autres fonctions de la bibliothèque de gestion des échange dynamique de données (DDEML) pour envoyer des transactions et gérer la conversation. Un client peut demander une conversation avec un seul serveur, ou il peut demander plusieurs conversations avec un ou plusieurs serveurs.

Les rubriques suivantes décrivent comment une application établit de nouvelles conversations et obtient des informations sur les conversations existantes.

-   [Conversations uniques](#single-conversations)
-   [Conversations multiples](#multiple-conversations)

## <a name="single-conversations"></a>Conversations uniques

Une application cliente demande une conversation unique avec un serveur en appelant la fonction [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) et en spécifiant des handles de chaîne qui identifient les chaînes contenant le nom de service de l’application serveur et le nom de la rubrique pour la conversation. le DDEML répond en envoyant la transaction [**XTYP \_ CONNECT**](xtyp-connect.md) à la fonction de rappel échange dynamique de données (DDE) de chaque application serveur qui a inscrit un nom de service qui correspond à celui spécifié dans **DdeConnect** ou a désactivé le filtrage du nom de service en appelant [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice). Un serveur peut également filtrer les transactions **XTYP \_ Connect** en spécifiant \_ l' \_ indicateur de filtre des connexions en échec CBF dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . Au cours de la transaction **XTYP \_ Connect** , Ddeml transmet le nom du service et le nom de la rubrique au serveur. Le serveur doit examiner les noms et retourner la **valeur true** s’il prend en charge la paire nom du service et nom de la rubrique, ou **false** dans le cas contraire.

Si aucun serveur ne répond de manière positive à la demande de connexion du client, le client reçoit la **valeur null** de [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) et aucune conversation n’est établie. Si un serveur retourne la **valeur true**, une conversation est établie et le client reçoit un descripteur de conversation (valeur **DWORD** qui identifie la conversation). Le client utilise le handle dans les appels DDEML suivants pour obtenir des données à partir du serveur. Le serveur reçoit la [**transaction \_ \_ Confirm XTYP Connect**](xtyp-connect-confirm.md) (à moins que le serveur n’ait spécifié l' \_ indicateur de filtre CBF Skip \_ Connect \_ Confirm). Cette transaction transmet le descripteur de conversation au serveur.

L’exemple suivant demande une conversation sur la rubrique du système avec un serveur qui reconnaît le nom du service MyServer. Les paramètres *hszServName* et *hszSysTopic* sont des handles de chaîne créés précédemment.


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



Dans l’exemple précédent, [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) force la fonction de rappel DDE de l’application monserveur à recevoir une transaction [**XTYP \_ Connect**](xtyp-connect.md) .

Dans l’exemple suivant, le serveur répond à la transaction [**XTYP \_ Connect**](xtyp-connect.md) en comparant la chaîne de nom de la rubrique gérer les Ddeml passés au serveur avec chaque élément du tableau de handles de chaîne de nom de rubrique que le serveur prend en charge. Si le serveur trouve une correspondance, il établit la conversation.


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



Si le serveur retourne la **valeur true** en réponse à la transaction [**XTYP \_ Connect**](xtyp-connect.md) , Ddeml envoie une transaction de [**\_ \_ confirmation de connexion XTYP**](xtyp-connect-confirm.md) à la fonction de rappel DDE du serveur. Le serveur peut obtenir le descripteur de la conversation en traitant cette transaction.

Un client peut établir une conversation générique en spécifiant **null** pour le descripteur de chaîne de nom de service, le handle de chaîne de nom de rubrique ou les deux dans un appel à [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect). Si au moins l’un des descripteurs de chaîne a la **valeur null**, Ddeml envoie la transaction [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) aux fonctions de rappel de toutes les applications DDE (à l’exception de celles qui filtrent la transaction **\_ WILDCONNECT XTYP** ). Chaque application serveur doit répondre en retournant un handle de données qui identifie un tableau de structures [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) se terminant par un caractère null. Si l’application serveur n’a pas appelé [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) pour enregistrer ses noms de service et si le filtrage est activé, le serveur ne reçoit pas de transactions **XTYP \_ WILDCONNECT** . Pour plus d’informations sur les handles de données, consultez [gestion des données](data-management.md).

Le tableau doit contenir une structure pour chaque paire nom de service/nom de rubrique qui correspond à la paire spécifiée par le client. Le DDEML sélectionne l’une des paires pour établir une conversation et retourne au client un descripteur qui identifie la conversation. DDEML envoie la transaction [**de \_ \_ confirmation de connexion XTYP**](xtyp-connect-confirm.md) au serveur (sauf si le serveur filtre cette transaction). L’exemple suivant montre une réponse de serveur typique à la transaction [**\_ WILDCONNECT XTYP**](xtyp-wildconnect.md) .


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



Le client ou le serveur peut mettre fin à une conversation à tout moment en appelant la fonction [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) . Cette fonction permet à la fonction de rappel du partenaire de la conversation de recevoir la transaction de [**\_ déconnexion XTYP**](xtyp-disconnect.md) (sauf si le partenaire a spécifié l' \_ indicateur de filtre CBF Skip \_ deconnections). En règle générale, une application répond à la transaction de **\_ déconnexion XTYP** à l’aide de la fonction [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) pour obtenir des informations sur la conversation qui s’est terminée. Une fois que la fonction de rappel a retourné le traitement de la transaction de **\_ déconnexion XTYP** , le descripteur de conversation n’est plus valide.

Une application cliente qui reçoit une transaction de [**\_ déconnexion XTYP**](xtyp-disconnect.md) dans sa fonction de rappel DDE peut tenter de rétablir la conversation en appelant la fonction [**DdeReconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) . Le client doit appeler **DdeReconnect** à partir de sa fonction de rappel DDE.

## <a name="multiple-conversations"></a>Conversations multiples

Une application cliente peut utiliser la fonction [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) pour déterminer si des serveurs intéressants sont disponibles dans le système. Un client spécifie un nom de service et un nom de rubrique lors de l’appel de **DdeConnectList**, ce qui amène le Ddeml à diffuser la transaction [**\_ WILDCONNECT XTYP**](xtyp-wildconnect.md) vers les fonctions de rappel DDE de tous les serveurs qui correspondent au nom du service (sauf ceux qui filtrent la transaction). La fonction de rappel d’un serveur doit retourner un handle de données qui identifie un tableau de structures [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) terminé par le caractère null. Le tableau doit contenir une structure pour chaque paire nom de service/nom de rubrique qui correspond à la paire spécifiée par le client. Le DDEML établit une conversation pour chaque structure **HSZPAIR** remplie par le serveur et retourne un descripteur de liste de conversations au client. Le serveur reçoit le descripteur de conversation par le biais de la transaction [**XTYP \_ Connect**](xtyp-connect.md) (sauf si le serveur filtre cette transaction).

Un client peut spécifier la **valeur null** pour le nom du service, le nom de la rubrique, ou les deux lorsqu’il appelle [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist). Si le nom du service est **null**, tous les serveurs du système qui prennent en charge le nom de la rubrique spécifiée répondent. Une conversation est établie avec chaque serveur qui répond, y compris plusieurs instances du même serveur. Si le nom de la rubrique est **null**, une conversation est établie sur chaque rubrique reconnue par chaque serveur qui correspond au nom du service.

Un client peut utiliser les fonctions [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) et [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) pour identifier les serveurs qui répondent à [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist). **DdeQueryNextServer** retourne le descripteur de conversation suivant dans une liste de conversations et **DdeQueryConvInfo** remplit une structure [**CONVINFO**](/windows/win32/api/ddeml/ns-ddeml-convinfo) avec des informations sur la conversation. Le client peut conserver les descripteurs de conversation dont il a besoin et ignorer le reste de la liste de conversations.

L’exemple suivant utilise [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) pour établir des conversations avec tous les serveurs qui prennent en charge la rubrique système, puis utilise les fonctions [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) et [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) pour obtenir les handles de chaîne de nom de service des serveurs et les stocker dans une mémoire tampon.


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



Une application peut mettre fin à une conversation individuelle dans une liste de conversations en appelant la fonction [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) . Une application peut mettre fin à toutes les conversations d’une liste de conversations en appelant la fonction [**DdeDisconnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) . Les deux fonctions obligent le DDEML à envoyer des transactions de [**\_ déconnexion XTYP**](xtyp-disconnect.md) à la fonction de rappel DDE de chaque partenaire. **DdeDisconnectList** envoie une transaction de **\_ déconnexion XTYP** pour chaque descripteur de conversation de la liste.

Un client peut récupérer une liste des descripteurs de conversation dans une liste de conversations en passant un handle de liste de conversations existant à [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist). Le processus d’énumération supprime les descripteurs des conversations terminées de la liste, et les conversations non dupliquées qui correspondent au nom du service et au nom de la rubrique spécifiées sont ajoutées.

Si [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) spécifie un descripteur de liste de conversations existant, la fonction crée une nouvelle liste de conversations qui contient les handles de toutes les nouvelles conversations et les descripteurs de la liste existante.

Si des conversations en double existent, [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) tente d’éviter les doublons de handles de conversation dans la liste de conversations. Une conversation dupliquée est une deuxième conversation avec le même serveur sur le même nom de service et le même nom de rubrique. Deux conversations de ce type ont des descripteurs différents, mais elles identifient la même conversation.

 

 




