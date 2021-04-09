---
title: Surveillance des applications de
description: Cette rubrique explique comment utiliser les éléments de la bibliothèque de gestion échange dynamique de données pour créer une application qui surveille l’activité d’échange de données dynamiques dans le système.
ms.assetid: 6705dc8e-d1e9-4057-9fa2-42cd5cf818af
keywords:
- Interface utilisateur Windows, échange dynamique de données (DDE)
- Échange dynamique de données (DDE), surveillance des applications
- DDE (échange dynamique de données), surveillance des applications
- échange de données, échange dynamique de données (DDE)
- Interface utilisateur Windows, bibliothèque de gestion des échange dynamique de données (DDEML)
- Bibliothèque de gestion des échange dynamique de données (DDEML), applications de surveillance
- DDEML (bibliothèque de gestion échange dynamique de données), surveillance des applications
- échange de données, bibliothèque de gestion des échange dynamique de données (DDEML)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f75685d4caa15e519485b2d8b37983faa35366
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028953"
---
# <a name="monitoring-applications"></a><span data-ttu-id="90471-111">Surveillance des applications de</span><span class="sxs-lookup"><span data-stu-id="90471-111">Monitoring Applications</span></span>

<span data-ttu-id="90471-112">Les éléments d’API de la bibliothèque de gestion échange dynamique de données (DDEML) peuvent être utilisés pour créer une application qui surveille l’activité de échange dynamique de données (DDE) dans le système.</span><span class="sxs-lookup"><span data-stu-id="90471-112">The API elements of the Dynamic Data Exchange Management Library (DDEML) can be used to create an application that monitors Dynamic Data Exchange (DDE) activity in the system.</span></span> <span data-ttu-id="90471-113">Comme n’importe quelle application DDEML, une application de surveillance DDE contient une fonction de rappel DDE.</span><span class="sxs-lookup"><span data-stu-id="90471-113">Like any DDEML application, a DDE monitoring application contains a DDE callback function.</span></span> <span data-ttu-id="90471-114">Le DDEML notifie la fonction de rappel DDE d’une application de surveillance chaque fois qu’un événement DDE se produit, en passant des informations sur l’événement à la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="90471-114">The DDEML notifies a monitoring application's DDE callback function whenever a DDE event occurs, passing information about the event to the callback function.</span></span> <span data-ttu-id="90471-115">L’application affiche généralement les informations dans une fenêtre ou les écrit dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="90471-115">The application typically displays the information in a window or writes it to a file.</span></span>

<span data-ttu-id="90471-116">Pour recevoir des notifications de DDEML, une application doit être inscrite en tant qu’analyseur DDE en spécifiant l' \_ indicateur de moniteur APPCLASS dans un appel à la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="90471-116">To receive notifications from the DDEML, an application must have registered as a DDE monitor by specifying the APPCLASS\_MONITOR flag in a call to the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span> <span data-ttu-id="90471-117">Dans ce même appel, l’application peut spécifier un ou plusieurs indicateurs d’analyse pour indiquer les types d’événements pour lesquels le DDEML doit notifier la fonction de rappel de l’application.</span><span class="sxs-lookup"><span data-stu-id="90471-117">In this same call, the application can specify one or more monitor flags to indicate the types of events for which the DDEML is to notify the application's callback function.</span></span> <span data-ttu-id="90471-118">Les indicateurs de surveillance suivants peuvent être spécifiés par une application :</span><span class="sxs-lookup"><span data-stu-id="90471-118">The following monitor flags can be specified by an application:</span></span>



| <span data-ttu-id="90471-119">Indicateur</span><span class="sxs-lookup"><span data-stu-id="90471-119">Flag</span></span>          | <span data-ttu-id="90471-120">Description</span><span class="sxs-lookup"><span data-stu-id="90471-120">Description</span></span>                                                                                                                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90471-121">\_rappels MF</span><span class="sxs-lookup"><span data-stu-id="90471-121">MF\_CALLBACKS</span></span> | <span data-ttu-id="90471-122">Notifie la fonction de rappel chaque fois qu’une transaction est envoyée à une fonction de rappel DDE dans le système.</span><span class="sxs-lookup"><span data-stu-id="90471-122">Notifies the callback function whenever a transaction is sent to any DDE callback function in the system.</span></span>                                                                                                                                           |
| <span data-ttu-id="90471-123">\_conv CONV</span><span class="sxs-lookup"><span data-stu-id="90471-123">MF\_CONV</span></span>      | <span data-ttu-id="90471-124">Notifie la fonction de rappel lorsqu’une conversation est établie ou terminée.</span><span class="sxs-lookup"><span data-stu-id="90471-124">Notifies the callback function whenever a conversation is established or terminated.</span></span>                                                                                                                                                                |
| <span data-ttu-id="90471-125">\_Erreurs MF</span><span class="sxs-lookup"><span data-stu-id="90471-125">MF\_ERRORS</span></span>    | <span data-ttu-id="90471-126">Notifie la fonction de rappel chaque fois qu’une erreur DDEML se produit.</span><span class="sxs-lookup"><span data-stu-id="90471-126">Notifies the callback function whenever a DDEML error occurs.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="90471-127">\_infos HSZ \_ MF</span><span class="sxs-lookup"><span data-stu-id="90471-127">MF\_HSZ\_INFO</span></span> | <span data-ttu-id="90471-128">Notifie la fonction de rappel lorsqu’une application DDEML crée, libère ou incrémente le décompte d’utilisation d’un handle de chaîne ou chaque fois qu’un handle de chaîne est libéré à la suite d’un appel à la fonction [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) .</span><span class="sxs-lookup"><span data-stu-id="90471-128">Notifies the callback function whenever a DDEML application creates, frees, or increments the usage count of a string handle or whenever a string handle is freed as a result of a call to the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function.</span></span> |
| <span data-ttu-id="90471-129">\_liens MF</span><span class="sxs-lookup"><span data-stu-id="90471-129">MF\_LINKS</span></span>     | <span data-ttu-id="90471-130">Notifie la fonction de rappel chaque fois qu’une boucle de notification est démarrée ou terminée.</span><span class="sxs-lookup"><span data-stu-id="90471-130">Notifies the callback function whenever an advise loop is started or ended.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="90471-131">\_POSTMSGS MF</span><span class="sxs-lookup"><span data-stu-id="90471-131">MF\_POSTMSGS</span></span>  | <span data-ttu-id="90471-132">Notifie la fonction de rappel chaque fois que le système ou une application publie un message DDE.</span><span class="sxs-lookup"><span data-stu-id="90471-132">Notifies the callback function whenever the system or an application posts a DDE message.</span></span>                                                                                                                                                           |
| <span data-ttu-id="90471-133">\_SENDMSGS MF</span><span class="sxs-lookup"><span data-stu-id="90471-133">MF\_SENDMSGS</span></span>  | <span data-ttu-id="90471-134">Notifie la fonction de rappel chaque fois que le système ou une application envoie un message DDE.</span><span class="sxs-lookup"><span data-stu-id="90471-134">Notifies the callback function whenever the system or an application sends a DDE message.</span></span>                                                                                                                                                           |



 

<span data-ttu-id="90471-135">L’exemple suivant montre comment inscrire une application de surveillance DDE afin que sa fonction de rappel DDE reçoive des notifications de tous les événements DDE.</span><span class="sxs-lookup"><span data-stu-id="90471-135">The following example shows how to register a DDE monitoring application so that its DDE callback function receives notifications of all DDE events.</span></span>


```
DWORD idInst; 
PFNCALLBACK lpDdeProc; 
hInst = hInstance; 
 
if (DdeInitialize( 
        (LPDWORD) &idInst,  // instance identifier 
        DDECallback,        // pointer to callback function 
        APPCLASS_MONITOR |  // this is a monitoring application 
        MF_CALLBACKS     |  // monitor callback functions 
        MF_CONV          |  // monitor conversation data 
        MF_ERRORS        |  // monitor DDEML errors 
        MF_HSZ_INFO      |  // monitor data handle activity 
        MF_LINKS         |  // monitor advise loops 
        MF_POSTMSGS      |  // monitor posted DDE messages 
        MF_SENDMSGS,        // monitor sent DDE messages 
        0))                 // reserved 
{
    return FALSE; 
}
```



<span data-ttu-id="90471-136">DDEML informe l’application de surveillance d’un événement DDE en envoyant une transaction de [**surveillance \_ XTYP**](xtyp-monitor.md) à la fonction de rappel DDE de l’application.</span><span class="sxs-lookup"><span data-stu-id="90471-136">The DDEML informs a monitoring application of a DDE event by sending an [**XTYP\_MONITOR**](xtyp-monitor.md) transaction to the application's DDE callback function.</span></span> <span data-ttu-id="90471-137">Au cours de cette transaction, DDEML transmet un indicateur d’analyse spécifiant le type d’événement DDE qui s’est produit et un handle vers un objet DDE qui contient des informations détaillées sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="90471-137">During this transaction, the DDEML passes a monitor flag that specifies the type of DDE event that has occurred and a handle to a DDE object that contains detailed information about the event.</span></span> <span data-ttu-id="90471-138">DDEML fournit un ensemble de structures que l’application peut utiliser pour extraire les informations de l’objet DDE.</span><span class="sxs-lookup"><span data-stu-id="90471-138">The DDEML provides a set of structures that the application can use to extract the information from the DDE object.</span></span> <span data-ttu-id="90471-139">Il existe une structure correspondante pour chaque type d’événement DDE.</span><span class="sxs-lookup"><span data-stu-id="90471-139">There is a corresponding structure for each type of DDE event.</span></span>



| <span data-ttu-id="90471-140">Structure</span><span class="sxs-lookup"><span data-stu-id="90471-140">Structure</span></span>                                  | <span data-ttu-id="90471-141">Description</span><span class="sxs-lookup"><span data-stu-id="90471-141">Description</span></span>                                                       |
|--------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="90471-142">**MONCBSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="90471-142">**MONCBSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)     | <span data-ttu-id="90471-143">Contient des informations sur une transaction.</span><span class="sxs-lookup"><span data-stu-id="90471-143">Contains information about a transaction.</span></span>                         |
| [<span data-ttu-id="90471-144">**MONCONVSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="90471-144">**MONCONVSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) | <span data-ttu-id="90471-145">Contient des informations sur une conversation.</span><span class="sxs-lookup"><span data-stu-id="90471-145">Contains information about a conversation.</span></span>                        |
| [<span data-ttu-id="90471-146">**MONERRSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="90471-146">**MONERRSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)   | <span data-ttu-id="90471-147">Contient des informations sur la dernière erreur DDE.</span><span class="sxs-lookup"><span data-stu-id="90471-147">Contains information about the latest DDE error.</span></span>                  |
| [<span data-ttu-id="90471-148">**MONLINKSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="90471-148">**MONLINKSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) | <span data-ttu-id="90471-149">Contient des informations sur une boucle de notification.</span><span class="sxs-lookup"><span data-stu-id="90471-149">Contains information about an advise loop.</span></span>                        |
| [<span data-ttu-id="90471-150">**MONHSZSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="90471-150">**MONHSZSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)   | <span data-ttu-id="90471-151">Contient des informations sur un handle de chaîne.</span><span class="sxs-lookup"><span data-stu-id="90471-151">Contains information about a string handle.</span></span>                       |
| [<span data-ttu-id="90471-152">**MONMSGSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="90471-152">**MONMSGSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)   | <span data-ttu-id="90471-153">Contient des informations sur un message DDE qui a été envoyé ou publié.</span><span class="sxs-lookup"><span data-stu-id="90471-153">Contains information about a DDE message that was sent or posted.</span></span> |



 

<span data-ttu-id="90471-154">L’exemple suivant illustre la fonction de rappel DDE d’une application de surveillance DDE qui met en forme les informations relatives à chaque événement de handle de chaîne, puis affiche les informations dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="90471-154">The following example shows the DDE callback function of a DDE monitoring application that formats information about each string handle event and then displays the information in a window.</span></span> <span data-ttu-id="90471-155">La fonction utilise la structure [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) pour extraire les informations de l’objet DDE.</span><span class="sxs-lookup"><span data-stu-id="90471-155">The function uses the [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) structure to extract the information from the DDE object.</span></span>


```
HDDEDATA CALLBACK DDECallback(uType, uFmt, hconv, hsz1, hsz2, 
    hdata, dwData1, dwData2) 
UINT uType; 
UINT uFmt; 
HCONV hconv; 
HSZ hsz1; 
HSZ hsz2; 
HDDEDATA hdata; 
DWORD dwData1; 
DWORD dwData2; 
{ 
    LPVOID lpData; 
    CHAR *szAction; 
    CHAR szBuf[256]; 
    DWORD cb;
    HRESULT hResult; 
 
    switch (uType) 
    { 
        case XTYP_MONITOR: 
            // Obtain a pointer to the global memory object. 
 
            if (lpData = DdeAccessData(hdata, &cb)) 
            { 
                // Examine the monitor flag. 
 
                switch (dwData2) 
                { 
                    case MF_HSZ_INFO: 
 
#define PHSZS ((MONHSZSTRUCT *)lpData) 
 
                        // The global memory object contains 
                        // string handle data. Use the MONHSZSTRUCT 
                        // structure to access the data. 
 
                        switch (PHSZS->fsAction) 
                        { 
                            // Examine the action flags to determine
                            // the action performed on the handle.
 
                            case MH_CREATE: 
                                szAction = "Created"; 
                                break; 
 
                            case MH_KEEP: 
                                szAction = "Incremented"; 
                                break; 
 
                            case MH_DELETE: 
                                szAction = "Deleted"; 
                                break; 
 
                            case MH_CLEANUP: 
                                szAction = "Cleaned up"; 
                                break; 
 
                            default: 
                                DdeUnaccessData(hdata); 
                                return (HDDEDATA) 0; 
                        } 
 
                        // Write formatted output to a buffer. 
                        hResult = StringCchPrintf(szBuf, 256/sizeof(TCHAR),
                            "Handle %s, Task: %x, Hsz: %lx(%s)", 
                            (LPSTR) szAction, PHSZS->hTask, 
                            PHSZS->hsz, (LPSTR) PHSZS->str);
                        if (FAILED(hResult))
                        {
                        // TO DO: Write error handler.
                            return;
                        } 
                        // Display text or write to a file. 
 
                        break; 
 
#undef PHSZS 
 
                    // Process other MF_* flags. 
 
                    default: 
                        break; 
                } 
            } 
 
            // Free the global memory object. 
 
            DdeUnaccessData(hdata); 
            break; 
 
        default: 
            break; 
    } 
    return (HDDEDATA) 0; 
} 
```



 

 




