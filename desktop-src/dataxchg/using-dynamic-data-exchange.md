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
# <a name="using-dynamic-data-exchange"></a>Utilisation de échange dynamique de données

Cette section contient des exemples de code sur les tâches suivantes :

-   [Initiation d’une conversation](#initiating-a-conversation)
-   [Transfert d’un seul élément](#transferring-a-single-item)
    -   [Récupération d’un élément à partir du serveur](#retrieving-an-item-from-the-server)
    -   [Envoi d’un élément au serveur](#submitting-an-item-to-the-server)
-   [Établissement d’une liaison de données permanente](#establishing-a-permanent-data-link)
    -   [Lancement d’une liaison de données](#initiating-a-data-link)
    -   [Lancement d’une liaison de données avec la commande Coller le lien](#initiating-a-data-link-with-the-paste-link-command)
    -   [Notification au client que les données ont été modifiées](#notifying-the-client-that-data-has-changed)
    -   [Arrêt d’une liaison de données](#terminating-a-data-link)
-   [Exécution de commandes dans une application serveur](#carrying-out-commands-in-a-server-application)
-   [Arrêt d’une conversation](#terminating-a-conversation)

## <a name="initiating-a-conversation"></a>Initiation d’une conversation

Pour initier une conversation d’échange dynamique de données (DDE), le client envoie un message de [**\_ \_ lancement DDE**](wm-dde-initiate.md) . En règle générale, le client diffuse ce message en appelant [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), avec-1 comme premier paramètre. Si l’application possède déjà le handle de fenêtre pour l’application serveur, elle peut envoyer le message directement à cette fenêtre. Le client prépare les atomes pour le nom de l’application et le nom de la rubrique en appelant [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma). Le client peut demander des conversations avec toute application serveur potentielle et pour toute rubrique potentielle en fournissant des atomes **null** (caractère générique) pour l’application et la rubrique.

L’exemple suivant illustre la façon dont le client initie une conversation, où l’application et la rubrique sont spécifiées.


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
> Si votre application utilise des atomes **null** , vous n’avez pas besoin d’utiliser les fonctions [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) et [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) . Dans cet exemple, l’application cliente crée deux atomes globaux contenant le nom du serveur et le nom de la rubrique, respectivement.

 

L’application cliente envoie un message [**WM de \_ \_ lancement DDE**](wm-dde-initiate.md) avec ces deux atomes dans le paramètre *lParam* du message. Dans l’appel à la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , le handle de fenêtre spécial – 1 indique au système d’envoyer ce message à toutes les autres applications actives. **SendMessage** ne retourne pas à l’application cliente tant que toutes les applications qui reçoivent le message n’ont pas retourné le contrôle au système. Cela signifie que tous les messages d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE qui sont envoyés en réponse par les applications serveur sont assurés d’être traités par le client au moment où l’appel **SendMessage** est retourné.

Une fois [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) retourné, l’application cliente supprime les atomes globaux.

Les applications serveur répondent selon la logique illustrée dans le diagramme suivant.

![logique de réponse de l’application serveur](images/csdde-01.png)

Pour accuser réception d’une ou plusieurs rubriques, le serveur doit créer des atomes pour chaque conversation (nécessitant des atomes de nom d’application en double s’il existe plusieurs rubriques) et envoyer un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE pour chaque conversation, comme illustré dans l’exemple suivant.


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



Lorsqu’un serveur répond avec un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE, l’application cliente doit enregistrer un descripteur dans la fenêtre du serveur. Le client recevant le descripteur en tant que paramètre *wParam* du message d’accusé de réception **\_ DDE \_ de WM** envoie ensuite tous les messages DDE suivants à la fenêtre du serveur que ce descripteur identifie.

Si votre application cliente utilise un atome **null** pour le nom de l’application ou le nom de la rubrique, attendez-vous à ce que l’application reçoive des accusés de réception de plusieurs applications serveur. Plusieurs accusés de réception peuvent également provenir de plusieurs instances d’un serveur DDE, même si votre application cliente n’utilise pas les atomes **null** . Un serveur doit toujours utiliser une fenêtre unique pour chaque conversation. La procédure de fenêtre de l’application cliente peut utiliser un descripteur de la fenêtre du serveur (fourni comme paramètre *lParam* de l' [**\_ \_ initialisation DDE WM**](wm-dde-initiate.md)) pour effectuer le suivi de plusieurs conversations. Cela permet à une seule fenêtre cliente de traiter plusieurs conversations sans avoir à arrêter et à se reconnecter avec une nouvelle fenêtre client pour chaque conversation.

## <a name="transferring-a-single-item"></a>Transfert d’un seul élément

Une fois qu’une conversation DDE a été établie, le client peut récupérer la valeur d’un élément de données à partir du serveur en émettant le message de [**\_ \_ requête**](wm-dde-request.md) de l’échange de données (DDE) WM ou envoyer une valeur d’élément de données au serveur en émettant le composant [**WM \_ DDE \_**](wm-dde-poke.md).

-   [Récupération d’un élément à partir du serveur](#retrieving-an-item-from-the-server)
-   [Envoi d’un élément au serveur](#submitting-an-item-to-the-server)

### <a name="retrieving-an-item-from-the-server"></a>Récupération d’un élément à partir du serveur

Pour récupérer un élément à partir du serveur, le client envoie un message [**de \_ \_ requête**](wm-dde-request.md) de l’échange de messages WM au serveur en spécifiant l’élément et le format à récupérer, comme illustré dans l’exemple suivant.


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



Dans cet exemple, le client spécifie le format **de \_ texte clair** du presse-papiers comme format préféré pour l’élément de données demandé.

Le récepteur (serveur) du message [**de \_ \_ demande DDE WM**](wm-dde-request.md) doit en général supprimer l’élément Atom, mais si l’appel [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) échoue, le client doit supprimer l’atome.

Si le serveur a accès à l’élément demandé et peut le rendre dans le format demandé, le serveur copie la valeur de l’élément en tant qu’objet mémoire partagée et envoie un message de données de l' [**\_ échange de \_ données (DDE**](wm-dde-data.md) ) au client, comme illustré dans l’exemple suivant.


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



Dans cet exemple, l’application serveur alloue un objet mémoire pour contenir l’élément de données. L’objet de données est initialisé comme une structure [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) .

L’application serveur définit ensuite le membre **cfFormat** de la structure sur le \_ texte CF pour informer l’application cliente que les données sont au format texte. Le client répond en copiant la valeur des données demandées dans le membre **value** de la structure [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) . Une fois que le serveur a rempli l’objet de données, le serveur déverrouille les données et crée un atome global contenant le nom de l’élément de données.

Enfin, le serveur émet le message de [**\_ \_ données DDE WM**](wm-dde-data.md) en appelant [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea). Le descripteur de l’objet de données et l’Atom contenant le nom de l’élément sont empaquetés dans le paramètre *lParam* du message par la fonction [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) .

Si [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) échoue, le serveur doit utiliser la fonction [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) pour libérer le paramètre condensé *lParam* . Le serveur doit également libérer le paramètre *lParam* condensé pour le message de [**\_ \_ requête DDE WM**](wm-dde-request.md) qu’il a reçu.

Si le serveur ne peut pas répondre à la demande, il envoie un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE négatif négatif au client, comme illustré dans l’exemple suivant.


```
// Negative acknowledgment. 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 0, atomItem));
```



À la réception d’un message de [**\_ \_ données DDE WM**](wm-dde-data.md) , le client traite la valeur de l’élément de données comme il convient. Ensuite, si le membre **fAckReq** désigné dans le message **de \_ \_ données de DDE de WM** est 1, le client doit envoyer au serveur un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE positif, comme indiqué dans l’exemple suivant.


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



Dans cet exemple, le client examine le format des données. Si le format n’est pas du **\_ texte CF** (ou si le client ne peut pas verrouiller la mémoire pour les données), le client envoie un message d’accusé de réception [**\_ DDE \_ de WM**](wm-dde-ack.md) négatif pour indiquer qu’il ne peut pas traiter les données. Si le client ne peut pas verrouiller un handle de données parce que le handle contient le membre **fAckReq** , le client ne doit pas envoyer de message d' **\_ \_ accusé** de réception DDE négatif négatif. Au lieu de cela, le client doit mettre fin à la conversation.

Si un client envoie un accusé de réception négatif en réponse à un message de données de l' [**\_ échange de \_ données (DDE**](wm-dde-data.md) ), le serveur est responsable de la libération de la mémoire (mais pas du paramètre *lParam* ) référencée par le message de données de l' **échange de \_ \_ données (DDE) WM** associé à l’accusé de réception négatif.

S’il peut traiter les données, le client examine le membre **fAckReq** de la structure [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) pour déterminer si le serveur a demandé qu’il soit informé que le client a reçu et traité correctement les données. Si le serveur a demandé cette information, le client envoie un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE positif au serveur.

Étant donné que le déverrouillage des données invalide le pointeur vers les données, le client enregistre la valeur du membre **fRelease** avant de déverrouiller l’objet de données. Après avoir enregistré la valeur, le client l’examine pour déterminer si l’application serveur a demandé au client de libérer la mémoire qui contient les données. le client agit en conséquence.

Lors de la réception d’un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE de WM négatif, le client peut demander à nouveau la même valeur d’élément, en spécifiant un autre format de presse-papiers. En règle générale, un client demande tout d’abord le format le plus complexe qu’il peut prendre en charge, puis pas à pas détaillé si nécessaire par le biais de formats progressivement plus simples jusqu’à ce qu’il trouve un serveur.

Si le serveur prend en charge l’élément formats de la rubrique système, le client peut déterminer à quel moment le format du presse-papiers est pris en charge par le serveur, au lieu de les déterminer chaque fois que le client demande un élément.

### <a name="submitting-an-item-to-the-server"></a>Envoi d’un élément au serveur

Le client peut envoyer une valeur d’élément au serveur à l’aide du message d’échange de messages de l' [**\_ échange \_**](wm-dde-poke.md) de messages WM. Le client restitue l’élément à envoyer et envoie le message de pagination **WM \_ DDE \_** , comme illustré dans l’exemple suivant.


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
> L’envoi de données à l’aide d’un message Colors de l' [**\_ échange \_**](wm-dde-poke.md) de données par l’intermédiaire de WM revient essentiellement à les envoyer à l’aide de [**\_ \_ données DDE WM**](wm-dde-data.md), à la différence que **WM \_ DDE \_** est envoyé du client au serveur.

 

Si le serveur est en mesure d’accepter la valeur de l’élément de données dans le format affiché par le client, le serveur traite la valeur de l’élément de manière appropriée et envoie au client un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE positif positif. S’il ne parvient pas à traiter la valeur de l’élément, en raison de son format ou pour d’autres raisons, le serveur envoie au client un message d' **\_ \_ accusé** de réception DDE négatif négatif.


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



Dans cet exemple, le serveur appelle [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) pour récupérer le nom de l’élément envoyé par le client. Le serveur détermine ensuite s’il prend en charge l’élément et si l’élément est rendu dans le format approprié (autrement dit, le \_ texte CF). Si l’élément n’est pas pris en charge et n’est pas rendu dans le format approprié, ou si le serveur ne peut pas verrouiller la mémoire pour les données, le serveur renvoie un accusé de réception négatif à l’application cliente. Notez que dans ce cas, l’envoi d’un accusé de réception négatif est correct, car les messages d’entourage [**\_ \_ DDE**](wm-dde-poke.md) sont toujours supposés avoir le membre **fAckReq** défini. Le serveur doit ignorer le membre.

Si un serveur envoie un accusé de réception négatif en réponse à un message [**WM \_ DDE \_**](wm-dde-poke.md) , le client est responsable de la libération de la mémoire (mais pas du paramètre *lParam* ) référencée par le message d’action de l' **\_ échange \_** de messages WM associé à l’accusé de réception négatif.

## <a name="establishing-a-permanent-data-link"></a>Établissement d’une liaison de données permanente

Une application cliente peut utiliser DDE pour établir un lien vers un élément dans une application serveur. Une fois ce lien établi, le serveur envoie des mises à jour périodiques de l’élément lié au client, en général, chaque fois que la valeur de l’élément change. Par conséquent, un flux de données permanent est établi entre les deux applications. ce flux de données reste en place jusqu’à ce qu’il soit explicitement déconnecté.

### <a name="initiating-a-data-link"></a>Lancement d’une liaison de données

Le client initie une liaison de données en publiant un message de [**\_ \_ notification**](wm-dde-advise.md) de l’échange de données (DDE) WM, comme indiqué dans l’exemple suivant.


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



Dans cet exemple, l’application cliente affecte à l’indicateur **fDeferUpd** du message de [**\_ \_ notification DDE WM**](wm-dde-advise.md) la **valeur false**. Cela indique à l’application serveur d’envoyer les données au client chaque fois que les données sont modifiées.

Si le serveur ne parvient pas à traiter la demande de [**\_ \_ notification DDE de WM**](wm-dde-advise.md) , il envoie un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE négatif négatif au client. Toutefois, si le serveur a accès à l’élément et peut le rendre dans le format demandé, le serveur remarque le nouveau lien (en rappelant les indicateurs spécifiés dans le paramètre *hOptions* ) et envoie au client un message d' **\_ \_ accusé** de réception DDE positif positif. À partir de là, jusqu’à ce que le client envoie un message d' [**\_ \_ invites WM DDE**](wm-dde-unadvise.md) correspondant, le serveur envoie les nouvelles données au client chaque fois que la valeur de l’élément change dans le serveur.

Le message de [**\_ \_ notification DDE de WM**](wm-dde-advise.md) établit le format des données à échanger pendant la liaison. Si le client tente d’établir un autre lien avec le même élément mais utilise un format de données différent, le serveur peut choisir de rejeter le deuxième format de données ou de tenter de le prendre en charge. Si un lien à chaud a été établi pour un élément de données, le serveur ne peut prendre en charge qu’un seul format de données à la fois. Cela est dû au fait que le message de [**\_ \_ données de DDE WM**](wm-dde-data.md) pour un lien chaud a un handle de données **null** , qui contient des informations de format. Par conséquent, un serveur doit rejeter tous les liens semi-chauffants pour un élément déjà lié et doit rejeter tous les liens pour un élément qui a des liens chauds. Une autre interprétation peut être que le serveur modifie le format et l’état chaud ou chaud d’un lien lorsqu’un deuxième lien est demandé pour le même élément de données.

En général, les applications clientes ne doivent pas tenter d’établir plusieurs liens à la fois pour un élément de données.

### <a name="initiating-a-data-link-with-the-paste-link-command"></a>Lancement d’une liaison de données avec la commande Coller le lien

Les applications qui prennent en charge les liaisons de données à chaud ou à chaud prennent en charge un format de presse-papiers enregistré nommé Link. Lorsqu’il est associé aux commandes de lien copier et coller de l’application, ce format de presse-papiers permet à l’utilisateur d’établir des conversations DDE entre les applications en copiant simplement un élément de données dans l’application serveur et en le collant dans l’application cliente.

Une application serveur prend en charge le format de lien du presse-papiers en plaçant dans le presse-papiers une chaîne contenant les noms de l’application, de la rubrique et de l’élément lorsque l’utilisateur choisit la commande **copier** dans le menu **Edition** . Le format de lien standard est le suivant :

*rubrique ***\\ 0 de l’application 0**** * * 0 ***\\ 0*** \\ \\**

Un caractère null unique sépare les noms et deux caractères null terminent la chaîne entière.

Les applications client et serveur doivent enregistrer le format du presse-papiers de liens, comme indiqué ci-dessous :


```
cfLink = RegisterClipboardFormat("Link");
```



Une application cliente prend en charge le format de lien du presse-papiers au moyen d’une commande Coller le lien dans son menu Edition. Quand l’utilisateur choisit cette commande, l’application cliente analyse les noms d’application, de rubrique et d’élément à partir des données du presse-papiers au format de lien. À l’aide de ces noms, l’application cliente lance une conversation pour l’application et la rubrique, si une telle conversation n’existe pas encore. L’application cliente envoie alors un message de [**\_ \_ notification**](wm-dde-advise.md) de l’échange de données (DDE) WM à l’application serveur, en spécifiant le nom de l’élément contenu dans les données du presse-papiers au format de lien.

Voici un exemple de réponse d’une application cliente lorsque l’utilisateur choisit la commande Coller le lien.


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



Dans cet exemple, l’application cliente ouvre le presse-papiers et détermine si elle contient des données au format de lien (autrement dit, cfLink) qu’elle avait précédemment inscrites. Si ce n’est pas le cas, ou s’il ne peut pas verrouiller les données dans le presse-papiers, le client retourne.

Une fois que l’application cliente a récupéré un pointeur vers les données du presse-papiers, elle analyse les données pour extraire les noms d’application, de rubrique et d’élément.

L’application cliente détermine si une conversation sur la rubrique existe déjà entre elle et l’application serveur. Si une conversation existe, le client vérifie s’il existe déjà un lien pour l’élément de données. Si un tel lien existe, le client affiche une boîte de message à l’utilisateur ; dans le cas contraire, elle appelle sa propre fonction *SendAdvise* pour envoyer un message de [**\_ \_ notification**](wm-dde-advise.md) de l’échange de messages. WM au serveur pour l’élément.

Si une conversation sur la rubrique n’existe pas déjà entre le client et le serveur, le client appelle d’abord sa propre fonction *SendInitiate* pour diffuser le message de [**\_ \_ lancement DDE**](wm-dde-initiate.md) pour demander une conversation et, ensuite, appelle sa propre fonction *FindServerGivenAppTopic* pour établir la conversation avec la fenêtre qui répond pour le compte de l’application serveur. Une fois la conversation commencée, l’application cliente appelle *SendAdvise* pour demander le lien.

### <a name="notifying-the-client-that-data-has-changed"></a>Notification au client que les données ont été modifiées

Lorsque le client établit un lien à l’aide du message de [**\_ \_ notification DDE WM**](wm-dde-advise.md) , avec le membre **fDeferUpd** non défini (autrement dit, égal à zéro) dans la structure [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) , le client a demandé au serveur d’envoyer l’élément de données chaque fois que la valeur de l’élément est modifiée. Dans ce cas, le serveur restitue la nouvelle valeur de l’élément de données dans le format spécifié précédemment et envoie au client un message de données de l' [**\_ échange de \_ données (DDE) WM**](wm-dde-data.md) , comme indiqué dans l’exemple suivant.


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



Dans cet exemple, le client traite la valeur de l’élément selon le cas. Si l’indicateur **fAckReq** de l’élément est défini, le client envoie un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE positif au serveur.

Lorsque le client établit le lien, avec le jeu de membres **fDeferUpd** (autrement dit, égal à 1), le client a demandé que seule une notification, et non les données lui-même, soit envoyée chaque fois que les données sont modifiées. Dans ce cas, lorsque la valeur de l’élément change, le serveur n’affiche pas la valeur, mais envoie simplement au client un message de [**\_ \_ données de l’échange WM**](wm-dde-data.md) avec un descripteur de données null, comme illustré dans l’exemple suivant.


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



Si nécessaire, le client peut demander la valeur la plus récente de l’élément de données en émettant un message de [**\_ \_ requête DDE**](wm-dde-request.md) normal, ou il peut simplement ignorer la notification du serveur dont les données ont été modifiées. Dans les deux cas, si **fAckReq** est égal à 1, le client est supposé envoyer un message [**d' \_ \_ accusé**](wm-dde-ack.md) de réception DDE positif positif au serveur.

### <a name="terminating-a-data-link"></a>Arrêt d’une liaison de données

Si le client demande l’arrêt d’un lien de données spécifique, le client envoie un message de [**\_ \_ notification**](wm-dde-unadvise.md) de l’échange de données à un serveur WM, comme indiqué dans l’exemple suivant.


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



Le serveur vérifie si le client dispose actuellement d’un lien vers l’élément spécifique de cette conversation. Si un lien existe, le serveur envoie au client un message [**d' \_ \_ accusé**](wm-dde-ack.md) de réception DDE positif positif ; le serveur n’est alors plus nécessaire pour envoyer des mises à jour concernant l’élément. S’il n’existe pas de lien, le serveur envoie un message d' **\_ \_ accusé** de réception DDE négatif négatif au client.

Le message [**WM \_ DDE \_ Unadvise**](wm-dde-unadvise.md) spécifie un format de données. Un format de zéro indique au serveur d’arrêter tous les liens pour l’élément spécifié, même si plusieurs liens sensibles sont établis et chacun utilise un format différent.

Pour mettre fin à tous les liens d’une conversation, l’application cliente envoie au serveur un message [**WM \_ DDE \_ Unadvise**](wm-dde-unadvise.md) avec un atome d’élément null. Le serveur détermine si la conversation a au moins un lien actuellement établi. Si un lien existe, le serveur envoie au client un message [**d' \_ \_ accusé**](wm-dde-ack.md) de réception DDE positif positif ; le serveur n’a plus à envoyer de mise à jour dans la conversation. S’il n’existe pas de lien, le serveur envoie un message d' **\_ \_ accusé** de réception DDE négatif négatif au client.

## <a name="carrying-out-commands-in-a-server-application"></a>Exécution de commandes dans une application serveur

Les applications peuvent utiliser le message d' [**\_ \_ exécution DDE de WM**](wm-dde-execute.md) pour déclencher l’exécution d’une certaine commande ou d’une série de commandes dans une autre application. Pour ce faire, le client envoie au serveur un message **WM d' \_ \_ exécution DDE** contenant un handle vers une chaîne de commande, comme illustré dans l’exemple suivant.


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



Dans cet exemple, le serveur tente d’exécuter la chaîne de commande spécifiée. En cas de tentative, le serveur envoie au client un message [**d' \_ \_ accusé**](wm-dde-ack.md) de réception DDE positif positif ; sinon, il envoie un message d' **\_ \_ accusé** de réception DDE négatif négatif. Ce message d' **\_ \_ accusé** de réception DDE de WM réutilise le descripteur *hCommand* passé dans le message d' [**\_ \_ exécution DDE DDE**](wm-dde-execute.md) d’origine.

Si la chaîne d’exécution de la commande du client demande que le serveur s’arrête, le serveur doit répondre en envoyant un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE positif, puis envoyer un message [**WM \_ DDE \_ Terminate**](wm-dde-terminate.md) avant de se terminer. Toutes les autres commandes envoyées avec un message d' [**\_ \_ exécution DDE de WM**](wm-dde-execute.md) doivent être exécutées de façon synchrone ; autrement dit, le serveur doit envoyer un message d’accusé de réception **\_ DDE \_ de WM** uniquement après la fin de la commande.

## <a name="terminating-a-conversation"></a>Arrêt d’une conversation

Le client ou le serveur peut émettre un message [**WM \_ DDE \_ Terminate**](wm-dde-terminate.md) pour mettre fin à une conversation à tout moment. De même, les applications client et serveur doivent être prêtes à recevoir ce message à tout moment. Une application doit mettre fin à toutes ses conversations avant de s’arrêter.

Dans l’exemple suivant, l’application qui termine la conversation publie un message [**WM \_ DDE \_ Terminate**](wm-dde-terminate.md) .


```
PostMessage(hwndServerDDE, WM_DDE_TERMINATE, 
    (WPARAM) hwndClientDDE, 0);
```



Cela indique à l’autre application que l’application émettrice n’enverra pas de messages supplémentaires et que le destinataire pourra fermer sa fenêtre. Dans tous les cas, le destinataire est censé répondre rapidement en envoyant un message [**WM de \_ \_ fin DDE**](wm-dde-terminate.md) . Le destinataire ne doit pas envoyer un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE négatif, occupé ou positif.

Une fois qu’une application a envoyé le message de [**\_ \_ fin**](wm-dde-terminate.md) de l’échange de messages avec le protocole WM DDE au partenaire dans une conversation DDE, elle ne doit pas répondre aux messages de ce partenaire, car le partenaire a peut-être détruit la fenêtre à laquelle la réponse est envoyée.

Si une application reçoit un message DDE autre que [**WM \_ DDE \_ Terminate**](wm-dde-terminate.md) après qu’elle a publié **WM \_ DDE \_ Terminate**, elle doit libérer tous les objets associés aux messages reçus, à l’exception des handles de données pour les [**\_ \_ données DDE WM**](wm-dde-data.md) ou des messages coscripteur [**WM \_ DDE \_**](wm-dde-poke.md) qui n’ont **pas** de membre **fRelease** .

Quand une application est sur le lieu de s’arrêter, elle doit mettre fin à toutes les conversations DDE actives avant de terminer le traitement du message [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) . Toutefois, si une application ne termine pas ses conversations DDE actives, le système met fin à toutes les conversations DDE associées à une fenêtre lorsque celle-ci est détruite. L’exemple suivant montre comment une application serveur met fin à toutes les conversations DDE.


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



 

 